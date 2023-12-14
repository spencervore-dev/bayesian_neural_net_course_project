# README #

This repo contains code and documentation for my ISYE6420 Bayesian Statistics course project at Georgia Tech, taken in the Fall of 2023. I asked the course Teaching Assistants in the course discussion board, and they said it would be ok for me to publish my code and report to a public repository, so here it is.

**Developer: Spencer Vore**  
**Published: Dec 2023**  


### Project Summary ###
This project tries to fit Bayesian Markov Chain Monte Carlo (MCMC) prediction models to the Abalone ring dataset from the UCI repository. The goal is to demonstrate how non-linear models can be fit to data.  PyMC is used as a probablistic programming language. 

3 models were fit. The first is a basic bayesian linear model. Since the General Linear model is essentially a neuron, multiple of these were created. The second model is a 2-layer neural network, and the final model is a 3-layer "deep" neural network. These are not large neural networks due to the computational intensity of running MCMC. This is meant as a demonstration of how a bayesian neural network can be fit in principle. 

A detailed whitepaper style project writeup is saved in this repository as a PDF as well for more information.

All this code and documentation was created in about 2 weeks, so forgive me if it isn't perfect.


### Installation and Setup ###

Hardware used:
System76 Lemur Pro (2021) laptop.  Everything was run on the 11th Gen Intel® Core™ i5-1135G7 × 8 CPU.

I installed this in a conda environment on a Fedora 38 system.  The PyMC documentation says it's available on conda-forge, so I used a conda virtual enviroment 
to be consistent with the PyMC documentation and get it working easy. Python 3.11.6 was used.
On Fedora, I needed to install gcc to solve error saying g++ not detected.
``` sudo dnf install gcc-c++ ```

WARNING: It is a bit tricky to get a working PyMC Python environment. Also, PyMC tends to have breaking changes fairly often, so this could all be outdated if you try a different version. The course website has some useful PyMC troubleshooting tips:
https://areding.github.io/6420-pymc/unit6/Unit6-probabilisticprogramming.html

First, create a PyMC python enviroment using the instructions on the PyMC website here: https://www.pymc.io/projects/docs/en/latest/installation.html

I was having some issues getting jupyterlab also installed. I think there is some versioning issue with conda-forge going on at the moment that will hopefully clear up at some point.

Then, install additional required third party libraries using conda. It works best if everything is installed
with the same python package manager.

``` pip install -r requirements.txt ```

Once the enviroment is set up, launch jupyter notebooks by typing:

``` jupyter lab ```


### Repo Structure ###
A description of important files, what they are for, and where they are located in this repo is below.

Project_Code_VoreSpencer.ipynb - This is the jupyter notebook containing all the project code
abalone - a directory containing the dataset downloaded from the UCI Machine Learning Repository
requirements.txt - File containing pip installable list of 3rd party Python libraries
Project_Report_VoreSpencer.pdf - A whitepaper style writeup describing the results of this project.


### References ###
Below are references and outside sources that helped build this project.

Dataset in this repo was downloaded from: 
Abalone dataset from UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/1/abalone

Useful whitepaper about Bayesian Neural Networks:
Jospin, Laurent Valentin, et al. "Hands-on Bayesian neural networks—A tutorial for deep learning users." IEEE Computational Intelligence Magazine 17.2 (2022): 29-48.
https://arxiv.org/pdf/2007.06823.pdf

Course Github website where the TA has created a number of useful examples of how to use PyMC. Much of this code was inspired from / modified from the code demoed on this course website.
Unit 6 onwards has most of the useful PyMC examples:
https://areding.github.io/6420-pymc/intro.html
