Galaxy wrapper for UCSC pslCDnaFilter tool (version: v340)
==========================================================
Filter cDNA alignments in psl format. Filtering criteria are comparative, selecting near best in genome alignments for each given cDNA and non-comparative, based only on the quality of an individual alignment.

parameters:
-----------
pslCDnaFilter parameters variable definitions by genome assembly category and type of cDNA sequence.

# common paramters used for all assembly categories

Same species: 
  -minQSize=20 -ignoreIntrons -repsAsMatch -ignoreNs -bestOverlap -polyASizes

Across species: 
  -minQSize=20 -ignoreIntrons -repsAsMatch -ignoreNs -bestOverlap -polyASizes

# common paramters used for local near best filtering

Same species: 
  -localNearBest=0.001 
Across species: 
  -localNearBest=0.010 

# finished assemblies

Same species: 
  -minId=0.95 -minCover=0.25 
Across species: 
  -minId=0.35 -minCover=0.25 

# well-ordered assemblies

Same species: 
  -minId=0.95 -minCover=0.15 
Across species: 
  -minId=0.35 -minCover=0.15 

# low-coverage assemblies

Same species: 
  -minId=0.94 -minAlnSize=80 
Across species: 
  -minId=0.33 -minAlnSize=80 

Reference:
++++++++++
`Configuration file for GenBank RefSeq alignment process <http://genome-source.cse.ucsc.edu/gitweb/?p=kent.git;a=blob;f=src/hg/makeDb/genbank/etc/genbank.conf;h=03c4f3dcd12b48cf52feaf4d09561bf0a58ee352;hb=9447c3aa53839f2adbb3c2ef14ba8540a1dea077>`_


Source code:
-------------

http://hgdownload.cse.ucsc.edu/admin/exe/

Licence
-------
Please note that commercial download and installation of the Blat and In-Silico PCR software may be licensed through Kent Informatics (http://www.kentinformatics.com).
