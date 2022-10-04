<img src="https://api.travis-ci.org/ModelEngineering/kinetics_validator.svg?branch=master" width="100"/>

[![Coverage](https://codecov.io/gh/ModelEngineering/kinetics_validator/branch/master/graph/badge.svg)](https://codecov.io/gh/ModelEngineering/kinetics_validator)

# SBMLKinetics

SBMLKinetics is a Python package to evaluate and classify kinetics in SBML models. 
There are many possible kinetics like zeroth order, mass action, Michaelis-Menten, 
Hill kinetics and others. This work characterizes the kinetics in the BioModels 
Database as an example to improve modeling best practices. Our tool can analyze any data sets 
with SBML files as input. Users can also use this tool to compare different data sets. For 
instance, we compare the distribution of kinetics for signaling and metabolic networks and 
find the substantial differences between two types of networks. If you are using any of the 
code, please cite the PYPI web page (https://pypi.org/project/SBMLKinetics/).

## For users
### Installation

``pip install SBMLKinetics``

## A Classification Example

Here is a classification example generated by SBMLKinetics:

<img src="https://raw.githubusercontent.com/ModelEngineering/kinetics_validator/master/docs/Figures/Fig1_curated.png" width="350" height="450">

Please see more examples in the documentation.

### Documentation
Please see the documentation at https://modelengineering.github.io/kinetics_validator/ for details.


## For developers
### Setup environment
- Install [spyder3](http://www.psych.mcgill.ca/labs/mogillab/anaconda2/lib/python2.7/site-packages/spyder/doc/installation.html)
- Clone the ``kinetics_validator`` repository using ``git clone https://github.com/ModelEngineering/kinetics_validator``
- Create a virtual environment for the project.
  - ``cd kinetics_validator``
  - ``python -m venv kv``
  - ``source kv/Scripts/activate``
(Use "\\" in windows.)
  - ``pip install -r requirements.txt``
  - ``deactivate``

To verify the setup:
- Return to the ``kinetics_evaluator`` directory.
- ``source kv/Scripts/activate``
(Use "\\" in windows.)
- ``export PYTHONPATH=`pwd` ``
- ``python tests/test_simple_sbml.py``. The
tests should run without error.
(Use "\\" in windows.)

### Running Codes
- ``cd kinetics_validator``
- ``source kv/bin/activate``
(Use "\\" in windows.)
When you're done, use ``deactivate``.

### Documentation
- ``examples/tutorial.py`` has code illustrating usage
- ``SBMLKinetics/common/*.py`` has codes for the 
SmpleSBML (``simple_sbml.py``),
Reaction (``reaction.py``),
and KineticLaw (``kinetic_law.py``).
