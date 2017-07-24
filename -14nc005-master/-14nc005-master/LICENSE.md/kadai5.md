https://github.com/mackhasegawa/lecture_image_processing.git

% 課題５　判別分析法
% 判別分析法を用いて画像二値化せよ．
% 下記はサンプルプログラムである．
% 課題作成にあたっては「Lenna」以外の画像を用いよ．

ORG=imread('NEKOIMG_7215_TP_V.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;
濃淡画像を表示させる。

C1 = H(1:i); %ヒストグラムを2つのクラスに分ける
C2 = H(i+1:256);
n1 = sum(C1); %画素数の算出
n2 = sum(C2);
myu1 = mean(C1); %平均値の算出
myu2 = mean(C2);
sigma1 = var(C1); %分散の算出
sigma2 = var(C2);
このコードでヒストグラムを２つのクラスに分け、それぞれの画素数、平均値、分散を算出し、
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出
if max_val<sigma_B/sigma_w
max_val = sigma_B/sigma_w;
max_thres =i;
このコードでクラス内外分散を算出する。

IMG = ORG > max_thres;
imagesc(IMG); colormap(gray); colorbar;
算出した結果を濃淡画像と比較し、濃淡画像より低ければ画像を表示する。

よって、下記の図のような背景と物体がはっきりとした判別分析法を用いた2値化画像を表示できる。

![kadai5_1](https://user-images.githubusercontent.com/28531844/28505510-9471feb0-705f-11e7-8e2d-94ca8a9ff377.png)

図1　判別分析法の2値化画像
