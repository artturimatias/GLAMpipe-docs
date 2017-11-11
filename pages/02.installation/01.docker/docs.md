---
title: Docker
---

Make sure that you have [Docker](https://www.docker.com/) installed and running. You'll also need "make" tool available. Linux has it by default but I'm not sure about Mac/Win. 

1. Fetch GLAMpipe source codes

		git clone https://github.com/artturimatias/GLAMpipe.git
		cd GLAMpipe

2. Build docker network and MongoDB and GLAMpipe images

		make create_network
        make build_mongo
        make build_glampipe
        
3. Start mongo and Nodejs (GLAMpipe) containers

		make start_mongo
        make start_glampipe
        
4. Start GLAMpipe inside Nodejs container

		node glampipe.js