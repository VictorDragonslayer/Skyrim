[**FAQ для ньюфагов**](http://pastebin.com/v0S70qvW)

Решив обмазать Скайрим модами, ты должен понять, что **легко не будет**. Ты можешь следовать шапке, а можешь и не следовать, но во втором случае тебе будет не только трудно, но и больно, т.к. игру ты похеришь не раз и не два. Список модов и утилит, приведённых ниже, **является необходимым минимумом**, поэтому не плачь и не вопи про злых анонов, когда тебя посылают на хуй из-за отсутствия МО/ENBoost'а/Crash Fixes и т.п. В шапке есть необходимые инструкции и документации, поэтому слова "читай шапку" ВНЕЗАПНО значат то, что значат. Итак, тебе нужны:

1. **Скайрим** последней версии (1.9.32.08, Legendary Edition). Если ставишь репак - проверяй, чтобы ничего не было вырезано/перекодировано™, а также что добрые васяны не напихали туда предустановленных модов.

2. [**SKSE**](http://skse.silverlock.org/) - скриптовое расширение, без которого накроется приличная часть модов. Запускать Скайрим ты будешь именно через него. В skse 1.7.0+ встроен MemoryPatch - увеличит стабильность (есть альтернатива получше - читай ниже). Встроенный патч активируется закидыванием [этого ini](http://www.nexusmods.com/skyrim/mods/51038/?) с заменой в папку \Data\SKSE\. Для пираток приписываем -forcesteamloader в свойствах ярлыка (путь к объекту; для МО - в строке "аргументы" в ярлыке запуска). Если игра запускается через МО - приписываем в нём это в любом случае, даже если стоит лицензия.

3. **Мод-менеджер**: Mod Organizer и Wrye Bash.
  [Mod Organizer](http://www.nexusmods.com/skyrim/mods/1334/?) - хорош тем, что не ставит моды в директорию игры. Он держит их в своих директориях и при запуске создает виртуальное окружение. То есть, в папке скайрима (в Data) ты ничего не найдёшь. Требует стандартный набор хромосом и прохождение обучалки, которая появится при первом запуске МО (если что, подробный гайд есть на STEP), но спасает в случае возникновения проблем в игре, предоставляя возможность отключить проблемный мод без необходимости переустановки всех остальных модов, а то и игры;
  **НЕ СТАВИШЬ МОДЫ ЧЕРЕЗ МО - В ТРЕДЕ ТЕБЕ НЕ ПОМОГУТ.**

  Видеогайды по программе: http://pastebin.com/GHC1aBLK

  Инструкция для не могущих в английский: http://gamer-mods.ru/load/tes_v_skyrim/instrumentarij/mod_organizer/59-1-0-2739

  Программы, которые в процессе работы обращаются к твоим модам (Wrye Bash, LOOT и т.д.) должны запускаться через МО, иначе они не увидят установленные моды. Для запуска программы через МО её нужно добавить: нажми на значок с двумя шестерёнками, после чего в поле *Исполняемый файл* укажи полный путь к файлу программы. Если программа была установлена через МО (например, так можно сделать с FNIS'ом), то в виртуальной папке Data (средняя вкладка) найди файл (.exe/.jar/т.п.), сделай по нему правый клик и выбери "Добавить как исполняемый".

  **Внимание**: создай профиль, отличный от Default, и обмазывай именно его.

  [Wrye Bash](http://skyrim.nexusmods.com/mods/1840/?) - прога, устанавливающая и патчящая моды. Нужно ставить для совмещения нескольких модов, изменяющих уровневые листы (leveled lists), посредством bashed patch'а, иначе в уровневых листах окажутся предметы лишь из последнего мода, который означенные листы затрагивает.

4. **Сортировщик порядка загрузки модов** - реорганизует порядок загрузки модов, т.к он очень важен. Однако, помни, что программа - не панацея, поэтому всегда сверяйся с описаниями модов и допроверяй вручную.

  [LOOT](http://loot.github.io) - преемник ныне почившего BOSS'а. При использовании Mod Organizer следует добавить LOOT к запускаемым программам и запускать через МО. Встроенный LOOT (кнопка Sort во вкладке Plugins) **НЕ ИСПОЛЬЗУЙ**, т.к. он косячит.

5. [**FNIS**](http://www.nexusmods.com/skyrim/mods/11811/?) - позволяет добавлять и использовать новые анимации. Необходим практически для всех модов, добавляющих\изменяющих какую-либо анимацию. Без него те просто не будут работать. Необходимо генерировать Data\tools\GenerateFNIS_for_Users\GenerateFNISforUsers.exe фнис КАЖДЫЙ раз, как установил\удалил мод на анимацию. Неписи встали враскоряку? Сгенерируй фнис. И всегда внимательно смотри, какие галочки в нём тыкаешь. Алсо, если ставишь нестандартных существ и после генерации FNIS-патча анимация сломана - удали из FNIS Creature Pack (кнопка De-Install Creatures прямо во FNIS).

6. [**TES5Edit**](http://www.nexusmods.com/skyrim/mods/25859/?) - инструмент для чистки "грязных" правок, сравнения перезаписей в плагинах и разрешения конфликтов. С его помощью также можно создать merged patch - данный плагин попытается устранить конфликты в записях (пример: один плагин изменяет урон меча, другой - вес; merged patch будет содержать в себе запись, в которой изменены и урон, и вес этого меча). Из патча рекомендуется удалить изменения, касающиеся уровневых листов, т.к. Wrye Bash справляется с их объединением лучше.

  Ссылки и гайды по программе: http://pastebin.com/raw.php?i=fXaYr3ad

  [Merge Plugins Standalone](http://www.nexusmods.com/skyrim/mods/69905/?) - позволяет соединять несколько плагинов вместе, дабы уложиться в лимит (255).

7. **Чистильщики сейвов** - очищают сейвы от ошибочных записей и скриптов (например, из удалённых модов), а также память объектов Havok (записи о каждой сдвинутой тобой тарелке). Может оживить убитый сейв и улучшить работу нормального (но сейв умер по твоей вине, поэтому борись с причиной, а не следствиями). Если любите расставлять всякие безделушки в доме - не чистите хавок, иначе всё сбросится. И делайте бэкап сейва, если программа сама его не делает.

  [Save Game Script Cleaner](http://www.nexusmods.com/skyrim/mods/52363/?) - более свежий и более простой, делает всю работу за два клика.
  Инструкция: http://pastebin.com/raw.php?i=pPvwkDVp

  [SKYRIM Save Cleaner](http://www.nexusmods.com/skyrim/mods/31724/?) - первый из созданных, требует некоторых телодвижений перед работой.
  Инструкция: http://pastebin.com/raw.php?i=WcWXpRPB

  [Papyrus Data Transfer](http://www.nexusmods.com/skyrim/mods/53045/?) - более сложная, но наиболее продвинутая утилита по очистке и правке работы скриптов.
  Видеоинструкция (на английском): http://pastebin.com/raw.php?i=BEv5w0Pw

  [ReSaver](http://www.nexusmods.com/skyrim/mods/76776/?) - позволяет чистить сохранения, в которых превышен лимит строк.

8. **Оптимизаторы текстур и мешей** - http://pastebin.com/raw.php?i=R9UvUmXd

9. [**SkyUI**](http://www.nexusmods.com/skyrim/mods/3863/?) - мод, обязательный для большинства модов, поскольку добавляет возможность их настройки через специальные меню (MCM Menu). К тому же ванильный интерфейс может понравиться только ~~говноеду~~ консольщику, а сабж приводит его в божеский вид. Если же хочешь иметь МСМ-меню, но оставить оригинальный интерфейс - то ставь к нему [SkyUI-Away](http://www.nexusmods.com/skyrim/mods/29440/?).

10. **ENBoost** - позволяет использовать фиксы производительности из ЕНБ без самих графических фич ЕНБ. Скачай архив последней версии с http://enbdev.com/download_mod_tesskyrim.html Файл enblocal.ini требует допиливания под конкретный компьютер, подробности читай тут: https://www.reddit.com/r/skyrimmods/wiki/enb и https://www.reddit.com/r/skyrimmods/wiki/enboost .

11. [**Crash Fixes**](http://www.nexusmods.com/skyrim/mods/72725/?) - SKSE-плагин, предотвращающий некоторые краши (настоятельно рекомендую включить аллокаторы, которые изменят механизм использования памяти игрой: http://pastebin.com/t5ry6eHb).

12. [**BethINI**](http://www.nexusmods.com/skyrim/mods/69787/?) - утилита для настройки инишников, имеет более качественные пресеты, дружит с МО.

13. [**USLEEP**](http://www.nexusmods.com/skyrim/mods/71214/?) - неофициальный патч, исправляющий хренову гору багов. Если хочешь играть с Hi-res DLC, то тебе также нужен [этот патч](http://www.nexusmods.com/skyrim/mods/31255/?).

14. **Работающий мозг (хотя бы 50%) и прямые руки (хотя бы 1 шт.)** - от тебя требуется знание основных понятий, таких как: порядок загрузки, чистый сейв, уровневый лист и т.п., а также изучение хотя бы одной статьи отсюда - http://wiki.tesnexus.com/index.php/Category:Elder_Scrolls_-_Installing_mods

**Так, теперь немного пастоты и ссылок:**

[**ликбез**](http://pastebin.com/R6nqTUB9)

[**список опасных модов**](https://www.reddit.com/r/skyrimmods/wiki/dangerous_mods_masterlist)

[**обучающие видео и список модов для оптимизации**](https://docs.google.com/document/d/15JX4Fygvc6bjve2EtCoOI_CBXqiqivR-R3mp5kX4iBI/)

[ссылкота](http://pastebin.com/3vmhptdC)

[**Пастебиновская версия шапки. При необходимости юзай для переката.**](http://pastebin.com/zz135qGb)

**С вопросами по Реквиему идём в их собственные отдельные треды, с вопросами по SkyRe и ПерМе идём в музей.**

**Сборок нет и НЕ БУДЕТ.** Ленивые/недовольные идут лесом.

**Гайды по решению наиболее распространённых проблем**:

https://www.reddit.com/r/skyrimmods/wiki/troubleshooting_guide

https://www.reddit.com/r/HiddenTroubleshooting/wiki/last_resort

Есть светлые идеи по поводу изменения шапки? Не устраивай срач и не вопи, что шапка говно - пости их в треде, облекая в конкретную форму.

Пока всё. Читай пасты, задавай вопросы, получай ответы. Добродвач же.
