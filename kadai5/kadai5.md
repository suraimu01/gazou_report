# 課題レポート５

判別分析法を用いて画像二値化せよ．

　原画像として以下のようなグレースケール画像を使用する．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai5/kadai5-1.png?raw=true)

図1　原画像

　この画像は以下のようなコードで再現できる．

	//ここからコード//
	ORG=imread('original.jpg'); 
	ORG = rgb2gray(ORG); colormap(gray); 
	imagesc(ORG); colorbar; axis image;
	//ここまでコード//

　この画像を判別分析法を用いて閾値を求め，二値化する．
　判別分析法は，ある閾値で二値化したときの双方をクラスとし，それらのクラス間分散とクラス内分散の比である分離度が最大となる値を閾値とする方法である．
判別分析法を実現し，二値化画像を表示するプログラムを以下に示す．

	//ここからコード//
	H = imhist(ORG); 
	myu_T = mean(H);
	max_val = 0;
	max_thres = 1;

	for i=1:255
		C1 = H(1:i); C2 = H(i+1:256);
		n1 = sum(C1);n2 = sum(C2);
		myu1 = mean(C1); myu2 = mean(C2);
		sigma1 = var(C1); sigma2 = var(C2);
		sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); 
		sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2);

		if max_val<sigma_B/sigma_w
			max_val = sigma_B/sigma_w;
			max_thres =i;
		end;
	end;

	IMG = ORG > max_thres;
	imagesc(IMG); colormap(gray); colorbar;axis image;
	//ここまでコード//

　画像のヒストグラムをC1，C2に分け，それらからクラス間分散sigma_Bとクラス内分散sigma_wを求める．
これらの比が以前のmax_valの値よりも大きければ更新し，閾値となるiの値をmax_thresに代入する．これらの操作をヒストグラムの数分繰り返し閾値を求める．
　以下に表示された画像を示す．

![原画像](https://github.com/suraimu01/gazou_report/blob/master/kadai5/kadai5-2.png?raw=true)

図2　判別分析法による二値化画像

