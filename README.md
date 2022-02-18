
# Contributing

This project welcomes contributions and suggestions. If you wonder what the Azure Container Compute team is working on, check out the [Project Board](https://github.com/Azure/container-compute-upstream/projects/1). If you would like to see the Azure Container Compute Upstream team work on something, first check if there is an [existing issue](https://github.com/Azure/container-compute-upstream/issues). If there isn't, please create a new one. If there is existing information elsewhere on the internet, please include the links.

This project is not setup for contributing code. It is intended only for tracking issues.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# Azure Container Compute Upstream Projects

This list of projects is maintained by the Azure container compute upstream team. This list is intended to help you make informed decisions about what projects to use (or not use) in the context of your goals (e.g. proof of concept vs. production). To make this decision you need to consider your goals, your need for formal support, the project's [maturity](#Maturity), governance, version level, and your willingness to work in open source.

## Support

Projects listed on this page are open source that Microsoft maintain or contribute to. These projects are [**NOT** covered by the Microsoft Azure support policy](https://support.microsoft.com/en-us/help/2941892/support-for-linux-and-open-source-technology-in-azure). To get help please search the open issues on the project using the links in the table. To communicate with the Azure Container Compute Upstream team please use the [issues](https://github.com/Azure/container-compute-upstream/issues) in this repo. If your issue isn't already represented, please open a new one. However, if you consume one of these projects as a part of a Microsoft or Azure product or service, you may be eligible for [support through that product or service](https://support.microsoft.com/en-us/hub/4343728/support-for-business).

## Project list

| Project Area | Project & (artifacts) | Goal | Project State & <br> API Version | Communication | Use on Azure |
|---|---|---|---|---|---|
| Kubernetes Cluster Management |  |  |  |  |
|  | [Cluster API Azure Provider](https://sigs.k8s.io/cluster-api-provider-azure) <br> ([releases](https://github.com/kubernetes-sigs/cluster-api-provider-azure/releases)) <br> [Tests](https://testgrid.k8s.io/sig-cluster-lifecycle-cluster-api-provider-azure) | Self-managed clusters on Azure using Cluster API | CNCF: incubating <br> API: v1alpha4 | [#cluster-api-azure](https://kubernetes.slack.com/archives/CEX9HENG7) <br> [kubernetes-sig-cluster-lifecycle@googlegroups.com](https://groups.google.com/forum/#!forum/kubernetes-sig-cluster-lifecycle) <br> [GitHub issues](https://github.com/kubernetes-sigs/cluster-api-provider-azure/issues) |  |
|  | [AKS Engine](https://github.com/Azure/aks-engine) <br> ([releases](https://github.com/Azure/aks-engine/releases)) | Self-managed clusters on Azure | Azure: winding down <br> API: N/A | [#aks-engine-users](https://kubernetes.slack.com/archives/CU3N85WJK) <br> [GitHub issues](https://github.com/Azure/aks-engine/issues) | <li>[Azure Stack Hub](https://docs.microsoft.com/en-us/azure-stack/user/azure-stack-kubernetes-aks-engine-overview)</li> |
| Kubernetes Enhancements |  |  |  |  |
|  | [Virtual Kubelet](https://github.com/virtual-kubelet/virtual-kubelet/) <br> ([releases](https://github.com/virtual-kubelet/virtual-kubelet/releases)) | Enable services to masquerade as kubelet - serverless | CNCF: sandbox <br> API: N/A | [#virtual-kubelet](https://kubernetes.slack.com/archives/C8YU1QP8W) <br> [GitHub issues](https://github.com/virtual-kubelet/virtual-kubelet/issues) | [AKS Virtual Nodes](https://docs.microsoft.com/en-us/azure/aks/virtual-nodes-cli) |
|  | [Windows containers](https://kubernetes.io/docs/setup/production-environment/windows/intro-windows-in-kubernetes/) <br> ([kubernetes releases](https://github.com/kubernetes/kubernetes/releases)) <br> [Tests](https://testgrid.k8s.io/sig-windows#aks-engine-azure-1-17-windows) | Run Windows server containers with Kubernetes | Kubernetes: stable <br> API: N/A | [#sig-windows](https://kubernetes.slack.com/archives/C0SJ4AFB7) <br> [kubernetes-sig-windows@googlegroups.com](https://groups.google.com/forum/#!forum/kubernetes-sig-windows) <br> [Windows Community Forum](https://discuss.kubernetes.io/c/general-discussions/windows) <br> [GitHub issues](https://github.com/kubernetes/kubernetes/issues?q=is%3Aissue+is%3Aopen+label%3Asig%2Fwindows+) | <li>[AKS Windows](https://docs.microsoft.com/en-us/azure/aks/windows-container-cli)</li><li>[AKS Engine Windows](https://github.com/Azure/aks-engine/blob/master/docs/topics/windows.md)</li> |
|  | [IPv4/v6 Dual-Stack](https://kubernetes.io/docs/concepts/services-networking/dual-stack/) <br> ([kubernetes releases](https://github.com/kubernetes/kubernetes/releases)) <br> [Tests](https://testgrid.k8s.io/provider-azure-dualstack) | IPv4/IPv6 dual-stack enables the allocation of both IPv4 and IPv6 addresses to Pods and Services. | Kubernetes: <br> IPv6: beta <br> Dual-stack: GA | [#sig-network](https://kubernetes.slack.com/archives/C09QYUH5W) <br> [kubernetes-sig-network@googlegroups.com](https://groups.google.com/forum/#!forum/kubernetes-sig-network) <br> [GitHub issues](https://github.com/kubernetes/kubernetes/labels/area%2Fipv6) | <li>[Use dual-stack with AKS Engine](https://github.com/Azure/aks-engine/tree/master/examples/dualstack)</li><li> [Use IPv6 with AKS Engine](https://github.com/Azure/aks-engine/tree/master/examples/ipv6) </li><li> [Use dual-stack with AKS](https://docs.microsoft.com/en-us/azure/aks/configure-kubenet-dual-stack) </li> |
| Cloud Native Governance and Security |  |  |  |  |
|  | [AAD Pod Identity](https://github.com/Azure/aad-pod-identity) <br> ([releases](https://github.com/Azure/aad-pod-identity/releases)) | Enables K8s applications to access cloud resources securely with Azure Active Directory | Azure: winding down <br> API: v1 | [GitHub issues](https://github.com/Azure/aad-pod-identity/issues) <br> [GitHub Project](https://github.com/Azure/aad-pod-identity/projects/3) | <li>[Use with AKS](https://docs.microsoft.com/en-us/azure/aks/developer-best-practices-pod-security#use-pod-managed-identities)</li><li>[Use with AKS Engine](https://github.com/Azure/aks-engine/tree/master/examples/addons/aad-pod-identity)</li> |
|  | [OPA Gatekeeper](https://github.com/open-policy-agent/gatekeeper) <br> ([releases](https://github.com/open-policy-agent/gatekeeper/releases)) | K8s native Open Policy Agent policy enforcement | CNCF: graduated <br> API: Config: v1alpha1; ConstraintTemplate: v1beta1; Constraints: v1beta1 | [#kubernetes-policy](https://openpolicyagent.slack.com/archives/CDTN970AX) <br> [GitHub issues](https://github.com/open-policy-agent/gatekeeper/issues) | <li>[Azure Policy for AKS](https://docs.microsoft.com/en-us/azure/governance/policy/concepts/rego-for-aks)</li><li>[Azure Policy for AKS Engine](https://docs.microsoft.com/en-us/azure/governance/policy/concepts/aks-engine)</li><li>[Azure Policy for Azure Arc connected clusters](https://docs.microsoft.com/en-us/azure/governance/policy/concepts/policy-for-kubernetes#install-azure-policy-add-on-for-azure-arc-enabled-kubernetes)</li> |
|  | [Secrets Store CSI Driver](http://sigs.k8s.io/secrets-store-csi-driver) <br> ([releases](https://github.com/kubernetes-sigs/secrets-store-csi-driver/releases)) <br> [Builds](https://testgrid.k8s.io/sig-auth-secrets-store-csi-driver) | Integrates secrets stores with Kubernetes via a [Container Storage Interface (CSI)](https://kubernetes-csi.github.io/docs/) volume | Kubernetes: GA <br> API: v1 | [#csi-secrets-store](https://kubernetes.slack.com/messages/csi-secrets-store) <br> [GitHub issues](https://github.com/kubernetes-sigs/secrets-store-csi-driver/issues) |  |
|  | [Azure KeyVault Provider for Secrets Store CSI Driver](https://github.com/Azure/secrets-store-csi-driver-provider-azure) <br> ([releases](https://github.com/Azure/secrets-store-csi-driver-provider-azure/releases)) | Enables mounting AKV secrets as volumes in K8s pods | Azure: GA <br> API: N/A | [GitHub issues](https://github.com/Azure/secrets-store-csi-driver-provider-azure/issues) | [Use with AKS](https://docs.microsoft.com/en-us/azure/aks/developer-best-practices-pod-security#use-azure-key-vault-with-secrets-store-csi-driver) |
|  | [KMS Plugin for Key Vault](https://github.com/Azure/kubernetes-kms) <br> ([releases](https://github.com/Azure/kubernetes-kms/releases)) | Enables encryption at rest of Kubernetes data in etcd using Azure Key Vault | Azure: incubation <br> API: N/A | [GitHub issues](https://github.com/Azure/kubernetes-kms/issues) | [Use with AKS Engine](https://github.com/Azure/aks-engine/blob/master/docs/topics/features.md#azure-key-vault-data-encryption) |
|  | [Azure Workload Identity](https://github.com/Azure/azure-workload-identity) <br> ([releases](https://github.com/Azure/azure-workload-identity/releases)) | Uses Kubernetes primitives to associate managed identities for Azure resources and identities in Azure Active Directory (AAD) with pods based on [Workload Identity federation](https://docs.microsoft.com/en-us/azure/active-directory/develop/workload-identity-federation) | Azure: incubation <br> API: N/A | [GitHub issues](https://github.com/Azure/azure-workload-identity/issues) | [How to use](https://azure.github.io/azure-workload-identity/docs/installation.html) |
| Cloud Native Service Mesh |  |  |  |  |
|  | [Service Mesh Interface (SMI) Spec](https://smi-spec.io/) | A standard interface for service meshes on Kubernetes | CNCF: sandbox <br> APIs: Traffic Access Control: v1alpha3; Traffic Metrics: v1alpha1; Traffic Specs: v1alpha4; Traffic Split: v1alpha4  | [#smi](https://cloud-native.slack.com/messages/smi) <br> [GitHub issues](https://github.com/deislabs/smi-spec/issues) |  |
|  | [Open Service Mesh (OSM)](https://openservicemesh.io/) | A lightweight, extensible, cloud native service mesh | CNCF: sandbox <br> APIs: N/A | [#openservicemesh](https://cloud-native.slack.com/archives/C018794NV1C) <br> [GitHub issues](https://github.com/openservicemesh/osm/issues) |  |
| Container Runtime |  |  |  |  |  |
|  | [Moby](https://github.com/moby/moby) <br> ([releases](https://github.com/moby/moby/releases)) | Toolkit for app containerization | Moby: ?? <br> API: N/A | [#opencontainers](https://opencontainers.slack.com/archives/C0LQVA03W) <br> [Moby Forums](https://forums.mobyproject.org/) <br> [GitHub issues](https://github.com/moby/moby/issues) | <li>[Azure Kubernetes Service](https://docs.microsoft.com/en-us/azure/aks/)</li><li>[Azure Stack Hub](https://docs.microsoft.com/en-us/azure-stack/user/azure-stack-kubernetes-aks-engine-overview)</li><li>many more</li> |
|  | [Containerd](https://github.com/containerd/containerd) <br> ([releases](https://github.com/containerd/containerd/releases)) | Complete container lifecycle management on Linux and Windows hosts | CNCF: graduated <br> API: N/A | [#opencontainers](https://opencontainers.slack.com/archives/C0LQVA03W) <br> [dev@opencontainers.org](https://groups.google.com/a/opencontainers.org/forum/#!forum/dev) <br> [GitHub issues](https://github.com/containerd/containerd/issues) | <li>[Use with AKS](https://docs.microsoft.com/en-us/azure/aks/cluster-configuration#container-runtime-configuration)</li><li>[Use with AKS Engine](https://github.com/Azure/aks-engine/blob/master/examples/kubernetes-containerd.json)</li> |
|  |  |  |  |  |  |

## Maturity

Open source project maturity can be assessed on many dimensions including age, number of contributors, diversity of contributor employers, and many more. Two you should consider are represented in the table as:

* Project state - The first entry in the Maturity column represents the project's status. Projects in the CNCF (kubernetes, kubernetes-sigs, prometheus, etc) use the [CNCF maturity model](https://github.com/cncf/toc/blob/master/process/graduation_criteria.adoc). Projects in the Azure, Microsoft, or deislabs GitHub orgs are working towards using the [guaduation guidelines](process/graduation_guidelines.md) defined in this repo. 
* [API or Feature Versions](https://kubernetes.io/docs/concepts/overview/kubernetes-api/#api-versioning) if relevant, are listed as the second entry of the Maturity column, and follow the Kubernetes convention except where noted
