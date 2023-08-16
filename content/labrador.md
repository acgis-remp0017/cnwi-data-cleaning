+++
title = "Labrador"
weight = 6
+++

The Labrador data came from three different field expeditions,
in 1993, 2004, and 2005. The 2004 and 2005 data has
polygon geometry, but I have depicted all the features here as
points so that they may be more easily discerned at this scale.

In this case the data was not so complicated as with
Newfoundland. It was easy to
determine that I had all the ground-truth data mentioned in the
reports that accompanied these datasets.

<figure>

<figcaption>Overview of classified wetland points &ndash;
Minipi region</figcaption>

<img src='../LB.jpg' width=874 height=1240>

</figure>

In total, these datasets yielded 116 classified points out of
131 total (that is, leaving out those with no class or
classified as 'not wetland').

## Challenges encountered

- Some of the classes in the 1993 data were a little mysterious, e.g. awsswamp – clearly a swamp, but does “aws” signify anything with regard to how it should be crosswalked? It turned out not to (it stands for “alder and willow”). 

- Again in the 1993 data, some of the points had dates (well,
  just one date) and data on soil composition, but for most
  points these attributes were null. These points were used in
  the original classification project, so it probably does not signify underlying issues with the quality of the data. 

- Alongside the shapefiles containing ground-truth data were
  MapInfo files (which I didn't recognize when I first saw
  them), some of which had filenames similar to those of the
  shapefiles containing field data. I used a tool from the open-source [GDAL
  project](https://gdal.org/) to convert these to shapefiles and
  determined that they all either duplicated shapefiles that
  I had already discovered or did not contain ground-truth data.
