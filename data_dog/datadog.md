# Datadog

## StatsD
opensource tool for sending logs to the forwarder

conf.d/stats.d/conf.yaml
init_config:

instances:
  -host: localhost
   port: 8126 # or wherever your statsd listens

