# Awesome Data Effectiveness

Communicating your data for the desired effect

Do you struggle with analyzing and communicating data to effect the changes you would like to see in the world? Do you have any approaches that work particularly well for your projects?

Welcome to a world in which other data professionals care about improving practice as much as you do! We invite you to join in a conversation and collective data collection experience about which data practices aid in maximizing effectiveness. _¡Vivan los datos efectivos!_

* [Poster from 2019-01-10 presentation](poster/awesome-data-effectiveness-poster.pdf)

## Purpose and planning (Discuss)

Why are your collecting the data? What decisions do you want to make based on the data? It's best practice to define a question and search for solutions, as opposed to being given a large set of data to explore for intersting queries.

### Advice
Below is an outline of the 'scientific method', the approach that should be taken when testing a theory.
1. Think about a question you're intersted in, try and frame this as best as you can about the intended outcomes and impacts.
1. Formulate a clear hypothesis
	1. This is the one question you want to address with your data, anything else is gravy (or to be reformulated into a new hypothesis).
	1. Understand what the NULL hypothesis means, that's the state of affairs if your predicted hypothesis is not true. 
1. Predict a testable outcome
	1. This step is important, all statistical results can do is give you an 'idea' of how true or false your prediction is. They do not provide an absolute truth.
	1. Try and distinguish what you're looking for from other possible influences (and corresponding data models). To expand, if there are two hypotheses with the same predictions, then observing that prediction will validate both hypotheses.	
1. Test your hypothesis using some analysis
	1. You may already have the data! (If not, you'll need to collect the data - and this beyond the scope of this document).
	1. Apply and tune the relevant fitting procedure or machine learning algorithm.
	1. This is the step most people think of when referring to anything 'data related'. In practice it's likely a short step, post data cleaning etc. Validation of results and quantifying uncertainties may (should?) take a longer amount of time.
1. Results
	1. Does your hypothesis align with results, or are results more consistent with the NULL hypothesis?
	1. Significance is only relevant with regard to the NULL hypothesis
	1. Attempt to quantify the uncertainty within the claimed results
	

### Resources

* [Synopsis of scientific method](https://www.thoughtco.com/steps-of-the-scientific-method-p2-606045)

## Collection

How can you design data collection to align with your purpose and ease analysis?

### Advice

1. Survey Creation
    1. Plan/think about how you will analyze the data from each question as you create them.
    1. Use data validation on user-input questions to regulate what kind of data is collected.
    1. Remember that what you are able to analyze later depends of what you collect. If you collect detailed information, you can always group answers together later, but if you ask for only broad data, you cannot break that into more detailed options afterward.
    1. Think about what data type is best for each question from the beginning (numeric vs text vs date, etc.)

### Resources

* Data Stories podcast about how to design survey questions (BV enter)

### Data types

Depending on the software tools used for analysis, there are multiple available data types. For the most part these tend to be divided into:
* Numerical values
1. To provide more detail, numerical values can represent integers or floating point values. 
	1. An integer is a whole number, for example 'age in years'. We'd expect to see a response given in a number without decimal places. Take someone who is 35 years old, the response expected is '35'.
	1. Alternatively, floating points allow decimal places (to some precision). If we're considering a continuous variables, such as a precise value of age, this can be represented in seconds arbitrary precision.
		1. As an example, a 35 year old may respond to age as 1.104e+9 seconds. Depending on what specific type is used to represent this, and the available computer memory, this could be 1.1045358974e+9 seconds.
* Strings or text
	1. This is useful for fields that represent values such as name.
	1. It's detrmiental to store fields that should be numeric as a string.
		1. In particular, it's especially irritating if age were represented as string. In this case we could end up with responses along the lines of '35', '35 years', '1.104e+9', making the consolidation of all responses difficult.
* Boolean values
	1. Represent values that only have a true or false value. 
	1. An example could be, 'are you 35 years old, or older?'. Following from our age example, in such a case for a 35 year old we'd store a response of 'true'. Note the explicit representation depends on the programming language used, but regardless it will be one of two possible values.
	

### Data validation and quality

Defining data types will spot immediate problems with data validation. If someone responds '35 years' to an age field that should be numeric, this will illicit an error as the string 'years' is not interpretable as a numerical value. Such validation (and addressing of said erroneous data) is necessary for any analysis.
Despite such checks, we can also have responses to an age field such as '45448752'. While this is a numeric value, it is obviously not a valid response to the question of age. This is now a data quality issue. Data quality issues may be difficult to find by glancing at data, but by visulizing the responses we can spot outliers that are non sensical. For example, by plotting the age variable as a histogram (a frequency count of responses), we'd spot an erroneous response as being many standard deviations from the mean value of age.

## Metadata

What additional information does one need to make sense of your data? How can it be used effectively?

### Advice

### Resources

## Storage and data quality (Discussion)

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
1. Data types
	1. Use the correct format and data types (e.g. dates should use ISO 8601 standard, are the numbers integers or floating point numbers) for each variable. If you don't know about data types, ask.
1. File Organization / Data Flow Management
    1. Especially for reports that will happen again, clearly organize and label all files and folders. One way is to use prefixes in front of the names and folders to keep them in a logical order (e.g. "01 original data", "02 edited data", "03 final report").
    1. Never edit the original data: keep a the original data clearly marked in one location, and make a copy of the original data to be edited.
    1. Keep track of changes made to the original data so your efforts can be reproduced. See Section "Reproducibility" below.

https://www.grow.com/blog/the-cost-of-poor-data-quality-and-how-to-avoid-it
### Resources

* Broman, K. W., & Woo, K. H. (2018). Data Organization in Spreadsheets. The American Statistician, 72(1), 2–10. https://doi.org/10.1080/00031305.2017.1375989
* [Condensed information about spreadsheet don'ts (and do's)](https://lgatto.github.io/spreadsheet-ecology-lesson/00-intro.html)
* Style guide for variable naming
  * [names for variable conventions (Allison Horst)](https://twitter.com/allison_horst/status/1205702878544875521/photo/1)
* CSV
  * [Doing a database join with CSV files](https://www.johndcook.com/blog/2019/12/31/sql-join-csv-files/) using [xsv](https://github.com/BurntSushi/xsv)
* Data Quality tips
  * [Qualities of 'good' data, and problems caused with 'bad' data'](https://www.grow.com/blog/the-cost-of-poor-data-quality-and-how-to-avoid-it)
  * [Monetary focused costs of 'bad' data](https://www.habiledata.com/blog/5-data-entry-errors-companies-should-avoid-to-improve-accuracy/)

## Transformation

Does the layout of your data permit easy analysis? Sometimes the transformation of the data will depend on the specific purpose. Can your data be transformed readily?

### Advice

1. Often, storing related data in separate tables and joining them when necessary works better than storing one big table with many rows of duplicate information. How can you find a tool that supports easy data joining?

Data quality and missing data

### Resources

## Communication and visualization (Discussion)

Do the visualizations communicate in a way that facilitates decisions?

### Advice

1. 

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

1. Have you designed systems so that errors in data are noted and can inform future practice?

### Resources

## Reproducibility (Discussion)

Will anyone else be able to carry out your analysis in your absence? Will you be able to carry out your own analysis again in 3 months? 3 years?

“non-reproducible single occurrences are of no significance to science” - Karl Popper
Can your public results be followed so that some other institutions can perform the same analysis?


### Advice

1. Document your work as you go! 
	1. Use the standard of 'can someone else re-perform these tasks based on what is written here?' In 3 months, you might be that 'someone else' in 3 months.
	1. Refrain from using too many acronyms and buzzwords that are difficult for others to follow.
1. Never edit the original data: keep a the original data clearly marked in one location, and make a copy of the original data to be edited.
1. Keep track of changes made to the original data so your efforts can be reproduced. For example, use code/syntax and/or keep detailed notes. If editing data in Excel, you can create a copy of the tab/sheet after each major set of changes to the data -- you would end of with lots of little tabs acting like "save points".


### Resources

* Wilson, G., Bryan, J., Cranston, K., Kitzes, J., Nederbragt, L., & Teal, T. K. (2017). Good enough practices in scientific computing. PLOS Computational Biology, 13(6), e1005510. https://doi.org/10.1371/journal.pcbi.1005510
* Stodden, V., & Miguez, S. (2014). Best Practices for Computational Science: Software Infrastructure and Environments for Reproducible and Extensible Research. Journal of Open Research Software, 2(1), e21. https://doi.org/10.5334/jors.ay

#### Python Resources

#### R Resources

* [Drake](https://github.com/ropensci/drake) is a build system in R for data science projects. It ensures that you only have to run the steps that changed.
* [renv](https://rstudio.github.io/renv/) provides local reproducible package environments for R similar to those that exist in other languages. Ensure that your colleagues or future you will be running the same versions of all your packages!
