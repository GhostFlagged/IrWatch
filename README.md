# IR Domains Archive

A curated archive of all .ir domains collected from Certificate Transparency logs.

## 📝 Purpose

The goal of this project is to collect all domains under the .ir TLD. Existing lists were expensive (ranging from $34 to $433), so I created this personal solution to collect, archive, and maintain the data myself.

This repository provides historical snapshots of .ir domains in JSON format, allowing easy tracking of newly issued domains over time.

## 📂 Contents

JSON files:
ir_domains_YYYYMMDD_HHMMSS.json

Each file is timestamped to track changes and monitor domain growth over time.

## 🚀 Use Cases & Practical Applications

This dataset is especially useful for threat hunting, attack surface discovery, and bug bounty automation.

By leveraging Certificate Transparency logs, we can detect newly issued SSL/TLS certificates and extract fresh .ir domains as soon as they appear. These newly created assets are often less hardened and more likely to contain misconfigurations or vulnerabilities.

A common workflow using this data includes:

Continuously collecting newly issued .ir domains from CT logs

Storing and tracking them over time to identify fresh assets

Running tools like httpx to gather metadata such as live hosts, technologies, and server details

Filtering targets by technology (e.g., React, Next.js) to focus on assets affected by newly released CVEs

Using scanners like Nuclei to test for known vulnerabilities shortly after disclosure

This approach enables rapid response to newly published CVEs. When a vulnerability is disclosed, the dataset allows immediate identification of potentially affected assets, making it possible to start threat hunting early and assess real-world exposure before patches are widely applied.

In practice, this methodology has led to the discovery of vulnerable assets that had been deployed only days or weeks earlier, demonstrating the value of Certificate Transparency logs as an early-warning system for vulnerability discovery.

For a full step-by-step example of how to filter .ir domains from CertStream and turn them into actionable bug bounty findings, check out my blog post:
From Certificate Transparency Logs to Vulnerabilities

## 💻 How to Use

You can download the JSON files and:

Load them into scripts or applications

Import them into databases or analytics tools

Analyze domain growth and newly issued certificates over time

Example (Python)
import json

with open("ir_domains_20251229_214500.json") as f:
    data = json.load(f)
print(data[:10])

## 💡 Motivation

Existing .ir domain lists were costly and often incomplete.
This repository provides a free, continuously updated archive of .ir domains sourced directly from Certificate Transparency logs.

If you want, I can also rewrite the README in fully Markdown-optimized style for GitHub, with badges, tables of contents, and collapsible code blocks — this makes it look super professional.
