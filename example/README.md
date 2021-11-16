# Command

## Apply new config

File name does not matter for k8s cluster

` $ kubectl apply -f pod.yaml`

to apply pod to cluster.

` $ kubectl apply -f service.yaml`

to apply service to cluster.


` $ kubectl apply -f .`

to apply all yaml file to cluster.

---

## Remove config from cluster
 
In the same way as kubectl apply, we can use delete to remove config out

` $ kubectl delete -f pod.yaml`

to delete pod in config from cluster

` $ kubectl delete -f .`

to remove all config yaml from cluster

---

## Rolling Updates
When a StatefulSet's `.spec.updateStrategy` type is set to `RollingUpdate`, the StatefulSet controller will delete and recreate each Pod in the StatefulSet. It will proceed in the same order as Pod termination (from the largest ordinal to the smallest), updating each Pod one at a time.

The Kubernetes control plane waits until an updated Pod is Running and Ready prior to updating its predecessor. If you have set .spec.minReadySeconds (see Minimum Ready Seconds), the control plane additionally waits that amount of time after the Pod turns ready, before moving on.

---

## ImagePullPolicy values

- `Always` Always pull the image.

* `IfNotPresent` Only pull the image if it does not already exist on the node.

- `Never` Never pull the image.