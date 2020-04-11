---
layout: page
title: Run FORCsensei locally
image: assets/images/local.jpg
nav-menu: true
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Run FORCsensei locally</h1>
		</header>

<!-- Content -->
<p> You can run FORCsensei locally, but there are a number of packages that you will need to install. If you are not familiar with Python, Jupyter notebooks and package management, we recommend that you use the <a href="https://forcaist.github.io/FORCaist.github.io/amybinder.html" target="_blank">cloud-based</a>
 version of FORCsensei.</p>

<h2>Option 1: Docker</h2>
<p>A relatively simple approach to running FORCsensei locally is via <a href="https://www.docker.com/" target="_blank">Docker</a>. Install <a href="https://www.docker.com/" target="_blank">Docker</a> and then create an image to run on your system directly from the FORCsensei GitHub repository using <a href="https://github.com/jupyter/repo2docker" target="_blank">repo2docker</a>.</p> 

<h2>Option 2: Local Installation</h2>
Locally installation should be straight-forward. This installation procedure has been tested on a number of systems, but we discuss potential installation issues at the bottom of this page.



Please be aware the local installation will add new packages (or potentially overwrite existing packages) on your system. If you are not comfortable with this, then you should not attempt local installation.


First, if you don't have Python and/or Jupyter installed, we recommend installing Anaconda from: https://www.anaconda.com/distribution/


To run FORCsensei locally requires a number of extra packages, which can be installed via ```pip``` or ```sudo```. Open a terminal and give the commands:

```
pip install appmode
pip install ipyfilechooser
pip install numba
pip install pandas
pip install IPython==7.2.0
pip install matplotlib==2.2.2
pip install numpy==1.15.0
pip install ipywidgets==7.5.1
pip install scipy==1.1.0
pip install bokeh==1.0.4
pip install git+https://github.com/FORCaist/forcsensei.git
pip install jupyter_contrib_nbextensions
pip install dask distributed --upgrade
jupyter contrib nbextension install --user
jupyter nbextension enable --py widgetsnbextension
jupyter nbextension enable --py --sys-prefix appmode
jupyter serverextension enable --py --sys-prefix appmode
```
<p>Once the dependencies are installed you can download the FORCsensei notebook <a href="https://github.com/FORCaist/forcsensei/blob/master/FORCsensei.ipynb" target="_blank">here</a>. Save the FORCsensei notebook into a folder of your choice</p> 

Now, ```cd``` into the folder where you placed ```FORCsensei.ipynb``` and give the command:
```
jupyter trust FORCsensei.ipynb
```

Everything should now be ready. You can start FORCsensei, using the command:
```
jupyter notebook FORCsensei.ipynb
```

<p> FORCsensei is designed to be run in <a href="https://github.com/oschuett/appmode" target="_blank">Appmode</a>, which should appear as a button once you open the notebook in Jupyter.</p> 

Click the ```Appmode``` button in the banner at the top and FORCsensei should be ready to run (see the video tutorial).

<h3>Solutions to potential installation issues</h3>
<HR SIZE="6">

An error appears when I give the command:

```pip install git+https://github.com/FORCaist/forcsensei.git```

It looks like your system can't install packages from from git repositories. Potential solutions are:

* MAC - give the commands ```xcode-select --install```, then ```xcode-select --reset```
* Windows - I don't know, buy a MAC

<HR SIZE="6">

An error appears when I give the command:

```pip install ...``` for a given package

This isn't a FORCsensei related error, but rather something to do with the third-party package you are trying to install. Visit the package homepage, or google the error to try to get more information.

<HR SIZE="6">

The ```FORCsensei.ipynb``` file is saved onto my system as ```FORCsensei.ipynb.html```

This may occur if you are using Safari, which has a nasty habit of appending ```.html``` to certain types of files. The easiest solution is to visit the FORCsensei GitHib repository (https://github.com/FORCaist/forcsensei). Download the entire repository as a ZIP file using the green ```Clone or Download``` button. Contained within the ZIP will be a copy of ```FORCsensei.ipynb``` without the random ```.html``` extension. 
