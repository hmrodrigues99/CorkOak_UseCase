.. _task1-label:

Task 1 - Plant Data Annotation
==============================

To make sense of biological data, we often annotate it with terms that help group and organize it.
Annotated data can be further analysed to gather new insights, such as identifying and/or understanding biological processes of interest.

The `Mercator4 Webtool <https://plabipd.de/portal/mercator4>`_ uses the **MapMan ontology**, a curated vocabulary tailored to annotate plant data. It differs from the more generic Gene Ontology as it describes terms with higher depth and specificity to plant species. A extensive comparison between them is acessible `here <https://www.frontiersin.org/articles/10.3389/fgene.2012.00115/full>`_.

This first task should be performed at the starting point of usage of this tool bundle, as further tasks require **MapMan** annotated data for a more in-depth analysis. If you haven´t already, please download the cork oak data required to follow this use-case in :ref:`download-data-label`. 

Annotating biological data using the MapMan Ontology
----------------------------------------------------

1. Open the `Mercator4 Webtool <https://plabipd.de/portal/mercator4>`_.
2. Select **Sequence Type** → **Protein** (*default*).
3. In **Upload FASTA file**, click **Choose File** and select the ``corkoak_proteins.faa`` file.

.. figure:: images/corkoak_proteins_mercator_input.png
   :scale: 25 %

   ``corkoak_proteins.faa`` - example of Mercator4 compatible Input (*FASTA File*)

4. Fill **Job name** with ``corkoak``.
5. Click **Submit Job**.
6. Upon job conclusion, click the blue links **MapMan mapping file** and **Mercator4 annotated FASTA file** to download the respective files.
7. Move the downloaded files into the ``corkoakdata`` folder.
8. Extract both .zip files.

Mercator4 Outputs
^^^^^^^^^^^^^^^^^

* | **Output 1**
  | In the example provided, Mercator4 annotated 45 (A) of the 69 submitted sequences (S), occupying 42 different bins (O).
  | The image shown highlights that most of our sequences are linked with polyamine metabolism, cell wall organization and enzyme classification.

.. figure:: images/corkoak_mercator_bins.PNG
   :scale: 80 %

   ``corkoak_mercator_bins.PNG`` - Mercator4 % of Occupied Bins

This is helpful as it provides a first look on which biological processes our query proteins are mostly putatively involved.

* | **Output 2**
  | The **Mercator4 annotated FASTA file** is equal to the input file with the addition of the retrieved annotations in the respective gene/protein headers.
  | In our case, the first entry (protein ID="CFP56_79658") is annotated as a nucleotide sugar transporter \*(URGT/UXT).

.. figure:: images/corkoak_proteins_mercator_output1.png
   :scale: 25 %

   ``corkoak.fa`` - Example of Mercator4 Annotated *FASTA File*

If the input file already had associated descriptions, these are kept in the new fasta (original description field).

* | **Output 3** 
  | Finally, the **MapMan mapping file** follows a tabular structure compatible with other tools which use the MapMan Ontology.

.. figure:: images/corkoak_proteins_mercator_output2.png
   :scale: 25 %

   ``corkoak.results`` - Example of Mercator4 Mapping Results (*Text Document*)

   * ``BINCODE`` - MapMan Ontology term/bin codes. Holds a bin number (for a generic bin) or bin numbers (for a bin cascade, starting left with the most generic term and going through to the most specific, separated by ".").
   * ``NAME`` - Name(s) of the bin(s).
   * ``IDENTIFIER`` - If a gene/protein ID is annotated in a bin, it's ID is shown here, otherwise this field is left empty. Multiple IDs annotated in the same bin appear in separate lines.
   * ``DESCRIPTION`` - A brief description of the gene/protein ID annotated in this bin.
   * ``TYPE`` - Annotation source.

**Video Guide:**

.. raw:: html

   <iframe width="560" height="315" src="https://www.youtube.com/embed/zG-bqquA1mQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

|

With our cork oak data now properly annotated, we are ready to move into further tasks in the use-case, such as :ref:`task2-label`.