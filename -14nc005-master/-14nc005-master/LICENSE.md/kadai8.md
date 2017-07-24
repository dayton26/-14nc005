% 課題８ ラベリング
% 二値化された画像の連結成分にラベルをつけよ．
% 下記はサンプルプログラムである． 
% 課題作成にあたっては「Lenna」以外の画像を用いよ． 

ORG = imread('NEKOIMG_7215_TP_V.jpg'); % 画像の読み込み
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
濃淡画像を表示させる。

IMG = ORG > 128; % 閾値128で二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
閾値128で二値化し、画像を表示する。

![kadai8_1](https://user-images.githubusercontent.com/28531844/28506199-95be39f0-7064-11e7-979b-3f9174cbce4a.png)

図1　閾値128の二値化画像

IMG = bwlabeln(IMG);
imagesc(IMG); colormap(jet); colorbar; % 画像の表示
bwlabeln関数で二値化画像にラベルをつけることで下記の画像が表示される。

![kadai8_2](https://user-images.githubusercontent.com/28531844/28506218-bbb19db4-7064-11e7-9f6a-1f52176df2a3.png)

図2　ラベリング後二値化画像

