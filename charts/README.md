# Helm Charts for Running SiteWhere 2.0

To deploy SiteWhere default configuration in a Kubernetes clusters as a Helm Chart, run the command:

## Install Rook

Install rook with the following command:

```
kubectl create -f rook/operator.yaml
kubectl create -f rook/cluster.yaml
kubectl create -f rook/storageclass.yaml
```

## Start Consul

Start Consul running the following command:

```sh
helm install --name consul ./consul
```

## Start SiteWhere

To start default configuration run:

```sh
helm install --name sitewhere ./sitewhere
```

To run minimal recipes, run the following command:

```sh
helm install --name sitewhere --set services.profile=minimal ./sitewhere
```

To remove sitewhere, execute the following command

```sh
helm del --purge sitewhere
```