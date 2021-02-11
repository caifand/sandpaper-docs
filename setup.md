---
sandpaper-digest: 27db8518d5912a82d466a92a48be78b3
sandpaper-source: /Users/runner/work/sandpaper-docs/sandpaper-docs/learners/setup.md

title: Setup
---

The {sandpaper} template requires [R] and [pandoc] to be installed, both of 
which are bundled in the [RStudio] IDE. 

## Foundational software

There are three programs that the template works with: Git, RStudio, and pandoc.
They can be installed from the following resources:

 - **Git** https://carpentries.github.io/workshop-template/#git
 - **R** https://carpentries.github.io/workshop-template/#r
 - **pandoc** we recommend installing this by [installing the RStudio IDE][RStudio]

::::: solution

### What if I don't want to use RStudio?

That's perfectly okay! If you do not want to use RStudio, you can install pandoc
directly to your computer by following the directions on https://pandoc.org/installing.html.
We recommend using RStudio because it is tightly integrated with pandoc. 

:::::::::

## Lesson Template Modules (R packages)

The template is divided into three R pakages, which are designed to be modular
and upgradable on the fly. Because these are still in developement, please use
the following to install (*and update*) the packages:

First, **open R/RStudio** and then follow the instructions based on your
operating system:

::::::::::: solution

### MacOS/Windows

```r
# register the repositories for The Carpentries and CRAN
options(repos = c(
  carpentries = "https://carpentries.github.io/drat/",
  CRAN = "https://cran.rstudio.com/"
))

# Install the template packages to your R library
install.packages(c("sandpaper", "varnish", "pegboard"))
```

::::::::::::::::::::


::::::::::: solution

### Linux

Note: we are using the RStudio package manager. This is set up for Ubuntu 20.04,

:::: callout

### What if I have a different version of Linux?

If you have a different version of linux, you can visit https://packagemanager.rstudio.com/client/#/repos/1/overview, 
select your system where it says "Use this URL to work with the latest binary
packages for Ubuntu 20.04 (Focal) **change**", and replace the packagemanager
URL below.

::::

```r
options(repos = c(
  carpentries = "https://carpentries.github.io/drat/",
  CRAN = "https://packagemanager.rstudio.com/all/__linux__/focal/latest"
))

install.packages(c("sandpaper", "varnish", "pegboard"))
```
::::::::::::::::::::



[R]: https://cran.rstudio.org/
[pandoc]: https://pandoc.org/
[RStudio]: https://rstudio.com/products/rstudio/download/#download