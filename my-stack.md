### В чем пишу код.

Ноутбук, на нем Windows 10 выпуска Pro или лучше, версии 21H1 и билда 19043.1266, позволяющие ~~без проблем~~ [устанавливать](https://docs.microsoft.com/en-us/windows/wsl/install) и [работать](https://code.visualstudio.com/docs/remote/wsl) с [WSL2](https://docs.microsoft.com/en-us/windows/wsl/about). (А еще [включен](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v) [Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/))
  
Текстовый редактор: [Visual Studio Code](https://code.visualstudio.com/), с [расширением](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) для [удобной работы](https://code.visualstudio.com/docs/remote/wsl-tutorial) с WSL.

Дистрибутив Linux для WSL: Ubuntu 20.04 LTS. На ней `gcc`, `g++`, `valgrind`, [сервер VSCode](https://code.visualstudio.com/docs/remote/wsl-tutorial#_run-in-wsl) (`code .`), и в VSCode локально на Ubuntu [расширение для C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools).

С компиляторами для C++ на Windows не дружу. На Ubuntu делаю всё из [интегрированного терминала VSCode](https://code.visualstudio.com/docs/editor/integrated-terminal) (<kbd>CTRL</kbd>+<kbd>SHIFT</kbd>+<kbd>`</kbd>).