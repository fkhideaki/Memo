## インストール
```
git clone https://github.com/microsoft/vcpkg
cd vcpkg
# Windowsの場合
.\bootstrap-vcpkg.bat
# Linux / macOSの場合
./bootstrap-vcpkg.sh
```

## パッケージの追加
`vcpkg install <package>`

## マニフェストモード使用方法
- インストール先フォルダにvcpkg.jsonというファイルを作成
- 下記のような内容にする  
```
{
  "name": "my-project",
  "version-string": "1.0.0",
  "dependencies": [
    "opencv4"
  ]
}
```
- そのファイルがあるフォルダで`vcpkg install`を実行する
