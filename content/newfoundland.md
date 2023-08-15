+++
title = "Newfoundland"
weight = 5
+++

The Newfoundland data consists of seven shapefiles and one Excel
spreadsheet. The data was collected in 2005 at various sites on
the Avalon Peninsula (St John's area).

The main challenge with this dataset was that these
shapefiles had some duplicate data between them:

* Some points, as identified by geometry or by the 'Site'
  attribute, were found in multiple shapefiles; other in only
  one.
* The attributes were mostly consistent: if the 'Date' attribute
  for a certain point was '2005-08-10', for example, in one
  shapefile, it was the same in the others.
* On the other hand, some attributes were inconsistent. In
  particular, the 'Class' and 'Comment' attributes sometimes had
  different values in different files for the same point.

The inconsistency with the 'Class' attribute was the real
problem. In the end, several points could not be used because of
this ambiguity.
