.. CorkOak_UseCase documentation master file, created by
   sphinx-quickstart on Thu Feb  2 16:41:08 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Plant Data Visualization Tool Bundle -  Cork Oak Use Case
==========================================================

.. note::

   This project is under active development.

Extensive phenotypic measurements and high-throughput RNA-seq experiments often make plant data fall in the scope of big data. The current plant data visualization tool bundle provides a set of interopable tools ranging from data annotation, analysis and visualisation to ease treatment and interpretation of plant data.

The present use-case aims to provide the user with the necessary knowledge to properly use and navigate this tool bundle. The use of data obtained from studies in Cork Oak, a non-model woody plant, highlights possible shortcomings which the user may also face regarding the lack of a full reference genome and absent/incomplete data annotations.

.. _download-data-label:

Download Cork Oak Data
----------------------

The first step to follow the present use-case is to download data which was obtained from cork oak studies. It can be mannualy downloaded from this ``github repository https://github.com/hmrodrigues99``, or by running the following from the command line:

**Linux users (bash):**

.. code-block:: Bash

   #Create and move to a new directory named corkoak_data
   mkdir corkoak_data
   cd corkoak_data
   #Download cork oak data from the hmrodrigues99 github repository
   wget https://githublinkwith_corkoak_data.zip
   #Unzip the downloaded file
   unzip corkoak_data.zip

**Windows users (R):**

.. code-block:: R

   #Installing R.utils package, if not already installed
   if (!require("utils")) install.packages("utils")
   suppressMessages(library("utils"))
   #Download cork oak data from the hmrodrigues99 github repository
   download.file(https://githublinkwith_corkoak_data.zip)
   #Unzip the downloaded file
   unzip(corkoak_data.zip)

Task Workflow:
--------------

After data download, it's all set to start performing the proposed tasks, starting with :ref:`task1-label`.

.. toctree::
   :maxdepth: 2
   :caption: Tasks
   :titlesonly:

   source/task1
   source/task2
   source/task3

.. toctree::
   :maxdepth: 2
   :caption: Tools
   :titlesonly:

   source/tool1_mercator
   source/tool2_mapman

.. toctree::
   :maxdepth: 2
   :caption: References
   :titlesonly:

   source/references

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`