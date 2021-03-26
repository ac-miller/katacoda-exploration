This is just a placeholder for now, while I do the initial commit.

Create Jenkins container
`docker run -d -u root --name jenkins \
    -p 8080:8080 -p 50000:50000 \
    -v /root/jenkins_2112:/var/jenkins_home \
    jenkins/jenkins:2.112-alpine`{{execute}}

Jenkins dashboard
https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com

The username is `admin`{{copy}}

The password can be found using this command
`docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword`{{execute}}