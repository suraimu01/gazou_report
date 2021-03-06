# 課題２レポート

２階調，４階調，８階調の画像を生成せよ．

　原画像として以下のようなグレースケール画像を使用する．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai2/kadai2-1.png?raw=true)

図1　原画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//ここまでコード//

　画像を表示する際，colorbarを同時に表示している．フルカラー画像をグレースケールに変換しているため，0〜255で表示されている．
　原画像を2階調の画像にするには，以下のコードで行う．

	//ここからコード//
	IMG = ORG>127;
	imagesc(IMG); colormap(gray); colorbar;  axis image;
	//ここまでコード//

　このコードではIMGに127より上の色のピクセルのみを1として代入し，表示している．これにより，127以下と128以上の2種類の部分が現れる．以下に表示された画像を示す．


![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai2/kadai2-2.png?raw=true)

図2　2階調画像

　このように白と黒の2種類で表される画像が得られる．
　4階調にするには，以下のコードで行う．

	//ここからコード//
	IMG0 = ORG>63;
	IMG1 = ORG>127;
	IMG2 = ORG>191;
	IMG = IMG0 + IMG1 + IMG2;
	imagesc(IMG); colormap(gray); colorbar;  axis image;
	//ここまでコード//

　IMG0，IMG1，IMG2にそれぞれ64以上，128以上，192以上の色のピクセルを1として代入し，それらを全て足すことで4階調を再現している．以下に表示された画像を示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai2/kadai2-3.png?raw=true)

図3　4階調画像

　4つの色によって原画像が表される．
　8階調も同じように，分割して代入したものを足してやればよい．以下にコードを示す．

	//ここからコード//
	IMG0 = ORG>31;
	IMG1 = ORG>63;
	IMG2 = ORG>95;
	IMG3 = ORG>127;
	IMG4 = ORG>159;
	IMG5 = ORG>191;
	IMG6 = ORG>223;
	IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
	imagesc(IMG); colormap(gray); colorbar;  axis image;
	//ここまでコード//

　以下に表示された画像を示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai2/kadai2-4.png?raw=true)

図4　8階調画像

　2階調画像と比べるとだいぶ原画像に近づいていることがわかる．