# �ۑ背�|�[�g�S

��f�̔Z�x�q�X�g�O�����𐶐�����D

�@���摜�Ƃ��Ĉȉ��̂悤�ȃO���[�X�P�[���摜���g�p����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai4/kadai4-1.png?raw=true)

�}1�@���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//�����܂ŃR�[�h//

�@���̉摜�̔Z�x�q�X�g�O�������ȉ��Ɏ����D�Z�x�q�X�g�O�����́C�摜�ɂ����f�̔Z�x�ʂ̕��z��\���D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai4/kadai4-2.png?raw=true)

�}2�@���摜�̔Z�x�q�X�g�O����

�@�Z�x�q�X�g�O��������C���̌��摜�͈Â߂̉�f���������Ƃ��킩��D
�@�Z�x�q�X�g�O�����̕\���́C�ȉ��̃R�[�h�ōČ��ł���D

	//��������R�[�h//
	imhist(ORG);
	//�����܂ŃR�[�h//

�@���ɁC���摜�̔Z�x�q�X�g�O�������ψꉻ�������̂�p�ӂ��C�Z�x�q�X�g�O������\������D
�ψꉻ�ɂ́C�ȉ��̃R�[�h���g�p����D

	//��������R�[�h//
	IMG = histeq(ORG,256);
	//�����܂ŃR�[�h//

�@����ɂ��C���摜��256�̔Z�x�q�X�g�O�����ɂ��ψꉻ�����摜��IMG�ɑ�������D
������256���w�肵�Ă��Ȃ���΁C64�̔Z�x�q�X�g�O�����ŋψꉻ���Ă��܂����߁C���摜�Ƃ̔�r�̂��ߎw�肵�Ă���D
�@�ȉ��ɋψꉻ���s�����摜�ƔZ�x�q�X�g�O�������ȉ��Ɏ����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai4/kadai4-3.png?raw=true)

�}3�@�ψꉻ���s�����摜

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai4/kadai4-4.png?raw=true)

�}4�@�ψꉻ���s�����摜�̔Z�x�q�X�g�O����

�@���摜���S�̓I�ɖ��邭�Ȃ�C�q�X�g�O���������邢��f�����������̂����Ď���D
