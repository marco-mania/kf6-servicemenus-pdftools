# KDE service menus for pdf file processing

KDE service menus for pdf file processing.

Originally from [kde-service-menu-pdf Version 2.3](https://www.egregorion.net/),
Copyright (C) 2018-2019 Giuseppe Benigno <giuseppe.benigno@gmail.com>, GPL-3.0+

## Prerequisites

* [Ghostscript](https://www.ghostscript.com/)
* [Poppler](https://poppler.freedesktop.org/)
* [PDFtk](https://www.pdflabs.com/tools/pdftk-the-pdf-toolkit/)
* [TeX Live](https://tug.org/texlive/)

## Installation (Plasma 6)

Install the requirements (Arch Linux):

    sudo pacman -S ghostscript texlive-bin poppler pdftk texlive-binextra texlive-latexrecommended

To install system wide:

    sudo cp servicemenus/* /usr/share/kio/servicemenus/
    sudo cp bin/* /usr/local/bin/

Per user installation:

    cp servicemenus/* ~/.local/share/kio/servicemenus/
    cp bin/* ~/.local/bin

In that case the directory `~/.local/bin` has to be be placed in the search path
environment variable `$PATH`.
Also make sure your .desktop files are execuatable
`chmod +x ~/.local/share/kio/servicemenus/pdf-tools*.desktop`.

Finally you need to restart your plasma session or call:

    kbuildsycoca6

## Uninstall

System wide installation:

    sudo rm /usr/share/kio/servicemenus/pdf-tools*.desktop
    sudo rm /usr/local/bin/pdf-tools-*-kdialog

Per user installation:

    rm ~/.local/share/kio/servicemenus/pdf-tools*.desktop
    rm ~/./local/bin/pdf-tools-*-kdialog

## Contributing

Pull requests are welcome. For major changes, please open an issue first to
discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[GPL-3.0+](https://www.gnu.org/licenses/gpl-3.0.de.html)
