## Utils commands to search for resources

Search by pod IP.
~~~
kubectl get --all-namespaces  --output json  pods | jq '.items[] | select(.status.podIP=="10.22.19.69")' | jq .metadata.name
~~~

List pods and their workers where they are assigned.
~~~
kubectl get pod -o=custom-columns=NAME:.metadata.name,STATUS:.status.phase,NODE:.spec.nodeName --namespace live
~~~

