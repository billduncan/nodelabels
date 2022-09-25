# nodelabels
k8s wrapper to get specific node labels

## Website

See https://billduncan.org/k8s-tips-and-scripts-2/ for some details

## Description

The kubectl command has a way to show the node labels, but too verbosely
and not useful by itself in my opinion.

This script will show just the node labels specified on the command line.

eg.

```
$ nodelabels node-pool tier
NAME           STATUS  ROLES  AGE  VERSION 
10.255.255.109 Ready   node   11d  v1.23.5  node-pool=infra_1 tier=infrastructure
10.255.255.148 Ready   node   11d  v1.23.5  node-pool=websv_1 tier=frontend
10.255.255.158 Ready   node   11d  v1.23.5  node-pool=runtm_3 tier=service
10.255.255.169 Ready   node   11d  v1.23.5  node-pool=infra_1 tier=infrastructure
10.255.255.175 Ready   node   11d  v1.23.5  node-pool=runtm_7 tier=service
10.255.255.192 Ready   node   11d  v1.23.5  node-pool=poolx_1 tier=service
10.255.255.230 Ready   node   11d  v1.23.5  node-pool=runtm_5 tier=service
10.255.255.239 Ready   node   11d  v1.23.5  node-pool=infra_1 tier=infrastructure
10.255.255.243 Ready   node   11d  v1.23.5  node-pool=runtm_1 tier=service
10.255.255.25  Ready   node   11d  v1.23.5  node-pool=runtm_5 tier=service
..
```

