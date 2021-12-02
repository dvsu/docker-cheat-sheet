# Installation

## Ubuntu

### Uninstall old version if exists

```none
sudo apt-get remove docker docker-engine docker.io containerd runc
```

### Update `apt` packages

```none
sudo apt-get update
```

### Install required packages

```none
sudo apt-get install ca-certificates curl gnupg lsb-release
```

### Add Docker's GPG key

```none
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

### Set up Docker repository

Note the `nightly` and `test` keywords after `stable` for `nightly` and `test` channels respectively.

`stable` channel

```none
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

`nightly` channel

```none
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable nightly" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

`test` channel

```none
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable test" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Install Docker engine

```none
sudo apt-get update
```

```none
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### Install specific version of Docker

```none
sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io
```

### Reference

- [Install Docker Enginer on Ubuntu](https://docs.docker.com/engine/install/ubuntu/)
