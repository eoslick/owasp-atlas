# Vulnerability Atlas

An interactive security reference that maps OWASP Top 10 vulnerability lists to 10 core flaw classes, providing architecture-aware defenses for modern applications.

**Live Site:** [vulnerability-atlas.true-positives.com](https://vulnerability-atlas.true-positives.com)

## Overview

The Vulnerability Atlas helps security professionals and developers understand how different vulnerability types relate to each other across multiple OWASP lists. Instead of treating each list in isolation, it identifies the underlying patterns that cause these vulnerabilities and provides targeted defenses based on where they appear in your architecture.

## Features

### OWASP List Coverage
- **OWASP Top 10 (Web Apps)** - A01 through A10
- **OWASP API Top 10** - API01 through API10
- **OWASP Top 10 for LLM Apps** - LLM01 through LLM10
- **OWASP Top 10 for Agentic Apps** - ASI01 through ASI10
- **OWASP Mobile Top 10** - M01 through M10
- **OWASP Kubernetes Top 10** - K01 through K10

### 10 Core Flaw Classes
Each vulnerability from the OWASP lists maps to one or more fundamental flaw classes:

| ID | Class | Description |
|----|-------|-------------|
| C01 | Control & Instruction Injection | Untrusted input becomes instruction/intent |
| C02 | Identity & Authorization Failure | Identity/scope binding fails |
| C03 | Trust Boundary & Confused Deputy | Trusted component misuses authority |
| C04 | Unsafe Execution & RCE | Untrusted content leads to execution |
| C05 | Untrusted State Persistence | Poisoned state persists and is reused |
| C06 | Supply Chain Compromise | Upstream artifacts are compromised |
| C07 | Communication Integrity Failure | Messages spoofed/replayed/downgraded |
| C08 | Failure Propagation & Blast Radius | Automation amplifies faults |
| C09 | Human Trust & Authority Exploitation | Humans manipulated into unsafe actions |
| C10 | Observability & Attribution Gaps | Poor logging/lineage obscures cause |

### Interactive Architecture Diagram
A visual representation of a modern application architecture showing:
- **Client Zone:** Mobile App, Web Client
- **Edge Zone:** Cloudflare/CDN, WAF, API Gateway
- **Runtime Zone:** Kubernetes Cluster, App Service Pods, Workers/Jobs, Agent/Orchestrator, Tools/Integrations
- **Data Zone:** Database, Cache, Vector DB/RAG, Logs/SIEM

Click any architecture node to see which flaw classes apply and get context-specific defense recommendations.

### Proactive Security Controls
Each flaw class includes recommended controls with detailed explanations:
- Parameterized queries and input validation
- Least privilege and per-action authorization
- Circuit breakers and rate limits
- SBOM/AIBOM for supply chain visibility
- Tamper-evident logging and end-to-end lineage
- And many more...

## Usage

1. **Select an OWASP list** from the dropdown to see its vulnerabilities
2. **Click any vulnerability** to see which core flaw classes it maps to
3. **Click a flaw class** to see all related vulnerabilities across lists
4. **Click architecture nodes** to see applicable flaws and defenses
5. **Multi-select** vulnerabilities or classes to see combined mappings

## Technology

Single-file HTML application with:
- No build process required
- No external JavaScript dependencies
- Responsive design for desktop and mobile
- CSS custom properties for theming

## License

This project is dual-licensed:

- **AGPL-3.0** for open source use
- **Commercial license** available for proprietary applications

See [LICENSE](LICENSE) for details.

## Author

Created by Evan Oslick

For commercial licensing inquiries: eoslick@snakeeeyessoftware.com
