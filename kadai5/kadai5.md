# �ۑ背�|�[�g�T

���ʕ��͖@��p���ĉ摜��l������D

�@���摜�Ƃ��Ĉȉ��̂悤�ȃO���[�X�P�[���摜���g�p����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai5/kadai5-1.png?raw=true)

�}1�@���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//�����܂ŃR�[�h//

�@���̉摜�𔻕ʕ��͖@��p����臒l�����߁C��l������D
�@���ʕ��͖@�́C����臒l�œ�l�������Ƃ��̑o�����N���X�Ƃ��C�����̃N���X�ԕ��U�ƃN���X�����U�̔�ł��镪���x���ő�ƂȂ�l��臒l�Ƃ�����@�ł���D
���ʕ��͖@���������C��l���摜��\������v���O�������ȉ��Ɏ����D

	//��������R�[�h//
	H = imhist(ORG); 
	myu_T = mean(H);
	max_val = 0;
	max_thres = 1;

	for i=1:255
		C1 = H(1:i); C2 = H(i+1:256);
		n1 = sum(C1);n2 = sum(C2);
		myu1 = mean(C1); myu2 = mean(C2);
		sigma1 = var(C1); sigma2 = var(C2);
		sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); 
		sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2);

		if max_val<sigma_B/sigma_w
			max_val = sigma_B/sigma_w;
			max_thres =i;
		end;
	end;

	IMG = ORG > max_thres;
	imagesc(IMG); colormap(gray); colorbar;axis image;
	//�����܂ŃR�[�h//

�@�摜�̃q�X�g�O������C1�CC2�ɕ����C����炩��N���X�ԕ��Usigma_B�ƃN���X�����Usigma_w�����߂�D
�����̔䂪�ȑO��max_val�̒l�����傫����΍X�V���C臒l�ƂȂ�i�̒l��max_thres�ɑ������D�����̑�����q�X�g�O�����̐����J��Ԃ�臒l�����߂�D
�@�ȉ��ɕ\�����ꂽ�摜�������D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai5/kadai5-2.png?raw=true)

�}2�@���ʕ��͖@�ɂ���l���摜
