# KDE Service Menus for PDF File Processing

Enhance your workflow with KDE service menus specifically designed for PDF file processing.

This project is an unofficial Plasma 6 port of **kde-service-menu-pdf Version 2.3**,  
Copyright (C) 2018-2019 Giuseppe Benigno (<giuseppe.benigno@gmail.com>), GPL-3.0+.

---

## Prerequisites

Ensure the following tools are installed:

- [Ghostscript](https://www.ghostscript.com/)
- [Poppler](https://poppler.freedesktop.org/)
- [PDFtk](https://www.pdflabs.com/tools/pdftk-the-pdf-toolkit/)
- [TeX Live](https://tug.org/texlive/)

---

## Installation (Plasma 6)

### Install Dependencies 

Run the following command to install the required tools:

**Arch Linux:**
```bash
sudo pacman -S ghostscript texlive-bin poppler pdftk texlive-binextra texlive-latexrecommended
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

This project is licensed under [GPL-3.0+](https://www.gnu.org/licenses/gpl-3.0.html).
