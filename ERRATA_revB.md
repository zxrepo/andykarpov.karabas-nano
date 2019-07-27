1) BUS_N_ROMCS - нет pull-down 10к резистора в схеме и на плате
2) BUS_N_IORQGE - нет pull-down 10k резистора в схеме и на плате
3) TAPE_IN - нет конденсатона 10нФ последовательно с R22 в схеме и на плате
4) Footprint под Z80 имеет некоррентный размер QFP-10x10mm, а нужен QFP-12x12mm, приходится гнуть ноги у процессора
5) Разъем JTAG - если ставить shrouder header, налазит на рядом стоящие резисторы
6) SRAM - отсутствует подача питания на пины 11 - VCC, 12 - GND.
7) LED - необходим светодиод для индикации подачи питания на плату
8) Нет возможности зашить Atmega8 на плате, нужно вывести JTAG пины и возможность не питать всю схему при программировании AVR
9) Нет джампера для (возможного) одключения DivMMC в режиме DivMMC.
10) У разъема клавиатуры нет выхода +5,GND для питания внешнего контроллера, предусмотреть
11) Нет pull-up резистора на линии SD_NCS, не критично, но нужно предусмотреть
12) Генератор: на 28МГц на 74HTC04 заводится с трудом, выкинуть C1 и заменить перемычкой
13) Footprint у 27C512 имеет достаточно короткие пятаки, паять панель руками очень неудобно. Предусмотреть либо длинные PADы, либо другую панель (THT).
