---
title: "Creating Grafana Alerts for High Pod Memory Usage"
datePublished: Wed Jul 23 2025 00:00:00 GMT+0000 (Coordinated Universal Time)
cuid: cmdhmgyzf000s02l72px5bw1g
slug: creating-grafana-alerts-for-high-pod-memory-usage
tags: computers

---

# Creating Grafana Alerts for High Pod Memory Usage

*July 23, 2025*

The blog post explains how to create a Grafana alert for monitoring pod memory usage:

## Key Points

* Use resource `requests` as the memory threshold
    
* Query to calculate memory percentage:
    
    ```plaintext
    (sum(container_memory_usage_bytes{namespace="<my-namespace>", container="<my-container-name>"}) by (pod) / sum(kube_pod_container_resource_requests{exported_namespace="<my-namespace>", container="<my-container-name>", resource="memory"}) by (pod)) * 100
    ```
    
* Set alert threshold at 80% of allocated memory
    

## Rationale

The author chooses to use `requests` instead of `limits` because they "want to know when a pod is getting close to the amount of memory I have allocated for it."

*Labels: Computers*