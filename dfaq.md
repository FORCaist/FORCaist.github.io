---
layout: page
title: FORCsensei FAQ
image: assets/images/excel2.jpg
nav-menu: True
---


<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>FORCsensei FAQ</h1>
		</header>

<!-- Content -->
<p>&nbsp;</p>
<p><h3>Why won't FORCsensei won't read my data file?</h3></p>
<p>FORCsensei has been written to read most Princeton Instrument and Lake Shore Cryotronics text file formats. If you have a file format that FORCsensei seems to be struggling with, then send us an example and we'll (try to) update FORCsensei's file reading routines.</p>
<hr />
<a id="progress1"></a>
<p><h3><a id="progress">Is there a progress bar to monitor the model comparison process?</a></h3></p>
<p>The model comparison can take some time. The good news is that if you are running FORCsensei locally you can monitor the process. Simply click on the address below:</p>
<p><a class="reference external" href="http://localhost:8787/status" target="_blank">http://localhost:8787/status</a></p>
<p>This will open a new brower tab and take you to a Dask dashboard, which will show you the progress of the computation, including the number of tasks completed, memory/CPU usage, etc.&nbsp;</p>
<p>Unfortunatly, third-party cloud services don't provide such diagnostic information to their users, so we can't offer the same Dask dashboard for the cloud version of FORCsensei.</p>
<hr />
<p><h3><a id="AssumeS">What does the Assume Sc<sub>0</sub> = Sb<sub>0</sub> option do?</a></h3></p>
<p>If enabled, this option means you will only search for VARIFORC models where the minimum horizontal and vertical smoothing factors are the same. Experience has shown that setting&nbsp;Sc<sub>0</sub> = Sb<sub>0</sub> can reduce artifacts in the final FORC plot and it has the added advantage of dramatically reducing the number of models that need to be compared.</p>
<hr />
<p><h3><a id="dask_workers">How many Dask workers should I use?</a></h3></p>
<p>Dask workers are the key to parallel processing in FORCsensei. Each worker can handle a seperate computation task, so the more workers you use, the faster FORCsensei should run. However, each worker uses memory and CPU power. If you choose too few workers, the calculation will be slow but given enough time will finish. If you try to use too many workers, FORCsensei will error due to insufficent memory/CPU resourses. In such cases you'll need to restart FORCsensei from scratch and try again with fewer workers.</p>
<p>So, how many workers should you use? This depends on your system. For a typical laptop between 4 and 8 workers should be okay. If you are working on a cloud service with limited resources, then choose 4 or less. If you have FORCsensei running on a high-end computer or HPC, then you can try more (up to a maximum of 20).</p>
<hr />
<p><h3>I've used FORCsensei in my work and I'd like to cite it.</h3></p>
<p>We plan to publish a manuscript about the FORCsensei algorithm. We'll provide citation details once they are available.</p>
hr{ background-color: white; height: 7px; border: 0; }
<p><h3>I've got a question, found a bug, or have a suggestion for FORCsensei</h3></p>
<p>We're all ears. Feel free to send it to us.</p>

