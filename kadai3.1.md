# 課題3レポート

標準画像「橋本環奈」を原画像とする．この画像は縦680画像，横453画素のディジタルカラー画像である．

clear; % 変数のオールクリア

ORG=imread('Lenna.png'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.1.jpg) 
図1 原画像

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;
pause;

 輝度値が64以上の画素を1，その他を0に変換の結果を図２に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.2.jpg)
図2  輝度値が64以上の画素を1，その他を0に変換

同様に原画像を輝度値が96以上の画素を1，その他を0に変換にするには，以下のプログラムを用いる

IMG = ORG > 96; % 輝度値が96以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;
pause;

とする．輝度値が96以上の画素を1，その他を0に変換の結果を図３に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.3.jpg)  
図3　輝度値が96以上の画素を1，その他を0に変換

同様に原画像を輝度値が128以上の画素を1，その他を0に変換にするには，以下のプログラムを用いる

IMG = ORG > 128; % 輝度値が128以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;
pause;

とする．輝度値が128以上の画素を1，その他を0に変換の結果を図4に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.4.jpg)
図4 輝度値が128以上の画素を1，その他を0に変換


同様に原画像を輝度値が192以上の画素を1，その他を0に変換にするには，以下のプログラムを用いる
IMG = ORG > 192; % 輝度値が192以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;

とする．輝度値が192以上の画素を1，その他を0に変換の結果を図5に示す．

![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai3.5.jpg)
図5　輝度値が192以上の画素を1，その他を0に変換

画素を１にする輝度値を高くすればするほど画素が0の割合が高くなり白より黒のほうが多い色黒画像になった。



