ENG
==================================================
Guide for compiling C code on Windows 95 (VirtualBox)
==================================================

1) Install Watcom C 386 9.01 from the archive. During installation, type "y" or "yes" everywhere.
2) It is recommended to install to C:\WATCOM to avoid additional configuration.

3) Create a SETENV.BAT file in the C:\WATCOM folder with the following content:

@echo off
SET WATCOM=C:\WATCOM
SET INCLUDE=%WATCOM%\H
SET PATH=%WATCOM%\BIN;%WATCOM%\BINW;%WATCOM%\BINP;%WATCOM%\BINB;%PATH%
SET LIB=%WATCOM%\LIB386
ECHO Watcom C 386 ready!

4) Before EVERY compilation, run:
   CALL C:\WATCOM\SETENV.BAT

Compilation commands:
-----------------------
• Console program:
  wcl386 filename.c

• Windows GUI program:
  wcl386 -bt=windows filename.c

• Windows DLL:
  wcl386 -bt=windows -bd filename.c

• 16-bit Windows:
  wcl386 -bt=windows -mf filename.c

• Multiple files:
  wcl386 file1.c file2.c

• With output file name specified:
  wcl386 filename.c -fe=myapp.exe

• Compile only (create .obj):
  wcc386 filename.c

• From .obj to .exe:
  wlink file filename.obj name filename.exe




RUS
==================================================
Гайд по компиляции C-кода на Windows 95 (VirtualBox)
==================================================

1) Установите Watcom C 386 9.01 из архива. Во время установки везде пишите "y" или "yes".
2) Рекомендуется устанавливать в C:\WATCOM, чтобы избежать лишних настроек.

3) Создайте файл SETENV.BAT в папке C:\WATCOM со следующим содержимым:

@echo off
SET WATCOM=C:\WATCOM
SET INCLUDE=%WATCOM%\H
SET PATH=%WATCOM%\BIN;%WATCOM%\BINW;%WATCOM%\BINP;%WATCOM%\BINB;%PATH%
SET LIB=%WATCOM%\LIB386
ECHO Watcom C 386 ready!

4) Перед КАЖДОЙ компиляцией запускайте:
   CALL C:\WATCOM\SETENV.BAT

Команды для компиляции:
-----------------------
• Консольная программа:
  wcl386 имя_файла.c

• Windows GUI программа:
  wcl386 -bt=windows имя_файла.c

• Windows DLL:
  wcl386 -bt=windows -bd имя_файла.c

• 16-bit Windows:
  wcl386 -bt=windows -mf имя_файла.c

• Несколько файлов:
  wcl386 файл1.c файл2.c

• С указанием имени выходного файла:
  wcl386 имя_файла.c -fe=myapp.exe

• Только компиляция (создать .obj):
  wcc386 имя_файла.c

• Из .obj в .exe:
  wlink file имя_файла.obj name имя_файла.exe




   ### Отказ от ответственности / Disclaimer
Данный репозиторий создан исключительно в образовательных целях и для сохранения истории ПО (архивации). 
Все права на Watcom C принадлежат их законным правообладателям. 
Если вы являетесь правообладателем и считаете, что размещение этих файлов нарушает ваши права, 
пожалуйста, создайте "Issue", и файлы будут удалены.

This repository is for educational and historical preservation purposes only. 
All rights to Watcom C belong to their respective owners. 
If you are the copyright holder and wish for these files to be removed, 
please open an "Issue".
