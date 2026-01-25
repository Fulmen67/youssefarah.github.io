---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "BMSE:Blockchain-based multi-keyword searchable encryption for electronic medical records"
authors: 
- me
- Lin Shi
- Jun Zhang
- Chao Xu
- Yong Chen
- Yanxiang He
date: 2024-04-08T18:00:43+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2024-04-08T18:00:43+08:00

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Computer Standards & Interfaces,Volume 89,2024,103824"
publication_short: ""

abstract: The storage of electronic medical records (EMRs) is an area of extensive research, and healthcare systems often delegate this task to cloud service providers (CSP). Typically, CSP transmits the encrypted EMRs to a cloud server with a searchable encryption scheme for easy retrieval. However, the enormous power held by centralized CSP poses a potential threat to patients’ personal privacy, as it can lead to unauthorized access and misuse of medical data by both CSP and data users, such as doctors. This paper proposes a blockchain-based multi-keyword searchable encryption (BMSE) electronic medical record solution. The scheme consists of two parts. On the one hand, our solution involves the integration of blockchain technology and the utilization of advanced encryption standard (AES) for symmetric data encryption. Additionally, we employ attribute-based encryption (ABE) to encrypt the search index. This approach aims to address the issue of excessive power held by centralized CSP, which can potentially result in the compromise of patients’ privacy. On the other hand, we use the K-means algorithm to cluster the documents, and use the relevance score of keywords and documents as the search index to solve the problem of low efficiency of the existing multi-keyword searchable encryption schemes. Finally, we verify the safety of BMSE through safety analysis, and the experimental analysis shows that BMSE improves the search efficiency.

# Summary. An optional shortened abstract.
summary: ""

tags: 
- 论文
- Security
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
    url: "https://www.sciencedirect.com/science/article/pii/S0920548923001058"


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
