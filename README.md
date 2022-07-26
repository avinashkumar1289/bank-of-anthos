# bank-of-anthos

Bank of Anthos is a sample HTTP-based web app that simulates a bank's payment processing network, allowing users to create artificial bank accounts and complete transactions.

These manifests have been tested in OKD 3.11 and GKE Kubernetes cluster

GKE Deployment

Run the below command to deploy BOA on a GKE kubernetes cluster

```
kubectl apply -f ./extras/jwt/jwt-secret.yaml
kubectl apply -f ./kubernetes-manifests
```


OKD Deployment

Create an admin policy and add the defualt service account 

`oc adm policy add-scc-to-user privileged system:serviceaccount:default:default`  
Deploy the manifest files 
```
oc apply -f bank-of-anthos/kubernetes-manifest/jwt/jwt-secret.yaml
oc apply -f bank-of-anthos/kubernetes-manifest/.
```
