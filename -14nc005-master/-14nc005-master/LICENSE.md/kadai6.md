% 課題６　画像の二値化
% 下記のプログラムを参考にして画像を二値化せよ．
% 下記はサンプルプログラムである．
% 課題作成にあたっては「Lenna」以外の画像を用いよ．

ORG=imread('NEKOIMG_7215_TP_V.jpg'); % 原画像の入力
ORG = rgb2gray(ORG);
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
初めに濃淡画像を表示する。

次に、IMG = ORG>128; % 128による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
画素数の半分の閾値を設定することによって2値化画像は表示できる。

![kadai6_1](https://user-images.githubusercontent.com/28531844/28505591-56253a04-7060-11e7-840a-0f75ed388847.png)

この処理をした後、
IMG = dither(ORG); % ディザ法による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
dither関数を使うことで、ディザ法による2値化をすることができ、2値化画像でありながら下記の図のような色の表現ができる。

![kadai6_2](https://user-images.githubusercontent.com/28531844/28505643-bc69c744-7060-11e7-92d1-1879f7830e1c.png)

図2　ディザ法による二値化画像
