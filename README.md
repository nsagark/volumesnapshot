# volumesnapshot



To use the snapshot functionality of the Amazon EBS CSI driver, you must install the external snapshotter before the installation of the EBS CSI driver. The external snapshotter components must be installed in the following order:
* [CustomResourceDefinition](https://github.com/kubernetes-csi/external-snapshotter/tree/master/client/config/crd) (CRD) for volumesnapshotclasses, volumesnapshots, and volumesnapshotcontents
* [RBAC](https://github.com/kubernetes-csi/external-snapshotter/blob/master/deploy/kubernetes/snapshot-controller/rbac-snapshot-controller.yaml)
* [controller deployment](https://github.com/kubernetes-csi/external-snapshotter/blob/master/deploy/kubernetes/snapshot-controller/setup-snapshot-controller.yaml)
* [VolumeSnapshotClass](https://gist.github.com/nsagark/be1c0a64bc7b2d44080dd9c6af4a53e6)

This repo consists of the files needed for deploying the CRD's, CR, RBAC, volumesnapshotclass nd the controller deployment. To deploy these components, create a git app in Nirmata and point it to this git repo. The git app in Nirmata needs to be deployed in the kube-system namespace

 
