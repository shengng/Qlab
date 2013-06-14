Qlab measurement and control software
=====================================

A MATLAB framework for superconducting qubit systems.

Installation
------------
To get started, simply download and unzip the latest release. Or, if you want the tip of the development repository, clone a local copy with

	git clone git@github.com:BBN-Q/Qlab.git localname

Navigate to the Qlab folder and run `installQlab` to setup the necessary preferences. The install script will also recommend a list of folder to add to the MATLAB path.

The code is loosely organized into

* `analysis/` - routines for data analysis
* `experiment/` - experiment control and measurement
* `common/` - instrument drivers, ExpManager, measurement filters, sweeps, and pulse calibration
* `common/util` - general utilities, including PatternGen for pulse sequence generation.
* `hardware/` - firmware and low-level drivers for custom BBN hardware

The main workhorse is the `ExpManager` class which provides a general framework for taking, processing, and saving data. The [ExpScripter example][scripter] shows an example workflow for using `ExpManager` with a set of instruments, sweeps, and measurements. This example makes use of configuration data stored in [JSON][] files. The [PyQLab][] project contains a GUI for creating these files.

See the [wiki][] for release notes and further help.

All source is distributed under the Apache open source [license][].

[wiki]: http://github.com/BBN-Q/Qlab/wiki
[Pulse-Generation]: http://github.com/BBN-Q/Qlab/wiki/Pulse-Sequence-Generation
[scripter]: http://github.com/BBN-Q/Qlab/blob/develop/experiments/muWaveDetection/ExpScripter.example.m
[JSON]: http://en.wikipedia.org/wiki/JSON
[PyQLab]: http://github.com/BBN-Q/PyQLab
[license]: http://github.com/BBN-Q/Qlab/blob/master/LICENSE