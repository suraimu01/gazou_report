# �ۑ背�|�[�g�P�O

�G�b�W���o��̌�����D

�@���摜�Ƃ��Ĉȉ��̂悤�ȃO���[�X�P�[���摜���g�p����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai10/kadai10-1.png?raw=true)

�}1�@���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//�����܂ŃR�[�h//

�@�܂��C�v���E�B�b�g�@�ɂ���ăG�b�W���o���s���D�ȉ��ɃR�[�h�Ɖ摜�������D

	//��������R�[�h//
	IMG = edge(ORG,'prewitt'); 
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//�����܂ŃR�[�h//

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai10/kadai10-2.png?raw=true)

�}2�@�v���E�B�b�g�@�ɂ��G�b�W���o

�@���ɁC�\�x���@�ɂ��G�b�W���o���s���D�ȉ��ɃR�[�h�Ɖ摜�������D

	//��������R�[�h//
	IMG = edge(ORG,'sobel');
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//�����܂ŃR�[�h//

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai10/kadai10-3.png?raw=true)

�}3�@�\�x���@�ɂ��G�b�W���o

�@�����̃G�b�W���o�@�͂ǂ�����CX�����CY�����ʁX�ɃG�b�W���o���s���C���ʂ�����������̂ł���D�v���E�B�b�g�@�ł͒�������1�C�\�x���̏ꍇ�͒������̉�f��2�Ƃ���邽�߁C�����̍����o�Ă���D
�@�Ō�ɃL���j�[�@�ɂ���ăG�b�W���o���s���D�ȉ��ɃR�[�h�Ɖ摜�������D

	//��������R�[�h//
	IMG = edge(ORG,'sobel');
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//�����܂ŃR�[�h//

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai10/kadai10-4.png?raw=true)

�}4�@�L���j�[�@�ɂ��G�b�W���o

�@�L���j�[�@�͕����X�e�b�v�ɂ���čs����G�b�W���o�@�ł���D���Ȃ荂���\�ȕ��@�ł���C�摜������G�b�W���o�����Ȃ�ł��Ă��邱�Ƃ����Ď���D
�@


