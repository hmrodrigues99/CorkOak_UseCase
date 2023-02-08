.. _task3-label:

Task 3 - Cytoscape into DiNaR Network Visualization
===================================================

DiNaR is a tool used to obtain a dynamic representation of a biological data network over multiple timepoints or different conditions.

Obtaining a dynamic network representation from a cork oak co-expression network
--------------------------------------------------------------------------------

1. Run the ``Cytoscape_DiNaR.R`` from the command line

   .. code-block:: R

      #Inside the directory of the downloaded cork oak data (should also contain ``Cytoscape_DiNaR.R`` )
      Rscript ./Cytoscape_DiNaR_link.R -n ./corkoak_node.csv -e ./corkoak_edge.csv -a ./corkoak_mercator.results -o corkoak_ready_to_process

This will process a Cytoscape network to firstly import into `DiNaR preprocessing subApp <https://nib-si.shinyapps.io/pre-processing/>`_ and then in `DiNaR App <https://nib-si.shinyapps.io/DiNAR/>`_. If the user wishes to load a network (node and edge tables) into DiNaR with different origin than Cytoscape, the input files should have the structure specified `here <https://nib-si.shinyapps.io/pre-processing/>`_.

2. Open the `DiNaR preprocessing subApp <https://nib-si.shinyapps.io/pre-processing/>`_ and select the **tables** option tab (at the top)
3. With the Tab default Separator, click **Choose Nodes File** and select ``node_corkoak_ready_to_process.txt``
4. Click **Choose Edges File** and select ``edge_corkoak_ready_to_process.txt``
5. Fill the **Type in desired network name:** with ``corkoak_processed``
6. Click download (at the bottom) **BOTH** in the Nodes tab, and in the Edges tab (both next to Plot), to ensure both the node and edge tables are downloaded

Video guide for `DiNaR preprocessing subApp <https://nib-si.shinyapps.io/pre-processing/>`_:

   .. raw:: html
 
      <iframe width="560" height="315" src="https://www.youtube.com/embed/TzcFTVTjDts" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

7. Go to the `DiNaR App <https://nib-si.shinyapps.io/DiNAR/>`_
8. In **select network**, choose **Custom network**
9. In **Upload nodes table**, select the ``processed_node`` file
10. In **Upload edges table**, select the ``processed_edge`` file
11. Download the animation with - get final .html output

Video guide for `DiNaR App <https://nib-si.shinyapps.io/DiNAR/>`_:

   .. raw:: html
 
      <iframe width="560" height="315" src="https://www.youtube.com/embed/TzcFTVTjDts" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Congratulations, this task concludes the present use-case.
Further questions or recomendations can be submitted to: `<hugo.miguelr99@gmail.com>`_.

