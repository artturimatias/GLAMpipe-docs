---
title: 'GLAMpipe as software library'
---

    async function createEMptyProject() {
        var GLAMpipe = require('../app/glampipe.js');
        var GP = new GLAMpipe();

        var project = await GP.createEmptyProject("My first projects");
        var collection = await GP.createCollection("my collection", project);

        // let's close DB connection
        GP.closeDB();
	}
    
    createEmptyProject();
    
