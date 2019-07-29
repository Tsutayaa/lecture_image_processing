# 課題6レポート

標準画像「橋本環奈」を原画像とする．この画像は縦680画像，横453画素のディジタルカラー画像である．

clear; % 変数のオールクリア

ORG=imread('Lenna.png'); % 原画像の入力

ORG = rgb2gray(ORG);

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause; % 一時停止

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai6.1.jpg) 
図1 原画像


IMG = ORG>128; % 128による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

pause;

　画素128二値化の結果を図２に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai6.2.jpg)
図2  画素128の二値化

同様に原画像をディザ法による二値化をするには以下のプログラムを用いる

IMG = dither(ORG); % ディザ法による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai6.3.jpg)  
図3　ディザ法による二値化

ディザ法による二値化は通常の二値化と比べて細かく白黒に分かれている。
