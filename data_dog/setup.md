# Setting up monitoring

# Data Dog
Setup and ingestion of logs from port-back-end server both locally and in AWS

## Setup Agent Locally
- Install the agent on macOS
- Setting up the agent:
    - conf.yaml file 

- query
type:file path:'/User/Desktop/CODE/port-project/port-back-end/log/app_logs.log' service:my-application source:custom sourcecategory:sourcecode

## Running in Ubuntu
Your Datadog Agent is running and functioning properly.
It will continue to run in the background and submit metrics to Datadog.
If you ever want to stop the Datadog Agent, run:
`sudo systemctl stop datadog-agent`
And to run it again run:
`sudo systemctl start datadog-agent`

## S3 bucket
http://<bucket-name>.s3.amazonaws.com/<path-to-file>

s3://port-front-end

index.html

http://port-front-end.s3.amazonaws.com/index.html