# CI/CD HW for Capstone Fall 2023

## Getting Started

These instructions will set up and run the project on your local machine.

### Prerequisites

- Python (version 3.9 and 3.10 recommended)
- MacOS Ubuntu Windows (latest version)

### Installation

1. Clone the repository:

   git clone https://github.com/Armadillq/397-hw6
   
Install dependencies:

Copy code

pip install -r requirements.txt


Set up pre-commit hooks:

bash


Copy code

pre-commit install
Pre-commit Configuration

We use pre-commit hooks to ensure code consistency and prevent the commit of large files and private keys. The .pre-commit-config.yaml file includes the following hooks:

check-added-large-files: Limits maximum allowed file size to 100KB.
detect-private-key: Detects the presence of private keys.


Code Quality Tools:

We utilize Flake8 for style checking and Black as a code formatter. These tools are integrated into our development workflow through the pyproject.toml file.

The int_sort.py script implements an integer sorting algorithm using bubble, quick, and insertion methods. We use Numpy to adhere to standard Python docstring practices.

GitHub Actions Workflow:

The python-workflow.yaml file defines a GitHub Actions workflow named "Python Package Workflow." This workflow is triggered on every push or pull request to the main branch. The workflow performs the following tasks:


Build and Test Job:

Builds the package for Ubuntu, MacOS, and Windows with Python versions 3.9 and 3.10.
Installs dependencies, lints with Flake8, formats with Black, and tests with pytest.


Deploy Job:

Builds the Python package using setup.py.
Publishes the package to the test PyPI server.


Authors:

Callen Shaeffer,
Caiden Emerson,
Kevin Bretthauer,
Jackson Cyr,
Christian Silva

License
LICENSE.md file for details.

Acknowledgments
https://stackoverflow.com/questions/3898572/what-is-the-standard-python-docstring-format
https://flake8.pycqa.org/en/latest/
https://black.readthedocs.io/en/stable/
https://docs.python.org/3/distributing/index.html
https://test.pypi.org/
