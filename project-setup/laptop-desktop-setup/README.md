# Laptop/Desktop Setup

As the logic tier of the project runs on the server (our laptop) side, some packages needs to be installed as prerequisite.

Install the conda environment on your laptop/desktop by following the instruction [here](https://docs.conda.io/en/latest/miniconda.html), create an environment and install the following packages

```
pip install numpy matplotlib ...... // install all thats being imported
```

Simplist way to do this is to try run the main.py file and install the packages according to the error message prompted.

OpenCV needs to be installed with a legacy edtion

```
pip install opencv-contrib-python==4.6.0.66
```

The latest version has made some change for a method we called, can be edited to fit the latest versoin for improvment.
