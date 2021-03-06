## Description of front-end server tests
The [front-end server](https://github.com/ldev-r3-t4/frontend-server) is responsible for handling the management of messages for our project.
For the sake of this document messages will be known as posts. Posts are stored in channels. A channel can contain as many posts as possible.

The testing for the front-end server is done through [Newman](https://github.com/postmanlabs/newman). Newman is a command-line tool for the popular [Postman application](https://www.getpostman.com/).  
The tests perform the following actions:
- Creating a new channel.
- Getting a channel.
- Creating a new post.
- Getting a post.
- Updating a post.
- Deleting a post.
- Deleting a channel.

These tests rely on the functionality of the [storage server](http://ec2-54-69-164-246.us-west-2.compute.amazonaws.com:8000/v1/ui/#/primary/).

All the tests are containerized in a docker image.
Running the docker image displays the results of the tests.
Instructions for running the image are located below.
## The following commands run the tests for the front-end server portion.
**Note:** Docker must be installed

### Using Server Hosted on AWS
```sh
docker pull mattg13/round3team4-front-end-server-aws-tests
```
```sh
docker run mattg13/round3team4-front-end-server-aws-tests
```  
### Using server running locally
```sh
docker pull mattg13/round3team4-front-end-server-local-tests
```
```sh
docker run mattg13/round3team4-front-end-server-local-tests
```  
