# kubectl commond
Troubleshooting and Debugging Commands:

`$ kubectl get` - list resources

`$ kubectl describe` - show detailed information about a resource

`$ kubectl logs` - print the logs from a container in a pod

`$ kubectl exec` - execute a command on a container in a pod

---
Example

`$ kubectl get` pods 

`$ kubectl get` pods --all-namespaces -o wide 

`$ kubectl describe` pods/aog000001-0 --watch

`$ kubectl get` nodes 

`$ kubectl get` namespace

`$ kubectl get` pods -n my-namespace

`$ kubectl get` statefulsets 

`$ kubectl get` statefulsets/cgsweb -o wide

`$ kubectl logs` -f statefulsets/aog000001-0 aog000001

`$ kubectl describe` statefulsets/cgsweb 

`$ kubectl get` services


