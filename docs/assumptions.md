# Assumptions and Formula Logic

This document summarizes the assumptions used in the Clara AWS cost optimization model.

## Baseline

| Item | Value |
|---|---:|
| Current AWS monthly spend | $250,000 |
| EC2 allocation | 40% |
| EBS allocation | 20% |
| RDS allocation | 15% |
| S3 allocation | 10% |
| EKS allocation | 10% |
| Lambda allocation | 5% |

## Formula Logic

| Metric | Formula |
|---|---|
| Service current cost | Total monthly spend × service allocation % |
| Estimated savings | Current service cost × optimization rate |
| Optimized cost | Current service cost - estimated savings |
| Total savings % | Total estimated savings / total current monthly spend |

## Conservative Assumptions

- EC2 savings are based on rightsizing, autoscaling, and selected commitment discounts.
- EBS savings are based on removal of unattached volumes, gp3 migration candidates, and snapshot lifecycle cleanup.
- S3 savings are based on lifecycle policies and transition of eligible data from S3 Standard to lower-cost storage classes.
- All recommendations require validation through AWS Cost Explorer, Cost and Usage Report, Compute Optimizer, CloudWatch metrics, and workload-owner approval.
