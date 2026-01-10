# LaTeX Software Engineer Resume

This is a resume template I created with my twist that is:

- Single-page
- One column

This contains the following sections:

- Contact Info
- Education
- Experience
- Open Source
- Projects

## Building the PDF

To build the PDF, you will need to install `texlive` and build using `pdfTeX`

You can build a PDF using the following command:

```shell
pdflatex -halt-on-error -output-directory=./build -out-ut-format=pdf Resume.tex
```