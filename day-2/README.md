# Day 2 - Docker fundamentals
Involves downloading the sample excercise app from the Docker repository and dockerising it.

## As a part of following this tutorial I'm also forcing myself to use as much bash (and also using vi motions)
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
```
