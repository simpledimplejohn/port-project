# Setting up the port project in AWS

## EC2
- Setup with Umbuntu
- get ssh key and store in `~/.ssh/keyhere.pem`
- ssh into the instance with
    `ssh - i ~/.ssh/keyhere.pem ubuntu@<instance-ip-address>`
    - clone the repository
    - cd to root directory
    - install 
        - node
        - npm
    - run `npm install`
    - run server
        `node server.js`
## DataDog Agent EC2
- ssh into the instance
    - 