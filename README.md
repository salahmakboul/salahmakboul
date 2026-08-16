### Salah Makboul — I build the layer most people won't touch: kernel drivers, Darija voice AI, and the backend under both.

**Live right now, not screenshots:**
- 💬 [FishoFisho](https://fishofisho-sm.onrender.com/) — Django + Channels real-time chat, 21 models, 202 tests, RBAC that's actually enforced not just modeled.
- 🔊 Windows Bluetooth A2DP Driver — KMDF kernel-mode driver built from raw AVDTP spec after proving Intel's stack blocks user-mode L2CAP. Three kernel crashes diagnosed via `cdb.exe`, zero Stack Overflow answers to copy from. *(repo pinned below)*
- 🌐 [Portfolio](https://salah-makboul-portfolio.vercel.app/) — WebGL hero, scroll-driven storytelling, and an on-page assistant that only answers from what's actually on the page — no hallucinated claims about me.

**The throughline:** I keep ending up at the boundary — Darija doesn't have clean NLU tooling so I built my own filter maps and STT pipeline; Windows Bluetooth internals aren't documented so I read the AVDTP spec directly and debugged crash dumps by hand. I'd rather spend three days proving *why* something breaks than three hours working around it.

Currently based in Morocco (GMT+1) — open to freelance and full-time backend/systems work. One thing I'd genuinely like help thinking through: a Darija code-switching ASR benchmark (`DarijaBench`) — 500 labeled clips, first of its kind for the dialect. If that's your kind of problem too, my inbox is open
