# Где писать код и как запускать программы?

> Это ни в коем случае не жесткие условия, вы вольны комбинировать подходы между собой, придумывать свои собственные, что-то искать и пробовать. В первую очередь всё это посвящается либо начинающим свой путь в области "работы на ЭВМ" на мехмате, либо продолжающим, но по каким-то причинам еще не успевшим познакомиться со способствующими продуктивности инструментами и отказаться от порочных практик, затрудняющих работу.

> Windows 11 по умолчанию имеет многие вещи, которые необходимо включать или устанавливать на Windows 10, поэтому если у вас 11 версия, то не задумываясь о требованиях можете выбрать "элегантный вариант" и наслаждаться жизнью.

Все решения будут так или иначе подразумевать работу с терминалом, ни в коем случае не стоит этого бояться! Страшно и непонятно только в стенах любимого вуза, а в реальности не сложнее чем написать сообщение в чате. Какие-то команды, на самом деле, можно настроить выполняться по нажатию кнопочек, но в свое время один преподаватель, не поняв такой магии, отказался принимать у меня задачи... так что от греха подальше обойдемся без кнопочек, тем более что всё будет действительно просто. [Тут](terminal-tiny-guide.md) есть всё необходимое для этого.

## Вариант 0 - «Грустный»

Речь про компьютеры на любимом факультете - всё действительно очень грустно. Установка сторонних программ, по возможности, заблокирована, поэтому пользоваться придется тем что есть - разок я попытался собрать [VSCode](https://code.visualstudio.com/) из исходников и это даже получилось! но учетная запись от таких приколов сломалась и до конца жизни (благо недолгой) сидеть мне приходилось под гостем.

Компилятор выбрать не получится, у вас есть только адски настроенный gcc 4й версии, который бьет по рукам за любую "ошибку". Довольно часто это доводится до абсурда: качественный код, за который заплачены огромные деньги и вложены умы лучших специалистов мира не скомпилируется, а говнокод пройдет все проверки на ура.

Зато получится выбрать текстовый редактор. Я начинал с [Geany](https://www.geany.org/), ибо был знаком с ним по школе, но посоветую открыть [QT Creator](https://www.qt.io/product/development-tools), хоть это и больше чем редактор, пользоваться большинством его возможностей вам не придется в любом случае. Самое главное: **не используйте** `vim`, `mcedit`, `gedit`, `cat`. В будущем, быть может, вам доведется поработать с ними, (и более того, вам так понравится, что вы не будете понимать как могли раньше без них обходиться) но пока что без острой необходимости - просто забудьте про них.

О терминале речь пойдет в конце этого руководства.

<!-- TODO: гайд по qt Creator (цветовая тема + автокомплит) -->

## Вариант 1 - «Элегантный»

### "Железо" и ОС

Требуется Windows 10 Pro или лучше, достаточно современной версии - полный список требований можете посмотреть по ссылкам на руководства. Если на каком-то этапе выяснится, что ваш компьютер и система не соответствуют им, то всегда можно выбрать "простой и надежный" вариант.

Установите WSL 2, выберите из доступных понравившейся дистрибутив Linux и наслаждайтесь простым и быстрым доступом прямо из вашей "домашней" системы. Я предпочитаю Ubuntu.

### "Компилятор и редактор"

Компилятор - `gcc` (`g++`) без вопросов. С редактором все интереснее. У VSCode есть специальное расширение для доступа к запущенным таким образом дистрибутивам. Вам не нужно устанавливать его отдельно на Ubuntu как это требуется в паре других вариантов - достаточно только на Windows.

> Если повезет, то к моменту прочтения этого гайда Microsoft добавили поддержку WSLg из коробки, может быть хотя бы для Windows 11 и вы сможете делать вообще всё, т.к. у вас будет легкий доступ к приложениям с графическим интерфейсом, иначе его тоже можно получить, установив и настроив специальные программы, но для "работы на ЭВМ" вам хватит связки WSL + VSCode. В прочем, я видел использование Ubuntu на WSL без графики, когда код редактировался при помощи vim - не наш вариант.

### Резюме

Это действительно элегантное решение и если получилось его "включить", то пользоваться точно имеет смысл.

## Вариант 2 - «Экзотический»

### "Железо" и ОС

Поскольку пользователи Linux дистрибутивов вряд ли читают это, то потребуется Windows, но какой версии - не известно. Речь пойдет про [Docker](https://www.docker.com/). У меня не получалось ни разу установить его легко и просто, каждый раз установка сопровождалась ошибками и непонятно как вообще всё работало. Кто-то даже несколько раз переустанавливал Винду после контакта с данной субстанцией.

Однако если всё получилось и заработало, то дальнейшая эксплуатация по изяществу сравнима с "элегантным" вариантом.

### Компилятор и редактор

У VSCode есть два расширения, одно позволяет относительно просто запускать контейнеры (в нашем случае в контейнерах будут лежать операционные системы - дистрибутивы Linux), а другое - подключаться к этим контейнерам совсем как это происходит в "Элегантном" варианте.

### Резюме

Сначала о плюсах. Это, пожалуй, наипростейший способ получить полную копию "мехмата" не переписывая настроек и не скачивая самостоятельно никаких программ кроме Докера. Но, конечно, может заставить вас поплеваться.

## Вариант 3 - «» (рабочее название: Простой и эффективный)

### "Железо"

[VirtualBox](https://www.virtualbox.org/) и ни слова больше. Не важно Windows 10 у вас или Windows 7, это простое в использовании решение заработает где угодно. Конечно, работа виртуальной машины требует якобы больших мощностей, но на самом деле если у вас не допотопный компьютер - можете не переживать. Иначе стоит обратить внимание на другие варианты, но попробовать в любом случае стоит - вы ничего не теряете и в любой момент можете всё удалить.

Есть огромное множество руководств по установке этого инструмента, я оставлю ссылки на парочку достаточно понятных и качественных из них.

### ОС

В мое время на мехмате стояла Fedora release 20 c ядром 3.15.10-201.fc20.x86_64. Не думаю, что у вас получится найти такую комбинацию ~~говна~~ сейчас, поэтому можете поставить, для идентичности некоторых команд, более современную [Федору](https://getfedora.org/), но в реальности вам эти команды не понадобятся, поэтому смело выбирайте "user-friendly" [Ubuntu](https://ubuntu.com/).

### Компилятор

`gcc` (`g++` для C++) и это не обсуждается. Установившаяся версия будет гораздо современнее, чем на мехмате, но сильно это вам жизнь не ухудшит (скорее, наоборот, улучшит). При желании можно будет настроить всё точь в точь как на мехмате, но, опять же, это не нужно - поберегите нервы и чувство прекрасного.

### Редактор

Для полного погружения текстовый редактор можете установить такой же, какой используете на мехмате. А вообще выбирайте любой на свой вкус. От себя могу посоветовать [Visual Studio Code](https://code.visualstudio.com/) - его возможностей вам хватит для прохождения этого многолетнего квеста чуть больше чем полностью.

### Резюме

Эта комбинация не требовательна к версии Windows, чем и хороша. Я долгое время пользовался виртуальной машиной для "работы на ЭВМ", но не VirtualBox'ом, а [VMWare](https://www.vmware.com/). Стратегия рабочая, разве что совет: сохраняйте важные для вас результаты работы где-то ещё - вне виртуальной машины. Это сбережёт вам время и силы если что-то сломается, а сломаться может. Не стоит тратить время на разбирательства как это починить, просто переустановите всё и продолжайте работу.

> Совет, в принципе, актуален для любого предложенного варианта: учетная запись на мехмате может "сломаться", виртуальная машина повредиться, "натурально" установленный Linux дистрибутив перестать запускаться, а задачи как-то писать и получать зачет надо. Неплохим вариантом было бы использовать `git`, я дам для этого самый минимальный минимум, но если для вас проще будет копировать все файлы на флешки и/или отправлять их в личные сообщения с самим собой - ничего страшного. В любом случае главное просто не остаться без сделанной работы в критически важный момент.

## Вариант 4 - «Ультимативный»

### "Железо" и ОС

Честная установка дистрибутива Linux. Если вы попробовали «простой и рабочий» вариант и имеющаяся скорость работы не устраивает, то можно установить ту же Ubuntu (или Fedora) на отдельный диск, либо на диск рядом с Windows. Если компьютер очень слабый, можно посмотреть в сторону [LXDE](http://www.lxde.org/), [Ubuntu Mate](https://ubuntu-mate.org/) и других, которые находятся по запросу "Lightweight Linux Distributions".

Установка на отдельный диск не представляет проблем, если вы освоили этот этап в VirtualBox, то всё будет хорошо. Установка рядом с Windows уже требует дополнительной подготовки, я приведу несколько подробных и качественных руководств, но коротко опишу что делаю сам.

> Создаю загрузочную флешку с Ubuntu при помощи [Universal USB Installer](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/), загружаюсь с нее в режиме live-cd, открываю `gparted`, выбираю диск с Windows, на который собираюсь установить Ubuntu и "отрезаю" у него с конца часть, как правило 256гб, но вам для "работы на ЭВМ" хватит и 60. Затем выбираю на рабочем столе установку и в процессе указываю получившийся "нераспределенный" участок диска для установки. "Отрезать" можно и из Windows, так получится сразу убедиться что ничего не сломалось, в каком-то руководстве обязательно будет такой метод, но я делаю как делаю.
>
> Из-за распространения SSD дисков может быть не актуально, но когда они не были так распространены, перед тем, как "отрезать" часть, я производил дефрагментацию HDD и консолидацию свободного места при помощи [PerfectDisk](https://www.raxco.com/products/perfectdisk-pro). Подобная функция есть во множестве программ, выбирайте понравившеюся если для вас это актуально.

### Компилятор и редактор

Работа с установленной системой ничем не отличается с описанными практиками для виртуальной машины - устанавливайте те же программы о которых шла речь, выполняйте те же команды - всё идентично. Если понравится можете даже остаться тут "жить".

### Резюме

Способ сложнее и "опаснее" виртуальной машины, но зато "натуральнее". Не советую пользоваться им исключительно для "работы на ЭВМ" - только если виртуальная машина действительно работает медленно. Если вы выбираете установку Linux дистрибутива "для себя", то это руководство в принципе не для вас.
