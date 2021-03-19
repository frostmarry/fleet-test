```yaml
kind: GitRepo
apiVersion: fleet.cattle.io/v1alpha1
metadata:
  name: coba
  namespace: fleet-default
spec:
  repo: https://github.com/frostmarry/fleet-test.git
  branch: main
  paths:
  - coba
  targets:
  - name: aws
    clusterSelector:
      matchLabels:
        env: aws

  - name: microgen
    clusterSelector:
      matchLabels:
        env: microgen
```
