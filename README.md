# Out of sync because OpenShift copied configmap

![image](https://user-images.githubusercontent.com/36604/221351238-fd552ec0-d517-4965-8209-9a43818005f6.png)

## GitOps Application

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: cluster-configuration
  namespace: openshift-gitops
spec:
  destination:
    server: https://kubernetes.default.svc
  project: default
  source:
    path: cluster-configuration/
    repoURL: https://github.com/rbo/gitops-problem-1.git
    targetRevision: main

```

