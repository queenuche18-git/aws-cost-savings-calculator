# AWS Cost Savings Calculator ☁️💰
This repository documents a technical case study on optimizing AWS foundational costs for single-server applications.
## 📊 Optimization Results
By analyzing the AWS Pricing Calculator, I identified a path to reduce recurring monthly costs by **60%**.
* **Initial Estimate:** $19.05 USD/month
* **Optimized Estimate:** $7.73 USD/month
### 🛠️ Strategic Changes Made:
* **Compute:** Switched to the ARM-based **t4g.nano** instance (more cost-efficient than standard x86).
* **Storage:** Upgraded from **gp2** to **gp3** volumes, which offers a lower price point and better performance.
## 🔗 Community Context
I shared these findings on LinkedIn to help other students realize that cloud learning doesn't have to be expensive. I also feel encouraged to document this properly here on GitHub
Original Post: https://www.linkedin.com/posts/uche-queeneth_rounding-up-this-week-i-just-finished-wrestling-activity-7387879769855467520-_0FQ?utm_source=share&utm_medium=member_android&rcm=ACoAAFRaoPcBs9Vra7L-XZH7JSIpFesxENBYj2w
## 🔍 Technical Assumptions & Architectural Context
To address performance and instance adequacy:

* **Baseline Choice:** The original estimate used a **t2.micro** instance, as it is the standard entry point for many beginners.
* **Instance Adequacy:** The move to **t4g.nano** (2 vCPUs, 0.5 GiB RAM) leverages the **AWS Graviton2** processor. For foundational, low-traffic workloads, the t4g series offers superior price-performance compared to older x86-based t2 instances.
* **Storage Performance:** Switching from **gp2 to gp3** decouples IOPS from storage size. This ensures a baseline of 3,000 IOPS even at small volumes, so performance is not sacrificed for cost
