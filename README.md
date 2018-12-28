# TCI - Tikal Jenkins-based CI solution

![tci](src/resources/images/tci.png)


### ***TCI - Tikal Jenkins-based CI solution***

We this repository, you can establish 2 kind of TCI Jenkins server types:
* <img src="./src/resources/images/tci-server.png" width="80" height="80"> **tci-server** - for loading a well-established Jenkins server.
* <img src="./src/resources/images/tci-local.png" width="80" height="80"> **tci-local** - for loading a local developement Jenkins environment.(Work in progress)

In order to establish a <img src="./src/resources/images/tci-server.png" width="20" height="20"> **tci-server**, follow the below instructions on the server you want to host it:

1. Make sure you have the following commands installed: **git**, **docker** & **docker-compose**.
1. Make sure you have an SSH private key file on the hosting server. The default path it looks for is ~/.ssh/id_rsa, but you can configure it to use a different file.
1. clone [this repository (git@github.com:TikalCI/tci.git)](git@github.com:TikalCI/tci.git) to a local folder and cd to it.
1. Run _**./tci-dev-env.sh info**_ to see that the path to the SSH private key file is correct. If it is not correct, change it in the generated **.config** file.
1. Run _**./tci-dev-env.sh start**_ to load the server. 
1. The first load will take at least 10 minutes, so please wait until the prompt is back.
1. Once the load is over, browse to [http://localhost:8080](http://localhost:8080) and login with admin/admin credentials.

Once the server is up, you can modify it (e.g. add LDAP configuration, add seed jobs, add credentials and much more) following the instructions as in [tci-master](https://github.com/TikalCI/tci-master).

The _**./tci-dev-env.sh**_ script have the following actions: **start**, **stop**, **restart**, **info**.


