# �ۑ背�|�[�g�U

�f�B�U�@��p���ĉ摜���l������D

�@���摜�Ƃ��Ĉȉ��̂悤�ȃO���[�X�P�[���摜���g�p����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai6/kadai6-1.png?raw=true)

�}1�@���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//�����܂ŃR�[�h//

�@�܂��C臒l�𒆉��ɂ����ꍇ�̉摜�Ǝ���������R�[�h�������D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai6/kadai6-2.png?raw=true)

�}2�@臒l128�̓�l���摜

	//��������R�[�h//
	IMG = ORG>128;
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//�����܂ŃR�[�h//

�@���ɁC�f�B�U�@�ɂ���ē�l�������摜�Ǝ���������R�[�h�������D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai6/kadai6-3.png?raw=true)

�}3�@�f�B�U�@�ɂ���l���摜

	//��������R�[�h//
	IMG = dither(ORG); 
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//�����܂ŃR�[�h//

�@��̓�l���摜���ׂ�ƁC�f�B�U�@�ɂ���l���摜�͈ꌩ�m�C�Y�������Ă��܂����悤�ɂ������邪�C���ʂ̓�l���摜�Ƃ͈Ⴂ�C���摜�Ǝ����F�����Ɍ�����D
���̂悤�ɁC�f�B�U�@�ɂ���āC�摜���͍̂r���Ȃ邪�C�r�b�g����}���čČ����邱�Ƃ��ł���D