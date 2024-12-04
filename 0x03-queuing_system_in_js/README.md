# 0x03. Queuing System in JS

 `Back-end` `JavaScript` `ES6` `Redis` `NodeJS` `ExpressJ` `Kue`

![image](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/1/1486e02a78cdf7b4557c.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20241204%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241204T081043Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=7676ec774f347eab70f53f95bf55e12430d39498c6a17f75b249fffed026bf30)

## Resources
#### Read or watch:

[Redis quick start](https://redis.io/docs/latest/integrate/)
[Redis client interface](https://redis.io/docs/latest/develop/tools/cli/)
[Redis client for Node JS](https://github.com/redis/node-redis)
[Kue](https://github.com/Automattic/kue) deprecated but still use in the industry

## Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

* How to run a Redis server on your machine
* How to run simple operations with the Redis client
* How to use a Redis client with Node JS for basic operations
* How to store hash values in Redis
* How to deal with async operations with Redis
* How to use Kue as a queue system
* How to build a basic Express app interacting with a Redis server
* How to the build a basic Express app interacting with a Redis server and queue


## Requirements
* All of your code will be compiled/interpreted on Ubuntu 18.04, Node 12.x, and Redis 5.0.7
* All of your files should end with a new line
* A `README.md` file, at the root of the folder of the project, is mandatory
* Your code should use the js extension

## Required Files for the Project
* [package.json]()
* [.babelrc]()
#### and….
Don’t forget to run `$ npm install` when you have the `package.json`

# Tasks

## 0. Install a redis instance
Download, extract, and compile the latest stable Redis version (higher than 5.0.7 - [https://redis.io/downloads/):](https://redis.io/downloads/)
```
$ wget http://download.redis.io/releases/redis-6.0.10.tar.gz
$ tar xzf redis-6.0.10.tar.gz
$ cd redis-6.0.10
$ make
```
* Start Redis in the background with `src/redis-server`
```
$ src/redis-server &
```
* Make sure that the server is working with a ping `src/redis-cli ping`
```
PONG
```
* Using the Redis client again, set the value `School` for the key `Holberton`
```
127.0.0.1:[Port]> set Holberton School
OK
127.0.0.1:[Port]> get Holberton
"School"
```
* Kill the server with the process id of the redis-server (hint: use `ps` and `grep`)
```
$ kill [PID_OF_Redis_Server]
```
Copy the `dump.rdb` from the `redis-5.0.7` directory into the root of the Queuing project.

#### Requirements:

Running `get Holberton` in the client, should return `School`

### Repo:

* GitHub repository: `alx-backend`
* Directory: `0x03-queuing_system_in_js`
* File: `README.md, dump.rdb`
