---
# UF thesis/dissertation fields
title: "Using gatordown to Create Dissertations"
author: "Anthony Raborn"
year: "2018"
month: "October"
program: "Rmarkdown"
degree: "DOCTOR OF RMARKDOWN"
chair: "Chair Person 1"
dedication: "pre/00-dedication.Rmd"
acknowledgements: "pre/00-acknowledgements.Rmd"
abstract: "pre/00-abstract.Rmd"
# abbreviations: "pre/00-abbreviations.Rmd" # OPTIONAL
# End of UF thesis fields
knit: "bookdown::render_book"
site: bookdown::bookdown_site
output: 
  gatordown::thesis_pdf: 
    latex_engine: xelatex
bibliography: bib/References.bib
# Download your specific bibliography database file and refer to it in the line above.
csl: csl/apa.csl
# Download your specific csl file and refer to it in the line above.
---


  

<!--
Above is the YAML (YAML Ain't Markup Language) header that includes a lot of metadata used to produce the document.  Be careful with spacing in this header!

If you'd like to include a comment that won't be produced in your resulting file enclose it in a block like this.
-->

<!--
If you receive a duplicate label error after knitting, make sure to delete the index.Rmd file and then knit again.
-->



<!-- 
You'll need to include the order that you'd like Rmd files to appear in the
_bookdown.yml file for PDF files and also delete the # before rmd_files: there.
You'll want to not include 00(two-hyphens)prelim.Rmd and 00-abstract.Rmd since
they are handled in the YAML above differently for the PDF version.
-->

<!-- 
The {-} option could be used here; it means that there would be no numbers on the introduction. You
can also use {.unnumbered} so the introduction would be "Chapter 0." However, UF's template doesn't allow for a "Chapter 0", so this is ignored.
-->

# Introduction

Welcome to the _R Markdown_ thesis template. This template is based on (and in
many places copied directly from) the [University of Florida LaTeX
template][0] and wrapped up into Anthony Raborn's [*gatordown* package][1], but
hopefully it will provide a nicer interface for those that have never used TeX
or LaTeX before (Multiple forks of the [*thesisdown* package][2], in particular the [*beaverdown* package][3], were used to improve how the UF template works with R). Using _R Markdown_ will also allow you to easily keep track of
your analyses in **R** chunks of code, with the resulting plots and output
included as well.  The hope is this _R Markdown_ template gets you in the habit
of doing reproducible research, which benefits you long-term as a researcher,
but also will greatly help anyone that is trying to reproduce or build onto your
results down the road.

Hopefully, you won't have much of a learning period to go through and you will
reap the benefits of a nicely formatted thesis.  The use of LaTeX in combination
with _Markdown_ is more consistent than the output of a word processor, much
less prone to corruption or crashing, and the resulting file is smaller than a
Word file. While you may have never had problems using Word in the past, your
thesis is likely going to be about twice as large and complex as anything you've
written before, taxing Word's capabilities.  After working with _Markdown_ and
**R** together for a few weeks, we are confident this will be your reporting
style of choice going forward.

<!-- 
If you're still on the fence about using _R Markdown_, check out the resource
for newbies available at <https://ismayc.github.io/rbasics-book/> or email us at
<data@reed.edu>.
-->

**Why use it?**

_R Markdown_ creates a simple and straightforward way to interface with the
beauty of LaTeX.  Packages have been written in **R** to work directly with
LaTeX to produce nicely formatting tables and paragraphs. In addition to
creating a user friendly interface to LaTeX, _R Markdown_ also allows you to
read in your data, to analyze it and to visualize it using **R** functions, and
also to provide the documentation and commentary on the results of your project.
Further, it allows for **R** results to be passed inline to the commentary of
your results.  You'll see more on this later.

<!-- 
Having your code and commentary all together in one place has a plethora of benefits!
-->

**Who should use it?**

Anyone who needs to use data analysis, math, tables, a lot of figures, complex
cross-references, or who just cares about the final appearance of their document
should use _R Markdown_. Of particular use should be anyone in the sciences, but
the user-friendly nature of _Markdown_ and its ability to keep track of and
easily include figures, automatically generate a table of contents, index,
references, table of figures, etc. should make it of great benefit to nearly
anyone writing a thesis project.

## Objective 

The purpose of this study is to... Lorem @smith ipsum dolor sit amet,
consectetur adipiscing elit. Sed venenatis nunc sapien. Praesent
imperdiet nulla eu rutrum venenatis. Fusce rhoncus urna a nunc semper,
non venenatis lorem tempor. Cras sollicitudin eget velit eu venenatis.
Mauris imperdiet pretium massa sed dapibus. Nunc ipsum ipsum, porttitor
ut urna ut, pretium feugiat leo. Nunc magna enim, facilisis a porttitor
eget, elementum ac turpis. Quisque et gravida justo. Etiam vulputate
quam at commodo suscipit. Vivamus ut adipiscing tortor. Phasellus quis
dolor et mi hendrerit sollicitudin.

Cras dapibus congue mauris, et imperdiet magna pellentesque non. Sed
venenatis adipiscing quam ut placerat. Praesent imperdiet dignissim
cursus. Phasellus mattis nibh vitae semper pellentesque. Lorem ipsum
dolor sit amet, consectetur adipiscing elit. Sed dignissim tellus id
adipiscing tempus. Aenean posuere malesuada rhoncus. Ut quis elit eros.

## Background 

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed venenatis
nunc sapien. Praesent imperdiet nulla eu rutrum venenatis. Fusce rhoncus
urna a nunc semper, non venenatis lorem tempor. Cras sollicitudin eget
velit eu venenatis. Mauris imperdiet pretium massa sed dapibus. Nunc
ipsum ipsum, porttitor ut urna ut, pretium feugiat leo. Nunc magna enim,
facilisis a porttitor eget, elementum ac turpis. Quisque et gravida
justo. Etiam vulputate quam at commodo suscipit. Vivamus ut adipiscing
tortor. Phasellus quis dolor et mi hendrerit sollicitudin.

Cras dapibus congue mauris, et imperdiet magna pellentesque non. Sed
venenatis adipiscing quam ut placerat. Praesent imperdiet dignissim
cursus. Phasellus mattis nibh vitae semper pellentesque. Lorem ipsum
dolor sit amet, consectetur adipiscing elit. Sed dignissim tellus id
adipiscing tempus. Aenean posuere malesuada rhoncus. Ut quis elit eros.



[0]: http://helpdesk.ufl.edu/application-support-center/etd-technical-support/ms-word-and-latex-templates/
[1]: https://github.com/AnthonyRaborn/gatordown
[2]: https://github.com/ismayc/thesisdown/
[3]: https://github.com/zkamvar/beaverdown
