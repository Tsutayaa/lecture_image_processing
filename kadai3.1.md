# 課題3レポート

標準画像「橋本環奈」を原画像とする．この画像は縦680画像，横453画素のディジタルカラー画像である．

clear; % 変数のオールクリア

ORG=imread('橋本環奈.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示
pause; % 一時停止

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.1.jpg) 
図1 原画像

原画像を2階調にするには，以下のプログラムを用いる

IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;
pause;


2階調の結果を図２に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.2.jpg)
図2 2階調画像

同様に原画像を4階調にするには，以下のプログラムを用いる

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;
pause;

とする．4階調の結果を図３に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.3.jp)  
図3　4階調画像

同様に原画像を8階調にするには，以下のプログラムを用いる

IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>224;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
imagesc(IMG); colormap(gray); colorbar;  axis image;

とする．8階調の結果を図4に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.4.jpg)
図5　８階調画像

このように階調が高くなるにつれ，画像を表現するドットは白、薄いグレー、グレー、濃いグレー、黒という様に濃淡をより細かく設定する事が出来るようになり、滑らかな画像を表現できる様になった。



% 課題３　閾値処理
% 閾値を4パターン設定し,閾値処理た画像を示せ．
% 下記はサンプルプログラムである．
% 課題作成にあたっては「Lenna」以外の画像を用いよ．

clear; % 変数のオールクリア

ORG=imread('Lenna.png'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;
pause;

IMG = ORG > 96;
imagesc(IMG); colormap(gray); colorbar;
pause;

IMG = ORG > 128;
imagesc(IMG); colormap(gray); colorbar;
pause;

IMG = ORG > 192;
imagesc(IMG); colormap(gray); colorbar;
