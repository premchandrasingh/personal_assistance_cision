# LINUX commands

- `whoami`
  To identify the user name. Or to identify instance is running on root user or custom user

- `uname -a`
  To identify the linux OS details like, distro, architechture (x86_64) etc

- `apt-get update && apt-get install curl -y`
  To install curl without promting Y/N

- `apt-get update && apt-get install -y iputils-ping`

- `apt-get update && apt-get install -y vim`
  Intall vim. Quick Vim tutorial - https://www.youtube.com/watch?v=ggSyF1SVFr4

- `apt-get update && apt-get install -y iputils-ping`
  Instal ping utility https://alexhost.com/faq/ping-command-not-found-how-to-install-ping-in-ubuntu

  - `ping -c 4 google`
  - `ping -c 4 media-service-active` Will send

- `apt-get update && apt-get install -y curl`

  This will help test POD to POD communication is good

  - `curl --location --request GET http://media-service-active:5000/api/v1/2222/assets`
