# Agent

## AWS Linux
- ssh with ec2-user@<ip-address>
- DD_API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx DD_SITE="us5.datadoghq.com" DD_APM_INSTRUMENTATION_ENABLED=host  bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"
    - etc/datadog-agent
    `datadog.yaml`
hostname: port-back-end

process_config:
    process_collection:
    enabled: true 

- restart agent
    `sudo systemctl restart datadog-agent`

- status
    `systemctl status datadog-agent`
    `ps -eaf | grep datadog`

- agent commands
    `datadog-agent status | more`


