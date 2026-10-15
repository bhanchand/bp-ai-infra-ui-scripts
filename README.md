# Google Cloud AI Infrastructure UI Suite (`bp-ai-infra-ui-scripts`)

A curated collection of interactive, client-side web applications and visual architects designed for planning, configuring, and provisioning Google Cloud AI Hypercomputer infrastructure, high-performance computing (HPC) clusters, scientific landing zones, capacity reservation strategies, and enterprise identity federation.

All tools are standalone HTML/JS applications with zero external backend dependencies—they can be opened directly in any modern web browser or served locally.

---

## 🚀 Quick Start

### 1. View in Browser
Open `index.html` directly in your favorite browser:
```bash
open index.html
```

Or start a local HTTP server:
```bash
# Python 3
python3 -m http.server 8080

# Or Node.js
npx serve .
```
Navigate to [http://localhost:8080](http://localhost:8080).

---

## 📦 Included Tools & Architecture Guides

| Tool | File | Focus Areas |
| :--- | :--- | :--- |
| **Cluster Toolkit Blueprint Generator** | [`cluster-toolkit-ui.html`](cluster-toolkit-ui.html) | Slurm on GCP, GKE AI Hypercompute, Cloud Batch, Lustre, Parallelstore, Filestore, TPU/GPU shapes (`ANY_SINGLE_ZONE` guardrails), automated deployment scripts |
| **DWS Flex-Spray Script Architect** | [`flex-spray.html`](flex-spray.html) / [`gpu-spray-generator.html`](gpu-spray-generator.html) | Dynamic Workload Scheduler (DWS) Flex-Start multi-zone capacity spraying, automatic loser cancellation, H100 / A100 / L4 provisioning |
| **DWS Flex Reservation Architect** | [`dws-reservation.html`](dws-reservation.html) | DWS Calendar & Flex reservation planning, Slurm partition config, GKE Kueue integration, slot alignment & capacity hunting |
| **Colab Enterprise & Workbench Architect** | [`colab-workbench.html`](colab-workbench.html) | GCP Colab Enterprise runtimes, Vertex AI Workbench instances, custom GPU shapes, VPC Service Controls, persistent disks |
| **Fast Science Landing Zone Builder** | [`fast-science-builder.html`](fast-science-builder.html) | Research computing landing zones, production Terraform modules, VPC security layouts, research compliance regimes |
| **Fast Science Datasets Hub** | [`fast-science-datasets.html`](fast-science-datasets.html) | Scientific data ingestion, Storage Transfer Service (STS) orchestration, AlphaFold / TCGA / PDB mirroring to GCS buckets |
| **Cloud Identity vs. WIF Architect** | [`gcp-identity.html`](gcp-identity.html) | Enterprise identity federation, Cloud Identity vs. Workforce Identity Federation (WIF) decision trees, SAML/OIDC setup, CEL attribute mappings, IAM policy generator |

---

## 🛠️ Tool Highlights

### 1. [Cluster Toolkit Blueprint Generator](cluster-toolkit-ui.html)
- **Multi-Orchestrator Support**: Configure Slurm clusters, GKE AI Hypercomputer topologies, or Cloud Batch environments.
- **Hardware Placement Safeguards**: Enforces Google Cloud's `ANY_SINGLE_ZONE` distribution requirement for Cloud TPUs (`v5p`, `v6e`) and clustered GPUs (A3 Mega, A3 High, A4), preventing `CODE_GCE_CONDITION_NOT_MET` errors.
- **High-Performance Storage**: Integrates Managed Lustre, Parallelstore, and Filestore CSI drivers.
- **One-Click Exports**: Generates ready-to-deploy `gcluster` YAML blueprints, deployment scripts, and teardown runbooks.

### 2. [DWS Flex-Spray Script Architect](flex-spray.html)
- **Multi-Zone Concurrency**: Submits simultaneous provisioning requests across candidate zones for scarce accelerator hardware.
- **Automated Loser Cancellation**: Monitors active requests in real-time, detecting when a zone wins capacity and immediately cleaning up trailing pending requests.
- **Cost Protection**: Eliminates orphaned instances and prevents over-allocation billing.

### 3. [DWS Flex Reservation Architect](dws-reservation.html)
- **Slurm & GKE Kueue Alignment**: Builds configurations for both Slurm partition schedulers and Kubernetes Kueue resource flavors.
- **Reservation Lifecycle Modeling**: Previews active reservation windows, lead-time requirements, and preemption policies.

### 4. [Colab Enterprise & Vertex AI Workbench Architect](colab-workbench.html)
- **Interactive Sizing & Pricing**: Balances vCPU, RAM, GPU accelerators (L4, A100, H100), and boot disk sizing.
- **Security & Networking**: Configures private VPC peering, Shared VPC, disabling public IPs, and custom service accounts.
- **Generated Deployment Shell Scripts**: Generates `colab-workbench-setup.sh` executable via Google Cloud Shell or Cloud SDK.

### 5. [Fast Science Landing Zone Builder](fast-science-builder.html)
- **Modular Infrastructure**: Produces clean Terraform modules for scientific research environments on GCP.
- **Compliance Regimes**: Adapts network topologies and logging sinks to match HIPAA, FedRAMP, or institutional data governance rules.

### 6. [Fast Science Datasets Workbench](fast-science-datasets.html)
- **Public Science Data Caching**: Streamlines mirroring of large public biological and physical science repositories.
- **Automated Transfer Service (STS)**: Generates one-off or scheduled sync jobs with IAM service account binding.

### 7. [Cloud Identity vs. Workforce Identity Federation (WIF)](gcp-identity.html)
- **Comprehensive Decision Tree**: Direct architectural evaluation between creating Google Cloud Identity accounts vs. federating third-party IdPs (Okta, Microsoft Entra ID, Ping Identity) directly via WIF.
- **SAML 2.0 & OIDC Step-by-Step Guides**: Full configuration walkthroughs with simulated token payloads and CEL expression evaluators.

---

## 📄 License

Apache License 2.0. Designed for use with Google Cloud AI Hypercomputer and infrastructure solutions.
