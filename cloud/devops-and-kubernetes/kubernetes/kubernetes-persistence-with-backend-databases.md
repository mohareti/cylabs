# Kubernetes Persistence with Backend Databases

##

In Kubernetes, maintaining persistence for backend databases even after restarting or recreating application pods is crucial for stateful applications like databases, where data must persist beyond the lifecycle of individual pods. Kubernetes achieves this through persistent volumes (PVs) and persistent volume claims (PVCs).

### Understanding Persistent Volumes (PV) and Persistent Volume Claims (PVC)

#### Persistent Volumes (PV)

* **PVs** are cluster resources that provide storage independent of the pod lifecycle. They are provisioned by administrators or dynamically provisioned using Storage Classes.
* PVs can represent storage from various underlying storage systems like NFS, iSCSI, or cloud storage services like AWS EBS, Azure Disk, or Google Persistent Disk.

#### Persistent Volume Claims (PVC)

* **PVCs** are requests for storage by a user. Pods use PVCs as volumes. A PVC specifies the size of the volume, access modes (like read/write), and can optionally request a specific storage class.
* When a PVC is created, it is automatically bound to a suitable PV in the cluster. If no PVs are available, and dynamic provisioning is configured, a new PV is created according to the storage class specified.

### How Kubernetes Maintains Data Persistence

When a database pod in Kubernetes needs to store data persistently, it uses a PVC to request storage. Here’s how the process works:

1. **Creating a PV**: An administrator provisions a chunk of storage in the cluster by creating a PV. Alternatively, a Storage Class is defined for dynamic provisioning.
2. **Defining a PVC**: The database deployment defines a PVC that requests a specific size and access mode for storage.
3. **Binding PV and PVC**: Kubernetes binds the PVC to an available PV. If dynamic provisioning is set up, Kubernetes automatically creates a PV matching the PVC’s requirements.
4. **Using PVC in Pods**: The database pod references the PVC in its volume configuration. Kubernetes mounts the bound PV at the specified mount path in the pod.
5. **Restarting/Recreating Pods**: When a database pod is restarted or recreated (maybe due to a deployment update or pod failure):
   * The PVC remains intact and is not deleted.
   * The new or restarted pod is once again bound to the same PVC, and therefore the same PV, ensuring that the data persists.
6. **Data Persistence**: As a result, the database retains its data across pod restarts and recreations, as the data is stored on the PV, which has a lifecycle independent of the individual pods.

### Example Scenario

Consider a PostgreSQL database running on Kubernetes:

* A PV is created, either manually or dynamically, representing a piece of storage on the cloud or on-premises.
* A PVC is defined in the PostgreSQL deployment YAML file, requesting storage of a certain size.
* The PostgreSQL pod uses this PVC as a volume.
* Even if the PostgreSQL pod is deleted, the PV and its data persist. When a new pod is created, it reattaches to the existing PVC, ensuring data continuity.

### Conclusion

Persistent Volumes and Persistent Volume Claims are key components in Kubernetes that enable stateful applications like databases to retain data across pod restarts or recreations. By abstracting the details of the underlying storage, Kubernetes provides a consistent and reliable way to handle persistent data, which is critical for applications that require stable and durable storage.
