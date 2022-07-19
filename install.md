# Installation Required for Dev Environment

## Repos
`git clone` the following repos from [Skynet Git Bucket](https://code.skynet.unc.edu/projects/SKYNET):
*   skynet-dashboard
*   skynet-dashboard-api
*   skynet-api
*   skynet-python
*   skynet-scripts

## Python Virtual Environment
### Install the correct python version
If your current python version is not 3.8, the install 3.8 from [python.org](https://www.python.org/downloads/release/python-3810/) or your prefered package manager.

For Mac
```sh
brew install python3.8
```
### Create a virtual environment
Create _a_ python virtual environment for all the repos you just installed.
```sh
python3.8 -m venv venv
source .venv/bin/activate # Mac or Linux
.\venv/Scripts/activate # Windows
```

### Install packages
To install packages, install pipenv first.
```sh
pip install pipenv
```
Then `cd` into theses the repos:
*   skynet-dashboard-api
*   skynet-api
*   skynet-python
*   skynet-scripts

And run
```sh
pipenv install
```
