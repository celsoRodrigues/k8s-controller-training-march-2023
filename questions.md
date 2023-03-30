# Questions

- What component handles the lifecycle of a Node object?
    - Kubelet can create Node objects. Or they can be created out of band.
    - The Node Controller is responsible to deleting Node objects for VMs that no longer exist in the cloud provider.
- Are objects persisted and then broadcasted or visa versa?
    - Etcd's built in watch mechanisms are used to serve watches.
    - So: Persistence, then watch broadcast.

## Future Followup Questions

- If a client requests a watch and the connection is severed is there a way it can re-attach to ensure it has missed nothing?