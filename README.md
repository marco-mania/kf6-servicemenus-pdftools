<!--
SPDX-FileCopyrightText: 2007-2019 Giuseppe Benigno <giuseppe.benigno(at)gmail.com>
SPDX-FileCopyrightText: 2026 Marco Nelles <dev at maniatek dot de>

SPDX-License-Identifier: GPL-3.0-or-later
-->

# KDE Service Menus for PDF File Processing

Enhance your workflow with KDE service menus specifically designed for PDF file processing.

This project is an unofficial Plasma 6 port of **kde-service-menu-pdf Version 2.3**,  
Copyright (C) 2018-2019 Giuseppe Benigno (<giuseppe.benigno@gmail.com>), GPL-3.0+.  
The KF6 port itself is maintained by Marco Nelles (<dev at maniatek dot de>). See the
`SPDX-FileCopyrightText` tags in each file for the full attribution history.

---

## Prerequisites

Ensure the following tools are installed:

- [KDE](https://www.kde.org/) (`kdialog`)
- [Ghostscript](https://www.ghostscript.com/)
- [Poppler](https://poppler.freedesktop.org/)
- [TeX Live](https://tug.org/texlive/) (`pdfjam`/`pdfbook2`, `pdfnup`)
- [pdf2djvu](https://github.com/jwilk/pdf2djvu) (for the DjVu conversion actions)
- [CUPS](https://www.cups.org/) (`lpstat`, `lpr`; for the print action)

---

## Installation (Plasma 6)

### Install Dependencies 

Run the following command to install the required tools:

**Arch Linux:**
```bash
sudo pacman -S kdialog ghostscript texlive-bin poppler pdf2djvu cups texlive-binextra texlive-latexrecommended
```

**Ubuntu Linux:**
```bash
sudo apt install ghostscript texlive-binaries poppler-utils pdftk-java texlive-extra-utils texlive-latex-base
```

### System-Wide Installation

Copy the necessary files to the system directories:

```bash
sudo cp servicemenus/* /usr/share/kio/servicemenus/
sudo cp bin/* /usr/local/bin/
```

### Per-User Installation

For a user-specific setup, copy the files as follows:

```bash
cp servicemenus/* ~/.local/share/kio/servicemenus/
cp bin/* ~/.local/bin
```

Make sure the `~/.local/bin` directory is included in your `$PATH` environment variable.  
Additionally, set the `.desktop` files to be executable:

```bash
chmod +x ~/.local/share/kio/servicemenus/pdf-tools*.desktop
```

Finally, restart your Plasma session or execute the following command:

```bash
kbuildsycoca6
```

---

## Uninstallation

### System-Wide Uninstallation

Remove the installed files:

```bash
sudo rm /usr/share/kio/servicemenus/pdf-tools*.desktop
sudo rm /usr/local/bin/pdf-tools-*-kdialog
```

### Per-User Uninstallation

Delete the corresponding files:

```bash
rm ~/.local/share/kio/servicemenus/pdf-tools*.desktop
rm ~/.local/bin/pdf-tools-*-kdialog
```

---

## Contributing

We welcome contributions! Please follow these guidelines:

- For major changes, open an issue first to discuss your ideas.
- Ensure any necessary tests are updated appropriately.

Pull requests are encouraged and appreciated.

---

## License

This project is licensed under [GPL-3.0-or-later](https://www.gnu.org/licenses/gpl-3.0.html),
the same license as the original `kde-service-menu-pdf` project it is ported from.
The project is [REUSE](https://reuse.software/) compliant; see the `LICENSES/` folder
and the SPDX tags in each file for details.
