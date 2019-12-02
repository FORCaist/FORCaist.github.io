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
<p> You can run FORCsensei locally, but there are a number of packages that you will need to install. If you are not familiar with Python, Jupyter notebooks and package management, we recommend that you use the cloud-based version of FORCsensei.</p>

<h2>Install Anaconda</h2>
<p>Anaconda is a free and open-source distribution of the Python. Anaconda comes with more than 1,400 packages as well as the Conda package and virtual environment manager, called Anaconda Navigator, so it eliminates the need to install each library independently. Anaconda also includes Jupyter Notebooks, which is the foundation for FORCsensei.</p> 

<p> 1) Visit the <a href="https://www.anaconda.com/distribution/" target="_blank">Anaconda Download site</a>, scroll downwards and select the 64-bit graphical installer for Python 3.7.</p> 

<p> 2) Once the installer is downloaded, you can run it and install Anaconda with a few clicks. During installation you will be asked about PATH options:

<ul>
<li>Windows - We recommend that you <b>do not</b> add Anaconda to the PATH.</li>
<li>macOS & Linux - We recommend that you <b>do</b> add Anaconda to the PATH.</li>
</ul></p>

<h2>Install Dependencies</h2>
<p>FORCsensei requires a number of extra packages, which can be installed via pip or sudo (some will be included in Anaconda).</p> 

<p>Specifically you'll need:
 <ul>
  <li>appmode</li>
  <li>ipyfilechooser</li>
  <li>numba</li>
  <li>IPython</li>
  <li>matplotlib</li>	 
  <li>numpy</li>
  <li>ipywidgets</li>
  <li>scipy</li>
  <li>bokeh</li>
  <li>jupyter_contrib_nbextensions</li>
  <li>dask distributed</li>
  <li>git+https://github.com/FORCaist/turbosensei.git</li>
</ul>
 
<h2>Running FORCsensei</h2>
<p>You can download the FORCsensei notebook <a href="https://github.com/FORCaist/turbosensei/blob/master/TURBOsensei.ipynb" target="_blank">here</a>.</p> 

<p> FORCsensei is designed to be run in <a href="https://github.com/oschuett/appmode" target="_blank">Appmode</a>, which should appear as a button once you open the notebook in Jupyter</p>

https://github.com/oschuett/appmode
