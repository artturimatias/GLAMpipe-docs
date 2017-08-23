---
title: 'Node technicalities'
---

### What is the purpose of nodes?

Nodes are mostly **configuration helpers**. For example, node script (pre_run.js actually) is responsible for creating URLs for any REST api call. They also execute data transforms.

### Where are the nodes located?

In the [nodes](https://github.com/GLAMpipe/GLAMpipe/tree/master/nodes) directory.

### How nodes work?

**Simple nodes** (synchronous nodes, like "split" and "search&replace") use current document as an input and create output based document and settings given.

**Complex nodes** (asynchronous nodes, like import or lookup nodes) works in phases. The node first gives "orders" to GLAMpipe of how it should make a certain IO task (for example, make a request to web API). Then the result of this IO task gets back to node which processes it and then outputs the final value.

The distinction between simple and complex nodes is purely technical and the end user should know nothing about it.

#### What happens when a simple node is executed?

The **name of the output field **(or fields) is defined when the node is created. This field(s) is added for all documents in the collection when the node is created. 


This what happens when the user clicks the "run" button:
1. Glampipe finds all documents from current collection
2. Script run.js is executed for each document (see [asyncloop](https://github.com/GLAMpipe/GLAMpipe/blob/master/app/async-loop.js) in source code)
3. Run.js can access the current document via **context.doc** variable. 
4. Run.js sets the desired output to **out.value** or **out.setter** (multiple output fields)
3. After run.js is executed, the result (out.value) is **added** to document.

#### What happens when a complex node is executed?

If node is a processing (i.e. not source node) node, then the **name of the output field **(or fields) is defined when the node is created. This field(s) is added for all documents in the collection when the node is created. 

However, if the node is an import, export or view node, then there is no output fields. 

This what happens when the user clicks the "run" button (FINNA import node):

1. The nodes's init.js script is called. This outputs the search query URL.
2. GLAMpipe executes the request and saves response to context.data.
3. Next GLAMpipe executes run.js, which processes....

If node is an import node, the collection is emptied from previous records imported by this node. 

#### Web import nodes

Web import nodes are a special case of complex nodes. There two ways of how importing data from web APIs work.
The firt one is that the API gives a list of IDs based on query and then one must fetch the details of every id separately. The other way is that the query gives a paged result with full details and one must page repeat query .

This means that 