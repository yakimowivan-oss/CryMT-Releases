# CryMT — сборки и лаунчер / builds and launcher

Многопоточный рендер, DirectX 12, NVIDIA DLAA и глобальное освещение для **Crysis (2007)**, 64 бита, патч 1.2.1.
Multithreaded rendering, DirectX 12, NVIDIA DLAA and global illumination for **Crysis (2007)**, 64-bit, patch 1.2.1.

**[Скачать последнюю сборку / Download the latest build](https://github.com/yakimowivan-oss/CryMT-Releases/releases/latest)** · [Исходники / Source](https://github.com/yakimowivan-oss/CryMT)

## Установка

1. Нужен Crysis 1.2.1, 64 бита (сборка 6156): Steam, GOG или диск с патчем 1.2.1.
2. Нужен [c1-launcher](https://github.com/ccomrade/c1-launcher/releases) как `Bin64\Crysis.exe`: GOG ставит v7 сам, подходит v7 или v8. Вылеты 64-битной игры из-за памяти выше 4 ГБ CryMT исправляет сам, если в c1-launcher этого исправления нет (оно есть только в v8).
3. Распакуйте `CryMT-v<N>.zip` в папку игры (туда, где `Bin64`).
4. Запустите `CryMT\CryMTLauncher.exe`, выберите режим и нажмите «Играть».

Режимы:
- **Ваниль** — игра как есть.
- **Только MT** — многопоточность, картинка не меняется. Подходит для модов со своими шейдерами.
- **MT + DX12** — наш рендер DirectX 12.
- **MT + DLAA** — то же + сглаживание NVIDIA DLAA (видеокарты RTX).
- **Полный** — DLAA, глобальное освещение, GTAO, контактные тени, освещение дыма.

Обновления лаунчер ставит сам из этого репозитория (вкладка «Обновления»):
- перед установкой проверяет подпись списка файлов и SHA-256 каждого файла;
- заменённые файлы сохраняет для отката;
- `CryMT.ini` не трогает.

## Install

1. You need Crysis 1.2.1, 64-bit (build 6156): Steam, GOG or disc with patch 1.2.1.
2. [c1-launcher](https://github.com/ccomrade/c1-launcher/releases) is needed as `Bin64\Crysis.exe` (GOG installs v7): v7 or v8. Only v8 fixes the 64-bit game's crashes with memory above 4 GB; with an older one CryMT applies its own fix.
3. Unpack `CryMT-v<N>.zip` into the game folder (where `Bin64` is).
4. Start `CryMT\CryMTLauncher.exe`, pick a mode and press Play.

The launcher installs updates from this repository:
- before installing, it checks the signature of the file list and the SHA-256 of every file;
- it keeps the replaced files for rollback;
- it never touches `CryMT.ini`.

## Uninstall / Удаление

Delete `Bin64\dbghelp.dll`, the `CryMT` folder and `Game\zzCryMT.pak` (if GI was on).
Удалите `Bin64\dbghelp.dll`, папку `CryMT` и `Game\zzCryMT.pak` (если включали GI).

## License / Лицензия

CryMT is GPL-3.0 ([source](https://github.com/yakimowivan-oss/CryMT)). Third-party components (NVIDIA Streamline and DLSS, Microsoft WebView2 Loader) are listed with their licenses in `CryMT\licenses` inside the package.

Crysis is (c) Crytek. The package contains no game files; you need your own legal copy.
