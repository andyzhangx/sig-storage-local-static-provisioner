# Release notes for v2.9.0

[Documentation](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/tree/master/docs)

## Changes by Kind

### Feature

- feat(helm): add support for configurable health probes on the provisioner container ([#568](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/568), [@andyzhangx](https://github.com/andyzhangx))
- feat(helm): allow configuring the full container `securityContext` via Helm values ([#569](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/569), [@andyzhangx](https://github.com/andyzhangx))
- feat(helm): support `accessMode` setting in `storageClassMap` ([#531](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/531), [@dud225](https://github.com/dud225))
- feat: add taint remover support (`ProvisionerNotReadyNodeTaint`) so the provisioner can remove a startup node taint once discovery is ready ([#501](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/501), [@saidjawad](https://github.com/saidjawad))
- feat: allow configuring the `updateStrategy` for the DaemonSet ([#498](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/498), [@johngmyers](https://github.com/johngmyers))
- feat: use helm chart manifests in the e2e tests ([#561](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/561), [@asungur](https://github.com/asungur))

### Documentation

- docs(helm): add discovery directory documentation to Helm chart README ([#570](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/570), [@andyzhangx](https://github.com/andyzhangx))
- docs: refine README for improved formatting and readability ([#546](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/546), [@andyzhangx](https://github.com/andyzhangx))
- Update comments to drop very old Kubernetes version references ([#528](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/528), [@kylepl](https://github.com/kylepl))

### Bug or Regression

- fix: honor `stderrthreshold` when `logtostderr` is enabled and handle `flag.Set` errors ([#553](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/553), [@pierluigilenoci](https://github.com/pierluigilenoci))
- fix(helm): add missing permissions to the `chart-release` workflow ([#502](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/502), [@sheyabernstein](https://github.com/sheyabernstein))
- fix: pin GitHub Actions to exact SHAs ([#549](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/549), [@jsafrane](https://github.com/jsafrane))
- fix: CVE-2024-45310 ([#511](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/511), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2025-5187 ([#511](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/511), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2025-13281 ([#532](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/532), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2025-22868 ([#511](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/511), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2025-31133 ([#521](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/521), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2025-47914 ([#530](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/530), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2025-58181 ([#524](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/524), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2026-24051 ([#541](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/541), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2026-25680 ([#573](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/573), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2026-33186 ([#545](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/545), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2026-39883 ([#551](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/551), [@andyzhangx](https://github.com/andyzhangx))
- fix: CVE-2026-56852 ([#584](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/584), [@andyzhangx](https://github.com/andyzhangx))

### Other (Cleanup or Flake)

- cleanup: use Go 1.25 ([#542](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/542), [@andyzhangx](https://github.com/andyzhangx))
- chore: bump Go version to 1.25.10 in trivy workflow ([#559](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/559), [@andyzhangx](https://github.com/andyzhangx))
- chore: bump Go version to 1.25.11 in trivy workflow ([#567](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/567), [@andyzhangx](https://github.com/andyzhangx))
- chore: bump Go version to 1.25.12 in trivy workflow ([#580](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/580), [@andyzhangx](https://github.com/andyzhangx))
- test: fix CVE-2025-4673 in trivy action ([#500](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/500), [@andyzhangx](https://github.com/andyzhangx))
- test: fix CVE-2025-47907 trivy test failure ([#506](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/506), [@andyzhangx](https://github.com/andyzhangx))
- test: fix CVE-2025-47912 GitHub Action failure ([#519](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/519), [@andyzhangx](https://github.com/andyzhangx))
- test: fix trivy CVE-2025-61727 ([#529](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/529), [@andyzhangx](https://github.com/andyzhangx))
- test: fix CVE-2025-61726 trivy failure ([#538](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/538), [@andyzhangx](https://github.com/andyzhangx))
- test: fix trivy CVE-2025-68121 failure ([#539](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/539), [@andyzhangx](https://github.com/andyzhangx))
- test: fix CVE-2026-25679 in trivy action ([#544](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/544), [@andyzhangx](https://github.com/andyzhangx))
- fix: use `go install` with latest tag on kubetest2 installer ([#515](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/515), [@asungur](https://github.com/asungur))
- fix: update example to use the correct tag on `startup-script` ([#513](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/513), [@asungur](https://github.com/asungur))
- e2e: create PVC within the memory limit and make GCE default IP quota compatible ([#526](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/526), [@asungur](https://github.com/asungur))
- security: update trivy-action to use SHA for v0.35.0 ([#547](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/547), [@Priyankasaggu11929](https://github.com/Priyankasaggu11929))
- helm release v2.8.0 ([#495](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/495), [@Doritanh](https://github.com/Doritanh))

### GitHub Actions / Dependencies

- chore(deps): bump actions/setup-python from 5.5.0 to 5.6.0 ([#497](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/497), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/checkout from 4 to 5 ([#507](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/507), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump azure/setup-helm from 4.3.0 to 4.3.1 ([#508](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/508), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/setup-go from 5 to 6 ([#509](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/509), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/setup-python from 5.6.0 to 6.0.0 ([#510](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/510), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump github/codeql-action from 3 to 4 ([#516](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/516), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump helm/kind-action from 1.12.0 to 1.13.0 ([#518](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/518), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump helm/chart-testing-action from 2.7.0 to 2.8.0 ([#520](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/520), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/checkout from 5 to 6 ([#523](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/523), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/setup-python from 6.0.0 to 6.1.0 ([#527](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/527), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/setup-python from 6.1.0 to 6.2.0 ([#537](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/537), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump helm/kind-action from 1.13.0 to 1.14.0 ([#540](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/540), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump azure/setup-helm from 4.3.1 to 5.0.0 ([#548](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/548), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump helm/chart-releaser-action to `cae68fe` ([#550](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/550), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump github/codeql-action from 4.35.1 to 4.35.2 ([#552](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/552), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump aquasecurity/trivy-action from 0.35.0 to 0.36.0 ([#554](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/554), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump github/codeql-action from 4.35.3 to 4.35.4 ([#558](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/558), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump github/codeql-action from 4.35.4 to 4.35.5 ([#560](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/560), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump github/codeql-action from 4.35.5 to 4.36.0 ([#562](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/562), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/checkout from 6.0.2 to 6.0.3 ([#563](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/563), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump github/codeql-action from 4.36.0 to 4.36.2 ([#565](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/565), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/checkout from 6.0.3 to 7.0.0 ([#572](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/572), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump azure/setup-helm from 5.0.0 to 5.0.1 ([#574](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/574), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/setup-go from 6.4.0 to 6.5.0 ([#575](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/575), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/setup-python from 6.2.0 to 6.3.0 ([#576](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/576), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump github/codeql-action init+analyze from 4.36.2 to 4.36.3 ([#579](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/579), [@andyzhangx](https://github.com/andyzhangx))
- chore(deps): bump github/codeql-action init+analyze from 4.36.3 to 4.37.0 ([#583](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/583), [@andyzhangx](https://github.com/andyzhangx))
- chore: bump github/codeql-action to 4.37.1 ([#588](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/588), [@andyzhangx](https://github.com/andyzhangx))
- chore(deps): bump actions/setup-go from 6.5.0 to 7.0.0 ([#586](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/586), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/checkout from 7.0.0 to 7.0.1 ([#589](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/589), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump actions/setup-python from 6.3.0 to 7.0.0 ([#590](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/590), [@dependabot](https://github.com/apps/dependabot))
- chore(deps): bump github/codeql-action init+analyze from 4.37.1 to 4.37.2 ([#593](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/593), [@andyzhangx](https://github.com/andyzhangx))
- chore(deps): bump github/codeql-action init+analyze from 4.37.2 to 4.37.3 ([#596](https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner/pull/596), [@andyzhangx](https://github.com/andyzhangx))

## Dependencies

Notable Go module upgrades since v2.8.0:

- Go: 1.23 → 1.25
- k8s.io/{api,apimachinery,apiserver,client-go,component-base,kubernetes,pod-security-admission}: v0.29.14 → v0.32.10
- k8s.io/klog/v2: v2.110.1 → v2.140.0
- k8s.io/utils: 20230726 → 20241104
- sigs.k8s.io/yaml: v1.3.0 → v1.4.0
- github.com/onsi/ginkgo/v2: v2.13.0 → v2.21.0
- github.com/onsi/gomega: v1.29.0 → v1.35.1
- github.com/prometheus/client_golang: v1.16.0 → v1.19.1
- github.com/google/go-cmp: v0.6.0 → v0.7.0
- github.com/golang/glog: v1.1.2 → v1.2.5
- golang.org/x/sys: v0.31.0 → v0.46.0
- Added: helm.sh/helm/v3 v3.15.4, k8s.io/cli-runtime v0.32.10
- Removed: gopkg.in/yaml.v2 (replaced by sigs.k8s.io/yaml)
