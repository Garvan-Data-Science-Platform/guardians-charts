# GUARDIANS

This is a helm chart that combines one or more GUARDIANS products along with nginx-ingress and cert manager to handle ingress and ssl certificates.

The goal is to offer an off-the-shelf, production-grade, opinionated deployment option that can be used on-prem on in the cloud.

## Installation

`helm install my-release oci://australia-southeast1-docker.pkg.dev/dsp-registry-410602/garvan-public/guardians`

## Values

To deploy Elsa and/or CTRL, set`ctrl.enabled` and `elsa.enabled`. Refer to the documentation of the respective helm charts [Elsa](../elsa) and [CTRL](https://github.com/Garvan-Data-Science-Platform/ctrl/tree/main/.helm/ctrl) for values.

Most values can be left as default, with the exception of:
`elsa.ingress.hosts.host`, `ctrl.userClient.hostname`, `ctrl.adminClient.hostname`, `ctrl.ingress.hosts`, which should match the urls that have been set up.
`elsa.config` should also be set.
