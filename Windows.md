## エクスプローラ右クリック

### VSCodeで開くメニューを追加
- HKEY_CURRENT_USER\Software\Classes\Directory\shell\VSCode\command
  - 規定に  
    "C:\Users\[USER]\AppData\Local\Programs\Microsoft VS Code\Code.exe" "%V"  
    と設定
- HKEY_CURRENT_USER\Software\Classes\Directory\Background\shell\VSCode\command
  - 規定に  
    "C:\Users\[USER]\AppData\Local\Programs\Microsoft VS Code\Code.exe" "%V"  
    と設定

### SakuraEditorで開くメニューを追加
- HKEY_CLASSES_ROOT\*\shell\Edit with Sakura Editor\command
  - 規定に  
    "C:\Program Files (x86)\sakura\sakura.exe" "%1"  
    と設定


## スリープ
- 最後にスリープが解除された原因を調べる
  - powercfg /lastwake
