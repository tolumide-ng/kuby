### Notes
Dynamic provisioning flow look like this:
1. User creates a StorageClass (defines "how" to provision storage)
2. User creates a PVC referencing that(the) StorageClaim
3. Kubernetes dynamically provisions a PV using the parameters and binds it to the PVC
4. The Pod mounts the PVC and uses the volume
5. When the PVC is deleted, the PV is handled according to the reclaim policy


StorageClasses help in dynamic volume provisioning and bring automation, flexibility, and standardization to Kubernetes storage management, making persistnet storage truly dynamic, scalable, and cloud native.




#### To Summarize
- PersistentVolumes (PVs) abstract the underlying storage infrastructure, providing a consistent and unified interdace