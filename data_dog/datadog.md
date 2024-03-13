# Datadog

## Curl Command for sending logs
# Path parameters
export metric_name="dist.http.endpoint.request"
# Curl command
curl -X POST "https://api.datadoghq.com/api/v2/metrics/${metric_name}/tags" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-H "DD-API-KEY: ${DD_API_KEY}" \
-H "DD-APPLICATION-KEY: ${DD_APP_KEY}" \
-d @- << EOF
{
  "data": {
    "type": "manage_tags",
    "id": "ExampleMetric",
    "attributes": {
      "tags": [
        "app",
        "datacenter"
      ],
      "metric_type": "gauge"
    }
  }
}
EOF

## StatsD
opensource tool for sending logs to the forwarder

conf.d/stats.d/conf.yaml
init_config:

instances:
  -host: localhost
   port: 8126 # or wherever your statsd listens

