# Ipopt Installation

To install ipopt on machine that runs windows os, follow the instructions on this [page](https://cyipopt.readthedocs.io/en/stable/install.html#using-conda). Start by activating your created conda environment, then use following command to install with conda.

```
conda install -c conda-forge cyipopt
```

Then run "conda list" and check if it is successfully installed.

However, at this point you might still get into error saying "ipopt" module is not found even it shows in the package list. To resolve this issue, go to this [site](https://www.coin-or.org/download/binary/Ipopt/) and download the package, install from the source.

Download 3.11.1 win64 version and extract to somewhere you like. Copy the path that has the .exe file add it to your system PATH.

To add the path that contains .exe file to the system PATH, go to advanced system settings -> environment variable -> Under system variable, click on edit -> add the path in clipboard to the end of the variable block, separated from the other with ";".
