1. Execute the steps then exit the container `docker-compose run --rm npm init`

---Output---
```
vibho@DESKTOP-A6FACL7 MINGW64 /d/Golang_Projects/Docker/Docker-Examples/4.Udemy_Utility_Containers_POC/node-project (main)
$ docker-compose run --rm npm init
[+] Running 1/1
 - Network node-project_default  Created                                                                                                                                                                    0.9s
[+] Building 3.6s (7/7) FINISHED
 => [internal] load build definition from Dockerfile                                                                                                                                                        0.1s
 => => transferring dockerfile: 91B                                                                                                                                                                         0.0s
 => [internal] load .dockerignore                                                                                                                                                                           0.1s
 => => transferring context: 2B                                                                                                                                                                             0.0s
 => [internal] load metadata for docker.io/library/node:14-alpine                                                                                                                                           3.3s
 => [auth] library/node:pull token for registry-1.docker.io                                                                                                                                                 0.0s
 => [1/2] FROM docker.io/library/node:14-alpine@sha256:12b14bdfa8c89a1a060c53b5714157085700660b12ab7c50a907a4e19d95b6bf                                                                                     0.1s
 => => resolve docker.io/library/node:14-alpine@sha256:12b14bdfa8c89a1a060c53b5714157085700660b12ab7c50a907a4e19d95b6bf                                                                                     0.1s
 => CACHED [2/2] WORKDIR /app                                                                                                                                                                               0.0s
 => exporting to image                                                                                                                                                                                      0.1s
 => => exporting layers                                                                                                                                                                                     0.0s
 => => exporting manifest sha256:e7236a5db9057936ea0e297ced14feffc18cec3763983b8439caafb006c3b32d                                                                                                           0.0s
 => => exporting config sha256:36870e11a12afacd62987dea23504eeff21101a94fab3ecc4a5a384ceaf0efab                                                                                                             0.0s
 => => naming to docker.io/library/node-project-npm:latest                                                                                                                                                  0.0s
 => => unpacking to docker.io/library/node-project-npm:latest                                                                                                                                               0.0s

Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (app) test
version: (1.0.0)
description: TestApplication
entry point: (index.js)
test command: npm init
git repository:
keywords:
author:
license: (ISC)
About to write to /app/package.json:

{
  "name": "test",
  "version": "1.0.0",
  "description": "TestApplication",
  "main": "index.js",
  "scripts": {
    "test": "npm init"
  },
  "author": "",
  "license": "ISC"
}


Is this OK? (yes)
```
