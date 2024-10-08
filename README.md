# :rocket: devops-accelerator-project

Welcome to the **DevOps Accelerator Project (DOAP)**. This repository helps you get your base infrastructure up and running quickly using well-known Terraform modules, GitOps blueprints, and tried-and-tested configurations for cloud automation, observability, alerting, and CI/CD.

## 📋 Project Overview

When starting a new project or startup, getting your cloud infrastructure, CI/CD pipelines, and GitOps automation in place can be overwhelming, especially with a small team. This project aims to simplify that process by providing scaffolding for:

- 🛠️ **Infrastructure as Code** using **Terraform**
- 🌐 **GitOps** integration with **ArgoCD**
- 🔍 **Observability** using popular tools
- 🧰 **CI/CD Pipelines** for seamless automation
- 📊 **Monitoring & Alerting** configuration
- 🧪 **Tested Configurations** from real-world experiences

## 🔥 Why DevOps Accelerator Project (DOAP)?

In today's fast-paced tech landscape, startups and projects are expected to scale quickly and efficiently. However, setting up the infrastructure needed to support such growth can be daunting, especially when:

- You have a small team or are a solo DevOps engineer.
- The demands of managing cloud infrastructure, CI/CD pipelines, GitOps, and observability often pull you in multiple directions.
- Time and resource constraints limit your ability to implement robust, scalable solutions from scratch.

## 🚀 Motivation

The **DevOps Accelerator Project (DOAP)** was born from the need to **simplify and streamline** the initial setup process for DevOps practices, allowing you to focus on building your product. We’ve encountered the same challenges—setting up everything manually takes time, effort, and can slow down progress. This project is designed to:

- **Accelerate** the process of getting your infrastructure up and running with minimal effort.
- **Standardize** the use of well-known and trusted Terraform modules and GitOps blueprints to ensure reliability and best practices.
- **Automate** the most time-consuming tasks in DevOps, like provisioning resources, monitoring, alerting, and configuring CI/CD pipelines, so you can focus on delivering features.
- **Empower** teams of any size to manage cloud infrastructure effortlessly by offering pre-built, reusable templates and configurations.

By leveraging this project, you'll gain a head start on all the essential infrastructure components needed to support modern applications, from deployment pipelines to cloud resources. We believe that automation should free you to innovate, not bog you down with repetitive configuration tasks.

## ✨ Features

This project aims to include a comprehensive set of tools and configurations to streamline DevOps processes. Here’s what you can expect:

### ⚙️ Development Environment
- **Tools Bootstrapping**: Bootstrap all the required software to your Laptop with Brewfile.
- **Local Development**: Develop locally using **Docker** and **[LocalStack](https://www.localstack.cloud/)** to simulate AWS services.
- **Preview Environments**: On-demand preview environments with the lifespan as long as your PR is open.
- **Version Control**: Centralized version control using **GitHub**.

### 🛠️ Infrastructure as Code (IaC)
- **Terraform**: Manage cloud infrastructure with **[Terraform](https://www.terraform.io/)** modules and configurations.
- **Infrastructure Deployment**: Automate infrastructure deployment via **[Atlantis](https://www.runatlantis.io/)** through pull requests.

### 🧑‍💻 Continuous Integration & Continuous Delivery (CI/CD)
- **CI with GitHub Actions**: Automate testing, linting, and build pipelines using **[GitHub Actions](https://github.com/features/actions)**.
- **CD with Argo CD**: Implement **GitOps** for continuous delivery of applications to Kubernetes clusters.

### 🚀 Application Deployment
- **Java Spring Boot Applications**: Build **Java Spring Boot** microservices with **Gradle**.
- **AWS EKS Deployment**: Deploy applications to **AWS EKS** clusters.
- **Container Management**: Build, tag, and push container images to **ECR** and manage them via **Helm Charts**.
  
### 🔐 Security
- **Security Scans**: Integrate security scanning tools like **[Trivy](https://github.com/aquasecurity/trivy)** for vulnerabilities in containers and **[Renovate](https://github.com/renovatebot/renovate)** for dependency management.

### 🔍 Observability & Monitoring
- **Observability Stack**: Integrated observability using **Prometheus**, **Grafana**, **Loki**, **Tempo**, and **OpenTelemetry** for monitoring, logging, tracing, and metrics.
- **Alerts**: Configure **Slack** alerts for system notifications and incidents.
- **Dashboards as Code**: Manage dashboard and alert configurations as code for reproducibility and version control.

### 🧪 Scalability & Performance
- **AutoScaling**: Scale your applications using **Karpenter** and **KEDA**.
- **Ingress Controllers**: Route traffic using **Ingress-Nginx** controllers.
- **Load Testing**: Perform load testing to ensure your applications can handle traffic under pressure.
- **Right-Sizing Pods**: Optimize your Kubernetes pods' resource requests and limits with [Goldilocks](https://github.com/FairwindsOps/goldilocks).

### 📦 Package & Helm Chart Management
- **Helm Charts**: Package and deploy applications using **Helm Charts**.
- **AWS Controllers for Kubernetes (ACK)**: Utilize **ACK Controllers** for managing AWS resources within Kubernetes via Helm charts.

## 🧱 Repository Structure

Here's a quick breakdown of the repository:

- **`.github/workflows/`**: 🛠️ CI/CD pipelines using GitHub Actions.
- **`argocd/`**: 🌐 ArgoCD configuration for GitOps, including app definitions and cluster configs.
- **`terraform/`**: 📦 Terraform modules and environment configurations to automate infrastructure provisioning.
- **`docs/`**: 📖 Documentation to guide users through setup, configuration, and troubleshooting.

```bash
.
├── .github/
│   └── workflows/        # CI/CD pipeline configuration (e.g., GitHub Actions)
├── argocd/
│   ├── apps/             # ArgoCD apps to be deployed via GitOps
│   └── clusters/         # ArgoCD cluster configuration
├── terraform/
│   ├── modules/          # Reusable Terraform modules
│   └── environments/     # Environment-specific configurations (e.g., dev, prod)
├── docs/
│   └── index.md          # Website: Documentation for users
└── README.md             # Project overview
```

## 🚀 Quickstart

### 1. Clone the repository

```bash
git clone https://github.com/ruanbekker/devops-accelerator-project.git doap
cd doap
```

### 2. Provision Infrastructure

Navigate to the `terraform/environments/` folder for your environment (e.g., `dev`, `prod`) and apply the Terraform code:

```bash
cd terraform/environments/dev
terraform init
terraform apply
```

### 3. Set Up GitOps

- Review the **ArgoCD** apps in `argocd/apps/` and make adjustments for your environment.
- Deploy the applications via ArgoCD:

```bash
kubectl apply -f argocd/apps/
```

### 4. Configure CI/CD Pipelines

Make sure your workflows are defined in the `.github/workflows/` directory, and customize them to fit your environment.

## 📚 Documentation

Comprehensive documentation is available in the `docs/` folder. Check out the [docs](https://devops-accelerator-project.netlify.app/) for a full guide on setting up your infrastructure, GitOps processes, and CI/CD pipelines.

## 🤝 Contributing

Contributions are welcome! Feel free to open issues, submit PRs, and suggest improvements.

## 🚧 Project Status: Under Development 🚧

This project is currently **under development** and is not yet ready for production use. We are actively working on building the core features and refining the infrastructure setup.

Please feel free to explore the repository, but be aware that breaking changes may occur frequently. Contributions and suggestions are welcome as we progress!

## 📢 Spread the Word

Love what we're building with **DevOps Accelerator Project (DOAP)**? Help us spread the word! Share this project with your community and follow along as we build out the future of DevOps automation.

Feel free to use our hashtag: **#TheDoapProject** across your favorite social platforms!

Ways to Share:

- 🌍 [Twitter](): Share with the hashtag **#TheDoapProject**
- 💼 [LinkedIn](): Post about the project on LinkedIn
- 📧 [Email](): Send this repo link to a colleague or friend

Let's build an amazing DevOps community together!

## 📜 License

This project is licensed under the MIT License.

