
Give the `default` service account in the `kube-system` namespace
the `cluster-admin` role so that Helm will have the necessary 
permissions to install the operator:

`kubectl apply -f tiller-cluster-admin.yaml`{{execute}}

Install tiller (the Helm server component):

`helm init`{{execute}}

Check that the `tiller` pod is ready (repeat this command if
necessary, do not proceed until the pod is ready):

`kubectl -n kube-system get pods | grep tiller`{{execute}}
