# diOpa
diOPA is a package of tools for the calculation of local order in atomistic clusters of matter. 



CONTENTS
--------

The diOPA package for order parameter analysis contains Mathematica notebooks for the calculation of local order in atomistic clusters. 
The following notebooks are included in the package:

- create_db.nb
- test_db.nb
- evaluate_order.nb
- evaluate_density.nb
- evaluate_pdf.nb

create_db is a program to create a database that contains rotation variants of a predefined coordination polyhedron. The database is used for the local order parameter determination on a dataset of atoms/molecules that can e.g. represent a crystalline condensate or a less ordered cluster.

test_db is a consistency check to evaluate database match, i.e. the match of a given coordination polyhedron with the rotation variants of the database. 

evaluate_order.nb calculates for a data set with xyz atom/molecule coordinates for each "atom" the best match, i.e. the minimum distance norm against all rotation variants in a database file of a given coordination. evaluate_order.nb creates a three dimensional temperature map for this best match of each atom/molecule
in the xyz data. 

evaluate_density.nb calculates for a data set with xyz atom/molecule coordinates for each "atom" the local density of atoms/molecules around this centre "atom". evaluate_density.nb creates a three dimensional temperature map for the local density.

evaluate_pdf.nb is a helper tool that calculates the pair correlation function for a data set with xyz atom/molecule coordinates. 

REQUIREMENTS
------------

Mathematica version 7.0.1 or higher is required, available from www.wolfram.com.
Mathematica is available for Windows, Mac, and Linux.


INSTALLATION 
-------------

Choose the 'master' branch and click on 'Clone or download', dowload diOPA as a zip package and unpack the full directory tree into a program folder of your choice. This procedure should take few seconds only.


DIRECTORY STRUCTURE
---------------------

The top directory contains the notebooks. 
The subfolder 'db' is an output folder where create_db.nb stores by default its database files. 
The subfolder 'data' contains exemplary xyz atomic cluster files, together with a description of the file format. 
The subfolder 'out' is used by evaluate_order.nb and evaluate_density.nb for data and graphics file output.
The subfolder 'extra' contains the pdf output of exemplary notebook evaluations. 


USAGE
-----

Each notebook contains header information about input, output and usage. Open a notebook in Mathematica and follow the instructions in the header information. In general each notebook requires a minimum input of parameter values in a marked section that starts with 'BEGIN USER INPUT' and ends with 'END USER INPUT'. Afterwards you simply delete all cell output and evaluate the notebook.
test_db.nb and evaluate_order.nb require a database file as input. This should be created with create_db.nb beforehand. evaluate_order.nb, evaluate_density.nb further require a file with xyz atomic/molecular coordinates for input. Details about the input file format for the xyz atomic/molecular coordinates are given in a README file in the "data" sub-folder.


AUTHOR INFORMATION
------------------
L. Houben <br />
Weizmann Institute of Science <br />
lothar.houben(at)weizmann.ac.il <br />


COPYRIGHT
--------- 

This software is licensed under the GNU GENERAL PUBLIC LICENSE Version 3. <br />
The full license text can be found in the LICENSE file. 



