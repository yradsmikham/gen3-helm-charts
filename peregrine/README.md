# peregrine

### Configuring Secrets

For `peregrine-secret`:
```
kubectl create secret generic peregrine-secret --from-file=local_settings.py=./peregrine_settings.py
```

For `peregrine-creds`:
```
kubectl create secret generic peregrine-creds --from-file=creds.json=../Secrets/peregrine_creds.json
```

For `config-helper`:
```
kubectl create configmap config-helper --from-file=./config_helper.py
```

service-ca

For `ca-volume`:
```
kubectl create secret generic "service-ca" --from-file=../Secrets/ca.pem
```