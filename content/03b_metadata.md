---
layout: default
title: Metadata
parent: Workshop Content
nav_order: 4
---

## Metadata

Recording data about your data (“metadata”) is essential. You may be on intimate
terms with your dataset while you are
collecting and analysing it, but the chances that you will still remember
the exact wording of the question you asked about your
informants' water use (the data recorded in the column `water use`), for
example, are slim.  

As well, there are many reasons other people may want to examine or use your data - to understand your findings, to verify your findings,
to review your submitted publication, to replicate your results, to design a
similar study, or even to archive your data for access and
re-use by others. While digital data by definition are machine-readable,
understanding their meaning is a job for human beings. The
importance of documenting your data during the collection and analysis phase of
your research cannot be overestimated, especially if your
research is going to be part of the scholarly record.  

However, metadata should not be contained in the data file itself. Unlike a table
in a paper or a supplemental file, metadata (in the
form of legends) should not be included in a data file since this information is
not data, and including it can disrupt how computer
programs interpret your data file. Rather, metadata should be stored as a
separate file in the same directory as your data file,
preferably in plain text format with a name that clearly associates it with your
data file. Because metadata files are free text format,
they also allow you to encode comments, units, information about how null values
are encoded, etc. that are important to document but can
disrupt the formatting of your data file.  

Some of this information may be familiar to learners who conduct analyses on
survey data or other data sets that come with codebooks. Codebooks will often
describe the way a variable has been constructed, what prompt was associated with
it in an survey or interview, and what the meaning of various values are. For example,
the [General Social Survey](http://gss.norc.org) maintains their entire codebook online.
Looking at an entry for a particular variable, such as
[the variable `SEX`](https://gssdataexplorer.norc.org/variables/81/vshow), provides
valuable information about what survey waves the variable covers, and the meaning
of particular values.

Additionally, file or database level metadata describes how files that make up
the dataset relate to each other; what format are they are
in; and whether they supersede or are superseded by previous files. A
folder-level readme.txt file is the classic way of accounting for
all the files and folders in a project.  

Metadata are most useful when they follow a standard. For example, the
[Data Documentation Initiative (DDI)](http://www.ddialliance.org) provides a
standardized way to document metadata at various points in the research cycle.
Research librarians may have specific expertise in this area, and can be
helpful resources for thinking about ways to purposefully document metatdata
as part of your research.

(Text on metadata adapted from the online course Research Data [MANTRA](http://datalib.edina.ac.uk/mantra) by EDINA and Data Library, University of Edinburgh. MANTRA is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).)

### Exercise

Step 1
{: .label .label-step}
Download a [clean version of this dataset](https://ndownloader.figshare.com/files/11492171) and open the file with your spreadsheet program. This data has many more variables and is formatted according to tidy data principles.
{: .step}

Step 2
{: .label .label-step}
Looking at the data, what kinds of metadata would be worthwhile to record about the dataset? What information do you need to know if you are someone new to the project?
{: .step}

<details>
  <summary><b>Solution</b></summary>
<br>
Some types of metadata that should be recorded:
<br><br> - The exact wording of questions used in the interviews (if interviews were structured) or general prompts used (if interviews were semi-structured)
<br><br> - A description of the type of data allowed in each column (e.g. the allowed range for numerical data with a restricted range, a list of allowed options for categorical variables, whether data in a numerical column should be continuous or discrete)
<br><br> - Definitions of any categorical variables (e.g. definitions of "burntbricks" and "sunbricks")
<br><br> - Definitions of what was counted as a "room", a "plot", etc. (e.g. was there a minimum size)
</details>
