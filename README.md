# Latex Expanded Thesis Template
This is a LaTeX template based on the [University of Oslo (UiO)'s official LaTeX template (~2023)](https://www.uio.no/english/about/designmanual/profile-in-use/latex/index.html) for a master's thesis; but expanded!


## Why?
To simplify the organization and writing of your thesis from "vanskelig" to "lett", hence the repository name.

### A full README is planned, featuring a tutorial of the "expanded"-part.
It will be written after the 6th of June, 2023, and published shortly after.

# How-to:
1. Download the `lett.zip`
2. Login at [Overleaf](https://www.overleaf.com)
3. Select `New Project/Upload project`
4. Upload the `lett.zip`
5. Start writing! 

# Expanded:
- Explanations on how to switch from easy-PDF-reading (oneside) to print-as-a-book (twoside),
- Explanations on how to change font-size from normal 11pt to 12pt,
- Setting to set 1.5 in 'linjeavstand',
- Paragraphs instead of indents,
- Single-space at the beginning of sentences: `This is a sentence. This is another one.` vs. `This is a sentence.  This is another one.`
- Glossaries and Acronyms,
- Appendices,
- `\citeyear` and `\citeyearpar` links the year to the bibliography: useful when citing author like "according to Author (Year), blablabla",
- Author-year separated by a comma: `this is from a reference (author, year)`,
- Todos with categories for editing,
- Figure Title (not usually needed; caption should be enough): add this inside and below \begin{figure}: `\figuretitle{This Title is necessary}`,
- Labels for text: If you need to reference text directly, instead of a part, chapter, section etc.,: add label with `\labeltext{see text on \vref{label}}{txt:myLabel}` and refer to label with either `\cref{txt:myLabel}` or `\vref{txt:myLabel}`,
- Preface / acknowledgements add-on: text-box in bottom-right corner; can be changed to bottom left,
- `\ExternalHref{the_link}{text_shown}` creates a link with a blue, link-colored link-symbol; example: '[great song](https://www.youtube.com/watch?v=Wd6tLmiylAY) ↗️',

## Rename 'Preface' to 'Acknowledgements' with:
`\renewcommand{\prefacename}{Acknowledgements}`

### Todos categories
See todos.tex: question, fact-check, confirm, suggestion, reorganize, delete, condense, add, expand, red-thread

# MVP:
## Citing references
You have a .bib-file with sources: probably generated from Zotero.
These sources have a key that you can reference them with and looks something like:
```
@book{yinCaseStudyResearch2018,
	location = {Los Angeles},
	edition = {Sixth edition},
	title = {Case study research and applications: design and methods},
	isbn = {978-1-5063-3616-9},
	shorttitle = {Case study research and applications},
	pagetotal = {319},
	publisher = {{SAGE}},
	author = {Yin, Robert K.},
	date = {2018},
	keywords = {Case method, Research Methodology, Social sciences},
}
```
Here, the key is `yinCaseStudyResearch2018`.

Use `\parencite{key}`, `\citeauthor{key}`, `\citeyear{key}`, `\citeyearpar{key}`, `\citetitle{key}` or if you want to specify a key directly: `\citefield{key}{field}` where fields can be `shorttitle` etc.

Example:
```
According to \citeauthor{yinCaseStudyResearch2018} \citeyearpar{yinCaseStudyResearch2018}, blablabla
% According to Yin (2018), blablabla
```

## Referencing in-document
Structurre: the thesis is structured in parts, chapters, sections, subsections, subsubsections ...
It can include figures and tables.
The structural elements, figures, and tables can be reffered to in-text by giving them a label:
`\label{myLabel}`
The label is placed below what is being labeled,
and it is helpful to add a prefix of what's being labelled: `prefix:myLabel`.
Example:
```
\part{Introduction}
\label{part:introduction}

As you can see in \cref{part:introduction} ... % in Part #
... which we already discussed in \vref{part:introduction}
% in Part # on page # (or previous page etc depending on where it actually is)
```

Here we used `cref` and `vref` to reference the label. Cref automatically knows that is being referenced: figure, table, part, chapter etc.
and vref adds the page number as well... 

## Glossaries
Check out how on:
https://ftp.fagskolen.gjovik.no/pub/tex-archive/macros/latex/contrib/glossaries/glossariesbegin.pdf
https://ftp.fagskolen.gjovik.no/pub/tex-archive/macros/latex/contrib/glossaries/glossaries-user.pdf

# Better README will come after my thesis.


# TODO:
- Unzip project to make files and folders easily available so people can contribute
- Write about structuring the thesis
- Write about glossaries
- Write about "how to make custom titles on set sections", and add toc lines.
- Write about how to sync Overleaf and Zotero with https://retorque.re/zotero-better-bibtex/ for generating keys.
- Write about auhtoryear-ibid vs apa bib-styles and how citations work for both --- some found that APA is best!
- Write about how to translate the "appendices" in Norwegian, as language does not update automatically.
- Write about how the bibliography (will use) iso-dates for all dates
