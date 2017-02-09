# Deployment of GlusterFS on a kubernete cluster. 

The document describes the procedure to deploy glusterFS across a cluster. GlusterFS needs to access block device on the cluster. For manipulation of block device, please refer to [Partition.md](Partition.md). 

1. When start a glusterFS cluster, please use command:
  ```
  deploy.py glusterFS start [param]
  ```
  The parameter can be a number, which simply translates into /dev/[s|h]d[^a][number], and will install the glusterFS on all #number partition of disk other than the system disk (/dev/sda or /dev/hda). 