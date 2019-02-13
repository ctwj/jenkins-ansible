# jenkins-ansible

Provides an image based on official jenkins/jenkins, with ansible support.

Ansible is installed by pip, to get the latest available version.

Will be updated each time a new jenkins image is provided. 

# Options

All standard jenkins options are available

## Ports

You have to bind port 8080 to access to the web interface.
You can bind port 5000 if you need to add other workers.

## Volumes

You can (and should) bind a volume to /var/jenkins_home to keep data persistant (plugins and configuration)

```$xslt
docker run -p 8080:8080 -p 50000:50000 -v /your/home/jenkins:/var/jenkins_home ctwj/jenkins-ansible
```
