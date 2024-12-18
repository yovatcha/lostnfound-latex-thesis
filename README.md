# LostnFound KMUTT thesis

CSC499 capstone project with LaTex

---

### Install LaTex

To compile this LaTeX project, ensure the following tools are installed on your system:

1. **LaTeX Distribution**:  
   - [TeX Live](https://tug.org/texlive/) (Linux/Mac)  
   - [MikTeX](https://miktex.org/) (Windows)

2. **Editor (Optional but Recommended for real)**:  
   - [VSCode](https://code.visualstudio.com/) with the `LaTeX Workshop` extension  
   - [Overleaf](https://www.overleaf.com/) for an online environment

3. **BibTeX**: For bibliography management.

---

### Install font TH Sarabun New

Fonts of this document in classes folder.

**Download TH Sarabun New** -> http://ubuntuhandbook.org/index.php/2016/05/manually-install-fonts-ubuntu-16-04/

---

### Setting in VSCode

-Install LaTeX Workshop (James Yu) extention.

-Add this code in `setting.json` file

```
"latex-workshop.latex.tools": [
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                // "-pdf",
                "%DOC%"
            ]
        }
    ],
"latex-workshop.latex.recipes": [
        {
            "name": "xelatex",
            "tools": [
                "xelatex"
            ]
        }
    ],
"latex-workshop.view.pdf.viewer": "tab"
```

---

### Steps to Compile the Project

```sh
xelatex thesis.tex    # Compile the document
bibtex thesis          # Generate bibliography
xelatex thesis.tex    # Recompile to include references
xelatex thesis.tex    # Final compilation for cross-references
```

---

### Cleanup

To clean auxiliary files generated during compilation, run:
```sh
cd path/to/your/mainlatex/file
./clean.sh

#or

bash clean.sh
```

This will delete files such as .aux, .log, .bbl, and .blg.