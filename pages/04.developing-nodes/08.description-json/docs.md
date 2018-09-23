---
title: description.json
taxonomy:
    category: docs
visible: true
---

    "nodeid": "source_web_finna",
    "title": "Finna.fi: query import",
    "type": "source",
    "subtype": "web",
    "core": "web.get.JSON",

If there is a core defined, then it defines what asynchronous operation gets called before run.js is executed.
For example, if node is a getting data from REST api in JSON format, then GLAMpipe calls "web.get.JSON" with parameters provided pre_run.js. 