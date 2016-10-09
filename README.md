## dombench
A benchmark suite for measuring framework rendering performance.

### Metrics
dombench uses [browser-perf](https://github.com/axemclion/browser-perf) to gather the following [metrics](https://github.com/axemclion/browser-perf/wiki/Metrics).

### Running the benchmarks
You will need Python and Chrome Driver to run this suite. The benchmark suite uses a simple python web server to host the application, 
and launches an instance of Chrome Driver to run the test in Chrome/Chromium.
```
$ brew install python
$ npm install -g chromedriver
$ npm install
```
To run the suite of tests, run the [run-benchmarks.js](run-benchmarks.js) script:
```
$ node run-benchmarks.js
```
You should now see some instances of Chrome start running the suite of tests listed in the `dirs` object [run-benchmarks.js](run-benchmarks.js) :
```
var dirs = {
	react: 'react',
	react_keys: 'react_keys',
	...
```
Note: You can add/remove items here to add new tests or run items individually.

### Analyzing Results
This suite also includes a handy script for creating a csv from the performance metrics gathered in [data.json](data.json). 
It will automatically run when the suite completes all tests, but can run it manually with:
```
$ node make-csv.js
```
Results are written to `results.csv`. 

### Samples
Some sample metrics collected from running the suite on a 2015 Mac Book Pro, 2.5 Ghz Core i7 can be found in [graphs](/graphs) and [results-graphs.numbers](results-graphs.numbers).

