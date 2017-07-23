% 課題４　画像のヒストグラム
% 画素の濃度ヒストグラムを生成せよ．
% 下記はサンプルプログラムである．
% 課題作成にあたっては「Lenna」以外の画像を用いよ．

ORG=imread('NEKOIMG_7215_TP_V.jpg'); % 原画像の入力
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;
このコードにて濃淡画像を表示させ、
imhist(ORG);
関数を用い、ヒストグラムを表示させる。

![kadai4_1](https://user-images.githubusercontent.com/28531844/28503658-eb75e1c8-7045-11e7-9e9a-acb72ba4da9e.png)

図1　濃淡画像

![kadai4_2](https://user-images.githubusercontent.com/28531844/28503659-eb780b10-7045-11e7-9eb4-1eff839ff1d5.png)

図2　ヒストグラム

ヒストグラムから約230付近の色の画素が多いことがわかる。
