### В чем пишу код.

Ноутбук, на нем Windows 10 выпуска Pro или лучше, версии 21H1 и билда 19043.1266, позволяющие ~~без проблем~~ [устанавливать](https://docs.microsoft.com/en-us/windows/wsl/install) и [работать](https://code.visualstudio.com/docs/remote/wsl) с [WSL2](https://docs.microsoft.com/en-us/windows/wsl/about). (А еще [включен](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v) [Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/))
  
Текстовый редактор [Visual Studio Code](https://code.visualstudio.com/), с [расширением](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) для [удобной работы](https://code.visualstudio.com/docs/remote/wsl-tutorial) с WSL.

В качестве Linux системы на WSL стоит Ubuntu 20.04 LTS. На ней установлены `gcc`, `g++`, `valgrind`:
```bash
sudo apt install gcc g++ valgrind
```

 [сервер VSCode](https://code.visualstudio.com/docs/remote/wsl-tutorial#_run-in-wsl) (`code .`), и в VSCode локально на Ubuntu установлено [расширение для C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools). Чтобы настроить как у меня надо нажать <kbd>CTRL</kbd>+<kbd>SHIFT</kbd>+<kbd>P</kbd>, ввести **>Preferences: Open Settings (JSON)**, нажать <kbd>Enter</kbd> и вставить следующий фрагмент, сохранив структуру JSON:
```json
"[cpp]": {
    "editor.tabSize": 4,
    "editor.wordBasedSuggestions": true,
    "editor.semanticHighlighting.enabled": true,
    "editor.defaultFormatter": "ms-vscode.cpptools"
},
"C_Cpp.vcFormat.indent.caseContents": false,
"C_Cpp.vcFormat.indent.namespaceContents": false,
"C_Cpp.vcFormat.newLine.beforeElse": false,
"C_Cpp.vcFormat.newLine.beforeWhileInDoWhile": true,
"C_Cpp.clang_format_fallbackStyle": "Google",
"C_Cpp.clang_format_style": "WebKit",
```
Нажать <kbd>CTRL</kbd>+<kbd>SHIFT</kbd>+<kbd>P</kbd>, ввести **>Preferences: Open Settings (JSON)** > <kbd>Enter</kbd>):

Можно включить [синхронизацию настроек](https://code.visualstudio.com/docs/editor/settings-sync), чтобы не настраивать все каждый раз заново.

С компиляторами для C++ на Windows не дружу. На псевдо Ubuntu делаю всё из [интегрированного терминала VSCode](https://code.visualstudio.com/docs/editor/integrated-terminal) (<kbd>CTRL</kbd>+<kbd>SHIFT</kbd>+<kbd>`</kbd>).