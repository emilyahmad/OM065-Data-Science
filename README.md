# OM065-Data-Science

[Anki deck](https://ankiuser.net/study)
___

Simple R installation
[download R]()
[download Jupyter/conda]()

open R in terminal, run
```
R

install.packages(c('repr', 'IRdisplay', 'evaluate', 'crayon', 'pbdZMQ', 'devtools', 'uuid', 'digest'))

install.packages('IRkernel')

IRkernel::installspec()

conda install -c conda-forge r-irkernel
```

___


repo to store hw, labs, etc.

↓ See if you can make this a dropdown
Class instructions (outdated links), [chat setup link](https://chatgpt.com/share/6a96cf85-65b0-83ea-babb-7dd1a58f8831)

```
R (and Jupyter) Download and Setup Instructions
Using Admin privileges:

Install R from https://cran.r-project.org/Links to an external site.
Install R Studio from https://www.rstudio.com/Links to an external site.
Install Anaconda (Python recommended version) from https://docs.anaconda.com/anaconda/install/index.htmlLinks to an external site. Next, follow the download instructions in the link for your operating system.
On Windows open Anaconda prompt and install jupyter_client by typing conda install -c anaconda jupyter_client from https://anaconda.org/anaconda/jupyter_clientLinks to an external site.
On MacOS there is no separate Anaconda prompt, install the Jypyter client directly from a terminal.
Install R kernel by following instructions from https://www.datacamp.com/community/blog/jupyter-notebook-rLinks to an external site.
(Note): Running R from R Studio OR the Program Icon will not work, you need to open a windows prompt/ bash/ your system prompt, find the executable file for R and run it in the shell, giving the full path to the executable R file. You need to do this only once. Running R inside the Anaconda Prompt and installing the IR kernel from within Anaconda also works.

(Windows): path for R executable is usually

"C:\Program Files\R\R-4.0.2\bin\x64\R.exe"

(MacOS): There is no separate Anaconda Prompt. Open a terminal and install the IRkernel from the terminal directly.

At the Anaconda prompt type jupyter notebook, if you have done everything successfully, R should be in the list of Kernels in the notebook under "New".
```

# Good to know

- Common errors
  When running in R Studio, and you get an "error: object 'x' not found"
  RStudio isn't automatically raeding the whole file, you must send its definition line to the console before using it as a variable by **highlighting the line where you assign the variable** and running with **Cmd + Return**

- Syntax
  name <- c("Greg", "Gill") concatenates everything & recognizes those are characters

- Subsets
  friends$name returns the variable within the data frame

friends[1:3,1] # blank: everything | rows, cols, can splice with : | subsets
friends[friends$age<50, 1:2] # select those with < 50 for friends variable & first & second column

- Packages/libraries
  Tidyverse %>%
  ggplot2
  grid
  gridExtra
  repr

# Helpful Commands

- Load dataset into dataframe
  MetroHealth83.df <- read.csv(file="PATH", header=TRUE, sep=",")
