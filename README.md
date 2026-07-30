# Curtis Compliance Pro

> Hosted compliance tier for fintech dev teams — **in development.**
> The MIT core is live at [JordanNewell/curtis-compliance](https://github.com/JordanNewell/curtis-compliance).

---

## Why a Pro tier

[Curtis Compliance](https://github.com/JordanNewell/curtis-compliance) is a
static regulatory scanner that runs at commit time, locally, per repo. It
ships the pre-commit gate, the hash-chained audit trail, and PAT-based PR
review under MIT.

Pro is the layer on top — the parts a fintech or dev team pays for so the
evidence the core produces rolls up to the org level auditors actually want
to see.

## What's planned

| Feature | What it does |
|---------|--------------|
| **Hosted GitHub App** | Install once per org. Every PR auto-reviewed. No per-developer PAT. |
| **Multi-repo audit rollup** | Aggregate `.curtis/audit` events across all repos into one evidence view for SOC2 / PCI-DSS auditors. |
| **PDF export** | Auditor-ready evidence packs, signed and timestamped. |
| **Custom frameworks** | Define your own rules + citations — ISO 27001, FedRAMP, internal policies — beyond the three built-in presets. |

## Status

**Phase 0 — foundation.** The license gate, CLI shape, and source-available
licensing model are designed locally. The four features above are not
shipped. There is no npm package to install yet, and no way to purchase a
license key yet.

| Phase | Status |
|-------|--------|
| 0 — license gate + CLI shape | designed, not published |
| 1 — activation + validation server | not started |
| 2 — hosted GitHub App | not started |
| 3 — multi-repo rollup + PDF export | not started |
| 4 — custom frameworks | not started |

## When will it ship

No dates yet. The MIT core is the priority; Pro follows once the core is
stable and there's real signal that teams want the hosted tier.

**Star this repo** to get a ping when Phase 1 lands and a purchase path
actually exists. Or open an issue if you want to talk about an early-access
arrangement.

## Pricing

Not announced. The model is per-seat for Pro and sales-led for Enterprise
(SSO, on-prem, SLA, custom rulesets). Numbers land when the features do.

## How it relates to the MIT core

```
curtis-compliance          (MIT, free, live)
  init · check · report · review:pr · audit · license

curtis-compliance-pro      (source-available, paid, in development)  ← here
  license · [P2] review:pr-org · [P3] rollup · [P4] framework:add
```

Pro wraps the core engine — it never forks or replaces it. Core's
`curtis-compliance license status` will detect Pro and defer to it when
Pro ships; until then it prints where Pro will live.

## License

Source-available once shipped. The MIT core is unaffected and always free.

© Jordan Newell


<p align="right">
  <a href="https://jordannewell.com" title="Built by Jordan Newell">
    <img src="assets/newell-badge.png" alt="Built by Jordan Newell" width="48" height="48">
  </a>
</p>