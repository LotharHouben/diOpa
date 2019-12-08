SUPER-CELL FILES 
----------------

A super-cell structure file is used used as input file for the xyz "atomic" coordinates.  
The super-cell has the most simple symmetry P1.
Two example are part of the diOPA distribution: 
Au-crystal.cel represents a truncated Au nanoparticle with perfect fcc structure.  Ferritin-agglomerate.cel is ferritin agglomerate in the early stages of nucleation and crystal growth which shows partial fcc ordering. 
The following description details the format of the super-cell file.
The common filename suffix for this format is ".cel". 

FORMAT SPECIFICATION
--------------------

Use ANSI character encoding when saving the .cel file, separate the values by at least one space character, use the "period" (.) as decimal delimiter.

line 01: # comment or structure name, no relevant structure data
line 02:   <zero>  <x cell size>  <y cell size>  <z cell size>  <alpha cell angle in deg>  <beta cell angle in deg>  <gamma cell angle in deg>  (currently only 90 degree cell angles!)
line 03:  <Atom symbol>  <x fractional coordinate>  <y fractional coordinate>  <z fractional coordinate>  <occupancy>  <vibration parameter for Debye-Waller factor in nm^2>  <zero>  <zero>  <zero>  (Example: " Ge  0.00000  0.00000  0.00000  1.0000  0.60000  0.00000  0.00000  0.00000")
line 04:  <Atom symbol>  <x fractional coordinate>  <y fractional coordinate>  <z fractional coordinate>  <occupancy>  <vibration parameter for Debye-Waller factor in nm^2>  <zero>  <zero>  <zero>  (Example: " Ge  0.50000  0.50000  0.50000  1.0000  0.55000  0.00000  0.00000  0.00000")
line 05:  ... ( more atomic data as in line 03 and 04)
....
line XX: * (final line, the "*" signalises the end of atomic data)

NOTES
-----

Note that for the order parameter analysis notebooks

(1) The nearest neighbour distance is required to be 1. You need to scale the cell dimensions x y z appropriately!
    Example: In Germanium the unit cell dimensions (x cell size, y cell size and z cell size) are 0.5657 nm. The nearest neighbour distance 
    between two Germanium atoms is 0.244944. In order to scale the nearest neighbour spacing to 1 the cell dimensions need to be multiplied by the factor
    1/0.24944.
(2) Atom symbol, occupancy, Debye-Waller factors and absorption parameters are ignored. You can safely choose any two-character symbol label and set 
    occupancy, Debye-Waller factors and absorption parameters to zero. 


EXAMPLES
--------

Example cell file:

# Germanium super cell file
  0  2.3094 2.3094  2.3094 90.0000 90.0000 90.0000
 Ge   0.750000  0.750000  0.250000  1.000000  0.005000  0.100000  0.100000  0.100000
 Ge   0.750000  0.250000  0.750000  1.000000  0.005000  0.100000  0.100000  0.100000
 Ge   0.500000  0.500000  0.000000  1.000000  0.005000  0.100000  0.100000  0.100000
 Ge   0.500000  0.000000  0.500000  1.000000  0.005000  0.100000  0.100000  0.100000
 Ge   0.250000  0.750000  0.750000  1.000000  0.005000  0.100000  0.100000  0.100000
 Ge   0.250000  0.250000  0.250000  1.000000  0.005000  0.100000  0.100000  0.100000
 Ge   0.000000  0.500000  0.500000  1.000000  0.005000  0.100000  0.100000  0.100000
 Ge   0.000000  0.000000  0.000000  1.000000  0.005000  0.100000  0.100000  0.100000
*
