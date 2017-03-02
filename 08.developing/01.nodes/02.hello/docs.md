---
title: Hello World node
---


### "Hello world" transform node 
This node will create a new field to all records in the collection and it writes "Hello world" in that field.

The node starts with nodeid, which must be unique. Type and subtype defines how node is executed and where it is displayed when creating new nodes.

	"nodeid": "transform_field_hello_world",
	"title": "Hello world",
	"type": "transform",
	"subtype": "string manipulation",
	"description": "My first node",
	"scripts": {

Scripts part is where the actual code is:

First we say "hello" to user when a node is added to project:

	"hello": "out.say('news', 'You added a HELLO WORLD node'); ",
	
And when if user deletes our node, then we say "bye":

	"bye": "out.say('news', 'Deleted HELLO WORLD node. Bye!'); ",

asd

	"init": "out.say('progress', 'Starting hello...'); ", 
	"run": 
		[
			"out.value = 'Hello World!'; "
		],
		
	"finish": "out.say('finish', 'Hello done!');"
	},
	
Views include html for parameters (for creating node), settings (for running node) and views (for showing data)

	"views": {
		"params":
		[
			"<label>output field</label> <input name='out_field'/ value='hello_world' />"
		],
        "settings":
        [
			"no settings"
        ]
	}





