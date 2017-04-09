---
title: Nodes
---

Nodes are the "pipe" part of the GLAMpipe. Nodes are building blocks that do one thing for data. 

GLAMpipe uses nodes for workflow management. By putting nodes in series one can make all kind of transforms of data. 

There are four groups of nodes:
* import
* process
* download
* export
* view (currently not implemented)

### Node principles

1. The idea of node is that node makes one, relatively **simple thing** for data or file. 

    By chaining these simple things one can build more complex transformations (pipes).


2. Nodes **do not edit** imported (original) data

    For example, if you use a "split" node for "author" field, you get a new field called "author_splitted". 
    This makes experimenting with setting easy, since you can not mess with original data



