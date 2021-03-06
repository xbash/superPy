![](https://web.superquery.io/wp-content/uploads/2019/03/sq-logotype@1x.svg)

# Python API for superQuery

Python package for using superQuery.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

* Python >= 3.1

### Installing

```
pip3 install superQuery
pip3 install jupyter
```

## Get your authentication details
* Go to superquery.io and log in/sign up
* In the left side-bar, scroll down and click on "Integrations"
* Scroll down until you see "Python" and click "Connect"
* Note the username and password

## Running `examples/start.ipynb` in Google Colab
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/superquery/superPy/blob/master/examples/start.ipynb)
* Update the credentials in the notebook by following the steps above under "Get your authentication details"
* Run it!

## Running `examples/start.ipynb` in Jupyter notebook
* Launch Jupyter locally with `jupyter notebook`
* Download `examples/start.ipynb` to your local machine and open it from Jupyter
* Update the credentials in the notebook by following the steps above under "Get your authentication details"
* Run it!


## Running `examples/start.py`
* Inside [`start.py`](https://github.com/superquery/superPy/blob/master/examples/start.py) exchange `xxxxxxx` with the username/password combination you got from superquery.io
* Update the SELECT statement to reflect a query you are interested in. Be careful to start with a low-cost query


```
mydata = sq.get_data(
    "SELECT field FROM `projectId.datasetId.tableID` WHERE _PARTITIONTIME = \"20xx-xx-xx\"", 
    get_stats=True, 
    dry_run=dryrun, 
    username="xxxxxxxxx", 
    password="xxxxxxxxx")
```
* Now run
```
python3 examples/start_here.py
```



## Tested With

* [Python3.7.3](https://www.python.org/downloads/release/python-373/) - Python version
* [Twine1.13.0](https://pypi.org/project/twine/) - Package publishing

## Authors

* **Eben du Toit** - *Initial work* - [ebendutoit](https://github.com/ebendutoit)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* The awesome people at superQuery
