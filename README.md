# POVRAY CONDOR
- Author: John Ed Quinn (git: johnedquinn) (ndid: jquinn13)

## Description
- This tool, `povray_condor`, renders a long movie quickly by submitting each frame to be rendered as a separate Condor job.

## Project Structure
- The project creates a workspace in the project's working directory.
- The main program submits a generated .submit file to condor specifying the multiple renders needed to be completed.
- Output files returned by the executing machine are stored within the workspace.
- The program then renders the .png files into an output file (.mpg).
- Note: to preserve the workspace, modify the global `PRESERVE_WORKSPACE` in `povray_condor`.

## POVray
- The file `atom.pov` was taken from the [POVray Collection](http://lib.povray.org/searchcollection/index.php). The specific item is Buckyball.

## To Run
- For help:
```console
foo@bar $ ./povray_condor
```
- Usage:
```console
foo@bar $ ./povray_condor IN_FILE OUT_FILE NFRAMES XSIZE YSIZE
```
