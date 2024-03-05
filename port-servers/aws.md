# Setting up the port project in AWS

## EC2
- Setup with Umbuntu (aws linux)
- get ssh key and store in `~/.ssh/keyhere.pem`
- ssh into the instance with
    `ssh - i ~/.ssh/keyhere.pem ubuntu(ec2-user)@<instance-ip-address>`
    - install github
        sudo yum update
        sudo yum install git
        git --version

    - clone the repository
    - cd to root directory
    - install 
    curl -sL https://rpm.nodesource.com/setup_14.x | sudo bash -
sudo yum install -y nodejs

        - node
        - npm
    - run `npm install`
    - run server
        `node server.js`
## DataDog Agent EC2
- ssh into the instance
    - 