## エクスプローラ右クリックにVSCodeで開くメニューを追加
- 下記キーを設定
- HKEY_CURRENT_USER\Software\Classes\Directory\shell\VSCode\command
  - 規定に  
    "C:\Users\fkhid\AppData\Local\Programs\Microsoft VS Code\Code.exe" "%V"  
    と設定
- HKEY_CURRENT_USER\Software\Classes\Directory\Background\shell\VSCode\command
  - 規定に  
    "C:\Users\fkhid\AppData\Local\Programs\Microsoft VS Code\Code.exe" "%V"  
    と設定
