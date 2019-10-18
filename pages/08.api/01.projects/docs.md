---
title: Projects
---

### Creating project

Creating projects is simple, just post the id (a-z, no spaces) of the project to /api/v2/projects:

	curl -XPOST -H "Content-Type: application/json" http://localhost:3000/api/v2/projects/DSpace
    
In addition, you can post a title for the project.  

	curl -H "Content-Type: application/json" -d '{"name":"Thesis from DSpace"}' http://localhost:3000/api/v2/projects/Dspace
    


| path                   | method | parameters    | info               |
|------------------------|--------|---------------|--------------------|
| api/v1/projects        | POST   | title (token) | Create project     |
| api/v1/projects        | GET    |               | Get all projects   |
| api/v1/projects/titles | GET    |               | Get project titles |