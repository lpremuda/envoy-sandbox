# envoy-practice

Basic Envoy configuration
``` 
envoy -c config/envoy-basic.yaml
curl -v localhost:10000
```

Merge configuration from `envoy-override.yaml` into `envoy-basic.yaml`:
```
envoy -c config/envoy-basic.yaml --config-yaml "$(cat config/envoy-override.yaml)"
curl -v localhost:9902
```