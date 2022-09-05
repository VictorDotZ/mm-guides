### В чем пишу код.

Ноутбук, на нем Windows 11, версии 21H2 и билда 22000.918, позволяющие ~~без проблем~~ [устанавливать](https://docs.microsoft.com/en-us/windows/wsl/install) и [работать](https://code.visualstudio.com/docs/remote/wsl) с [WSL2](https://docs.microsoft.com/en-us/windows/wsl/about).
  
Текстовый редактор: [Visual Studio Code](https://code.visualstudio.com/), с [расширением](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) для [удобной работы](https://code.visualstudio.com/docs/remote/wsl-tutorial) с WSL.

Дистрибутив Linux для WSL: Ubuntu 22.04 LTS. На ней `gcc`, `g++`, `valgrind`, [сервер VSCode](https://code.visualstudio.com/docs/remote/wsl-tutorial#_run-in-wsl) (`code .`), и в VSCode локально на Ubuntu [расширение для C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools).

На Windows `отсутствует` какой-либо компилятор C/C++. На Ubuntu всё запускается из [интегрированного терминала VSCode](https://code.visualstudio.com/docs/editor/integrated-terminal) (<kbd>CTRL</kbd>+<kbd>SHIFT</kbd>+<kbd>`</kbd>, последняя клавиша это ~ (тильда), обычно там буква "Ё", она располагается под Esc (эскейпом)).

> [см. как сделать также](my-stack-guide.md)