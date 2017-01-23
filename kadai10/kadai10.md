# 課題レポート１０

エッジ抽出を体験せよ．

　原画像として以下のようなグレースケール画像を使用する．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai10/kadai10-1.png?raw=true)

図1　原画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//ここまでコード//

　まず，プレウィット法によってエッジ抽出を行う．以下にコードと画像を示す．

	//ここからコード//
	IMG = edge(ORG,'prewitt'); 
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//ここまでコード//

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai10/kadai10-2.png?raw=true)

図2　プレウィット法によるエッジ抽出

　次に，ソベル法によるエッジ抽出を行う．以下にコードと画像を示す．

	//ここからコード//
	IMG = edge(ORG,'sobel');
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//ここまでコード//

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai10/kadai10-3.png?raw=true)

図3　ソベル法によるエッジ抽出

　これらのエッジ抽出法はどちらも，X方向，Y方向別々にエッジ抽出を行い，結果を合成するものである．プレウィット法では中央部が1，ソベルの場合は中央部の画素が2とされるため，多少の差が出ている．
　最後にキャニー法によってエッジ抽出を行う．以下にコードと画像を示す．

	//ここからコード//
	IMG = edge(ORG,'sobel');
	imagesc(IMG); colormap(gray); colorbar; axis image;
	//ここまでコード//

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai10/kadai10-4.png?raw=true)

図4　キャニー法によるエッジ抽出

　キャニー法は複数ステップによって行われるエッジ抽出法である．かなり高性能な方法であり，画像からもエッジ抽出がかなりできていることが見て取れる．
　


