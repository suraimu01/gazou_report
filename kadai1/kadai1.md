# �ۑ�P���|�[�g

�摜���_�E���T���v�����O���ĕ\������D

�@���摜�Ƃ��Ĉȉ��̂悤�ȉ摜���g�p����D�摜�̕\���ɂ́CMATLAB�ɂ���Ĉȉ��̃R�[�h���g���čs���D

	//��������R�[�h//
	ORG=imread('original.jpg');
	imagesc(ORG); axis image;
	//�����܂ŃR�[�h//

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-1.png?raw=true)
�}1 ���摜

�@���摜��1/2�T���v�����O�������̂��Č�����ɂ́C���摜��1/2�{�ɏk�����C2�{�ɂ��邱�ƂōČ��ł���D
1/2�ɏk������ƌ��摜�̔����̃s�N�Z�����ŕ\�����ꂽ�摜�ƂȂ�D�����2�{�ɂ��邱�ƂŁC���摜�Ɠ����傫���Ńs�N�Z�����������ƂȂ����摜��������D
�@�ȉ���1/2�T���v�����O���s���R�[�h�������D

	//��������R�[�h//
	IMG = imresize(ORG,0.5);
	IMG2 = imresize(IMG,2,'box');
	//�����܂ŃR�[�h//

�@IMG�ɂ͌��摜��1/2�ɏk�������摜���CIMG2�ɂ͌��摜�Ɠ����傫���ɖ߂����摜�������Ă���D
�ȉ���IMG2��\���������ʂ������D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-2.png?raw=true)

�}2 1/2�T���v�����O�摜

�@�኱�����摜���r���Ȃ����̂����Ď���D
�@����Ƀ_�E���T���v�����O���s���ɂ́CIMG������ɏk�����CIMG2�Ɍ��摜�Ɠ����傫���ɂȂ�悤�g�傷��΂悢�D
�����1/4�C1/8�C1/16�C1/32�T���v�����O���s�����D��Ƃ���1/4�T���v�����O���s�����ꍇ�̃R�[�h���ȉ��Ɏ����D

	//��������R�[�h//
	IMG = imresize(IMG,0.5);
	IMG2 = imresize(IMG,4,'box');
	//�����܂ŃR�[�h//

�@IMG�ɂ͂��łɌ��摜��1/2�̑傫���ɏk�����ꂽ�摜�������Ă���C�����1/2�ɏk�����Ă��邽�߁C���摜��1/4�̑傫���ƂȂ��Ă���D
�����4�{�Ɋg�傷�邱�Ƃ�1/4�T���v�����O���Č������D���̂悤��IMG��1/2�ɏk�����Ă���8�{�Ɋg��C1/2�ɏk������16�{�Ƒ����Ă������Ƃł��ꂼ��̃T���v�����O���ʂ��Č������D
�@�ȉ��ɂ��ꂼ��̌��ʂ������D

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-3.png?raw=true)

�}3 1/4�T���v�����O�摜

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-4.png?raw=true)

�}4 1/8�T���v�����O�摜

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-5.png?raw=true)

�}5 1/16�T���v�����O�摜

![���摜](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-6.png?raw=true)

�}6 1/322�T���v�����O�摜

�@���̂悤�ɃT���v�����O�����傫���Ȃ�ƁC���U�C�N��̃T���v�����O�c���������Ă����D�@
�@