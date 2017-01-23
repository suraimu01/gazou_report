# 課題レポート４

画素の濃度ヒストグラムを生成せよ．

　原画像として以下のようなグレースケール画像を使用する．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai4/kadai4-1.png?raw=true)

図1　原画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//ここまでコード//

　この画像の濃度ヒストグラムを以下に示す．濃度ヒストグラムは，画像にある画素の濃度別の分布を表す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai4/kadai4-2.png?raw=true)

図2　原画像の濃度ヒストグラム

　濃度ヒストグラムから，この原画像は暗めの画素が多いことがわかる．
　濃度ヒストグラムの表示は，以下のコードで再現できる．

	//ここからコード//
	imhist(ORG);
	//ここまでコード//

　次に，原画像の濃度ヒストグラムを均一化したものを用意し，濃度ヒストグラムを表示する．
均一化には，以下のコードを使用する．

	//ここからコード//
	IMG = histeq(ORG,256);
	//ここまでコード//

　これにより，原画像を256の濃度ヒストグラムにより均一化した画像がIMGに代入される．
ここで256を指定してやらなければ，64の濃度ヒストグラムで均一化してしまうため，原画像との比較のため指定している．
　以下に均一化を行った画像と濃度ヒストグラムを以下に示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai4/kadai4-3.png?raw=true)

図3　均一化を行った画像

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai4/kadai4-4.png?raw=true)

図4　均一化を行った画像の濃度ヒストグラム

　原画像より全体的に明るくなり，ヒストグラムも明るい画素が増加したのが見て取れる．
