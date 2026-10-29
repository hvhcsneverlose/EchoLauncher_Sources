# Echo Launcher - Decompiled Files

## RU

Разобрал Echo Launcher для Fortnite, вытащил из установщика всё, что получилось, и разложил по папкам. Тут файлы лаунчера, ресурсы, часть восстановленного кода и дампы нативной части.

Что внутри:
- `01_INSTALLS_ON_WINDOWS` — файлы, которые лежат в установочном пакете.
- `02_NSIS_TEMP_DLL_NOT_GAME_MODS` — 6 DLL установщика NSIS, это не игровые DLL.
- `04_FILES_EMBEDDED_IN_LAUNCHER` — встроенные JS, CSS, картинки и `FortniteLauncher.exe`.
- `05_RECOVERED_CODE` — 17 деобфусцированных JS, .NET IL (42 метода) и дизассемблированная нативная часть.
- `06_REPORTS_PREVIOUS` — команды, заметки по коду и отчёты.
- `07_REPRODUCE_READONLY` — скрипты, которыми можно повторить статический разбор.
- `08_MANIFEST` — список файлов и хеши.

Нативная часть собрана из Rust, так что оригинальных `.rs` тут нет — только ассемблер, импорты, строки и карта функций. Код .NET восстановлен в IL, это тоже не исходный C# проект.

`echo-client.dll`, `sinum.dll` и игровые DLL, которые могут скачиваться при запуске, в самом установщике не нашлись. Не стал добавлять левые файлы и выдавать их за оригинальные.

EXE не запускал, анализ статический. Это не готовый проект для сборки и не официальные исходники Echo Launcher.

## EN

Unpacked the Echo Launcher installer for Fortnite and recovered everything I could: launcher files, embedded assets, readable JavaScript, .NET IL and native disassembly.

Folders:
- `01_INSTALLS_ON_WINDOWS` — packaged installation files.
- `02_NSIS_TEMP_DLL_NOT_GAME_MODS` — 6 NSIS installer DLLs (not Fortnite mods).
- `04_FILES_EMBEDDED_IN_LAUNCHER` — JS, CSS, images and `FortniteLauncher.exe`.
- `05_RECOVERED_CODE` — 17 deobfuscated JS files, 42 .NET method entries and native disassembly.
- `06_REPORTS_PREVIOUS` — notes, command list and reports.
- `07_REPRODUCE_READONLY` — read-only extraction/analysis scripts.
- `08_MANIFEST` — file inventory and hashes.

The native part is compiled Rust, so there are no original `.rs` sources here. The .NET part was recovered as IL, not the original C# project.

Game DLLs such as `echo-client.dll` and `sinum.dll` were not embedded in this installer. No fake or unrelated binaries were added.

Static analysis only; the EXEs were not executed. This is a reverse-engineering dump, not an official or buildable source release.
