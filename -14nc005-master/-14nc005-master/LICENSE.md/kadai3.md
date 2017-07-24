https://github.com/mackhasegawa/lecture_image_processing.git

% 課題３　閾値処理
% 閾値を4パターン設定し,閾値処理た画像を示せ．
% 下記はサンプルプログラムである．
% 課題作成にあたっては「Lenna」以外の画像を用いよ．

ORG=imread('NEKOIMG_7215_TP_V.jpg'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
にて原画像を白黒濃淡画像に変換し、表示させる。

![kadai3_1](https://user-images.githubusercontent.com/28531844/28503565-c6217b18-7044-11e7-9d30-39c9ffc7c23e.png)

図1　白黒濃淡画像

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;
のコードにて、閾値を64と決め、輝度値が64以上の画素が黒の2階調画像が表示させる。

![kadai3_2](https://user-images.githubusercontent.com/28531844/28503549-596b8edc-7044-11e7-8014-2badbc42601d.png)

図2　閾値64の時の画像

閾値を96、128、192と変えたとき以下の図のようになる。

![kadai3_3](https://user-images.githubusercontent.com/28531844/28503576-18da2cd8-7045-11e7-8681-9e905dcb52f7.png)

図3　閾値96の時の画像

![kadai3_4](https://user-images.githubusercontent.com/28531844/28503577-18db11d4-7045-11e7-88d5-7daf94155b9b.png)

図4　閾値128の時の画像

![kadai3_5](https://user-images.githubusercontent.com/28531844/28503578-18dfbb76-7045-11e7-8867-0a4d9a8aa9c6.png)

図5　閾値192の時の画像

