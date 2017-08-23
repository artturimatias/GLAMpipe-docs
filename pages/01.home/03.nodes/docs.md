---
title: Terminology
---

## Pipe
The workflow in GLAMpipe consists of actions that are done with the data. The actions are called nodes and the workflow is called a pipe.

## Node
Nodes are the building blocks of GLAMpipe. The idea of a node is that each node makes one, relatively **simple thing** with the data or file. By chaining nodes one can make different transformations to the data.

There are four groups of nodes:
* Importing data
* Processing data
* Getting files
* Exporting files and data

Nodes **do not overwrite** original data. For example, if you use a "split" node for the "author" field, you get a new field called "author_splitted". This makes experimenting easy, since you can not destroy the original data
    
## Project
A user can create a project that contains everything that is used in the project.

## Collection
A collection is a dataset used in the project. There may be several datasets in a project. They can be used for subsets of data, such as the data for authors or places that are recurrent in the main dataset.


