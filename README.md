# ELK stack running on Docker

The goal of this project is to have an easy way to have the ELK stack running to explore it.


## setup

Edit the .env file and set a password for

```
ELASTIC_PASSWORD=<your-secure-elastic-password>
KIBANA_PASSWORD=<your-secure-kibana-password>
```

This setup has been tested for STACK_VERSION=8.2.0 but might work for future releases, just need to follow the guides for future versions.

This has been inspired from this guide:

- https://www.elastic.co/guide/en/elastic-stack-get-started/current/get-started-stack-docker.html#run-docker-secure



## How to run

From within this directory root, run the following command to pull the required images and start up the ELK stack.

```
docker-compose up
```


http://localhost:5601


## 



# download agent from here

https://www.elastic.co/downloads/past-releases/elastic-agent-8-2-0


Extract the agent (Linux manjaro)

tar -xvzf elastic-agent-8.2.0-linux-arm64.tar.gz 


NOTE: This command can be copied from the wizard "add agent"


![Add agent](images/add_agent.png "add agent")


sudo ./elastic-agent install  \
  --fleet-server-es=http://localhost:9200 \
  --fleet-server-service-token=AAEAAWVsYXN0aWMvZmxlZXQtc2VydmVyL3Rva2VuLTE2NTI4ODYwNTY0NTU6QWdua2tlc21RR1NjUW5kLVNWM3ZxQQ \
  --fleet-server-policy=fleet-server-policy