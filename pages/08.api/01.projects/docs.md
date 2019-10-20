---
title: Projects
---

### Creating project

Creating a project is simple, just make a POST request /api/v2/projects/[project_id]. Project id can contain letters from a-z, numbers and but no spaces.

	curl -XPOST -H "Content-Type: application/json" http://localhost:3000/api/v2/projects/DSpace
    
In addition, you can post a title for the project.  

	curl -H "Content-Type: application/json" -d '{"title":"Thesis from DSpace"}' http://localhost:3000/api/v2/projects/Dspace
    


| path                   | method | parameters    | info               |
|------------------------|--------|---------------|--------------------|
| api/v1/projects        | POST   | title (token) | Create project     |
| api/v1/projects        | GET    |               | Get all projects   |
| api/v1/projects/titles | GET    |               | Get project titles |