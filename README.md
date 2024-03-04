# port-project
A miniature microservice for testing logging applications on.

## Repositories
- port-back-end
    a server that accepts `{"word":"your-word"}` and logs it
- port-front-end
    html/javascript form to send the word using fetch
- port-script
    node.js script sending a randomly generated word every 5 seconds
- port-selenium
    a node.js selenium script sending a randomly generated word every 5 seconds to the port-front-end

## APM tools
- Splunk
    - loaded UF on port-back-end
    - sent to local instance of splunk
- DataDog
    - loaded the agent 
    - unable to send logs
- Rapid7
- GreyLog

## Deployments
- Local 
    - raspberry pi
- AWS 
    - ec2 instances
- Azure