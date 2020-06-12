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
<p>You can run FORCsensei locally, but there are a number of packages that you will need to install. If you don't want to install packages locally, we recommend that you use the&nbsp;<a href="https://forcaist.github.io/FORCaist.github.io/amybinder.html" rel="nofollow">cloud-based</a>&nbsp;version of FORCsensei (it is, however, very slow).</p>


<p>Once you have have completed a local installation (detailed instructions below), this <a href="https://youtu.be/1ylBnYteVxI" target="_blank">tutorial video</a> will show you how to start FORCsensei.</p> 

<h2><a id="user-content-option-1-docker" aria-hidden="true" href="https://github.com/FORCaist/FORCaist.github.io/blob/master/brunlocal.md#option-1-docker"><svg viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Option 1: Docker</h2><p>A relatively simple approach to running FORCsensei locally is via&nbsp;<a href="https://www.docker.com/" rel="nofollow">Docker</a>. Install&nbsp;<a href="https://www.docker.com/" rel="nofollow">Docker</a>&nbsp;and then create an image to run on your system directly from the FORCsensei GitHub repository using&nbsp;<a href="https://github.com/jupyter/repo2docker">repo2docker</a>.</p><h2><a id="user-content-option-2-local-installation" aria-hidden="true" href="https://github.com/FORCaist/FORCaist.github.io/blob/master/brunlocal.md#option-2-local-installation"><svg viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Option 2: Local Installation</h2><p>Local installation should be straight-forward. This installation procedure has been tested on a number of systems, but we discuss potential installation issues at the bottom of this page.</p><p>Please be aware the local installation will add new packages (or potentially overwrite existing packages) on your system. If you are not comfortable with this, then you should not attempt local installation.</p><p>First, if you don't have Python and/or Jupyter installed, we recommend installing Anaconda from:&nbsp;<a href="https://www.anaconda.com/distribution/" rel="nofollow">https://www.anaconda.com/distribution/</a></p><p>To run FORCsensei locally requires a number of extra packages, which can be installed via&nbsp;<code>pip</code>&nbsp;or&nbsp;<code>sudo</code>. Open a terminal and give the commands:</p><pre><code>pip install appmode
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
</code></pre><p>Once the dependencies are installed you can download the FORCsensei notebook&nbsp;<a href="https://github.com/FORCaist/forcsensei/blob/master/FORCsensei.ipynb">here</a>. Save the FORCsensei notebook into a folder of your choice</p><p>Now,&nbsp;<code>cd</code>&nbsp;into the folder where you placed&nbsp;<code>FORCsensei.ipynb</code>&nbsp;and give the command:</p><pre><code>jupyter trust FORCsensei.ipynb
</code></pre><p>Everything should now be ready. You can start FORCsensei, using the command:</p><pre><code>jupyter notebook FORCsensei.ipynb
</code></pre><p>FORCsensei is designed to be run in&nbsp;<a href="https://github.com/oschuett/appmode">Appmode</a>, which should appear as a button once you open the notebook in Jupyter.</p><p>Click the&nbsp;<code>Appmode</code>&nbsp;button in the banner at the top and FORCsensei should be ready to run (see the video tutorial).</p><h3><a id="user-content-solutions-to-potential-installation-issues" aria-hidden="true" href="https://github.com/FORCaist/FORCaist.github.io/blob/master/brunlocal.md#solutions-to-potential-installation-issues"><svg viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Solutions to potential installation issues</h3><hr size="6"><p>An error appears when I give the command:</p><p><code>pip install git+https://github.com/FORCaist/forcsensei.git</code></p><p>It looks like your system can't install packages from from git repositories. Potential solutions are:</p><ul><li>MAC - give the commands&nbsp;<code>xcode-select --install</code>, then&nbsp;<code>xcode-select --reset</code></li></ul><hr size="6"><p>An error appears when I give the command:</p><p><code>pip install ...</code>&nbsp;for a given package</p><p>This isn't a FORCsensei related error, but rather something to do with the third-party package you are trying to install. Visit the package homepage, or google the error to try to get more information.</p><hr size="6"><p>The&nbsp;<code>FORCsensei.ipynb</code>&nbsp;file is saved onto my system as&nbsp;<code>FORCsensei.ipynb.html</code></p><p>This may occur if you are using Safari, which has a nasty habit of appending&nbsp;<code>.html</code>&nbsp;to certain types of files. The easiest solution is to visit the FORCsensei GitHib repository (<a href="https://github.com/FORCaist/forcsensei">https://github.com/FORCaist/forcsensei</a>). Download the entire repository as a ZIP file using the green&nbsp;<code>Clone or Download</code>&nbsp;button. Contained within the ZIP will be a copy of&nbsp;<code>FORCsensei.ipynb</code>&nbsp;without the random&nbsp;<code>.html</code>&nbsp;extension.</p><br>
