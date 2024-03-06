# Setting up an instance with Ubunutu
## ssh into the instance
- `sudo su` change to rrot user

## Install Datadog Agent
- DD_API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx DD_SITE="us5.datadoghq.com" DD_APM_INSTRUMENTATION_ENABLED=host  bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"


## Enable process monitoring
- Uncomment /etc/data-dog/etc/datadog.conf
process_config:
    process_collection:
    enabled: true 
-check wiht this command
`datadog-agnet configcheck`
`datadog-agent config`

## Install node.js
- Github already installed
- git clone <repository>
- cd into the directory
- install node.js
    `sudo apt update`
    `sudo apt install nodejs`
    `apt install npm`
- update packages
    `npm install`

## Install python 