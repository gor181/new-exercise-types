---
title: Test
description: Test
---

## An exercise title written in sentence case

```yaml
type: NormalExercise
key: da178ff2d5
lang: python
xp: 100
skills: 2
```

This is the assignment text. It should help provide students with the background information needed.
The instructions that follow should be in bullet point form with clear guidance for what is expected.

`@instructions`
- Instruction 1
- Instruction 2
- Instruction 3

`@hint`
- Here is the hint for this setup problem. 
- It should get students 50% of the way to the correct answer.
- So don't provide the answer, but don't just reiterate the instructions.
- Typically one hint per instruction is a sensible amount.

`@pre_exercise_code`
```{python}
# Load datasets and packages here.
```

`@sample_code`
```{python}
# Your
# sample
# code
# should
# be
# ideally
# 10 lines or less,
# with a max
# of 16 lines.
```

`@solution`
```{python}
# Answer goes here
# Make sure to match the comments with your sample code
# to help students see the differences from solution
# to given.
```

`@sct`
```{python}
# Update this to something more informative.
success_msg("Some praise! Then reinforce a learning objective from the exercise.")
```

---

## Using Visualizations: distplot

```yaml
type: SingleProcessExercise
key: 345b78dcfb
lang: python
xp: 100
skills: 2
```

assignment texta

`@instructions`
* Using the loaded data set `df` filter it down to a single column 'OriginalListPrice' with `select()`.
* Sample 50% of the dataframe with `sample()` making sure to not use replacement and setting the random seed to 42.

`@hint`
Becareful with the dictionary when applying agg functions its .agg({'foo\_column': 'bar\_agg_func'}). The function name is a string.

`@pre_exercise_code`
```{python}
_init_spadsadasda
dasdasda
```

`@sample_code`
```{python}
dasdasd
_____
```

`@solution`
```{python}
dsadsdasda
```

`@sct`
```{python}
success_msg("Awesome, checking the distribution visually is a great way to get an idea of what steps will need to be taken before applying a model.")
```

---

## Create slideshows

```yaml
type: MarkdownExercise
key: 3fbc35eb2b
xp: 100
skills: 1,5
```

You can also export your file as a slideshow by changing the output field to:

    ---
    output: beamer_presentation
    ---

which creates a beamer pdf slideshow,

    ---
    output: ioslides_presentation
    ---

which creates an ioslides HTML slideshow or

    ---
    output: slidy_presentation
    ---

which creates a slidy HTML slideshow.

R Markdown will start a new slide at each first or second level header in your document. You can insert additional slide breaks with Markdown's horizontal rule syntax:

    ***

Everywhere you add these three asterisks in your text, pandoc will create a new slide.

`@instructions`
- Change the output type of the cloud report to a slidy HTML slideshow.
- dsadasdasdas

`@hint`
dsadsadasdas

`@sample_code`
{{{my_document.Rmd}}}
---
title: "Cloud Cover"
author: "Anonymous"
date: "December 2, 2014"
output: html_document
---

## Data

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam convallis fringilla mauris vel suscipit. Aliquam non ex pharetra, fringilla nulla eget, volutpat est. Integer sed nunc ac ipsum semper fringilla sed a velit. Donec id justo sed tellus malesuada vulputate id viverra ante. Sed ultricies orci ac magna consequat mollis

* **cloudlow** - The mean percent of the sky covered by clouds at low altitudes.

* **cloudmid** - The mean percent of the sky covered by clouds at mid-range altitudes.

* **cloudhigh** - The mean percent of the sky covered by clouds at high altitudes.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam convallis fringilla mauris vel suscipit. Aliquam non ex pharetra, fringilla nulla eget, volutpat est. Integer sed nunc ac ipsum semper fringilla sed a velit. Donec id justo sed tellus malesuada vulputate id viverra ante. Sed ultricies orci ac magna consequat mollis

## Cleaning

```{r echo = FALSE}
year <- 2000
```

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam convallis fringilla mauris vel suscipit. Aliquam non ex pharetra, fringilla nulla eget, volutpat est. Integer sed nunc ac ipsum semper fringilla sed a velit. Donec id justo sed tellus malesuada vulputate id viverra ante. Sed ultricies orci ac magna consequat mollis

```{r echo = FALSE, message = FALSE}
library(nasaweather)
library(dplyr)
library(tidyr)
```

```{r}
import a from b
```

`@solution`
{{{solution.Rmd}}}
---
title: "Cloud Cover"
author: "Anonymous"
date: "December 2, 2014"
output: slidy_presentation
---

## Data

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam convallis fringilla mauris vel suscipit. Aliquam non ex pharetra, fringilla nulla eget, volutpat est. Integer sed nunc ac ipsum semper fringilla sed a velit. Donec id justo sed tellus malesuada vulputate id viverra ante. Sed ultricies orci ac magna consequat mollis

***

Some of the variables in the `atmos` data set are:

* **cloudlow** - The mean percent of the sky covered by clouds at low altitudes.

* **cloudmid** - The mean percent of the sky covered by clouds at mid-range altitudes.

* **cloudhigh** - The mean percent of the sky covered by clouds at high altitudes.

***

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam convallis fringilla mauris vel suscipit. Aliquam non ex pharetra, fringilla nulla eget, volutpat est. Integer sed nunc ac ipsum semper fringilla sed a velit. Donec id justo sed tellus malesuada vulputate id viverra ante. Sed ultricies orci ac magna consequat mollis

## Cleaning

```{r echo = FALSE}
year <- 2000
```

For the remainder of the report, we will look only at data from the year `r year`. We aggregate our data by location, using the *R* code below.

```{r echo = FALSE, message = FALSE}
library(nasaweather)
library(dplyr)
library(tidyr)
```

```{r}
dsadsdasda
```

`@sct`
```{r}
test_error()
test_yaml_header(options = "title")
test_yaml_header(options = "author", check_equality = FALSE)
test_yaml_header(options = "date", check_equality = FALSE)
test_yaml_header(options = "output")
test_rmd_group(1, {
test_text(text = "dataexpo/2006/\\).[[:space:]]+\\*\\*\\*[[:space:]]+Some of the ", not_called_msg = "Make sure to add three asteriks before the line that starts with \"Some ofthe variables\". Insert these asterisks on a new line.")
test_text(text = "high altitudes.[[:space:]]+\\*\\*\\*[[:space:]]+You can convert", not_called_msg = "Make sure to add three asteriks before the line that starts with \"You canconvert\". Insert these asterisks on a new line.")
})
success_msg("Great job! When you render R Markdown documents on your own computer, R Markdown will save a copy of the file (in the output file type) on your machine. It will appear in the same folder that the .Rmd file lives in. Feel free to experiment with the other slideshow formats in this exercise!")
```

---

## Insert exercise title here

```yaml
type: MultipleChoiceExercise
key: 47db0b9b42
xp: 50
```



`@instructions`


`@hint`


`@pre_exercise_code`

```{python}

```


`@sct`

```{python}

```
