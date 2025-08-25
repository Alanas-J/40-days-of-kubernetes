# Day 2 - Docker fundamentals
Involves downloading the sample excercise app from the Docker repository and dockerising it.
Running through a Dockerfile and the fundamental docker cli commands.

### Commands used
```sh
# Basic git instead of using GUI eg.
git init
git remote add origin <origin>
git status

# Basic filesystem commands
mkdir <dirname>
touch <filename>
ls

# Downloading files via the CLI
curl -L -o getting-started-app.zip https://github.com/docker/getting-started-app/archive/refs/heads/main.zip
# -L = follow redirects , -o is necessary to curl outputs to files from stdin (equivalent to the pipe operator).
unzip getting-started-app.zip
rm getting-started-app.zip
# Can chain all of these with conditional running via '&&'

# Docker
docker build -t day02:first .
docker tag day02:first alanasjdocker/tutorial-repo:day2image
docker login 
docker push alanasjdocker/tutorial-repo:day2image
docker pull alanasjdocker/tutorial-repo:day2image
docker run -it --name day02 -p 3000:3000 alanasjdocker/tutorial-repo:day2image
# ^Interractive/stdin + pseudo tty (-it), to run detached you can use (-d)
# Images expose ports, but these still need to be mapped to host ports on container instaciation. Cannot publish before or after.
docker start -i day02
docker rm day02
docker exec -it day02 sh
# ^Can execute other processes on a running container.
```
