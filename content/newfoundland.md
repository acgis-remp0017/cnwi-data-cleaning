+++
title = "Newfoundland"
weight = 5
+++

The Newfoundland data consists of seven shapefiles and one Excel
spreadsheet. The data was collected in 2005 at various sites on
the Avalon Peninsula. This dataset yielded 57 definitively classified points out of 107 total features.

<figure>

<figcaption>Overview of classified wetland points &ndash;
Avalon Peninsula</figcaption>

<img alt="A map depicting 41 points upon the Avalon peninsula,
symbolized by wetland class, with satellite image basemap."
src='../NF.jpg' width=874 height=1240>

</figure>

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

In the case of the class attribute, some of the inconsistency
may be attributed to using a finer-grained classification
system when collecting the data and using a coarser-grained
system when using the data to validate a classified image.

The report accompanying the data said that they collected 89
field points and that they found 57 of them usable for
training/validation of their classification; the others, they
said, could not be classified definitively or represented too
small an area.

Initially I had trouble tracking down the 57 high-quality
points; once I found the relevant shapefile, though, I used the
class attribute from those points and joined it with the field
notes, date and time attributes, etc. from the other shapefiles
to create a consolidated source dataset. These 57 were the
points I crosswalked.

On the other had, I could not determine definitively which
points were the 89 that had been visited.
