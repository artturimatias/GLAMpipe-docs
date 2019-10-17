---
title: Projects
---

### Creating project

Creating projects is simple, just post the name of the project to /api/v2/projects:

	curl -H "Content-Type: application/json" -d '{"name":"My first project"}' http://localhost:3000/api/v2/projects
    
In addition, you can post id for the project. This makes it possible to write scripts that refer projects by static ids, not uuids that change every time you create a project.  

	curl -H "Content-Type: application/json" -d '{"name":"Thesis from DSpace", "id":"thesis"}' http://localhost:3000/api/v2/projects
    
Then you can refer to project by id ignoring the UUID returned by the request:

	curl -H "Content-Type: application/json"  http://localhost:3000/api/v2/projects/thesis

| path                   | method | parameters    | info               |
|------------------------|--------|---------------|--------------------|
| api/v1/projects        | POST   | title (token) | Create project     |
| api/v1/projects        | GET    |               | Get all projects   |
| api/v1/projects/titles | GET    |               | Get project titles |