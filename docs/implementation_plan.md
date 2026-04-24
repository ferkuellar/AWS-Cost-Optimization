# Implementation Plan

## Phase 1: Quick Wins — Weeks 1–2

- Validate and remove unattached EBS volumes.
- Review excessive snapshot retention.
- Identify idle and underutilized EC2 resources.
- Enable baseline AWS Budgets and anomaly detection.
- Review S3 buckets for lifecycle eligibility.

## Phase 2: Compute and Storage Optimization — Weeks 3–6

- Rightsize EC2 instances based on utilization data.
- Implement autoscaling for variable workloads.
- Review Savings Plans or Reserved Instance opportunities after rightsizing.
- Optimize EKS node groups using autoscaling or Karpenter.
- Apply S3 lifecycle policies and EBS snapshot governance.

## Phase 3: FinOps Governance — Ongoing

- Enforce tagging standards.
- Establish product/team cost ownership.
- Publish recurring cost reports.
- Integrate cost checks into CI/CD and IaC workflows.
- Track savings, utilization, budget variance, and tag compliance.
