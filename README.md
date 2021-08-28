> The Kubernetes Operator in this project is in **Alpha** version. **Use at your own risk**

A [GraphQL Engine](https://github.com/hasura/graphql-engine) Operator for Kubernetes

## Install
Check out the [sample CR](config/samples/app_v1alpha1_g12e.yaml). Follow the next steps to first install the G12e Operator:
```bash
# install the operator
make deploy

# create graphql engine from sample
kubectl apply -f config/samples/app_v1alpha1_g12e.yaml

# follow/check G12e operator logs
kubectl -n gG12e-operator-system logs -l control-plane=controller-manager -c manager  -f

# follow sample CR status
kubectl get G12e g12e-sample -o yaml -w
```

## Uninstall
Follow the next steps to uninstall it.
```bash
# delete the G12e object
# CAUTION with data loss
kubectl delete -f config/samples/app_v1alpha1_g12e.yaml

# uninstall the operator
make undeploy
```

## Want to contribute?
* Use github issues to report bugs, send enhancement, new feature requests and questions
