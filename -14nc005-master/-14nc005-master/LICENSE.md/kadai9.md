https://github.com/mackhasegawa/lecture_image_processing.git

% 課題９ メディアンフィルタと先鋭化
% メディアンフィルターを適用し，ノイズ除去を体験せよ．
% 各自，Lenna以外の画像を用いよ．
% 例

ORG = imread('NEKOIMG_7215_TP_V.jpg'); % 画像の読み込み
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;
IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;
f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計
IMG = filter2(f,IMG,'same'); % フィルタの適用
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;

![kadai9_1](https://user-images.githubusercontent.com/28531844/28506406-2b6713f4-7066-11e7-8af0-39467b4d9838.png)

![kadai9_2](https://user-images.githubusercontent.com/28531844/28506407-2ee39106-7066-11e7-84c4-25b3f89a1502.png)

![kadai9_3](https://user-images.githubusercontent.com/28531844/28506408-2ef8a794-7066-11e7-8ca6-3fbf5bb1d8a1.png)

![kadai9_4](https://user-images.githubusercontent.com/28531844/28506409-2efc4b92-7066-11e7-9c4b-5789d195f71c.png)










