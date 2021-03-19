kind: GitRepo
apiVersion: fleet.cattle.io/v1alpha1
metadata:
  name: helm
  namespace: default
spec:
  repo: https://github.com/frostmarry/fleet-test.git
  paths:
  - coba
  targets:
  - name: aws
    clusterSelector:
      matchLabels:
        fleet.cattle.io/cluster-name: c-nsg6f

  - name: microgen
    clusterSelector:
      matchLabels:
        fleet.cattle.io/cluster-name: c-kdkrk
