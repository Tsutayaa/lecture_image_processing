# 課題4レポート

標準画像「橋本環奈」を原画像とする．この画像は縦680画像，横453画素のディジタルカラー画像である．
clear; % 変数のオールクリア

ORG=imread('Lenna.png'); % 原画像の入力
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar;
pause;
によって，原画像を読み込み，表示した結果を図１に示す．
![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai4.1.jpg)
図1 原画像

 ヒストグラムの表示を図２に示す．
imhist(ORG); % ヒストグラムの表示
![原画像](https://github.com/Tsutayaa/lecture_image_processing/blob/master/image/kadai4.2.jpg)
 図2 ヒストグラムの表示

濃度の高いところにグラフの山ができていることが分かった。
