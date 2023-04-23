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
- Paragraphs instead of indents,
- Single-space at the beginning of sentences: `This is a sentence. This is another one.` vs. `This is a sentence.  This is another one.`
- Glossaries and Acronyms,
- Appendices,
- `\citeyear` and `\citeyearpar` links the year to the bibliography: useful when citing author like "according to Author (Year), blablabla",
- Author-year separated by a comma: `this is from a reference (author, year)`,
- Todos with categories for editing,
- Labels for text: If you need to reference text directly, instead of a part, chapter, section etc.,: add label with `\labeltext{see text on \vref{label}}{txt:myLabel}` and refer to label with either `\cref{txt:myLabel}` or `\vref{txt:myLabel}`,
- Preface / acknowledgements add-on: text-box in bottom-right corner; can be changed to bottom left,
- `\ExternalHref{the_link}{text_shown}` creates a link with a blue, link-colored link-symbol; example: '[great song](https://www.youtube.com/watch?v=Wd6tLmiylAY) ↗️',

### Todos categories
See todos.tex: question, fact-check, confirm, suggestion, reorganize, delete, condense, add, expand, red-thread
