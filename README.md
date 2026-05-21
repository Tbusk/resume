# LaTeX Software Engineer Resume

This is a resume template I created with my twist that is:

- Single-page
- One column
- Made up of modular components, of which the underlying details are abstracted

## Preview

![Resume Preview](media/ResumeScreenshot.png)

## Getting Started

To get started, you can add things to the document starting between the begin and the end portions.

```latex
\begin{document}
    % anything you want
\end{document}
```

To build the PDF, you will need to install `texlive` and build using `latexmk`.

You likely will need to install dependencies, but on the Solus Linux Distrobution, you only need `texlive` and `latexmk`.

You can build a PDF without keeping the extra output files using the following command:

```shell
latexmk -pdf Resume.tex && latexmk -c
```

This first half will build the pdf and the rest will clean up the extra files.

### Sections

To declare a section, all you need to do is add a section with a title of it in a parameter.

I use this for section headers, such as `Education`, `Experience`, `Projects`, `Skills`, and `Open Source`.

```latex
\section{Section Name}
```

### Lists

Three types of lists are supported: bullet (filled circle), circle (unfilled circle), or empty (no circles).

#### Bullet

```latex
\rListBeginBullet

% any list items

\rListEndBullet
```

#### Circle

```latex
\rListBeginCircle

% any list items

\rListEndCircle
```

#### Empty

```latex
\rListBeginEmpty

% any list items

\rListEndEmpty

```

### Headings

Two types of headings are supported: general and project.

#### General

This has four parameters, which is a tabular layout of a bolded title on the top left, an item on the top right, an
italicized item on the bottom left, and an italicized item on the bottom right.

I use this for education items and experience items, which param 1 shows either the university or company name, param 2
shows the location, param 3 shows the degree name or job title, and param 4 shows the date range or completion date.

```latex
\rGeneralHeading{Company Name}{Location}{Job Title}{Start Date to End Date (or Present)}
```

#### Project

This has two parameters, which is a bolded title on the left and a link to the project on the right side.

You can use this for projects you've worked on, such as personal projects or contributions you made to open source ones.

I use this for my open source work.

```latex
\rProjectHeading{Project Name}{Link without https or www)}
```

### List Items

#### Plain Item

This is the default item you want when you want to list something. It is just a regular list item.

This has one parameter for whatever text you want to show up in the list.

```latex
\rPlainItem{List item description}
```

#### Bolded Item with a description

This is used when you want to highlight something before you give a description, such as a project name, a skill, or a
tech stack item.

It has two parameters, one is a bolded title with a colon and a space appended to it, and the other is a description.

```latex
\rBoldedItemAndDescription{Name}{Description}
```

### Links

You can add a link to something pretty easily

It has two parameters, the first is the full url, and the second is what the user actually sees.

```latex
\href{full url}{user-facing display}
```

## Additional Resources

- [Latexmk Documentation](https://mgeier.github.io/latexmk.html)

## Inspiration

This was inspired by [sb2nov's LaTeX Resume](https://github.com/sb2nov/resume/).

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT) found [here](LICENSE).