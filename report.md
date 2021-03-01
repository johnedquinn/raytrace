# Report
- Author: John Ed Quinn
- Date: 2021 March 01

## POVray Object
- The object used can be found [here](http://lib.povray.org/searchcollection/index.php) and searching for Buckyball.

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
- 
