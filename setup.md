---
title: Setup
---

__Workshop Data Files__  
Prior to the workshop, you must set up a project folder, download the example data files into it, and test importing them into R. To do this:

1) Open RStudio and create a new **RStudio Project** for the workshop: go to `File -> New Project... -> New Directory -> New Project`. Give it a name (e.g. "LinearRegressionWorkshop"), and choose **Desktop** (or another convenient location) as the location for the project. This creates a dedicated project folder containing an `.Rproj` file. Opening this file (or selecting the project from RStudio's project menu, top right) will always set your working directory to this folder automatically, every time.  

2) Download the example datasets (a `.zip` file) from [here](https://drive.google.com/uc?export=download&id=1URnPkGBwcguRE89vYlvF3JOqNWqFc-Op).   

3) Extract the downloaded `.zip` file - this will create a directory called 'data'. Then move this 'data' folder into your new project folder.
   * **Mac:** double-click the file or right-click and choose "Open With -> Archive Utility".
   * **Windows:** right-click the file and choose "Extract All...".  

4) Read in the workshop data by typing the command `heart <- read.csv("data/heart_disease.csv", stringsAsFactors = TRUE)` in the RStudio console pane (usually bottom left). This should complete without any warnings.

If you get a message starting `Error in file(file, "rt") : cannot open the connection`, the data folder is not inside your project folder - recheck step 3 and repeat step 4.

N.B. The 'stringsAsFactors' argument is required because of a change made between R versions 3.6 and 4.0 - this option means that you will generate a data frame of the same structure whichever version of R you are using.

__Install Packages__
The following packages are required during the workshop and must be installed beforehand:
* ggplot2
* GGally
* lmtest
* car
* MASS

To install packages, use the command `install.packages("PACKAGE_NAME")`, substituting PACKAGE_NAME with the name of the required package (this is case sensitive). To install all five packages in a single command, run `install.packages(c("ggplot2", "GGally", "lmtest", "car", "MASS"))`. If you are asked whether to install packages from source, select "No".
