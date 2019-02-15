# Learning locker LRS installation in a Ubuntu 14.04 LTS server

## Requirements
The server needs to have  HTTPS configured with an SSL certificate

## Steps

### Update
```
sudo apt-get update
sudo apt-get upgrade
```
### Node.js installation
```
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
```
### MongoDB installation
```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4
echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/4.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list
sudo apt-get install -y mongodb-org
sudo service mongod start
```
### Run the install script

```
wget -qO deployll.sh http://lrnloc.kr/installv2
sudo bash deployll.sh
```
