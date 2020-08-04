# A Quick Intro to To Test Coverage in Python
For full information, please reffer to https://medium.com/@khalid.nwb/a-quick-intro-to-to-test-coverage-in-python-9bf299711c6c
## Quick Guide:
### Installation:
$pip install coverage

If you are using anaconda distribution, you can use:
$conda install coverage

You can verify your Coverage installation by checking the version:
$coverage –version

## Using Coverage
### Pytest
$coverage run -m pytest arg1 arg2 arg3

### Unittest
$coverage -m unittest test_code

## Generating report
$coverage report

## Generating HTML report
$coverage html

## Excluding code from coverage
Add a comment after the line "# pragma: no cover"
