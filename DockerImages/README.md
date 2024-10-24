In this section we disscuss how to install the docker in ubuntu 22.04 and then build a docker file for our app and run it in docker container.

# Install docker in Ubuntu 22.04

**Step 1. Set up Docker's apt repository.**

```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc


# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

```
**Step 2. Install the Docker packages.**
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

**Step 3. Verify that the Docker Engine installation is successful by running the hello-world image.**
```
 sudo docker run hello-world
```

# Now download the files present in this folder and run the following commands 

```
docker build -t rest-apis-flask-python .
docker ps
docker images
docker run -d -p 5000:5000 --name my-flask-app rest-apis-flask-python
docker stop my-flask-app
docker compose up
```
