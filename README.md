## Install stuff
```text
$ pip3 install coverage
$ pip3 install -U pytest
```

## Get Test Coverage output
See https://stackoverflow.com/a/70556981/3412545
1. Run the following:
```text
$ file="test_tutorial.py" && coverage run $file && coverage report -m $file && coverage xml $file

Name               Stmts   Miss  Cover   Missing
------------------------------------------------
test_tutorial.py      17     10    41%   10-15, 18-23
------------------------------------------------
TOTAL                 17     10    41%
Wrote XML report to coverage.xml
```
2. Set `-Dsonar.python.coverage.reportPaths=coverage.xml`

## Get Test Execution output
1. Run `pytest --junitxml=py-results1.xml`
1. Set `-Dsonar.python.xunit.reportPath=py-results1.xml`


-------
-------

### A Quick Intro to To Test Coverage in Python
For full information, please reffer to https://medium.com/@khalid.nwb/a-quick-intro-to-to-test-coverage-in-python-9bf299711c6c
#### Quick Guide:
##### Installation:
```text
$ pip install coverage
```
If you are using anaconda distribution, you can use:
```text
$ conda install coverage
```

You can verify your Coverage installation by checking the version:
```text
$ coverage –version
```

##### Using Coverage
###### Pytest
```text
$ coverage run -m pytest arg1 arg2 arg3
```

###### Unittest
```text
$ coverage -m unittest test_code
```

##### Generating report
```text
$ coverage report
```

##### Generating HTML report
```text
$ coverage html
```
##### Excluding code from coverage
Add a comment after the line "# pragma: no cover"
