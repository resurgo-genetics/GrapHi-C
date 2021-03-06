# GrapHi-C
GrapHi-C: graph-based visualization of Hi-C data

If you use this method, please cite: Kimberly MacKay, Anthony Kusalik and Christopher H. Eskiw. GrapHi-C: graph-based visualization of Hi-C datasets. BMC Research Notes. (2018) 11:418. DOI: https://doi.org/10.1186/s13104-018-3507-2

generate_adjacency_graph.pl is the script used to generate an adjacency graph from Hi-C data where: linear, cis and trans interactions are represented

So far, GrapHi-C has been tested with output from the hiclib pipeline form Mirny Lab (https://bitbucket.org/mirnylab/hiclib)

*** Caution: depending on what network layout you choose to use you will want the above script to output either the direct interaction frequency or the inverse of the interaction frequency. Be mindful of your selection to insure the inverse of the interaction frequency is represented in the final layout. ***

------------------------------------------------------------------------------------------

Example command line for Cytoscape Visualization:

./generate_adjacency_graph.pl GSM1379427_wt_999a-corrected-matrix_hic2.tsv  1258 3 10000 1 C 999a_wt.tsv
enter the starting genomic bin number for each chromosome. Enter d when complete: 1
559
1013
d
enter the ending genomic bin number for each chromosome. Enter d when complete: 558
1012
1258
d


Example command line for Gephi Visualization:

./generate_adjacency_graph.pl GSM2446256_HiC_20min_10kb.txt 1258 3 10000 1 G 20min_edges.tsv
enter the starting genomic bin number for each chromosome. Enter d when complete: 1
559
1013
d
enter the ending genomic bin number for each chromosome. Enter d when complete: 558
1012
1258
d

------------------------------------------------------------------------------------------

This work is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-sa/3.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.
