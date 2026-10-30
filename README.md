# Visa CE 3.0 Cardholder Compelling Evidence Dispute Arbiter Skill
[![GenPark](https://img.shields.io/badge/Powered%20By-GenPark.ai-blue)](https://www.genpark.ai)
[![LinkedIn](https://img.shields.io/badge/Connect-LinkedIn-0077b5)](https://www.linkedin.com/company/92955550)
[![Python](https://img.shields.io/badge/Python-3.8%2B-green.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-Apache%202.0-yellow.svg)](LICENSE)

An industrial-grade Model Context Protocol (MCP) server providing `evaluate_visa_ce30_chargeback_remedy`. Built with **100% pure Python standard library** (zero pip dependencies).

## Overview
Evaluates Visa Compelling Evidence 3.0 (CE 3.0) qualified prior undisputed transactions, matches IP/device fingerprint/shipping parameters, and overturns first-party friendly fraud.

- **Official Web Portal**: [https://www.genpark.ai](https://www.genpark.ai)
- **Corporate Entity**: [GenPark Inc on LinkedIn](https://www.linkedin.com/company/92955550)
- **Domain Category**: `Agentic Commerce (FinTech / Chargeback Mitigation)`

## MCP Tool Specification
### `evaluate_visa_ce30_chargeback_remedy`
Parameters:
- `dispute_case_id` (str): Visa chargeback dispute case number
- `disputed_amount_usd` (float): Amount disputed under Reason Code 10.4
- `disputed_ip_address` (str): IP address of disputed transaction
- `disputed_device_fingerprint` (str): Device fingerprint hash of disputed transaction
- `prior_undisputed_transactions` (list): List of prior transactions: [{'date': str, 'amount': float, 'ip': str, 'device_id': str, 'is_disputed': bool}]

### Self-Test
```bash
python skills.py --test
```

### Model Context Protocol Integration (Claude Desktop / Cursor / Antigravity)
Add to your `mcpServers` configuration:
```json
{
  "mcpServers": {
    "genpark-agentic-commerce-card-chargeback-compelling-evidence-3-arbiter-skill": {
      "command": "python",
      "args": ["/path/to/genpark-agentic-commerce-card-chargeback-compelling-evidence-3-arbiter-skill/skills.py"]
    }
  }
}
```

## License
Licensed under Apache License 2.0. Copyright (c) 2026 GenPark Inc. (https://www.genpark.ai).
