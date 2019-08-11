# Introducction

This is a simple list containing quick guides to make a decission regarding different aspects of the technological world. If you want just a list of libre alternatives, please, refer to my [libre list](https://github.com/Irvise/Documents/blob/master/Cheatsheets/Libre/Packages.md).

## Disclaimer

This list is created based on my own experience (or lack thereof). Take everything with a pich of salt and more of a recommendation, rather than anything that I am telling you to do. Always, always do what works for you.

## Choosing a programming language, technology

This list should be used by reading from top to bottom and selecting the first language which suits the requirements.

* **Lua** use it as an scripting language and to extend software where the user is not expected to write performing code. It is easily embeddable in any language. If extending the program is one of it's mayor features, then, consider using Scheme/Guile.

* **Julia** as a quick way to interact whit programs and write performant systems (unless the languages below suit that requirement better). If python is good for that job (unless Lua or Guile suit it better), then you should use Julia. It should also be embedded as an application programming interface in more complex software where the user is expected to write quite some (performant) code.

* **FORTRAN** if the program has to be as performant as possible, and it will mainly consist on (math/logic) operations, rather than memory management. Use modern fortran: it is more flexible, clearer and has a wonderfully simple yet powerful type system. Please, take a look into CoArrays, OpenMP and OpenMPI.

* **C** for embedded devices or resource constrained systems; when performance is of great importance. Please, use C99 or newer. And take your time to learn it.

* **Ada/Spark** for critical software where not just the code but the logic HAS to be correct.

* **LISP/SCHEME** when the complexity of the problem outgrows the necessity of performance. As an extra addition, it is a joy to write.

* **Haskell** for the defacto functional programming language. **OCaml** is also worth trying.

* **Rust** when the program is of great complexity, has to be correct (code-bug-free), performant and development speed is important.

* **Prolog** when the problem faced is easier with a logical approach. Also, anything AI.

* **Coq/F\*** for formally provable programs. If the program has to be compiled to machine code or other languages, F* is a great choice.

* **Assembly** when there is nothing that will suit the performace. Or just to have access to all the functionallity that the hardware has to offer. It is also great fun writting it when done as a hobby, and you will learn more than what you would have imagined.

### Web related languages

* **Elixir/Erlang** for web services where stability and scalability need to be ensured. Efficiency nor performance should be the main characteristic for the project. Consider using the [Phoenix Framework](https://phoenixframework.org/) and [Drab](https://tg.pl/drab).

* **Golang** for web related services where performance is important. By performance I mean that the backend will have to do some heavy lifting tasks and the user should not be left waiting for.

### Builders

* The **Autotools** suit and **Meson**. **Meson** is a much simpler, quicker and modern approach. However, **autotools** goes better for simpler hardware, it is also much more fine-grained. Make sure your programms cross-compile without any issues.

### Databases

* **SQLite** for simple projects.

* **PostgreSQL** for any project where the schema is well defined and performance is a must.

* **Redis** in memory database.

* **TODO** expand descriptions and are other types.

### GUI Toolkits

* **Qt**

* **Gtk (FORTRAN)**

* **Tk**

* **[IUP](http://webserver2.tecgraf.puc-rio.br/iup/)**

* **Motif**

### Directives when writing a program

I find this section to be the most important of them all. Here, we will discuss how to structure a program and all the infraestructure required for it's correct development. However, do note that this is mostly aimed at scientific software.

1. Densely document your code.
    * While the code should in most cases be clear enough, explain what it does, reference any articles, principles or formulae from which it is derived.
    * If a function/subroutine requires some input, explain what that input is in the function/subroutine and if some special conditions should be met prior to its processing, such as dimentions. There are tools such as doxygen which facilitate this task.

2. If the program is ment to be primarily used without knowing the internals or messing with parts of the code; non-technical documentation targeted directly to users has to be written. There are tools such as doxygen which facilitate this task. Give examples, these examples may come form tests, see below.

3. Do not write code if you are not going to comment it or explain it. Do not allow code which is not up to quality.

4. Write tests for ALL the features that your program has. They should be clean, small and fast to run. Do not write code which cannot be tested or that cannot be ensured to be correct.

5. Use branches and meaningful commit messages. Things like WIP, or cont. should not be allowed.

6. Be incremental. Go little by little, compile, test and then merge the branch.

7. Keep a CHANGELOG. As sailors kept a diary of their travels, so should you with your program. Commit messages may help, but a CHANGELOG should contain mayor features and not-so-technical information. Lets say that a CHANGELOG is a high level abstraction of the commits.

8. Be modular. Keep the code clean and portable. However, as stated above, be incremental: one cannot creat all the abstractions in one go. Little by little.

9. Reuse code wherever it makes sense. Use third party libraries if they are of enough quality.

10. Tests and continous integration.
    * Related to the above points. Design an infraestructure which will save you time by automatically running tests, checking the code, etc.
    * Tests should be small, comprehensive and quick to run. They exist to help the programmer, not make us wait.

11. Leave optimizations as the last thing to do.
    * "Premature optimization is the root of all evil" - Donald Knuth.
    * [Rules of Optimization Club](http://wiki.c2.com/?RulesOfOptimizationClub)
        1. You do not optimize.
        2. You do not optimize, without measuring first.
        3. When the performance is not bound by the code, but by external factors, the optimization is over.
        4. Only optimize code that already has full unit test coverage.
        5. One factor at a time.
        6. No unresolved bugs, no schedule pressure.
        7. Testing will go on as long as it has to.
        8. If this is your first night at Optimization Club, you have to write a test case.
    * Not all code may benefit from going parallel. Actually, the efficiency of any program decreases the more core it runs in. Single threadding performace should usualy be the priority (specially chache locality).
    * If once the optimization is done, the optimized code diverges greatly from the original idea/design; the old code should be left commented for future reference. It would also not hurt to explain how the optimization was achived and in which ways the earlier implementation had to be changed.

12. It goes without saying that you should modularize the code. Reuse as much code as possible without losing clarity.

## Formats

### Text files

If it has to be human readable, please, use plain text. Even if the file should, very rarely, be read by a person; still, make it a plain text.

* **Org files** may be used to take advantage of most of the mentioned properties of the formats below. Use it as your heart's desire.

* **TOML** for structured data and configuration.

* **Markdown** for simple documentation texts aimed at the web.

* **TeX** for scientific and formal documentation of projects. Try to keep it as simple and as barebones as possible, don't be fancy. If you need anything more flexible than the default classes, use KOMA. Also, partition your .tex files!

* **ODF** (Open Document Format) for more complex texts and automated forms. If the design of the document is a primary concern, such as in posters or magazines, use [Scribus](https://www.scribus.net/).

* **PDF or PostScript** for printing or read-only copies.

* **MusicXML** while XML is something that boggles my mind, if you have to exchange music between to programs (such as the wonderful [MuseScore](https://musescore.org/en) or [Denemo](http://www.denemo.org/)), use MusicXML, since it is a standard understood by many and works well.

### LaTeX

This section will name and explain some of the packages that I would personally recommend to _allways_ use. Read their documentation.

* `inputenc` to set the input encoding. Preferably either `utf8` or `latin1` (which is the ISO/IEC 8859-1 standard).

* `fontspec` to easily define and change fonts. Only works with XeLaTeX and LuaLaTeX.

* `KOMA-Script` provides replacement for the basic styles and puts extra emphasis on typography and versatillity. Please, refer to its [homepage](http://www.komascript.de/).

* `microtype` allows for fine-grained control over the typography being used.

* `polyglossia` for localization if you use XeLaTeX or LuaLaTeX. If you use PdfLaTeX or standard .dvi/.ps use `babel`. Please, refer to their documentation for more information. See `toptesi` below.

* `biblatex` a more modern Bibliography engine. I personally recommend it instead of BibTeX. Use biber and natbib for customization and preprocessing.

* `geometry` to modify the spacing of different parts of the document.

* `glossaries` to create glossaries.

* `fancyhdr` for header and footer customization.

* `graphicx` to import graphics. Use `svg` to import svgs. `pdfpages` to insert pdfs.

* `hyperref` for better referencing.

* `booktabs` to creat simpler, more readable tables.

* `multicol` and `multirow` to work with multiple columns and rows in a document.

* `listingss` to list text. Great when outputting code.

* `enumitem` for more control over lists.

* `xcolor` to define colors.

* `csquotes` everything related to quotes is found here. It is specially useful when writing text in multiple languages.

* `algorithm2e` write pseudo code. Aimed at logical analysis.

* `tikz` for drawing.

* `pgfplots` for plotting.

* `lipsum` historical dummy text to test formatting and output.

* `pgfornament` for beautiful vectorized ornaments.

* `shapepar` to write text inside shapes easily.

* `beamer` for writing presentations.

#### Beamer

Extra styles for Beamer:

`beamer2theis`, as the name implies, a theme geared towards thesis presentations.

---

Some more specific packages, should be used as a reference:

* `clasicthesis` for theses. You may prefer the `arsclassica` package.

* `toptesi` is a package aim to multilingual papers, such as master or PhD thesis. This is a common necessity in Europe. There is also `hagenberg-thesis`.

* `latex-refsheet` is a cheatsheet for `KOMA-Script` aimed at writing a thesis.

* `siunitx` type units as the BIPM recommends. Very useful when writing scientific documents.

---

Books and other references, all free. The documentation goes without saying.

* **[The not so short introduction to LaTeX](https://www.ctan.org/pkg/lshort):** Short and simple introduction to LaTeX. Latest revision in 2018. Available in multiple languages.

* **[More math Into LaTeX](https://osl.ugr.es/CTAN/info/Math_into_LaTeX-4/Short_Course.pdf):** while the book itself is not free, the introductory part is freely abvailable (linked). The first part introduces LaTeX in a simple and direct way. Latest eddition from 2016. In English.

* **[LaTeX Tutorials a Primer](https://tug.org/twg/mactex/tutorials/ltxprimer-1.0.pdf):** a book from 2003 that is simple and straight to the point. In English.

* **[LaTeX Wikibook](https://en.wikibooks.org/wiki/LaTeX):** it is one of the most complete user references out there. Has a large amount of examples and introduces the most used packages. In English.

* **[Dickimaw LaTeX Series](https://www.ctan.org/pkg/dickimaw):** it has three entries. A book for begginers, a followup for students wanting to write a thesis, and how to write a minimal example to debbug TeX code. Latest version as of 2012. In English.

* **[The Art of LaTeX](http://math.ecnu.edu.cn/~latex/docs/Eng_doc/LaTeX_Manual_8_6.pdf):** short and direct introduction. In English.

* **[The LaTeX Mathematics Companion](http://blog.analogmachine.org/wp-content/uploads/2013/09/TheLaTeXMathematicsCompanionGai.pdf):** continuation of _The Art of LaTeX_ and as the name implies, aimed at mathematical notation. In English.

For other languages please, refer to [this Stackexchange post](https://tex.stackexchange.com/questions/84384/latex-introductions-in-languages-other-than-english).

As an extra addition, the book **[LaTeX and Friends](http://csweb.ucc.ie/~dongen/LAF/LAF.html)** is worth every dime.

## Editors

* **[Joe](https://joe-editor.sourceforge.io/),** which stands for _Joe's Own text Editor,_ is a simple yet featureful editor, it strikes a great balance between complexity and flexibility. It can even emulate Emacs or Wordstar.

* **[Vis](https://github.com/martanne/vis),** a wonderful _Vi_ based editor. Aims to be small, fast and simple; while maintaining all the features that make _Vi_ like editors great. It is also inspired by SAM and uses Lua as an extention language.

* **[GNU Emacs](https://www.gnu.org/software/emacs/),** also know as a Lisp machine that happens to edit text. It is the most complex one on the list by far, also the most extendable one. Even if you may not like it, it is worth even if it is just for the [Org](http://orgmode.org/) and [Magit](https://magit.vc/) extensions.

## Fonts

Most of the fonts discussed here are in [The LaTeX Font Catalogue](http://www.tug.dk/FontCatalogue/), which I greatly recommend. The vast mayority of exceptions to the fonts listed are in the monospaced family.

All of the fonts listed here are under a _libre_ license.

### Serif

This fonts are mainly targeted to formal documents or literature writing meant to be read on paper. Most of the faces listed in this section also add a sans variant, which won't be listed in the following section. However, it does not mean they are not recommended, quite the oposite, specially if you are already using the Serif variant.

**[Accanthis](http://www.tug.dk/FontCatalogue/accanthis/)** focuses mostly on european languages. It is a light face and has a lovely traditional feel to it, while having fluid strokes and being easy to read.

**[Alegreya](http://www.tug.dk/FontCatalogue/alegreya/)** is a face which resembles those of old mechanical printing machines. It has an option for a heavier boldface. I would personally use it to quote old notes.

**[Antiqua](http://www.tug.dk/FontCatalogue/antiqua/)** is a simple face with, with an average weight. Its style is a mix between a light serif font with a typewriter style.

**[Asana Math](http://www.tug.dk/FontCatalogue/asanamath/)** tasteful mix between Accanthis and Antiqua.

**[Baskerval ADF](http://www.tug.dk/FontCatalogue/baskervaldadf/)** simple serif typeface with a reduced size while maintaining the density.

**[Coelacanth](http://www.tug.dk/FontCatalogue/coelacanthregular/)** small face with a light variant.

**[Computer Modern](http://www.tug.dk/FontCatalogue/computermodern/)** the default LaTeX font. When in doubt, use this font, **it is one of the most readable, complete and formal faces in the world.**

**[Cormorant Garamond](http://www.tug.dk/FontCatalogue/cormorantgaramond/)** is a simple formal, light and compact font. Similar to Computer Modern, but is smaller by design.

**[Crimson Pro](http://www.tug.dk/FontCatalogue/crimsonproregular/).** It has several variants. Defined font with a reduced size face. Modern and clean design.

**[Erewhom](http://www.tug.dk/FontCatalogue/erewhon/)** an improved version of Andry V. Panov's Heuristica. Dense face with a clean and _roundy_ design.

**[Garamond Expert (with mathdesing)](http://www.tug.dk/FontCatalogue/garamondexpertmathdesign/)** simple and clean type with tons of customizations. There is also a [newtx](https://www.ctan.org/pkg/newtx) variant.

**[GFS Bodoni](http://www.tug.dk/FontCatalogue/gfsbodoni/)** _square_ design with round strokes. For more styles, specially ones with terminations, see the rest of the GFS family.

**[GNU Freefont](http://www.tug.dk/FontCatalogue/gnufreefontserif/)** is one of the most complete fonts in the world. It is a quite compact face and it is ment to be readeable. It has a large amount of variants.

**[IBM Plex family](http://www.tug.dk/FontCatalogue/ibmplexserifregular/)** was created, as the name suggests by IBM to suit all the needs that the company may had had. This has lead to a typeface with a large display of styles in which you may find what you are looking for.

**[Inria Serif](http://www.tug.dk/FontCatalogue/inriaserifregular/)** with its regular and light face it will suit all the engineers out there _specially the light variant for the mechanics._

**[Latin Modern](http://www.tug.dk/FontCatalogue/latinmodernroman/)** is a common alternative to Computer Modern.

**[Linux Libertine](http://www.tug.dk/FontCatalogue/linuxlibertine/)** is one of the most commonly used serif fonts, it is worth checking.

**[TeX Gyre Pagella](http://www.tug.dk/FontCatalogue/texgyrepagella/).** While the TeX Gyre collection is large, the one that I feel suits formal writing the most is its Pagella variant. It is a simple, clean and sober font.

TODO Romande ADF, Venturis ADF, Poltawski

### Monospaced/Typewritter

TODO

### Calligraphical

TODO, Miama Nueva, TeX Gyre Chorus

### Uncial and Blackletter

TODO

### Decorative

TODO

## CLI and TUI tools

TODO
