# Datadog

## Curl Command for sending logs
- DD_API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx DD_SITE="us5.datadoghq.com" DD_APM_INSTRUMENTATION_ENABLED=host  bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"

## StatsD
opensource tool for sending logs to the forwarder

conf.d/stats.d/conf.yaml
init_config:

instances:
  -host: localhost
   port: 8126 # or wherever your statsd listens

