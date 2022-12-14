----

When building your custom model server you can include any Python packages your heart desires. All you have to do is specify these using a `requirements.txt` file.

First, create the file itself.

```(bash)
touch requirements.txt
```{{execute}}

Next, add the Python packages which have been imported in the `RandomForest.py` file to your `requirements.txt`.

```(text)
numpy
pypmml
seldon-core
google-cloud-storage
werkzeug==2.0.3
```

Finally, install any system dependencies that are required.

```(bash)
apt install default-jre
```

You will need to type `Y` when prompted. 


## Creating the Virtual Environment

As per best practices you will use a virtual environment to setup the Python dependencies needed for the local testing of your Dataiku model deployment.

Start by installing the virtual env manager:

```(bash)
apt install python3.8-venv
```

Next create a new `venv` in your current directory: 

```(bash)
python3 -m venv .
```

Finally activate the environment: 
```(bash)
source ./bin/activate
```

## Installing Python Packages

You can now install the necessary Python packages using your recently created `requirements.txt`.

```(python)
pip3 install -r requirements.txt
```

You can ignore any errors that may show here.