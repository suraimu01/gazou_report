# 課題レポート３

閾値を4パターン設定し,閾値処理した画像を示せ．

　原画像として以下のようなグレースケール画像を使用する．


![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-1.png?raw=true)

図1　原画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//ここまでコード//

　原画像の横にカラーバーを出しており，0～255の輝度が表示されている．
　閾値を64とし，輝度値が64以上のピクセルを1，その他を0とした場合の画像を以下に示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-2.png?raw=true)

図2　閾値64の画像

　輝度が64以上のピクセルが白く表示され，63以下は黒く表示されている．
上の画像を再現するためのコードを以下に示す．

	//ここからコード//
	IMG = ORG >= 64;
	imagesc(IMG); colorbar; colormap(gray); axis image;
	//ここまでコード//

　このように閾値をそれぞれ96，128，192とし，閾値以上を1，その他を0とした画像をそれぞれ以下に示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-3.png?raw=true)

図3　閾値96の画像

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-4.png?raw=true)

図4　閾値128の画像

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai3/kadai3-5.png?raw=true)

図5　閾値192の画像

　また，それぞれを再現するコードを以下に示す．

	//ここからコード//
	//閾値96//
	IMG = ORG >= 96;
	imagesc(IMG);colorbar;colormap(gray); axis image;

	//閾値128//
	IMG = ORG >= 128;
	imagesc(IMG);colorbar;colormap(gray); axis image;

	//閾値192//
	IMG = ORG >= 192;
	imagesc(IMG);colorbar;colormap(gray); axis image;
	//ここまでコード//

　原画像とそれぞれの閾値処理した画像を見比べると，閾値以上が白く，その他が黒くなっていることが確認できる．閾値を低く設定すれば暗い部分が強調され，高くすれば明るい部分が強調される．
　
