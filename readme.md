## gitlab install
-   requires cert manager install as prerequisite
-   wait until cert manager running so webhook does not fail
-   set GL_OPERATOR version to 0.13.3
-   deploy gitlab cr mygitlab.yaml into gitlab-system namespace
- kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.10.1/cert-manager.yaml certmanager


## frsca
    - setup requires docker socker
    - setup requires jq
    - setup require cue

dev/prod env
    - cert-manager
    - registry
    - SPIFFE/Spire
    - Vault (hasicorp)
        - https://www.vaultproject.io/docs/

frsca:
    - tekton pipelines
    - tekton chains
    - kyverno

software supply chain
  - look at this

oci (open container initiatives)
  - look at this

trivy
 - code anaylsis?
crane
cosign

 steps:
  - clone repo
    - put secret to clone repo somewhere (vault)
  - trivy-scan-local-fs
  - build
  - test
  - kaniko build and push
  - syft SBOM scan


kyverno:
  - blocks images from running if not in list
  - kubectl describe cpol verify-image

  sigstore:
    - how to sign image?
    - uses cmd cosign

slsa.dev
  - look at this


kubectl create piplinerun-file.yml to create new pipeline