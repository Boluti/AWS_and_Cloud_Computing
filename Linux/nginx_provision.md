### Scripting ###

#!/bin/bash

# update
sudo apt update

# upgrade
sudo apt upgrade -y

# install nginx
sudo apt install nginx -y

# restart nginx
sudo systemct1 restart nginx

# enable nginx
sudo systemct1 enable nginx