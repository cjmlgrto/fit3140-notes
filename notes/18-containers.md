[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Containers

- A **container** image is a lightweight, standalone, executable package of software that includes everything needed to run it (i.e. source code, environment, libraries, packages, etc)
- Containers ensure that software within will always run the same, regardless of the environment surrounding it

#### Containers vs VMs

- **Virtual Machines** — an app running on a VM would mean it would have to boot an OS on top of the host hardware's OS just to run it
- **Containers** — an app running on a container can boot instantly since it shares the same kernel as the host hardware's OS, just isolated with their own environments

## Dockerizing a NodeJS Web App

- **Docker** is a software company that popularised the use of containers
- Docker provides a tool that can package an application and its dependencies in a virtual container that ca n run on any Linux server
- Docker utilises a script called a `Dockerfile` that executes commands needed to setup the container — called a "Docker Image"

### 1 — Create the NodeJS App

```javascript
const express = require('express')
const PORT = 8000
const app = express()
app.get('/', function(req, res) {
	res.send('Hello world\n')
})
app.listen(PORT)
console.log('Running on http://localhost:' + PORT)
```

### 2 — Create the Dockerfile

```dockerfile
FROM node:boron
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY package.json /usr/src/app/
RUN npm install
COPY . /usr/src/app
EXPOSE 8080
CMD ["npm", "start"]
```

### 3 — Build and Run

- `$ docker build -t <your username>/node-web-app`
- `$ docker run -p 49160:8080 -d <your username>/node-web-app`


