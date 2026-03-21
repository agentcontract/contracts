# contracts

**Community contract library for [AgentContract](https://github.com/agentcontract/spec).**

Ready-to-use `.contract.yaml` files for common agent types. Pick one, adapt it, and enforce it on your agent in minutes.

[![Spec](https://img.shields.io/badge/spec-v0.1.0-orange)](https://github.com/agentcontract/spec/blob/main/SPEC.md)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue)](LICENSE)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen)](CONTRIBUTING.md)

---

## Use a Contract

```bash
pip install agentcontract
curl -O https://raw.githubusercontent.com/agentcontract/contracts/main/customer-support/basic.contract.yaml
```

```python
from agentcontract import load_contract, enforce

@enforce(load_contract("basic.contract.yaml"))
def run_agent(user_input: str) -> str:
    return my_llm.run(user_input)
```

---

## Available Contracts

| Category | Contract | Description |
|---|---|---|
| `customer-support/` | `basic.contract.yaml` | Tier-1 support agent, no PII, escalation policy |
| `coding-agent/` | `basic.contract.yaml` | Coding assistant with filesystem access |
| `research-agent/` | `basic.contract.yaml` | Research agent with citation requirements |
| `data-pipeline/` | `basic.contract.yaml` | Data processing agent with schema validation |
| `regulated/` | `gxp.contract.yaml` | GxP/pharma agent (21 CFR Part 11, GAMP5) |

*More contracts added weekly. [Submit yours.](#contributing)*

---

## Contributing

Submit a contract for any agent type:

1. Fork this repo
2. Create `<category>/<name>.contract.yaml`
3. Add a brief comment header explaining the use case
4. Open a PR

Every merged contract is credited to its author. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License

Apache 2.0 — *Part of the [AgentContract](https://github.com/agentcontract) open standard.*
