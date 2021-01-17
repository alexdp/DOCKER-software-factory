"# DOCKER-software-factory" 

Configuratiuon proxy docker hub :

https://mtijhof.wordpress.com/2018/07/23/using-nexus-oss-as-a-proxy-cache-for-docker-images/



Click on Repository -> Repositories, and click on ‘Create repository’.
Select the ‘docker (proxy)’ recipe and start the configuration.
Check Allow anonymous docker pull ( Docker Bearer Token Realm required )

Click on Administration -> Security -> Realms and enable Docker Bearer Token Realm


Configuration du client docker (daemon docker)

/etc/docker/daemon.json on Linux
Docker Engine GUI settings on Windows
{
        "insecure-registries": ["192.168.3.91:8282"],
        "registry-mirrors": ["http://192.168.3.91:8282"]
}