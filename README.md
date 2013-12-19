# Hugarian book template

This is a template for writing a [Softcover](http://www.softcover.io/) book in Hungarian. The key modifications happen in `custom.sty`:

```latex
% Change the word used for chapters.
\renewcommand{\chaptername}{Fejezet}

% Define any Unicode characters that don't work natively in the PDF.
% See http://en.wikibooks.org/wiki/LaTeX/Special_Characters for reference.
\usepackage{newunicodechar}
\newunicodechar{ő}{\H{o}}
\newunicodechar{ű}{\H{u}}
```

The `\renewcommand` changes the word used for chapters, while the `\newunicodechar` commands define characters that LaTeX doesn't know how to process natively. When building PDFs, care should be taken to create a new `newunicodechar` line for every character that "disappears" (i.e., that LaTeX doesn't understand).