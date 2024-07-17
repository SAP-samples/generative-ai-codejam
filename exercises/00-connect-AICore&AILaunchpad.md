# Setup SAP AI launchpad and SAP AI Core

## [1/10] Open SAP Business Technology Platform
-> link BTP, we added user

## [2/10] Open SAP AI Launchpad and connect to SAP AI Core
In Instances and Subscriptions you will find an SAP AI Core instance. With the extended service plan you will be able to use the generative AI hub. Open the service key.
Assign all the necessary role collections to your user for SAP AI Launchpad.
Open SAP AI Launchpad, in this subaccount the connection is already established. Otherwise you would have had to add a new runtime using the SAP AI Core service key information.
Make sure to create a new resource group for your team.

## [3/10] Create a new Dev Space for CodeJam exercises

Go to your instance of SAP Business Application Studio (further referred to as "BAS").

For this SAP CodeJam exercise create a new Dev Space called `CodeJamHANAML` of a kind **Basic** with an additional extension **Python Tools** in BAS:

|Screen element|Value|
|-|-|
|Dev Space name|`CodeJamHANAML`|
|Kind|**Basic**|
|Additional extension|**Python Tools**|

![Create a Dev Space](img/setup0021.png)

You should see the dev space **STARTING**.

![Dev Space is Starting](img/setup0023.png)

Wait for the dev space to get into the **RUNNING** state and then open that dev space.

![Dev Space is Running](img/setup0026.png)

## [4/10] Clone the exercises from the Git repository

Once your dev space is open in the BAS, use one of the available options to clone this Git repository with exercises using the URL 👇🏼 
```sh
https://github.com/SAP-samples/hana-ml-py-codejam.git
```
☝🏻 into your `project` directory in the BAS Dev Space.

![Clone the repo](img/setup0030.png)

Click **Open** to open a project in the Explorer view.

![Open a project](img/setup0040.png)

## [5/10] Open the Workspace

The cloned repository contains a file `codejam.code-workspace` and therefore you will be asked, if you want to open it. Click **Open Workspace**.

![Automatic notification to open a workspace](img/setup0042.png)

If you missed the previous dialog, then you can go to the BAS Explorer, click on the `codejam.code-workspace` file, and then click on the **Open Workspace**.

![Open a workspace](img/setup0045.png)

You should see:
* **CODEJAM** as the workspace at the root of the hierarchy of the project, and
* **`hana-ml-py-codejam`** as the name of the top level folder.

![Open a workspace](img/setup0047.png)

## [6/10] Check that the required extensions are installed

> SAP provides you with a mechanism to access third-party sites to view and download open-source, 3rd party or its own tools, libraries, or software components ("Extensions") to dev spaces in SAP Business Application Studio. Using this mechanism, you can view and install VS Code Extensions from the [VSX Open Registry](https://open-vsx.org/) at your own risk.

Go to **Extensions** using the activity bar (the left-most bar in the IDE) and type `@builtin Py` in the search bar. 

You should see **Python** and **Jupyter** extensions installed already.

![Extensions to install](img/setup0051.png)

## [7/10] Create a virtual environment with `venv` from a command line

The built-in [venv module](https://docs.python.org/3.9/library/venv.html#module-venv) in Python provides support for creating lightweight “virtual environments”. Each virtual environment has its own Python binary (which matches the version of the binary that was used to create this environment) and can have its own independent set of installed Python packages in its site directories.

Open a built-in terminal in BAS, eg. using the menu option.

![Open a terminal](img/setup0060.png)

Make sure you are in the `/home/user/projects/hana-ml-py-codejam` directory, e.g., using the `pwd` command.

Use `venv` to create a virtual environment for your project in the new directory `~/projects/hana-ml-py-codejam/env` by using the following command:

```shell
python3 -m venv ~/projects/hana-ml-py-codejam/env --upgrade-deps
```

Check that the virtual environment was successfully created:

```shell
ls -l ~/projects/hana-ml-py-codejam/env
```

![Create an venv](img/setup0071.png)

## [8/10] Activate the virtual environment `env` from a command line

Activate the virtual environment using the following command:

```shell
source ~/projects/hana-ml-py-codejam/env/bin/activate
```

You should see you are in a virtual environment as indicated by the `(env)` prefix in a shell's prompt.

![Activate the venv](img/setup0080.png)

## [9/10] Install required Python packages in the virtual environment

Install:

1. the `ipykernel` package to be able to run Python code in a Jupyter extension using the following command:

```shell
python -m pip install --require-virtualenv --no-cache-dir ipykernel
```

![Install ipykernel](img/setup0090.png)

2. the [Python machine learning client for SAP HANA](https://pypi.org/project/hana-ml/) (`hana-ml`) and other required dependencies listed in https://help.sap.com/doc/cd94b08fe2e041c2ba778374572ddba9/2024_1_QRC/en-US/Installation.html#installation-guide using the following command:

```shell
python -m pip install --require-virtualenv --no-cache-dir 'hana-ml==2.21.24062400' ipywidgets 'jinja2>=3.0.0' pydotplus graphviz 'shapely>=1.7.1' 'matplotlib==3.8.*' plotly
```

![Install hana-ml and dependencies](img/setup0100.png)

3. Install Jupyter's own [utilities for programmatic work with notebook documents](https://docs.jupyter.org/en/latest/projects/conversion.html): `nbformat` to be able to run one notebook from another, and `nbconvert` to be able to clean the output of notebooks, eg. before pushing to the Git repository, using the following command:

```shell
python -m pip install --require-virtualenv --no-cache-dir nbformat nbconvert
```

![Install nbformat and nbconvert](img/setup0102.png)

## [10/10] Open the "Check Setup" notebook from the exercises

In your BAS hide the terminal.

![Hide the terminal](img/setup0108.png)

Go to Explorer and open a `exercises/010-check_setup.ipynb` notebook. 

The notebook should open in a Jupyter extension.

Next, select a kernel `env` (the virtual environment you set up earlier) from **Python Environments**.

![Select the kernel](img/setup0111.png)

The kernel should be set in a few seconds. You should get messages about Jupyter server processes started in the background ready to execute code from your notebook.

![Ready to go!](img/setup0120.png)

## 🤓 Now you are ready to use SAP Business Application Studio to go one-by-one through exercises! 

### Engage, learn and enjoy!
