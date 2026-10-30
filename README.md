# Awesome FinOps

A curated catalog of **practical FinOps** tools and frameworks for cloud cost — visibility, allocation, Kubernetes spend, IaC estimates, and adjacent carbon metrics.

Inspired by how [awesome-x402](https://github.com/Audie-glitch/awesome-x402) keeps rows short and honest. **Not** a scrape of [jmfontaine/awesome-finops](https://github.com/jmfontaine/awesome-finops) or [LeanerCloud/awesome-finops](https://github.com/LeanerCloud/awesome-finops). Every blurb here is original. Prefer open source; SaaS is labeled clearly. No vendor spam dumps.

PRs welcome: one link + 1–2 sentences you wrote. No star-farming.

## Index

- [Specs & foundations](#specs--foundations)
- [Cost visibility / allocation](#cost-visibility--allocation)
- [Kubernetes cost](#kubernetes-cost)
- [IaC cost estimate](#iac-cost-estimate)
- [Carbon / sustainability](#carbon--sustainability)
- [Learning & communities](#learning--communities)
- [Contributing](#contributing)

## Specs & foundations

| Link | Notes |
|------|--------|
| [FinOps Foundation](https://www.finops.org/) | Linux Foundation home for the FinOps practice — framework, working groups, community |
| [FinOps Framework](https://www.finops.org/framework/) | Operating model: personas, phases, domains, capabilities (updated for 2026 scope) |
| [Framework principles](https://www.finops.org/framework/principles/) | Shared “teams need to see real-time data / everyone takes ownership” ground rules |
| [FOCUS](https://focus.finops.org/) | FinOps Open Cost & Usage Spec — normalize multi-vendor bills into one schema |
| [FOCUS Spec (GitHub)](https://github.com/FinOps-Open-Cost-and-Usage-Spec/FOCUS_Spec) | Spec source + versioned docs for implementers and exporters |

## Cost visibility / allocation

Open source first. Native cloud consoles are free with the account; third-party SaaS is called out.

| Link | Kind | Notes |
|------|------|--------|
| [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) | Native | First pane for AWS trends, filters, and forecasts — start here before buying a platform |
| [Azure Cost Management](https://learn.microsoft.com/en-us/azure/cost-management-billing/) | Native | Budgets, exports, and allocation views for Azure / Microsoft billing |
| [Google Cloud cost management](https://cloud.google.com/cost-management) | Native | Billing export, budgets, and cost reports for GCP projects |
| [Cloud Custodian](https://cloudcustodian.io/) | OSS | YAML policy engine to find idle waste and enforce cleanup across clouds |
| [cloud-custodian/cloud-custodian](https://github.com/cloud-custodian/cloud-custodian) | OSS | Upstream repo — policies for cost, compliance, and governance |
| [Steampipe](https://steampipe.io/) | OSS | SQL over cloud APIs; Cost Explorer tables for ad-hoc spend queries |
| [Powerpipe](https://powerpipe.io/) | OSS | Dashboards-as-code on top of Steampipe mods (security + cost views) |
| [instances.vantage.sh](https://instances.vantage.sh/) | OSS data | EC2 / RDS instance catalog with pricing — fork of ec2instances.info |
| [vantage-sh/ec2instances.info](https://github.com/vantage-sh/ec2instances.info) | OSS | Source for the instance/pricing browser above |
| [AWS Cloud Intelligence Dashboards](https://www.wellarchitectedlabs.com/cloud-intelligence-dashboards/) | OSS (AWS) | Deployable CUDOS / CID stacks that turn CUR into executive-ready views |
| [OptScale](https://github.com/hystax/optscale) | OSS | Self-hostable FinOps + MLOps cost platform (Hystax); SaaS option exists |
| [Vantage](https://www.vantage.sh/) | SaaS | Multi-cloud cost UI with clean reports; free tier for smaller footprints |
| [VPSLedger](https://vpsledger.pages.dev/) | Free web + OSS data | VPS true-cost comparison (list price plus IPv4, backups and egress) with sourced dated prices and open JSON (CC BY 4.0) |
| [CloudZero](https://www.cloudzero.com/) | SaaS | Unit-cost / “cost as a product metric” framing beyond raw bills |
| [IBM Cloudability](https://www.apptio.com/products/cloudability/) | SaaS | Enterprise multi-cloud FinOps reporting under Apptio / IBM |
| [Finout](https://www.finout.io/) | SaaS | Virtual tagging and allocation when real tags are messy |
| [nOps](https://www.nops.io/) | SaaS | AWS-heavy automation (commitments, waste, k8s) — share-of-savings model |

## Kubernetes cost

| Link | Kind | Notes |
|------|------|--------|
| [OpenCost](https://opencost.io/) | OSS (CNCF) | Vendor-neutral K8s + cloud cost allocation API; Prometheus-friendly |
| [opencost/opencost](https://github.com/opencost/opencost) | OSS | Allocation engine + REST API — start here if you want primitives, not a product |
| [opencost/opencost-ui](https://github.com/opencost/opencost-ui) | OSS | Optional web UI for OpenCost |
| [IBM Kubecost](https://www.apptio.com/products/kubecost/) | Free tier + SaaS/enterprise | Product built on OpenCost: dashboards, multi-cluster, governance |
| [Karpenter](https://karpenter.sh/) | OSS | Just-in-time node provisioning — cuts idle capacity vs static node groups |
| [CAST AI](https://cast.ai/) | SaaS | Automated K8s rightsizing / bin-packing; evaluate against your risk tolerance |

## IaC cost estimate

Shift-left: see spend impact in PRs before `apply`.

| Link | Kind | Notes |
|------|------|--------|
| [Infracost](https://www.infracost.io/) | OSS CLI + SaaS | Cost diffs for Terraform / Terragrunt / CloudFormation / CDK in CI and editors |
| [infracost/infracost](https://github.com/infracost/infracost) | OSS | CLI + core engine; Cloud product adds policies, guardrails, team dashboards |

## Carbon / sustainability

Short adjacent list — carbon often tracks the same waste FinOps already hunts.

| Link | Kind | Notes |
|------|------|--------|
| [Cloud Carbon Footprint](https://www.cloudcarbonfootprint.org/) | OSS | Multi-cloud energy / CO₂e estimates from utilization (Thoughtworks origins) |
| [cloud-carbon-footprint](https://github.com/cloud-carbon-footprint/cloud-carbon-footprint) | OSS | CLI + dashboard apps; methodology docs on the project site |
| [FinOps Framework — Sustainability](https://www.finops.org/framework/) | Spec | Sustainability sits as a Framework capability alongside usage optimization |

## Learning & communities

| Link | Notes |
|------|--------|
| [Training & certification](https://www.finops.org/training-certification/) | FinOps Foundation Practitioner / Professional paths and FAQs |
| [Community Slack](https://www.finops.org/community/community-slack/) | Member Slack — practice channels, working groups (membership required) |
| [FinOps community hub](https://www.finops.org/community/) | Events, meetups, how to participate |
| [r/FinOps](https://www.reddit.com/r/FinOps/) | Public practitioner Q&A without a vendor pitch deck |
| [Cloud FinOps (book)](https://www.amazon.com/dp/1098117235) | Storment & Fuller — still the common onboarding text |
| [AWS Well-Architected Cost labs](https://www.wellarchitectedlabs.com/cost-optimization/) | Hands-on CUR queries, CFM playbooks, cost pillar exercises |
| [Last Week in AWS](https://www.lastweekinaws.com/) | Sharp cost / billing commentary (newsletter + podcasts) |
| [Duckbill Group](https://www.duckbillhq.com/) | Independent AWS cost consulting — useful essays, not a tool |

## Contributing

1. PR = one live URL + a short blurb **you** wrote.
2. Prefer tools you have run (or docs that clearly show how to run them).
3. Label **SaaS** vs **OSS** honestly. No paid starring, no dumping other awesome lists, no fake badges.
4. Skip pure marketing pages with no product or open source behind them.

## License

List text: [CC0 1.0](./LICENSE). Linked projects keep their own licenses.
