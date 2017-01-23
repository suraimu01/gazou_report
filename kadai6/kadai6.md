# 課題レポート６

ディザ法を用いて画像を二値化せよ．

　原画像として以下のようなグレースケール画像を使用する．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai6/kadai6-1.png?raw=true)

図1　原画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//ここまでコード//

　まず，閾値を中央にした場合の画像と実現させるコードを示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai6/kadai6-2.png?raw=true)

図2　閾値128の二値化画像

	//ここからコード//
	IMG = ORG>128;
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//ここまでコード//

　次に，ディザ法によって二値化した画像と実現させるコードを示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai6/kadai6-3.png?raw=true)

図3　ディザ法による二値化画像

	//ここからコード//
	IMG = dither(ORG); 
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//ここまでコード//

　二つの二値化画像を比べると，ディザ法による二値化画像は一見ノイズが入ってしまったようにも見えるが，普通の二値化画像とは違い，原画像と似た色合いに見える．
このように，ディザ法によって，画像自体は荒くなるが，ビット数を抑えて再現することができる．