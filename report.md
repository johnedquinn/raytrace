# Report
- Author: John Ed Quinn
- Date: 2021 March 01

## POVray Object
- The object used can be found [here](http://lib.povray.org/searchcollection/index.php) by searching for Buckyball.

## Single Machine Estimates
- Executing POVray directly, using the following resolutions, we can determine the amount of time needed to render a single video frame:
	- 320x400: 0.901s
	- 640x480: 1.186s
	- 1280x720: 1.870s
	- 1920x1080: 2.877s
- Below is the estimate (based on the preliminary results above) for how long it would take to render a minute-long video at 10 frames per second for the following resolutions.
	- 320x400: 540.6s
	- 640x480: 711.6s
	- 1280x720: 1122.0s
	- 1920x1080: 7726.2s

## Analysis of Distributed Computation

### General Analysis
- At each run of `condor_povray`, in the order from 320 to 1920, the time between submission and first execution becomes greater and greater. This may have been due to resource limits and additional condor submissions across the condor pool at Notre Dame.

### 320x400 Log Analysis
- Log file can be found [here](movie320.log)
- The corresponding Condor Analyzer page can be found [here](http://condorlog.cse.nd.edu/logs/c7/95/c795f4a2e27377fb94f675fb28f307d1/)
- At the peak of the distributed computation, 120 jobs ran at once.
- For the most part, the computation ran smoothly. There was a steady completion of jobs, with a small number of jobs taking longer than usual (causing the completion to not be perfectly linear) towards the end of the run.
- The total elapsed time was 208s.

### 640x480 Log Analysis
- Log file can be found [here](movie640.log)
- The corresponding Condor Analyzer page can be found [here](http://condorlog.cse.nd.edu/logs/44/ba/44ba1e4c6c756484a41fb5dcbc8cfdc4/)
- At the peak of the distributed computation, 115 jobs ran at once.
- For the most part, the computation ran smoothly. There was a steady completion of jobs, with a small number of jobs taking longer than usual (causing the completion to not be perfectly linear) towards the end of the run.
- The total elapsed time was 229s.

### 1280x720 Log Analysis
- Log file can be found [here](movie1280.log)
- The corresponding Condor Analyzer page can be found [here](http://condorlog.cse.nd.edu/logs/29/59/2959ab3dca9de8d6fda8cfb68e82bcfb/)
- At the peak of the distributed computation, 120 jobs ran at once.
- For the most part, the computation ran smoothly. There was a steady completion of jobs, with a small number of jobs taking longer than usual (causing the completion to not be perfectly linear) towards the end of the run.
- The total elapsed time was 389s.

### 1920x1080 Log Analysis
- Log file can be found [here](movie1920.log)
- The corresponding Condor Analyzer page can be found [here](http://condorlog.cse.nd.edu/logs/38/2d/382df6c3a61cc4025a1750a16c9b293c/)
- At the peak of the distributed computation, 120 jobs ran at once.
- For the most part, the computation ran smoothly. There was a steady completion of jobs, with a small number of jobs taking longer than usual (causing the completion to not be perfectly linear) towards the end of the run.
- The total elapsed time was 384s.
