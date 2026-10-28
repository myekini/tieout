# Tieout

**Settlement reconciliation across payment providers.**

> **Status: design stage.** Nothing is built yet. Work starts after CostTrail ships its first release.

**The question:** does the money from every provider match, and what happens to what doesn't?

## What v1 will do

- Synthetic provider settlement files and an internal ledger, in several formats
- Matching rules: exact, tolerance and many-to-one
- Handling for late files, duplicates and partial settlements
- An exception queue and dispute workflow
- **Idempotent reruns:** a second run changes nothing
- **An LLM triage assistant.** It proposes a cause and a fix from the evidence, a human approves, and every action is audit-logged.

Evaluation: match rate, triage precision and recall against the planted fault types, and rerun safety.

## What it won't do (yet)

Fraud scoring, real-time scoring, provider-specific edge cases beyond three providers.

## Known limitations

Data is synthetic with planted faults. Results show performance against the generator's assumptions, not production fraud detection or commercial impact.

## License

MIT
