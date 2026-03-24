### PersistentVolumes(PV)
A PersistentVolume(PV) represents a piece of storage in the cluster that has been provisioned by an administrator (static provisioning) or dynmically through a StorageClass. It is an abstraction layer that hides the underlying storage technilify--Whether it is cloud disk, a newtwork file system, or a local disk on a node.



### PersistentVolumeClaims (PVC)
A PersistentVolumeClaim is a user's request for storage similar to how a Pod requests CPU and memory. It allows developers to specify the amount of storage, access mode, and optionally a StorageClass that describes the type or performance tier of the desired storage.
When a PVC is created, Kubernetes looks for an available PV that matches its request (based on size, access mode, and storage class), If such a PV exists, it is bound to the PVC. If not, and if a StorageClass is dfined, Kubernetes dynamically provisions a new PVthat satisifies the claim. Once bound, the PV is dedicated exclusively to that PVC until it is released.



### StorageClass
A storageClass in kubernetes defines how dynamic volume provisioning works within a cluster. In simple terms, it tells Kubernetes which type of storage to use, how to create it, and which parameters or performance tiers to apply when a Pod requests persistent storage.