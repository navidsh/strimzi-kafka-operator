# Install the Strimzi operator using an `OperatorSource`

Apply the following `OperatorSource`:

```console
cat <<EOS |kubectl apply -f -
---
apiVersion: operators.coreos.com/v1
kind: OperatorSource
metadata:
  name: strimzi-operators
  namespace: openshift-marketplace
spec:
  type: appregistry
  endpoint: https://quay.io/cnr
  registryNamespace: navidsh
  displayName: "Bindable Strimzi Operators"
EOS
```

Then navigate to the **Operators** -> **OperatorHub** in the OpenShift console and select the Strimzi operator.

