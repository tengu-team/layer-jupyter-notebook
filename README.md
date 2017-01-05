# Overview

This Charm deploys the [Jupyter notebook](http://jupyter.org) including the python3 kernel.The notebook is protected using an automatically-generated [easy to remember password](https://xkcd.com/936/).

The Jupyter Notebook is a web application that allows you to create and share documents that contain live code, equations, visualizations and explanatory text. Uses include: data cleaning and transformation, numerical simulation, statistical modeling, machine learning and much more.

# Usage

Deploy the notebook.

```bash
juju deploy cs:~tengu-team/jupyter-notebook-spark
```

After deployment is complete, you can see the password in the status message. Run `juju status` or look at the details of the notebook unit to get the password.

```
$juju status
Unit                 Workload  Agent  Machine   Public address  Ports     Message
jupyter-notebook/0   active    idle   0         192.168.0.1     8888/tcp  Ready (Pass: "shmuck technical eschew Aqaba")
```

Open https://<public-address>:<open-port> in your browser, login using the password and you're ready to go!.

# Config options

The `pip3-dependencies` config option lets you install additional python3-pip dependencies. Use this if you want to install additional kernels.


# Contact Information

## Authors

This software was created in the [IDLab research group](https://www.ugent.be/ea/idlab) of [Ghent University](https://www.ugent.be) in Belgium. This software is used in [Tengu](http://tengu.intec.ugent.be), a project that aims to make experimenting with data frameworks and tools as easy as possible.

 - Sebastien Pattyn <sebastien.pattyn@qrama.io>
 - Merlijn Sebrechts <merlijn.sebrechts@gmail.com>
