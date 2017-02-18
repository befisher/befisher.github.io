# Setup A Linux Server

<!-- > Created by Fisher at 15:32 on 2016-11-24. -->

This is a simple guide for newbies to set up a Linux(Ubuntu) server.

## Update server

After installing a Linux system, updating the server is **necessary**.
Run the following scripts to update server.

- `sudo apt update`
- `sudo apt upgrade`

## Install basic programs.

Some basic programs are useful, but it is up to you whether to install it or not.

0. Install `git`
	- $ `sudo apt install git`
0. [Install `pip`][article-install-pip]
	- $ `sudo apt install python-pip python-dev build-essential`
	- $ `sudo pip install --upgrade pip`
	- $ `sudo export LC_ALL=C`
	- $ `sudo pip install --upgrade pip`
	- $ `sudo pip install --upgrade virtualenv`
0. Shadowsocks: to access Google.
	- $ `sudo pip install shadowsocks`
0. `screen`: to run multi processes in the same time.
	- $ `sudo apt-get install screen`
	- $ `screen -S session-name`
0. nodejs: to run NodeJs scripts.
	0. Install from apt
		0. nodejs
			- $ `sudo apt-get install nodejs`
			- $ ```sudo ln -s `which nodejs` /usr/bin/node```
		1. npm
			- $ `sudo apt-get install npm`
	1. Download and extract
		- $ `wget https://nodejs.org/dist/v6.9.1/node-v6.9.1-linux-x64.tar.xz`
		- $ `ln -s /opt/nodejs/bin/node /usr/bin/node`
		- $ `ln -s /opt/nodejs/bin/npm /usr/bin/npm`
0. mongodb
	0. For project development.
		- $ `wget https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-ubuntu1604-3.2.9.tgz`
		- $ `mongod --config <config-file.cfg>`
	1. Install from apt(very old)
		- $ `sudo apt install mongodb`
0. redis: for project development.
	- $ `wget http://download.redis.io/releases/redis-3.2.5.tar.gz`
	- $ `tar -xf redis-3.2.5.tar.gz`
	- $ `mv redis-3.2.5 redis`
	- $ `cd redis`
	- $ `make`
	- $ `sudo /opt/redis/src/redis-server /usr/bin/redis-server`
	- $ `sudo /opt/redis/src/redis-cli /usr/bin/redis-cli`
0. nginx
	- $ `apt install nginx`
0. mkdir: Built up folders
	- $ `cd ~`
	- $ `mkdir assets backups cooperations data get-started projects workspace`
0. forever: run programs(scripts) forever without unexpected exit.
	- $ `npm install forever`

## [Set up a HTTP static server][gist-http-static-server]

Run one of the following command to start a server that serve static files.

- $ `python -m SimpleHTTPServer 3000`
- $ `ruby -run -ehttpd ./ -p3000`





[article-install-pip]: http://www.saltycrane.com/blog/2010/02/how-install-pip-ubuntu/
[gist-http-static-server]: https://gist.github.com/willurd/5720255 "One line to set up HTTP static server"
