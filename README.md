# cf-monitor - Cloudflare Zone Monitoring

Aminimal docker-compose configuration to establish a Cloudflare observability solution. It consists of; 

- cloudflare-exporter - https://github.com/lablabs/cloudflare-exporter
- prometheus - https://hub.docker.com/r/prom/prometheus
- grafana - https://hub.docker.com/r/grafana/grafana

## Configuration Required

- docker-compose.yml inputs
    - CF_API_TOKEN: "${CF_API_TOKEN}"  -- Create Cloudflare API token with [required permissions](https://github.com/lablabs/cloudflare-exporter?tab=readme-ov-file#api-token)
    - CF_ZONES: "${CF_ZONE_ID}"  -- Zone ID which is available via the Cloudflare dashboard
- prometheus.yml inputs
    - ${HOST_IP} -- localhost or host ip of cloudflare-exporter