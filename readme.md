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

trivy
 - code anaylsis?
crane
cosign

 steps:
  - clone repo
    - put secret to clone repo somewhere
  - trivy-scan-local-fs
  - build
  - test
  - kaniko build and push


kubectl create piplinerun-file.yml to create new pipeline