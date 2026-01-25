---
title: "TPE-BFL:Training Parameter Encryption scheme for Blockchain based Federated Learning System"
authors: 
- me
- Qiwei Liang
- Lijie Hui
- Bofan Yang
- Chao Xu
- Jun Feng
- Yanxiang He
date: 2024-10-08T18:00:43+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2024-10-01T18:00:43+08:00

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Computer Networks,Volume 252,2024,110691"
publication_short: ""

abstract: Blockchain technology plays a pivotal role in addressing the single point of failure issues in federated learning systems, due to the immutable nature and decentralized architecture. However, traditional blockchain-based federated learning systems still face privacy and security challenges when transmitting training model parameters to individual nodes. Malicious nodes within the system can exploit this process to steal parameters and extract sensitive information, leading to data leakage. To address this problem, we propose a Training Parameter Encryption scheme for Blockchain based Federated Learning system (TPE-BFL). In TPE-BFL, the training parameters of the system model are encrypted using the paillier algorithm with the property of addition homomorphism. This encryption mechanism is integrated into the workflows of three distinct roles within the system:workers, validators, and miners. (1) Workers utilize the paillier encryption algorithm to encrypt training parameters for local training models. (2) Validators decrypt received encrypted training parameters using private keys to verify their validity. (3) Miners receive cryptographic training parameters from validators, validate them, and generate blocks for subsequent global model updates. By implementing the TPE-BFL mechanism, we not only preserve the immutability and decentralization advantages of blockchain technology but also significantly enhance the privacy protection capabilities during data transmission in federated learning systems. In order to verify the security of TPE-BFL, we leverage the semantic security inherent in the Paillier encryption algorithm to theoretically substantiate the security of our system. In addition, we conducted a large number of experiments on real-world data to prove the validity of our proposed TPE-BFL, and when 15% of malicious devices are present, TPE-BFL achieve 92% model accuracy, a 5% improvement over the blockchain-based decentralized FL framework (VBFL).

# Summary. An optional shortened abstract.
summary: ""

tags: 
- 论文
- federated learning
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

links:
  - type: pdf
    url: https://www.sciencedirect.com/science/article/pii/S1389128624005231

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
