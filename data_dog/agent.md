# Agent

## AWS Linux
- ssh with ec2-user@<ip-address>
- DD_API_KEY=ed4d01c0eddfbf26e883bd7d3e98bcd4 DD_SITE="us5.datadoghq.com" DD_APM_INSTRUMENTATION_ENABLED=host  bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"
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
    

## Collecting logs
- update /etc/datadog-agent/datadog.yaml
    logs_enabled: true
- update /etc/datadog-agent/conf.d/conf.yaml
logs:
  - type: file
    path: /port-back-end/log/app_logs.log
    source: port-back-end
    service: port
## now change permissions so datadog can read
chmod +rx /port-back-end/log
## Restart Agent
sudo systemctl restart datadog-agent
## check status
datadog-agent status | grep -A 40 "Logs Agent"

/home/ec2-user/port-back-end
