---
title: Introduction
---

Currently there are lot of tools for data manipulation: One can write scripts, use some spesific libraries like Catmandu, use ETL tools, there is Open Refine and so on. 

! How GLAMpipe differs from other tools?

Transformations and processing of GLAM data differs, let's say, from transforming scientific data. Typically GLAM data has:


- multiple values for one field
    - language versions (language codes)
    - multiple authors, types etc.
- inconsistent data
    - data itself is created over the years

### Different ways of making transformations



#### Spreadsheet editing

Spreadsheet editing is the easiest way for non-programmers to transform data. However, this approach has several problems:

- requires lot of work
- complex processing is tricky
- multiple values per cell are not really multiple values
- can not operate with files or uploads
- repeating process for automatically  with another data set is not possible

#### Writing scripts

For programmers, the usual way of making data transformations or data uploads is to write *ad hoc* scripts. This works, but it also has some downsides:

- Scripts are usually not documented and therefore re-using them might be tricky. 
- Writings scripts requires technical expertise.
- It is difficult to make manual fixes to data between transformations. 


#### GLAMpipe

GLAMpipe is trying to combine the strengths of scripting and spreadsheet editing.  

- real multiple values possible for one field (arrays)
    - especially important for GLAM-data (multiple authors etc.)
- easy manual intervention  (like in spreadsheet editing)
    - one can fix values manually if necessary
- graphical user interface
    - usable by non-programmers
- extensible
    - new functionality can be added by writing new nodes
- re-usable pipeline
    - once the pipeline is constructed, it can be re-used for similar cases
    - also via REST API (without GUI)


What are facets?

For example, if you have a database of concerts where there is a year mentioned in own field. Facet first finds unique values and then counts how many times that unique value exists in the records.






