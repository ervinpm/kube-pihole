# Pihole for Kubernetes

Configuration to spin up pihole into your kubernetes cluster

## How to use
```sh
$ kubectl -f deployment.yaml
```

## Notes
If you are able to go to the ip address but unable to load the dashboard,
check if the cpu usage of `lsof` is close to 100%. This symptom is caused
by containerd not running under docker. Disable with the following commands:

```sh
$ systemctl stop containerd
# systemctl disable containerd
```
