# �ۑ背�|�[�g�W

��l�����ꂽ�摜�̘A�������Ƀ��x��������D 

�@���摜�Ƃ��Ĉȉ��̂悤�ȃO���[�X�P�[���摜���g�p����D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai8/kadai8-1.png?raw=true)

�}1�@���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//�����܂ŃR�[�h//

�@�����Č��摜���l���摜�ɕϊ������摜���ȉ��ł���D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai8/kadai8-2.png?raw=true)

�}2�@��l���摜

�@���̉摜�͈ȉ��̂悤�ȃR�[�h�ōČ��ł���D

	//��������R�[�h//
	IMG = ORG > 128;
	imagesc(IMG); colormap(gray);  colorbar; axis image;
	//�����܂ŃR�[�h//

�@���̉摜��bwlabeln�ɂ���ĂW�A���Ń��x�����O���C���x�����ƂɐF��������ƁC�ȉ��̂悤�ȉ摜�ƂȂ�D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai8/kadai8-3.png?raw=true)

�}3�@���x�����ƂɐF���������摜

�@�F�������ꏊ���A�����Ă��镔���ł���D
�@���̉摜�͈ȉ��̃R�[�h�ɂ���čČ������D

	//��������R�[�h//
	IMG = bwlabeln(IMG); 
	imagesc(IMG); colormap(gray);  colorbar; axis image;
	//�����܂ŃR�[�h//