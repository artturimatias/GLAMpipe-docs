---
title: Projects
---

### Creating project

Creating projects is simple, just send the name of the project:

	curl -H "Content-Type: application/json" -d '{"name":"My first project"}' http://localhost:3000/api/v2/projects

| path                   | method | parameters    | info               |
|------------------------|--------|---------------|--------------------|
| api/v1/projects        | POST   | title (token) | Create project     |
| api/v1/projects        | GET    |               | Get all projects   |
| api/v1/projects/titles | GET    |               | Get project titles |