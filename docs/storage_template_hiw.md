---
title: "Storage Templates"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/storage_template_hiw.html"
last_updated: "1/13/2026"
product_version: "8.0.1.202"
---

# Storage Templates


A storage template is a collection of settings that allows you to define target locations for backups and archived backups. A target location is a repository where an SLA-based backup policy stores restore points; it can be the same repository for all Azure regions protected by the policy, or you can specify separate repositories for each region.

Using region-specific repositories allows you to avoid cross-region transaction costs associated with data transfer between Azure regions during backup and archive operations, while using a single default repository may help you ensure data protection regardless of the source location.

Related Topics

[Adding Storage Templates](storage_add.md)


