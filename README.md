# CloseFew

> Found the gaps? **Close the few that matter.** An AI-guided remediation companion for your GapFew assessment.

CloseFew is part of the **Few** toolkit, alongside the rest of the suite (see the full list below). It is a single, free, fully client-side HTML page.

🔗 **Live:** https://silvestroparisi.github.io/CloseFew/

---

## What it is

Finding gaps isn't closing them. The real work comes after: deciding whether a control is *really* partial or already there, and knowing the next concrete step. A coverage score doesn't do that — a conversation does.

CloseFew reads a [GapFew](https://silvestroparisi.github.io/GapFew/) assessment and, control by control, asks you up to **three** short clarifying questions, judges where you really stand, and hands you a to-do: **what you already have** and **what to do to become compliant**. It works for all four GapFew frameworks — NIS2, NIST CSF 2.0, ISO/IEC 27001 and GDPR.

## Your AI, your call

Like [FixFew](https://silvestroparisi.github.io/FixFew/), the AI is your choice:

- **In-browser (default, no key)** — a model runs locally on your GPU via **WebGPU** ([WebLLM](https://github.com/mlc-ai/web-llm)). Nothing leaves your device. The first run downloads the model once (≈1–5 GB), then it's cached. It's slower than a cloud API and a small local model is weaker at reasoning — treat its verdicts as a first draft.
- **Your own key** — plug in a key for **OpenAI, Anthropic, Gemini, OpenRouter**, a local **Ollama / LM Studio**, or any OpenAI-compatible endpoint, for sharper reasoning. The key lives **in memory only** and is never stored. Only the calls you make go to that provider.

## You stay in control

The AI **suggests** a status; **you confirm** it. CloseFew never sets a compliance status on its own — it proposes "Partial / Implemented / Not implemented", and you accept (or override) it with one click. The questions are capped at three per control, asked one at a time.

## How it works

1. **Assess in GapFew** — rate each control and write your evidence.
2. **Import here** — load the GapFew **JSON** (best — lossless, joins by control ID) or the exported **CSV**. Or click **Try a demo** and pick a framework to load a worked SME example.
3. **Pick your AI** — in-browser model, or your own key.
4. **Assist** — on any control, answer up to three questions; get a verdict, *what you have* and a *to-do*.
5. **Confirm & plan** — accept the suggested status, then **export the remediation plan** (printable HTML) or save it as JSON.

Use Assist on the controls you're unsure about — there's no need to run it on all of them.

## Privacy

100% client-side. Your assessment is parsed in the browser. With the in-browser model nothing leaves your device at all; with your own key, only your calls go to that provider, and the key stays in memory. It's open source — open the Network tab and check.

## Requirements

The in-browser model needs a **WebGPU** browser (desktop **Chrome or Edge** work best; Safari is improving). No WebGPU? Use your own API key with a cloud or local provider instead — that path needs no WebGPU. You can also import and read your assessment with no AI at all.

## What CloseFew is — and isn't

**CloseFew gives orientation, not certification, audit or legal advice.** The AI suggests; you decide. A small local model can be wrong or generic, and even a frontier model doesn't know your full context. Verify anything that matters with a qualified assessor, DPO or lawyer. The framework caveats from GapFew apply here too (ISO control text is copyrighted; GDPR and NIS2 applicability are context- and jurisdiction-dependent).

## Deploy it yourself

1. Create a repository named `CloseFew`.
2. Add `index.html` (this single file) to the root.
3. Enable GitHub Pages (Settings → Pages → deploy from the `main` branch, root).
4. It's live at `https://<your-username>.github.io/CloseFew/`.

## The Few toolkit

- [**FirstFew**](https://silvestroparisi.github.io/FirstFew/) — prioritize the few that matter
- [**FixFew**](https://silvestroparisi.github.io/FixFew/) — verify and remediate vulnerabilities
- [**MaskFew**](https://silvestroparisi.github.io/MaskFew/) — anonymize a file before you share it
- [**AskFew**](https://silvestroparisi.github.io/AskFew/) — a private AI that runs in your browser
- [**ScrubFew**](https://silvestroparisi.github.io/ScrubFew/) — strip hidden metadata before you share
- [**RopaFew**](https://silvestroparisi.github.io/RopaFew/) — build your GDPR Article 30 register
- [**GapFew**](https://silvestroparisi.github.io/GapFew/) — a multi-framework compliance gap self-assessment
- **CloseFew** — turn your gaps into a remediation plan
