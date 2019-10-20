---
title: 'creating nodes'
---

Importing, processing and exporting nodes are always added to a collection, not a project. In order to add a node to a collection, you have to know the collection id, node id and parameters for that node.

Create DSpace 6 import node:

	curl -H "Content-Type: application/json" -d "{}" http://localhost:3000/api/v2/nodes

	POST /projects/DSpAce
    POST /projects/DSpace/collections/thesis_2019
	POST projects/DSpace/collections/thesis_2019/nodes/get_data

