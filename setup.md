---
title: Setup
---

__Workshop data files__  
Prior to the workshop, you must download the example datafiles and test importing them into R. To do this:

1) Download the example datasets from [here](https://cloudstor.aarnet.edu.au/plus/s/v8mgCgNGdQoUJIg).   

2) Save the downloaded file to Downloads, Desktop or another convenient location on your computer, and double-click to expand it - it will create a 
directory called 'data'.  

3) Open RStudio and set your working directory to **the same location where you saved the downloaded file** - not the data directory itself. The easiest 
way to do this is click on the Files tab (normally in the bottom right pane) and navigate to the folder that way, then use the function "Set as working 
directory" from the More (cog icon) menu just at the top of the file window.  

4) Read in the workshop data by typing the command `heart <- read.csv("data/heart_disease.csv", stringsAsFactors = TRUE)` in the RStudio console pane 
(usually bottom left). This should complete without any warnings. If you get a message starting `Error in file(file, "rt") : cannot open the connection` 
you have not set your working directory to the correct location - recheck where you saved and extracted the workshop datafile and repeat step 3.  
N.B. The 'stringsAsFactors' argument is required because of a change made between R versions 3.6 and 4.0 - this option means that you will generate the 
same structure dataframe whichever version of R you are using.


__Install Packages__
The following packages are required during the workshop and must be installed beforehand:
* ggplot2
* GGally
* lmtest
* car
* MASS

To install packages, use the command `install.packages("PACKAGE_NAME")`, substituting PACKAGE_NAME with the name of the required package (this is case 
sensitive). To install all five packages in a single command run `install.packages(c("ggplot2", "GGally", "lmtest", "car", "MASS"))`. If you are asked 
whether to install packages from source, select "No".

