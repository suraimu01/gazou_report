# 課題レポート８

二値化された画像の連結成分にラベルをつけよ． 

　原画像として以下のようなグレースケール画像を使用する．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai8/kadai8-1.png?raw=true)

図1　原画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//ここまでコード//

　そして原画像を二値化画像に変換した画像が以下である．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai8/kadai8-2.png?raw=true)

図2　二値化画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	IMG = ORG > 128;
	imagesc(IMG); colormap(gray);  colorbar; axis image;
	//ここまでコード//

　この画像をbwlabelnによって８連結でラベリングし，ラベルごとに色分けすると，以下のような画像となる．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai8/kadai8-3.png?raw=true)

図3　ラベルごとに色分けした画像

　色が同じ場所が連結している部分である．
　この画像は以下のコードによって再現される．

	//ここからコード//
	IMG = bwlabeln(IMG); 
	imagesc(IMG); colormap(gray);  colorbar; axis image;
	//ここまでコード//