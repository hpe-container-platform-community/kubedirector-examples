# kubedirector-centos-ad-ldap

```
kubectl -n your-ns apply -f https://raw.githubusercontent.com/hpe-container-platform-community/kubedirector-examples/main/03-centos-ad-ldap/cr-app-centos.json
```

- Ensure your tenant has external authentication configured with an AD/LDAP group
- In the UI provision a centos 7 cluster with `hpecp-ext-auth-secret`

```
...
spec: 
  ...
  connections: 
    secrets: [
      hpecp-ext-auth-secret
    ]
```

### Exercises

1. Try to apply the concepts in this example to Ubuntu `bluedata/ubuntu18x`
