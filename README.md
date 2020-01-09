# Awesome Data Effectiveness

Communicating your data for the desired effect

Do you struggle with analyzing and communicating data to effect the changes you would like to see in the world? Do you have any approaches that work particularly well for your projects?

Welcome to a world in which other data professionals care about improving practice as much as you do! We invite you to join in a conversation and collective data collection experience about which data practices aid in maximizing effectiveness. _¡Vivan los datos efectivos!_

* [Poster from 2019-01-10 presentation](poster/awesome-data-effectiveness-poster.pdf)

## Purpose / Planning (Discuss)

Why are your collecting the data? What decisions do you want to make based on the data?

### Advice

### Resources

## Collection

How can you design data collection to align with your purpose and ease analysis?

### Advice

### Resources

* Data Stories podcast about how to design survey questions (BV enter)

### Data types

### Data validation and quality

## Metadata

What additional information does one need to make sense of your data? How can it be used effectively?

### Advice

### Resources

## Storage (Discussion)

Does the storage of your data permit its best use?

### Advice

1. Use spreadsheets effectively. See Broman & Woo, 2018.
    1. Use the correct format and data types (e.g. dates should use ISO 8601 standard, are the numbers integers or floating point numbers) for each variable. If you don't know about data types, ask.
    1. Never merge cells.
    1. Do not rely on color or formatting to store information.
    1. Put each table on a different, named sheet.
    1. Put units or notes or additional information in another column. Don't pack more than one piece of information in a single cell.
    1. Always start in the top-left cell of each sheet.
    1. Keep column (variable) names short and unique with no spaces.
    1. If opening a CSV with special characters as an Excel spreadsheet, import the text rather than opening the file to preserve text encoding. If you don't know what this means, ask.
    1. Learn about tidy data shapes.
1. Think about data security. Does your data include PHI, PII, or other sensitive elements? Talk to your IT team.

### Resources

* Broman, K. W., & Woo, K. H. (2018). Data Organization in Spreadsheets. The American Statistician, 72(1), 2–10. https://doi.org/10.1080/00031305.2017.1375989
* Style guide for variable naming
  * [names for variable conventions (Allison Horst)](https://twitter.com/allison_horst/status/1205702878544875521/photo/1)
* CSV
  * [Doing a database join with CSV files](https://www.johndcook.com/blog/2019/12/31/sql-join-csv-files/) using [xsv](https://github.com/BurntSushi/xsv)

## Transformation

Does the layout of your data permit easy analysis? Sometimes the transformation of the data will depend on the specific purpose. Can your data be transformed readily?

### Advice

Often, storing related data in separate tables and joining them when necessary works better than storing one big table with many rows of duplicate information. How can you find a tool that supports easy data joining?

Data quality and missing data

### Resources

## Communication and visualization (Discussion)

Do the visualizations communicate in a way that facilitates decisions?

### Advice

### Resources

* Books
    * [Data Visualization: A practical introduction by Kieran Healy](https://socviz.co/)
* Chart choosers
    * [Qualitative Chart Chooser 3.0 by Jennier Lyons and Stephanie Evergreen](https://stephanieevergreen.com/qualitative-chart-chooser-3/)
* Checklists and frameworks
    * [Interactive Data-Visualization Checklist](https://stephanieevergreen.com/interactive-data-visualization-checklist/)
    * [Junk Charts Trifecta Checkup](https://junkcharts.typepad.com/junk_charts/junk-charts-trifecta-checkup-the-definitive-guide.html)
* People to follow
    * [Ann K. Emery](https://depictdatastudio.com/) [@evergreendata on Twitter](https://twitter.com/evergreendata)
    * [Stephanie Evergreen](https://stephanieevergreen.com/) [@AnnKEmery on Twitter](https://twitter.com/AnnKEmery)
* Processes
    * [The Dashboard Sketch Process](https://stephanieevergreen.com/the-dashboard-sketch-process/)
* Visualization help
    * [Four Ways to Show Projections](https://stephanieevergreen.com/four-ways-to-show-projections/)
    * #betterposter
        * [Better Scientific Poster](https://osf.io/ef53g/) &mdash; templates in PowerPoint and InDesign
        * LaTeX
            * <https://github.com/rafaelbailo/betterposter-latex-template>
            * <https://github.com/LanaSina/better_poster_latex>

## Feedback

### Advice

Have you designed systems so that errors in data are noted and can inform future practice?

### Resources

## Reproducibility

Will anyone else be able to carry out your analysis in your absence? Will you be able to carry out your own analysis again in 3 months? 3 years?

### Advice

### Resources

* Wilson, G., Bryan, J., Cranston, K., Kitzes, J., Nederbragt, L., & Teal, T. K. (2017). Good enough practices in scientific computing. PLOS Computational Biology, 13(6), e1005510. https://doi.org/10.1371/journal.pcbi.1005510
* Stodden, V., & Miguez, S. (2014). Best Practices for Computational Science: Software Infrastructure and Environments for Reproducible and Extensible Research. Journal of Open Research Software, 2(1), e21. https://doi.org/10.5334/jors.ay

#### Python Resources

#### R Resources

* [Drake](https://github.com/ropensci/drake) is a build system in R for data science projects. It ensures that you only have to run the steps that changed.
* [renv](https://rstudio.github.io/renv/) provides local reproducible package environments for R similar to those that exist in other languages. Ensure that your colleagues or future you will be running the same versions of all your packages!
