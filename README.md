
Implementation Scope
====================

The goal of this project is outline how to implement event monitoring 
for a kubernetes cluster that hosts a financial application.

This document lists how the repository will be created a manifest of sorts.

Installing the Scripts
=======================

Each of these tools is a Python script, designed to be run by themselves or part of other platforms.
Written in python3, all scripts are listed below, and there is a Pipfile to show what modules are required to run.

You will need to use Python 3.6 or higher and the modules listed in the dependency section.  

Installing Source Code and This Repository
==========================================

Please follow the following steps to install:

    1. Download and install git for your platform if you don't already have it installed.
       It can be downloaded from https://git-scm.com/downloads
    
    2. Clone this repository. This will create a new folder. If you do not have git, you can 
       download the repository as a zip file, where you can copy and extract the files into a new folder.
              
    3. Change into the new folder. Type the following to install all the package dependencies 
       (this may take a while as this will download all of the libraries required)
        
Installing Python and Dependencies on Windows
=============================================

Please follow the following steps to install:

    1. Recommended: Please install Chocolatey for Windows by following these [instructions](https://chocolatey.org/install)

    2. Once done, please install Python 3.6 or better. 

       prompt> choco install python311
    
    3. Now install other dependencies for the toolkit. Currently, this is ffmpeg.

       prompt> choco install ffmpeg

       prompt> choco install ffmpeg-full
    
    4. Execute the following command in Powershell to install pipenv, which will manage all of the library dependencies:
    
        prompt> python3 -m pip install pipenv
 
    5. Clone this repository. This will create a new folder

    6. Change into the new folder. Type the following to install all the package dependencies 

        prompt> python3 -m pipenv install

Installing Python and Dependencies on MacIntosh or Unix
=======================================================

Please follow the following steps to install:

    1. Download and install Python 3.6 or higher from python.org. Append python3 to the LIB and PATH env.

    2. Download and install git for your platform if you don't already have it installed.
       It can be downloaded from https://git-scm.com/downloads
    
    3. Open a new shell/command prompt. It must be new since only a new shell will include the new Python 
       path that was created in step 1. Cd to the folder where you want to install the scripts.
    
    4. Execute the following command to install pipenv, which will manage all of the library dependencies:
    
        sudo -H pip3 install pipenv 
 
    5. Clone this repository. This will create a new folder

    6. Change into the new folder. Type the following to install all the package dependencies 
       (this may take a while as this will download all of the libraries required):

        pipenv install
        
Dependencies
============

See the contents of the "pipfile"

Manifest of Items
=================

This is an example of the output of tree for the components. 

```
crypto-web3-app/
├── README.md
├── LICENSE
├── docs/
│   ├── introduction.md
│   ├── architecture.md
│   ├── microservices/
│   │   ├── authentication.md
│   │   ├── risklimit.md
│   │   ├── getprice.md
│   │   ├── sellitem.md
│   │   ├── buyitem.md
│   │   ├── blockchain.md
│   └── kubernetes_deployment.md
├── examples/
│   ├── kubernetes/
│   │   ├── deployment.yaml
│   │   ├── service.yaml
│   │   ├── ingress.yaml
│   ├── web3_integration/
│       ├── README.md
│       ├── buy_item_example.js
│       ├── sell_item_example.js
├── images/
│   ├── architecture_diagram.png
├── scripts/
│   ├── clientorder-simulate_trade.py
│   ├── test_event_collection.py
│   ├── test_event_processing.py
│   ├── clientorder-risk_check.py
│   ├── generate_portfolio_report.py
│   ├── generate_event_report.py
│   ├── generate_activity_report.py
├── kubernetes/
│   ├── authentication/
│   │   ├── deployment.yaml
│   │   ├── service.yaml
│   ├── risklimit/
│       ├── deployment.yaml
│       ├── service.yaml
│   ├── blockchain/
│       ├── deployment.yaml
│       ├── service.yaml
├── infrastructure/
│   ├── logstash/
│   │   ├── logstash-dockerfile
│   ├── kafka/
│   │   ├── kafka-dockerfile
│   ├── elasticsearch/
│   │   ├── elasticsearch-dockerfile
│   ├── kibana/
│   │   ├── kibana-dockerfile
│   ├── prometheus/
│   │   ├── prometheus-installation.yaml
│   ├── fluentd/
│   │   ├── fluentd-installation.yaml
├── data/
│   ├── cryptocurrencies.json
│   ├── sample_orders.csv
├── CONTRIBUTING.md
└── .gitignore
```
To-Do List:
===========

* Expand the components to deal with docker files

* Expand the components to use a terraform provider

* Expand the to use Jinja to create templates for the configs

License
=======

Copyright 2024 Wayne Kirk Schmidt
https://www.linkedin.com/in/waynekirkschmidt

Licensed under the Apache 2.0 License (the "License");

You may not use this file except in compliance with the License.
You may obtain a copy of the License at

    license-name   APACHE 2.0
    license-URL    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Support
=======

Feel free to e-mail me with issues to: 

*   wayne.kirk.schmidt@gmail.com

I will provide "best effort" fixes and extend the scripts.
