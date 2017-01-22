# 課題１レポート

画像をダウンサンプリングして表示せよ．

　原画像として以下のような画像を使用する．画像の表示には，MATLABによって以下のコードを使って行う．

	//ここからコード//
	ORG=imread('original.jpg');
	imagesc(ORG); axis image;
	//ここまでコード//

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-1.png?raw=true)
図1 原画像

　原画像を1/2サンプリングしたものを再現するには，原画像を1/2倍に縮小し，2倍にすることで再現できる．
1/2に縮小すると原画像の半分のピクセル数で表現された画像となる．これを2倍にすることで，原画像と同じ大きさでピクセル数が半分となった画像が得られる．
　以下に1/2サンプリングを行うコードを示す．

	//ここからコード//
	IMG = imresize(ORG,0.5);
	IMG2 = imresize(IMG,2,'box');
	//ここまでコード//

　IMGには原画像を1/2に縮小した画像を，IMG2には原画像と同じ大きさに戻した画像を代入している．
以下にIMG2を表示した結果を示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-2.png?raw=true)

図2 1/2サンプリング画像

　若干だが画像が荒くなったのが見て取れる．
　さらにダウンサンプリングを行うには，IMGをさらに縮小し，IMG2に原画像と同じ大きさになるよう拡大すればよい．
今回は1/4，1/8，1/16，1/32サンプリングを行った．例として1/4サンプリングを行った場合のコードを以下に示す．

	//ここからコード//
	IMG = imresize(IMG,0.5);
	IMG2 = imresize(IMG,4,'box');
	//ここまでコード//

　IMGにはすでに原画像の1/2の大きさに縮小された画像が入っており，それを1/2に縮小しているため，原画像の1/4の大きさとなっている．
これを4倍に拡大することで1/4サンプリングが再現される．このようにIMGを1/2に縮小してして8倍に拡大，1/2に縮小して16倍と続けていくことでそれぞれのサンプリング結果が再現される．
　以下にそれぞれの結果を示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-3.png?raw=true)

図3 1/4サンプリング画像

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-4.png?raw=true)

図4 1/8サンプリング画像

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-5.png?raw=true)

図5 1/16サンプリング画像

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai1/kadai1-6.png?raw=true)

図6 1/322サンプリング画像

　このようにサンプリング幅が大きくなると，モザイク状のサンプリング歪が発生していく．　
　