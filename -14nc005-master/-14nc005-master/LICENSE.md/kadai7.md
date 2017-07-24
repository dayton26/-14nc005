https://github.com/dayton26/lecture_image_processing.git

% 課題7　ダイナミックレンジの拡大
% 画素のダイナミックレンジを０から２５５にせよ． 
% 下記はサンプルプログラムである． 
% 課題作成にあたっては「Lenna」以外の画像を用いよ． 

ORG = imread('NEKOIMG_7215_TP_V.jpg'); % 画像の読み込み
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
濃淡画像を表示させる。
次に下記の関数で濃淡画像のヒストグラムを生成する。
imhist(ORG);

![kadai7_1](https://user-images.githubusercontent.com/28531844/28506055-6fda7ba0-7063-11e7-8bc6-fe48c5198b4d.png)

図1　濃淡画像のヒストグラム

mn = min(ORG(1)); % 濃度値の最小値を算出
mx = max(ORG(255)); % 濃度値の最大値を算出
ORG = (ORG-mn)/(mx-mn)*255;
ここで濃度値の最大値と最小値を算出し、濃度値の平均を求める。

ORG = uint8(ORG); % この行について考察せよ
imhist(ORG); % 濃度ヒストグラムを生成、表示
unit8関数を用いてdouble型であった数値を8ビットに変換することで、下記のようなダイナミックレンジを拡大したヒストグラムを表示させることができる。

![kadai7_2](https://user-images.githubusercontent.com/28531844/28506071-8dc6c54c-7063-11e7-93e7-f2d94fe40af3.png)

図2　ダイナミックレンジ拡大後のヒストグラム
