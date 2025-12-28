# PHP

## PHPをVSCode+XAMPPでデバッグする設定 (XAMPP設定)
- phpにXdebugをインストールする
  - https://xdebug.org/
  - https://xdebug.org/wizard  
    に対象のphpinfoを張り付ける。
  - ウィザードに必要なdllと使い方の説明が出てくるのでそれに従う。
    - 指定されたファイルを指定パスに移動(要ファイルリネーム)
    - php.iniの編集
      - zend_extension = xdebug
  - php.iniの最後に下記を追加(要パス調整)
```
[XDebug]
zend_extension = "E:\xampp\php\ext\php_xdebug.dll"
xdebug.mode = debug
xdebug.start_with_request = yes
xdebug.client_host = 127.0.0.1
xdebug.client_port = 9003
xdebug.log = "E:\xampp\tmp\xdebug.log"
xdebug.log_level = 7
```

## PHPをVSCode+XAMPPでデバッグする設定 (VSCode設定)
- VSCode に PHPDebugをインストールする
- ワークスペース設定
  - サイドバーの「実行とデバッグ」アイコンをクリック
  - 「create a launch.json file」をクリック
  - 「PHP : Listen for Xdebug」を選択
    - 基本的には自動生成された内容で良いが下記のような内容
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Listen for Xdebug",
            "type": "php",
            "request": "launch",
            "port": 9003,
            "pathMappings": {
                "/var/www/html": "${workspaceFolder}"
            }
        },
        {
            "name": "Launch currently open script",
            "type": "php",
            "request": "launch",
            "program": "${file}",
            "cwd": "${fileDirname}",
            "port": 9003
        }
    ]
}
```
