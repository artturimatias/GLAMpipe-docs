---
title: 'creating nodes'
---

Importing, processing and exporting nodes are always added to a collection, not a project. In order to add a node to a collection, you have to know the collection uuid, node id and parameters for that node.

Create DSpace 6 import node:

	curl -H "Content-Type: application/json" -d "{}" http://localhost:3000/api/v2/nodes
