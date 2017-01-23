# 課題レポート９

メディアンフィルターを適用し，ノイズ除去を体験せよ．

　原画像として以下のようなグレースケール画像を使用する．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai9/kadai9-1.png?raw=true)

図1　原画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//ここまでコード//

　原画像に'salt & pepper'ノイズを添付する．このノイズは白い点と黒い点を散らすものである．以下のコードで再現できる．

	//ここからコード//
	ORG = imnoise(ORG,'salt & pepper',0.02); 
	imagesc(ORG); colormap(gray);  colorbar; axis image;
	//ここまでコード//

　ノイズを添付した画像が以下である．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai9/kadai9-2.png?raw=true)

図2　ノイズを添付した画像

　この画像に対し，フィルタをかけてノイズ除去を行う．
　まず，平滑化フィルタによってノイズ除去を行う．以下に再現するコードと画像を示す．

	//ここからコード//
	IMG = filter2(fspecial('average',3),ORG); 
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//ここまでコード//

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai9/kadai9-3.png?raw=true)

図3　平滑化フィルタをかけた画像

　ノイズが減っていることが見て取れる．
　次に，メディアンフィルタによってノイズ除去を行う．以下に再現するコードと画像を示す．

	//ここからコード//
	IMG = medfilt2(ORG,[3 3]);
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//ここまでコード//

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai9/kadai9-4.png?raw=true)

図4　メディアンフィルタをかけた画像

　こちらもノイズが減っている．二つを比べると平滑化フィルタよりメディアンフィルタのほうがノイズの名残が少なく見える．
このことからメディアンフィルタのほうが優れているといえる．