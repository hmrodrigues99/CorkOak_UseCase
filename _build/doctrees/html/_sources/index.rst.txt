.. CorkOak_UseCase documentation master file, created by
   sphinx-quickstart on Thu Feb  2 16:41:08 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Plant Data Visualization/Orthology Bundle -  Cork Oak Use Case
==============================================================

.. note::

   This project is under active development.

Extensive phenotypic measurements and high-throughput RNA-seq experiments often make plant data fall in the scope of big data. The current plant data visualization/orthology bundle provides a set of interopable tools ranging from data annotation, analysis and visualisation to ease treatment and interpretation of plant data.

The present use-case aims to provide the user with the necessary knowledge to properly use and navigate this tool bundle. The use of data obtained from studies in Cork Oak, a non-model woody plant, highlights possible shortcomings which the user may also face regarding the lack of a full reference genome and absent/incomplete data annotations.

.. _download-data-label:

Download Cork Oak Data
----------------------

The first step to follow the present use-case is to download data obtained from cork oak studies. It can be manually downloaded from `github <https://github.com/hmrodrigues99/CorkOak_UseCase_Data>`_ (``https://github.com/hmrodrigues99``), or by running the following in the command line:

**Linux users:**

.. code-block:: Bash

   # 1. Open the bash shell (command line)

   # 2. Create and move to a new directory named corkoak_usecase
   # This folder will be used to store our data. It's full path can be seen by running $PWD.
   mkdir corkoak_usecase
   cd corkoak_usecase

   # 3. Download all necessary data, including the cork oak data files from github
   wget https://github.com/hmrodrigues99/CorkOak_UseCase_Data/archive/main.zip

   # 4. Unzip the downloaded folder and move into it's directory
   unzip ./CorkOak_UseCase_Data-main.zip
   cd CorkOak_UseCase_Data-main

   # 4.1 If unzip fails, install it using ``sudo apt install unzip`` and try again
   unzip ./CorkOak_UseCase_Data-main.zip
   cd CorkOak_UseCase_Data-main

   # 4.2 If for some reason the error persists, search the folder on your system (outside the bash shell) and unzip the file manually.
   # Then, go back into the bash shell and move into the folder directory
   cd CorkOak_UseCase_Data-main

**Windows R Users:**

.. code-block:: R

   #Create and move to a new directory named corkoak_usecase
   dir.create("corkoak_usecase")
   setwd("corkoak_usecase")

   #Installing R.utils package, if not already installed
   if (!require("utils")) install.packages("utils")
   library("utils")

   #Download the cork oak data folder from github
   download.file(https://github.com/hmrodrigues99/CorkOak_UseCase_Data/archive/main.zip)

   #Unzip the downloaded file and move into it's directory
   unzip(CorkOak_UseCase_Data-main.zip)
   setwd("CorkOak_UseCase_Data-main")

**Windows Python (3.7+) Users:**

.. code-block:: python

   #Within the Command line, install the requests package
   pip install requests

   #Now in a Python IDE, download the cork oak data folder [replace "PathToFile" with a target directory (e.g. "C://Users//hrodrigues//Data//")]
   import requests
   file = requests.get("https://github.com/hmrodrigues99/CorkOak_UseCase_Data/archive/main.zip")
   open('PathToFile//CorkOak_UseCase_Data-main.zip', 'wb').write(file.content)

Cork Oak Data Contents:
-----------------------

``corkoak_proteins.faa``
   A FASTA file containing aminoacid sequences of cork oak proteins.

``corkoak_edge``
  | Table (.csv) with cork oak co-expressed gene predictions.
  | The first two collumns hold the interacting genes, and the third column the type of interaction (e.g. co_expressed).
  | These predictions were obtained from cork oak RNA-seq datasets using the `Seidr toolkit <https://seidr.readthedocs.io/en/latest/>`_ and filtered for genes putatively involved in lignin biosynthesis dependent on seasonal cues (identified in `DOI: https://doi.org/10.1038/s41598-021-90938-5 <https://doi.org/10.1038/s41598-021-90938-5>`_).

``corkoak_node``
   List (.csv) of cork oak protein IDs present in the interactions described above.

``corkoak_LogFC_April``, ``corkoak_LogFC_June``, ``corkoak_LogFC_July`` and ``corkoak_LogFC_July_April``
   Files containing cork oak experimental data (log2FC values obtained from gene differential expression analysis in cork oak tissue samples collected in the months of April, June and July)

``Cytoscape_to_DiNAR.R``
   R script used to process a Cytoscape network ready to be imported into DiNAR.

``Ensembl_Plants_Query.R``
   R script used to perform predefined queries (retrieval of gene descriptions, annotations and orthologs) from the Ensembl Plants database.

Task Workflow:
--------------

After data download, we are ready to start performing the proposed tasks, starting with :ref:`task1-label`.

.. toctree::
   :maxdepth: 2
   :caption: Tasks
   :titlesonly:

   source/task1
   source/task2
   source/task3
   source/task4

.. toctree::
   :maxdepth: 2
   :caption: Tools
   :titlesonly:

   source/tool1_mercator
   source/tool2_mapman
   source/tool3_dinar

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