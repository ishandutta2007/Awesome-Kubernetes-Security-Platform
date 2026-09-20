# Awesome-Kubernetes-Security-Platform

Top Kubernetes Security Platforms Ecosystem

Curated List of SaaS Products & Open-Source GitHub Projects
Focused on Container Security, Runtime Threat Detection, Posture Management & Supply Chain Security
Last updated: September 2026

This repository tracks notable SaaS platforms and open-source projects for Kubernetes Security. These tools help platform teams, security engineers, and DevOps practitioners protect containerized workloads across the build, deploy, and runtime phases—covering vulnerability scanning, configuration hardening, network policy enforcement, admission control, and real-time threat detection.

Examples include Aqua Security, Wiz, Palo Alto Prisma Cloud, Sysdig Secure, ARMO, Cast AI Security, Kubescape, NeuVector, Chainguard, Red Hat ACS, Snyk, Tigera Calico, StackRox, and Fairwinds Insights (the category leaders).

Open-source emphasis: This section is heavily expanded with every major active project for self-hosting, custom policy enforcement, and transparent security workflows—ideal for platform teams and security engineers who need deep visibility and control without vendor lock-in.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

Table of Contents

SaaS/Hosted Platforms

Open-Source GitHub Projects

How to Contribute

Disclaimer

SaaS/Hosted Platforms

Aqua Security
Enterprise CNAPP with the Aqua Enforcer runtime sensor (userspace + kernel-module hybrid). Notable for drift prevention and immutable container policies, with SOC 2 Type II certification. MalwareScan engine catches trojanized base images and crypto-miners.

Wiz
Cloud security platform with Kubernetes visibility via KBOM (Kubernetes Bill of Materials) and Network Graph. The Wiz Runtime Sensor provides eBPF-based detection. Wiz Admission Controller enforces policies before workloads reach production -
1
-
15
.

Palo Alto Prisma Cloud
Comprehensive CNAPP assembled from Twistlock and RedLock acquisitions. Provides Kubernetes CIS Benchmark checks with severity scoring, continuous image scanning, and deeper cluster awareness including CRI-O runtime mapping -
2
-
16
.

Sysdig Secure
CNAPP built by the creators of Falco. Deep runtime detection with eBPF instrumentation, syscall-level forensics, and managed Falco rule tuning. Host Shield and Cluster Shield consolidate runtime threat detection, vulnerability scanning, and KSPM -
3
.

ARMO Platform
Commercial platform built around Kubescape. Provides full workload inventory visibility with real-time security graph, application profiles, and runtime security posture integration -
4
.

Cast AI Security
Kubernetes cost optimization platform with built-in Security Insights. Powered by Kvisor, provides vulnerability scanning and compliance checks (running every 30–60 seconds) against Cast AI security benchmark with CVSS scoring -
5
-
19
.

Chainguard
Zero-CVE container images and FIPS-validated EKS add-ons for core cluster components (kube-proxy, CoreDNS, VPC CNI, EBS/EFS CSI drivers). Available through AWS Marketplace with drop-in compatibility -
6
.

Red Hat Advanced Cluster Security (ACS)
Kubernetes-native security platform powered by StackRox. Protects applications across build, deploy, and runtime with policy engine covering CIS, NIST, PCI, and DISA STIG. Available self-managed or as managed SaaS -
12
.

Snyk
Developer-first security platform with Kubernetes integration. The Snyk Controller scans running workloads for image vulnerabilities and configuration issues, with continuous monitoring and Slack/email notifications -
8
.

Tigera Calico Cloud
Commercial Kubernetes security platform built on Calico. Provides L7 network policy enforcement on eBPF dataplane, runtime threat detection, and compliance reporting. New Calico AI assistant and integrated Istio ambient mode -
9
.

Fairwinds Insights
Kubernetes security and governance platform with admission control policies, CVE auditing, and managed services dashboard. Allows per-cluster and org-wide admission settings for flexible policy enforcement -
10
.

StackRox
Kubernetes-native security platform (now Red Hat Advanced Cluster Security). Admission policy correlation bundled with OpenShift. Provides runtime threat detection and compliance controls.

Open-Source GitHub Projects

Kubescape
CNCF incubating project and the first Kubernetes security scanner to achieve CNCF status. Comprehensive lifecycle security: posture management, vulnerability scanning, hardening recommendations, and eBPF-based runtime threat detection via Inspektor Gadget. CLI tool + Kubernetes operator. ~18k stars. License: Apache-2.0 -
13
.

Falco
The CNCF graduated runtime security engine. Monitors syscalls and kernel events for anomalous behavior. Powerful rule language, extensive detection library, and broad community adoption. Detection-only—pair with Falcosidekick or SIEM for alerting. Apache-2.0.

Cilium Tetragon
eBPF-based security observability and runtime enforcement from the Cilium team (now Cisco). Deep kernel visibility with process-level enforcement via bpf_send_signal(). Strong synergy with Cilium networking. Apache-2.0.

KubeArmor
Runtime security enforcement system using LSMs (AppArmor, BPF-LSM) for workload hardening and least-permissive policies. Provides inline prevention—blocks actions before execution. Apache-2.0.

Tracee
Linux runtime security and forensics using eBPF from Aqua Security. Syscall tracing and Perf event analysis for detecting sophisticated attacks and eBPF-based malware. Apache-2.0.

Kubewarden
Kubernetes policy engine using WebAssembly. Supports context-aware policies that fetch information from the cluster at runtime (v1.6.0+), with RBAC-controlled read access to prevent abuse. CNCF project -
11
.

NeuVector
Full lifecycle container security platform (now SUSE Security). Runtime detection with process/file/network behavioral learning. Apache-2.0.

KubeCop
Runtime detection and response for malicious events in Kubernetes workloads from ARMO. Apache-2.0.

Trivy
Comprehensive security scanner for vulnerabilities, misconfigurations, secrets, and SBOMs. Widely used in CI/CD pipelines and Kubernetes admission controllers. Apache-2.0.

Kyverno
Kubernetes-native policy engine for admission control, mutation, validation, and generation. Declarative YAML policies without learning a new language. CNCF incubating project. Apache-2.0.

OPA Gatekeeper
Open Policy Agent admission controller for Kubernetes. Enforces policies using Rego language with constraint templates. CNCF graduated project. Apache-2.0.

Additional Strong Open-Source Options

eBPF Observability: Pixie (CNCF sandbox, eBPF-based Kubernetes observability), Inspektor Gadget (eBPF introspection tooling, powers Kubescape runtime detection) -
13
.

Container Scanning: Clair (CoreOS vulnerability scanner), Grype (Anchore vulnerability scanner), Syft (SBOM generation).

Admission Control: Kubewarden (WASM-based policies), Kyverno, OPA Gatekeeper.

Supply Chain: Cosign/Sigstore (image signing), in-toto (supply chain attestation), SLSA frameworks.

Reference Stack: The 2026 reference container security stack pairs Falco or Tetragon for runtime, Kyverno for admission, Trivy for scanning, and Sigstore/Cosign for signing.

Frameworks for building custom systems: Combine Kubescape for posture and runtime, Falco or Tetragon for detection, Kyverno for admission, Trivy for scanning, and Prometheus + Grafana for observability. Add Falcosidekick for alert routing and Slack/Teams for notifications.

How to Contribute

Fork the repo.

Add/edit entries in README.md (follow existing format).

Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

Submit PR with a short explanation.

Star the repo if you find it useful!

Disclaimer

This is a community-curated list — not exhaustive and not an endorsement.

Kubernetes security tools require kernel compatibility checks (eBPF vs kernel modules) and careful performance testing in production.

Detection-only tools (Falco, Tracee) do not block attacks — pair with enforcement tools (Tetragon, KubeArmor, Kyverno) for prevention.

Made for platform engineers, Kubernetes operators, security architects, and DevSecOps teams.
Let's make Kubernetes security more open, observable, and enforceable.
