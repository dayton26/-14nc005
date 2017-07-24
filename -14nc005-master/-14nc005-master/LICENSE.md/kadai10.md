https://github.com/dayton26/lecture_image_processing.git

% 課題10 画像のエッジ抽出 
% 次のプログラムを参考にして，エッジ抽出を体験せよ．
% 各自，Lenna以外の画像を用いよ．

ORG = imread('NEKOIMG_7215_TP_V.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); %カラーからグレイへの変換
imagesc(ORG); colormap('gray'); colorbar;% 画像表示
濃淡画像を表示する。

![kadai3_1](https://user-images.githubusercontent.com/28531844/28506783-b8519ce2-7068-11e7-92ac-73c76c096000.png)

図1　濃淡画像
IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
pause; % 一時停止

図2はプレウィット法によるエッジ抽出は縦横どちらかを先に算出してからそれぞれの平均を取る方法である。コードではedge関数を用いて属性をprewittにすること
によって図2のように表示することができる。

![kadai10_1](https://user-images.githubusercontent.com/28531844/28506608-8e1fb388-7067-11e7-9ba9-0420f5b34e4c.png)

図2　プレウィット法によるエッジ抽出

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
pause; % 一時停止

ソベル法は、注目画素に近いほど平均値の計算の時重みを大きくし、遠いほど小さくするというエッジ抽出である。コードではプレウィット法と同じように属性をsobelにす
ることで図3のように表示することができる。

![kadai10_2](https://user-images.githubusercontent.com/28531844/28506609-8e20315a-7067-11e7-95f6-787a349c778b.png)

図3　ソベル法によるエッジ抽出

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
pause; % 一時停止

キャニー法も他と同じように関数の属性をcannyにすることで実装できる。エッジ抽出後は図4のような画像になる。

![kadai10_3](https://user-images.githubusercontent.com/28531844/28506610-8e221c22-7067-11e7-8b92-ca5d13314685.png)

図4　キャニー法によるエッジ抽出
