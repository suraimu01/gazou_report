# �ۑ�Q���|�[�g

�Q�K���C�S�K���C�W�K���̉摜�𐶐�����D

�@���摜�Ƃ��Ĉȉ��̂悤�ȃO���[�X�P�[���摜���g�p����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai2/kadai2-1.png?raw=true)

�}1�@���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//�����܂ŃR�[�h//

�@�摜��\������ہCcolorbar�𓯎��ɕ\�����Ă���D�t���J���[�摜���O���[�X�P�[���ɕϊ����Ă��邽�߁C0�`255�ŕ\������Ă���D
�@���摜��2�K���̉摜�ɂ���ɂ́C�ȉ��̃R�[�h�ōs���D

	//��������R�[�h//
	IMG = ORG>127;
	imagesc(IMG); colormap(gray); colorbar;  axis image;
	//�����܂ŃR�[�h//

�@���̃R�[�h�ł�IMG��127����̐F�̃s�N�Z���݂̂�1�Ƃ��đ�����C�\�����Ă���D����ɂ��C127�ȉ���128�ȏ��2��ނ̕����������D�ȉ��ɕ\�����ꂽ�摜�������D


![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai2/kadai2-2.png?raw=true)

�}2�@2�K���摜

�@���̂悤�ɔ��ƍ���2��ނŕ\�����摜��������D
�@4�K���ɂ���ɂ́C�ȉ��̃R�[�h�ōs���D

	//��������R�[�h//
	IMG0 = ORG>63;
	IMG1 = ORG>127;
	IMG2 = ORG>191;
	IMG = IMG0 + IMG1 + IMG2;
	imagesc(IMG); colormap(gray); colorbar;  axis image;
	//�����܂ŃR�[�h//

�@IMG0�CIMG1�CIMG2�ɂ��ꂼ��64�ȏ�C128�ȏ�C192�ȏ�̐F�̃s�N�Z����1�Ƃ��đ�����C������S�đ������Ƃ�4�K�����Č����Ă���D�ȉ��ɕ\�����ꂽ�摜�������D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai2/kadai2-3.png?raw=true)

�}3�@4�K���摜

�@4�̐F�ɂ���Č��摜���\�����D
�@8�K���������悤�ɁC�������đ���������̂𑫂��Ă��΂悢�D�ȉ��ɃR�[�h�������D

	//��������R�[�h//
	IMG0 = ORG>31;
	IMG1 = ORG>63;
	IMG2 = ORG>95;
	IMG3 = ORG>127;
	IMG4 = ORG>159;
	IMG5 = ORG>191;
	IMG6 = ORG>223;
	IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
	imagesc(IMG); colormap(gray); colorbar;  axis image;
	//�����܂ŃR�[�h//

�@�ȉ��ɕ\�����ꂽ�摜�������D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai2/kadai2-4.png?raw=true)

�}4�@8�K���摜

�@2�K���摜�Ɣ�ׂ�Ƃ����Ԍ��摜�ɋ߂Â��Ă��邱�Ƃ��킩��D