+++
title = "Workflow"
weight = 2
+++

In general, my workflow followed these major steps:

1. Read the report accompanying the data, noting especially the context in which the data was collected, the number of datasets collected, when and how they were collected, and the number of sites in each dataset. This told me what to look for when identifying the data itself. 
2. Discern which files contain the field data, and if multiple similar files are present, which ones are most suitable. For example, in the case of the 1993 Labrador data, there was one file (actually several files containing identical data) that had all the field data, and another that had only
2. Check if it has a (sensible) spatial reference. Display it on
   a map in ArcGIS Pro; see if it shows up in the expected
   location.
3. Check for any oddities or inconsistencies in the geometry or
   attributes. Flag any features that appear dodgy, possibly
   omitting them from the final database.
4. Locate any pictures taken in the field that came along with the dataset; find
   the correspondence between pictures and features.
5. Select those features that have a wetland class attribute
   that can be mapped onto the
   <abbr title="Canadian National Wetlands Inventory">CNWI</abbr>
   classification system and crosswalk them into the CNWI
   system: that is, reclassify them from their source
   classification to the corresponding classification in the
   CNWI system, and fill in the other CNWI attributes where
   possible. For a lot of the points, the wetland class was the
   only useful attribute present. Where pictures were present,
   these were also attached.

I used the Python libraries Pandas and GeoPandas for much of my
data analysis and transformation. This includes checking the
consistency of attributes with themselves and with other
attributes; ensuring there were no e.g. duplicate points;
integrating multiple incomplete datasets into one (relevant for
the Newfoundland data); and
selecting features that matched my criteria (e.g. has a usable
'class' attribute).

At first I had expected to do more of this work in ArcGIS Pro,
perhaps automating workflows with ModelBuilder, but because the
datasets each had unique characteristics and challenges, this
approach turned out not really to be workable. The small size of
the datasets also limited the benefit of automating things to
this degree. Moreover, ArcGIS Pro's tools for working with
tabular data (as opposed to spatial operations) are sort of
limited; I experimented in rectifying this by creating my own
geoprocessing tool, but in the end I used Pandas more because
its tools were faster and more useful for my purposes.
