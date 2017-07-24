https://github.com/mackhasegawa/lecture_image_processing.git

% 課題２　階調数と疑似輪郭
% ２階調，４階調，８階調の画像を生成せよ．
% 下記はサンプルプログラムである．
% 課題作成にあたっては「Lenna」以外の画像を用いよ．

原画像は全ての課題で「NEKOIMG_7215_TP_V.jpg」を使う。

IMG = ORG>128;
このコードで256色を2分割し、表示させることにより2階調を表現できる。

![kadai2_2kai](https://user-images.githubusercontent.com/28531844/28501368-9c69f7f2-7015-11e7-8a9e-bc3b2f488351.png)

図1　2階調の画像

4階調、8階調では、64色ごとに分け、それらを加算することにより表現できる。

![kadai2_4kai](https://user-images.githubusercontent.com/28531844/28501386-e65d12ea-7015-11e7-93da-6fc1372c162d.png)

図2　4階調の画像

![kadai2_8kai](https://user-images.githubusercontent.com/28531844/28501391-fce0bf1c-7015-11e7-8a0d-a8dc34b21887.png)

図3　8階調の画像
