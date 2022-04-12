## Exploring and plotting customer data pulled from MongoDB

### Installation

Git clone this repository:

```
git clone https://github.com/KyleOS/useractivity.git
```

Download and install the [Anaconda Python distribution](https://www.anaconda.com/distribution/).
Then activate a conda virtual environment with

```
conda env create -f environment.yml
conda activate dev

```

### Usage

Make sure to define your Mongo connection url with

```
export MONGO_CONNECTION_URL="YOUR_CONNECTION_STRING"
```

Start programming! Open jupyter with

```
jupyter lab
```

And start working.


### Installing extra libraries

Install any libraries you need with

```
conda install <library>
```

Make sure to run the following command to save the installed libraries into the environment.yml file, this allows others to run the report easily.

```
conda env export --no-builds > environment.yml
conda activate dev
python -m pip install plotly
jupyter labextension uninstall @jupyterlab/plotly-extension
jupyter labextension install jupyterlab-plotly
python -m pip install cufflinks
python -m pip install psutil
python -m pip install statsmodels 
```

### MongoDB Connection

You have to make sure that you have MongoDB installed on your machine. If not, install it in command line with:
```
brew install mongodb-community
brew services start mongodb-community
python -m pip install pymongo
```

Look at your MongoDB connection URI. If your connection begins with "mongodb+srv:" you need to make sure to install dnspython with: 

```
python -m pip install dnspython
```

If you use MongoDB Atlas, you can find some steps to find your URI at https://docs.atlas.mongodb.com/driver-connection/.