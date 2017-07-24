https://github.com/dayton26/lecture_image_processing.git

$ git branch <14nc005kadai>

課題1
% 課題１　標本化間隔と空間解像度
% 画像をダウンサンプリングして（標本化間隔を大きくして）
% 表示せよ．
% 下記はサンプルプログラムである．
% 課題作成にあたっては「Lenna」以外の画像を用いよ．

この課題で使用する画像は、「NEKOIMG_7215_TP_V.jpg」である。

ORG=imread('NEKOIMG_7215_TP_V.jpg'); % 原画像の入力
ORG = rgb2gray(ORG);
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
このコードで原画像を表示させる。

原画像に図1のようになる。

![kadai1_1](https://user-images.githubusercontent.com/28531844/28501269-7538354c-7013-11e7-9e75-d190c64a9362.png)
図1


次に
IMG = imresize(ORG,0.5); % 画像の縮小
IMG2 = imresize(IMG,2,'box'); % 画像の拡大
の値を変えることによって標本化間隔を調整することができ、サンプリング間隔が細かいほど画像は粗くなる。

![kadai1_4](https://user-images.githubusercontent.com/28531844/28501329-a66eba9a-7014-11e7-95c1-f5d6cb14cd8a.png)

図2　1/8サンプリング画像

![kadai1_5](https://user-images.githubusercontent.com/28531844/28501337-d57046d8-7014-11e7-8293-8c8a02d6b650.png)

図3　1/16サンプリング画像

![kadai1_6](https://user-images.githubusercontent.com/28531844/28501339-eba4b1b4-7014-11e7-8b2e-b95965f936e3.png)

図4　1/32サンプリング画像
