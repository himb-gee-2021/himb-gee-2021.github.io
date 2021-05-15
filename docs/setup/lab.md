# Labs

### Method 1: Launch JupyterLab Locally
* This assumes you can launch jupyterlab on your machine and we are using Python 3.
* There are a couple of ways to launch this clone the [master branch](https://github.com/samapriya/education-research)

<center>
    ```
    git clone https://github.com/samapriya/education-research.git
    ```
</center>

* Unzip the folder and launch jupyter lab locally by simply typing

<center>
```
jupyter lab
```
</center>

### Method 2: Launch JupyterLab on BinderHub
* Open this link in a new tab
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/samapriya/education-research/master)
* This allows you to run the analysis remotely and handles dependencies
* Binder run launches a jupyterhub instance but you can easily convert that to jupyterlab by replacing the trailing **/tree** with **/lab**
