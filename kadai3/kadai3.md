# �ۑ背�|�[�g�R

臒l��4�p�^�[���ݒ肵,臒l���������摜�������D

�@���摜�Ƃ��Ĉȉ��̂悤�ȃO���[�X�P�[���摜���g�p����D


![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-1.png?raw=true)

�}1�@���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//�����܂ŃR�[�h//

�@���摜�̉��ɃJ���[�o�[���o���Ă���C0�`255�̋P�x���\������Ă���D
�@臒l��64�Ƃ��C�P�x�l��64�ȏ�̃s�N�Z����1�C���̑���0�Ƃ����ꍇ�̉摜���ȉ��Ɏ����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-2.png?raw=true)

�}2�@臒l64�̉摜

�@�P�x��64�ȏ�̃s�N�Z���������\������C63�ȉ��͍����\������Ă���D
��̉摜���Č����邽�߂̃R�[�h���ȉ��Ɏ����D

	//��������R�[�h//
	IMG = ORG >= 64;
	imagesc(IMG); colorbar; colormap(gray); axis image;
	//�����܂ŃR�[�h//

�@���̂悤��臒l�����ꂼ��96�C128�C192�Ƃ��C臒l�ȏ��1�C���̑���0�Ƃ����摜�����ꂼ��ȉ��Ɏ����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-3.png?raw=true)

�}3�@臒l96�̉摜

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-4.png?raw=true)

�}4�@臒l128�̉摜

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-5.png?raw=true)

�}5�@臒l192�̉摜

�@�܂��C���ꂼ����Č�����R�[�h���ȉ��Ɏ����D

	//��������R�[�h//
	//臒l96//
	IMG = ORG >= 96;
	imagesc(IMG);colorbar;colormap(gray); axis image;

	//臒l128//
	IMG = ORG >= 128;
	imagesc(IMG);colorbar;colormap(gray); axis image;

	//臒l192//
	IMG = ORG >= 192;
	imagesc(IMG);colorbar;colormap(gray); axis image;
	//�����܂ŃR�[�h//

�@���摜�Ƃ��ꂼ���臒l���������摜������ׂ�ƁC臒l�ȏオ�����C���̑��������Ȃ��Ă��邱�Ƃ��m�F�ł���D臒l��Ⴍ�ݒ肷��ΈÂ���������������C��������Ζ��邢���������������D
�@
