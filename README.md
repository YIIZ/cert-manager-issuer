# cert-manager-issuer
Letsencrypt cluster issuer for [cert-manager](https://github.com/helm/charts/blob/master/stable/cert-manager/)


## Install & Usage
```
helm install tgz --set email=your@email.com
```

Update default issuer of cert-manager
```
helm upgrade NAME stable/cert-manager --set ingressShim.defaultIssuerKind=ClusterIssuer,ingressShim.defaultIssuerName=letsencrypt-prod
```


## Configuration

| Parameter |         Description         |     Default      |
|-----------|-----------------------------|------------------|
| `email`   | Email for ACME registration | `your@email.com` |
