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

<h2>Option 1: Docker</h2>
<p>A relativly simple approach to running FORCsensei locally is via Docker. Install Docker and then create an image to run on your system directly from the GitHub repository using repo2docker.</p> 

<h2>Option 2: Install Dependencies</h2>
<p>To run FORCsensei locally requires a number of extra packages, which can be installed via pip or sudo (some will be included in Anaconda). You can find a list of the dependencies in the <a href="https://github.com/FORCaist/turbosensei/blob/master/requirements.txt" target="_blank">requirements.txt</a> file.</p>

<p>Some of the packages require extra commands to activate them, check on the developers' sites to obtain this information for your system. </p>

<p>Once the dependencies are installed you can download the FORCsensei notebook <a href="https://github.com/FORCaist/turbosensei/blob/master/TURBOsensei.ipynb" target="_blank">here</a>.</p> 

<p> FORCsensei is designed to be run in <a href="https://github.com/oschuett/appmode" target="_blank">Appmode</a>, which should appear as a button once you open the notebook in Jupyter.</p>
