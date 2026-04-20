# ImageMagick Setup

## 事前準備
- 下記ををそれぞれ普通にインストール
  - ImageMagick
  - XAMPP
- インストールしたImageMagickにパスを設定

## PHP バージョンとアーキテクチャの確認
- phpinfoから
  - 冒頭のPHP Version からphpのバージョンを確認
  - Thread Safety という項目の値を確認

## php用dll準備
- PECL Windows版ダウンロードページ  
  https://downloads.php.net/~windows/pecl/releases/imagick/  
  の最新版フォルダを開く
- 使用しているバージョンのphpに対応するzipを保存  
  8.2のThreadSafeであれば  
  php_imagick-x.x.x-8.2-ts-xxxx-x64.zip  
  をダウンロード
- zip内の  
  php_imagick.dll  
  を  
  D:\xampp\php\ext  
  に配置
- C:\xampp\php\php.ini  
  に  
  extension=imagick  
  と追加

## インストール確認
- phpinfoに  
  imagick  
  というブロックが表示されれば成功。
