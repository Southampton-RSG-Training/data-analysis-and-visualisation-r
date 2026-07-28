---
title: 'Reference'
---

## Other Resources and Further Learning

*   [R for Data Science (2e) - free online book](https://r4ds.hadley.nz/)
*   [RStudio IDE cheatsheet](https://github.com/rstudio/cheatsheets/raw/master/rstudio-ide.pdf)
*   [dplyr documentation and cheatsheet](https://dplyr.tidyverse.org/)
*   [tidyr documentation and cheatsheet](https://tidyr.tidyverse.org/)
*   [ggplot2 documentation and cheatsheet](https://ggplot2.tidyverse.org/)
*   [lubridate documentation](https://lubridate.tidyverse.org/)
*   [tidyverse style guide](https://style.tidyverse.org/)
*   [R documentation search](https://www.rdocumentation.org)
*   [Stack Overflow `r` tag](https://stackoverflow.com/questions/tagged/r?tab=Votes)
*   [RStudio Community forum](https://community.rstudio.com/)
*   [CRAN Task Views (browse packages by topic)](https://cran.r-project.org/web/views/)


## Glossary

[argument]{#argument}
:   A value passed to a [function](#function) when it is called, used to
    control what the function does. Some arguments are required; others
    have default values and are called [options](#option).

[assignment operator]{#assignment-operator}
:   The `<-` symbol used in R to assign a [value](#value) to an
    [object](#object), e.g. `weight_kg <- 55`. Can be read as "55 goes
    into `weight_kg`". The `=` sign can also perform assignment but is
    conventionally reserved for setting function arguments.

[class]{#class}
:   The type of an R [object](#object) (e.g. `numeric`, `character`,
    `data.frame`, `factor`), which determines how functions handle it.
    Found using the `class()` function.

[coercion]{#coercion}
:   The automatic conversion of values from one [class](#class) to
    another when they are combined, for example when mixed data types
    are placed in a single [vector](#vector). Coercion follows a
    hierarchy: logical → integer → numeric → character.

[comment]{#comment}
:   A remark in a script intended to help human readers understand the
    code, but ignored when the code runs. Comments in R start with a
    `#` character and run to the end of the line.

[console]{#console}
:   The pane in RStudio where R commands can be typed and are executed
    immediately, and where results are displayed. Indicated by a `>`
    prompt when ready for input, or a `+` prompt when an incomplete
    command is still being entered.

[coordinates]{#coordinates}
:   In the context of a data frame, the row and column position (e.g.
    `surveys[1, 6]`) used with square-bracket indexing to extract
    specific data. Row numbers are specified first, followed by column
    numbers.

[data frame]{#data-frame}
:   A tabular [data structure](#data-structure) in which columns are
    [vectors](#vector) of equal length, and each column holds a single
    type of data. The standard structure for tabular data in R, most
    commonly created by `read.csv()` or `read.table()`.

[data structure]{#data-structure}
:   A way of organising and storing data in R. Common data structures
    include vectors, lists, matrices, data frames, factors, and arrays.

[factor]{#factor}
:   A [data structure](#data-structure) used to represent categorical
    data. Factors are stored internally as integers associated with
    text [levels](#level), and can be ordered or unordered.

[filtering]{#filtering}
:   Subsetting rows of a data frame based on a logical condition, most
    commonly with the **`dplyr`** function `filter()`, e.g.
    `filter(surveys, year == 1995)`.

[function]{#function}
:   A named, reusable set of instructions that performs a task, usually
    taking one or more [arguments](#argument) as input and returning a
    [value](#value) as output. Running a function is called *calling*
    it, e.g. `sqrt(10)`.

[geom]{#geom}
:   Short for "geometric object"; a **`ggplot2`** layer function that
    determines how data is visually represented in a plot, such as
    `geom_point()` for scatter plots, `geom_boxplot()` for boxplots, or
    `geom_line()` for line plots.

[aesthetic mapping]{#aesthetic-mapping}
:   In **`ggplot2`**, the association between variables in a dataset and
    visual properties of a plot (position, colour, size, shape), set
    using the `aes()` function, e.g. `aes(x = weight, y = hindfoot_length)`.

[faceting]{#faceting}
:   A **`ggplot2`** technique that splits a single plot into multiple
    small panels based on the values of one or more variables, using
    `facet_wrap()` or `facet_grid()`.

[level]{#level}
:   One of a pre-defined set of possible values that a [factor](#factor)
    can take. By default, R sorts levels alphabetically. Found using the
    `levels()` function.

[library]{#library}
:   A collection of R [functions](#function), data, and documentation
    bundled together as a [package](#package); also the name of the
    function (`library()`) used to load an installed package into an R
    session.

[missing value]{#missing-value}
:   A value that is absent from a dataset, represented in R by `NA`.
    Many functions return `NA` if any input contains missing values
    unless told to ignore them, typically with the argument
    `na.rm = TRUE`.

[object]{#object}
:   A named "container" in R that stores a [value](#value), such as a
    number, character string, vector, or data frame. Also referred to as
    a *variable*. Created using the [assignment operator](#assignment-operator).

[option]{#option}
:   An [argument](#argument) to a function that has a default value,
    typically used to alter how the function behaves (e.g. `digits` in
    `round()`). Can be left out to use the default, or specified to
    override it.

[package]{#package}
:   A collection of R functions, data, and documentation that extends
    R's built-in capabilities. Must be installed once with
    `install.packages()` and loaded in each session with `library()`.

[pipe]{#pipe}
:   An operator that passes the result of one expression as the first
    argument to the next, allowing multiple operations to be chained
    together in a readable sequence. Written as `|>` in base R (or
    `%>%` from the **`magrittr`**/**`tidyverse`** packages).

[pivoting]{#pivoting}
:   Reshaping a data frame between "wide" and "long" formats using
    **`tidyr`** functions: `pivot_longer()` converts columns into rows
    (wide to long), and `pivot_wider()` converts rows into columns (long
    to wide).

[reproducibility]{#reproducibility}
:   The ability for someone else, including your future self, to obtain
    the same results from the same dataset using the same documented
    analysis steps, typically achieved by working from saved scripts
    rather than manual, undocumented actions.

[script]{#script}
:   A plain text file containing a saved sequence of R commands, which
    can be run and re-run to reproduce an analysis. Written and edited
    in the RStudio Source pane.

[split-apply-combine]{#split-apply-combine}
:   A data analysis strategy in which data is split into groups (using
    `group_by()`), a function is applied to each group (e.g. with
    `summarize()`), and the results are combined into a single output.

[subsetting]{#subsetting}
:   Extracting specific elements from a [vector](#vector) or
    [data frame](#data-frame), using numeric indices, logical
    conditions, or column/row names inside square brackets, or with
    **`dplyr`** functions like `select()` and `filter()`.

[tibble]{#tibble}
:   The **`tidyverse`** version of a [data frame](#data-frame) (class
    `tbl_df`), with slightly different default printing and behaviour,
    typically created by `read_csv()` rather than `read.csv()`.

[value]{#value}
:   A piece of information stored and retrieved by an [object](#object),
    such as a number, a character string, or a collection of these, such
    as a [vector](#vector).

[vector]{#vector}
:   The most basic [data structure](#data-structure) in R: an ordered
    collection of values of the same [class](#class), created with the
    `c()` function.

[working directory]{#working-directory}
:   The folder R uses as the default location to look for and save
    files. Best managed using an RStudio Project, and checked with
    `getwd()`. Scripts should not hard-code changes to it with `setwd()`,
    since this will not work on someone else's computer.



