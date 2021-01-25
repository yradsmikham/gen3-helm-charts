# fence

### Configuring Secrets

For `cert-fence-service`:
```
k create secret generic cert-fence-service --from-file=./scripts/service.crt --from-file=./scripts/service.key
```

For `fence-config`:
```
k create secret generic fence-config --from-file=./scripts/fence-config.yaml
```

For `fence-jwt-keys`:
```
k create secret generic fence-jwt-keys --from-file=./scripts/jwt_keys/jwt_private_key.pem --from-file=./scripts/jwt_keys/jwt_public_key.pem
```

For `service-ca`:
```
k create secret generic service-ca --from-file=./scripts/ca.pem
```

### Configuring ConfigMaps

For `fence-yaml-merge`:
```
k create configmap fence-yaml-merge --from-file=./scripts/yaml_merge.py
```

For `logo-config`:
```
k create configmap logo-config --from-file=./scripts/logo.svg
```

For `privacy-policy`:
```
k create configmap privacy policy --from-file=./scripts/privacy_policy.md
```

### API Documentation

[OpenAPI documentation available here.](http://petstore.swagger.io/?url=https://raw.githubusercontent.com/uc-cdis/fence/master/openapis/swagger.yaml)
