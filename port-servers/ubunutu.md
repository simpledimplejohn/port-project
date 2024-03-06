# Setting up an instance with Ubunutu
- Github already installed
- git clone <repository>
- cd into the directory
- install node.js
    `sudo apt update`
    `sudo apt install nodejs`
    `apt install npm`
- update packages
    `npm install`

## Enable process monitoring
- Uncomment /etc/data-dog/etc/datadog.conf
process_config:
    process_collection:
    enabled: true 
-check wiht this command
`datadog-agnet configcheck`
`datadog-agent config`

