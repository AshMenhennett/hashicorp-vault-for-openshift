# Spring Example 

## Build the Application

```

oc project dev

oc new-build --name=api-inventory-v2  registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift~https://github.com/AshMenhennett/hashicorp-vault-for-openshift --context-dir=/examples/api-inventory-v2
```

## Deploy
 
### Manual Sidecar Container

```
    oc apply -f examples/api-inventory-v2/spring-example.yaml
```

### Mutating Webhook Configuration

```
    oc apply -f examples/api-inventory-v2/spring-inject.yaml
```