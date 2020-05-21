# docker-node-oracle

Docker image to be used for building a container ready with Oracle instant client binaries and all necessary environment variables needed to use the primary Node.js Oracle Database driver libraries:

[strong-oracle](https://github.com/strongloop/strong-oracle)  
[node-oracledb](https://github.com/oracle/node-oracledb)


## Usage

In this project you will find two dockerfiles.
One that mounts the image from local version 12 files and one that mounts remote version 19 files. You can clearly download version 19 and replace version 12 locally, just change the file names.

**Pulling from docker hub:**
```
FROM jhomarolo/docker-node-oracle:{VERSION}
```

**Run localy**

First, download or clone this repo to download docker file. After that, you can customize your docker file to suit your application.  Just be aware if you are going to use the docker file that uses local or remote files.

If you are using the local docker, don't forget to copy the oracle folder from this repository to your project.

Then build using Dockerfile.local or remote :
```
docker build -t mycontainername -f Dockerfile.local .
```

### :latest

Using "latest" (FROM jhomarolo/docker-node-oracle) as the version will use "FROM NODE:12" as it's base image.  It is recommended that you use a specific version (X.X.X) but if you only want the latest version of Node 12.X.X then latest will work.


This repository was inspired and based on the repository: [https://github.com/CollinEstes/docker-node-oracle]https://github.com/CollinEstes/docker-node-oracle. Its need for creation was due to the need to work with remote files only.

