## Utils commands to search for resources

Search by pod IP.
~~~
kubectl get --all-namespaces  --output json  pods | jq '.items[] | select(.status.podIP=="10.22.19.69")' | jq .metadata.name
~~~

List pods and their workers where they are assigned.
~~~
kubectl get pod -o=custom-columns=NAME:.metadata.name,STATUS:.status.phase,NODE:.spec.nodeName --namespace live
~~~

List all resources, literally.
~~~
kubectl get $(kubectl api-resources| awk '{ print $1 }'|grep -v "NAME"|xargs|sed -e 's/ /,/g')
~~~

List all resources, in a specific namespace.
~~~
kubectl api-resources --verbs=list --namespaced -o name \
  | xargs -n 1 kubectl get --show-kind --ignore-not-found -n ingress-nginx
~~~
