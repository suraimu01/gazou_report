# �ۑ背�|�[�g�X

���f�B�A���t�B���^�[��K�p���C�m�C�Y������̌�����D

�@���摜�Ƃ��Ĉȉ��̂悤�ȃO���[�X�P�[���摜���g�p����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai9/kadai9-1.png?raw=true)

�}1�@���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//�����܂ŃR�[�h//

�@���摜��'salt & pepper'�m�C�Y��Y�t����D���̃m�C�Y�͔����_�ƍ����_���U�炷���̂ł���D�ȉ��̃R�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG = imnoise(ORG,'salt & pepper',0.02); 
	imagesc(ORG); colormap(gray);  colorbar; axis image;
	//�����܂ŃR�[�h//

�@�m�C�Y��Y�t�����摜���ȉ��ł���D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai9/kadai9-2.png?raw=true)

�}2�@�m�C�Y��Y�t�����摜

�@���̉摜�ɑ΂��C�t�B���^�������ăm�C�Y�������s���D
�@�܂��C�������t�B���^�ɂ���ăm�C�Y�������s���D�ȉ��ɍČ�����R�[�h�Ɖ摜�������D

	//��������R�[�h//
	IMG = filter2(fspecial('average',3),ORG); 
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//�����܂ŃR�[�h//

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai9/kadai9-3.png?raw=true)

�}3�@�������t�B���^���������摜

�@�m�C�Y�������Ă��邱�Ƃ����Ď���D
�@���ɁC���f�B�A���t�B���^�ɂ���ăm�C�Y�������s���D�ȉ��ɍČ�����R�[�h�Ɖ摜�������D

	//��������R�[�h//
	IMG = medfilt2(ORG,[3 3]);
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//�����܂ŃR�[�h//

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai9/kadai9-4.png?raw=true)

�}4�@���f�B�A���t�B���^���������摜

�@��������m�C�Y�������Ă���D����ׂ�ƕ������t�B���^��胁�f�B�A���t�B���^�̂ق����m�C�Y�̖��c�����Ȃ�������D
���̂��Ƃ��烁�f�B�A���t�B���^�̂ق����D��Ă���Ƃ�����D