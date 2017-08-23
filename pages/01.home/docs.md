---
title: GLAMpipe
---

![](piippu.small.png)

 **GLAMpipe** is an extensible open source web-app for transforming datasets and uploading data and media to online repositories.
 
 ! NOTE: GLAMpipe is under development, but you are free to experiment with it already!
 
 If you want to start experimenting directly, go to the [online tool](http://glampipe.org:3000). If you plan to work more extensively with the tool, check out [installation pages](../installation).
 
 The basic idea of GLAMpipe is to read data and files from different sources, process the metadata and export the data and files to different destinations. The workflow is based on **documents and nodes** instead of rows and cells. 
 
 A building block of the data flow is called a node. Each node can do one thing. For example, a node can import data from a source. Another node can modify the data in different ways: split text, combine strings, format Wikimedia templates etc. Finally, a node can export data as files or as data in different formats and to different services like Wikimedia Commons or Wikidata.
 
 GLAMpipe can be used to: 
- browse metadata
- read metadata + files
- process metadata + files
- write metadata + files

