# ansible-role-app-jenkins

An Ansible Role installs and configures a jenkins environment on Ubuntu.

Work in Progress..

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see defaults/main.yml):

```yml
vol_dir: "/store/volumes"
```

Path to volume directory which will contain docker volume mounts.

```yml
app_dir: "/store/app"
```

Path to application directory which will contain docker images and compose-files.

```yml
docker_network: "172.16.232.0/24"
```

Network-ID which will be used for the docker-compose application.

```yml
docker_network_gateway: "172.16.232.1"
```

Gateway which will be used within the docker containers representing the docker host.

```yml
offline_mode: true
```

Define if internet access is possible to use jenkins with github or use local gogs container.

```yml
repositories:
  - name: "jenkins-task-play01"
    url: "https://github.com/BadFever/jenkins-task-play01.git"
```

List of repositories to import with internet access.

```yml
gogs_user: "ansible"
```

Username for gogs account.

```yml
gogs_password: "VMware1!"
```

Password for gogs account.

## Dependencies

None.
