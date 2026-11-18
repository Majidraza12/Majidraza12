<h1 align="center">Majid Raza</h1>

<p align="center">
  Software engineer · CS at Illinois Tech, graduating May 2027 · Chicago
</p>

<p align="center">
  <a href="https://majidraza-portfolio-site.vercel.app"><img src="https://img.shields.io/badge/Portfolio-0F172A?style=flat-square&logo=vercel&logoColor=white" alt="Portfolio"></a>
  <a href="https://linkedin.com/in/majid-raza"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:majidraza.bss@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://majidraza-portfolio-site.vercel.app/MajidRaza_Resume.pdf"><img src="https://img.shields.io/badge/Resume-PDF-334155?style=flat-square" alt="Resume"></a>
</p>

---

I build software that has to be right, not only work in a demo: a job-eligibility engine that cites the exact sentence behind every verdict, a dictation app that runs Whisper on your own GPU with no network calls, and ML experiments that report the result I didn't want.

I work across the stack, from Postgres row-level security to Rust audio pipelines to PyTorch training loops. I like problems where correctness, latency or privacy actually matter, and I write down the numbers, including the unflattering ones.

**Looking for:** new-grad software engineering roles starting 2027. Backend, full-stack, or applied AI.

## Selected work

### [JobGate](https://github.com/Majidraza12/JobGate) · [live](https://jobgate-three.vercel.app)
Tells a student whether they're actually eligible for an internship or new-grad posting, and shows the exact sentence from the job description behind each verdict.
- Fetches JDs from six ATS platforms (Greenhouse, Lever, Ashby, Workday, Oracle HCM, SmartRecruiters); an LLM extracts eligibility rules into a fixed schema, and every quote is verified as an exact substring of the source.
- LLM runs once per JD and is cached by content hash, so cost scales with postings, not users; matching is deterministic, unit-tested TypeScript.
- Hand-labeled 60-JD eval set: work-auth detection at 100% precision / 100% recall vs. 88% / 70% for a regex baseline (dev set, n=10, documented as such).

`Next.js` `TypeScript` `Supabase / Postgres + RLS` `Claude API` `Zod` `GitHub Actions` `Vitest`

### [Scribbet](https://github.com/Majidraza12/Scribbet)
Local-first Windows dictation: hold a hotkey, speak, and clean text is typed into whatever app has focus. No cloud, no account.
- Pipeline: Silero VAD → whisper.cpp (Vulkan GPU, CPU fallback) → 9-stage rule-based cleanup → universal text insertion (UIA / SendInput / clipboard).
- ~200–400 ms finalize on a mid-range GPU; zero network code in the default build apart from a checksum-pinned model download.
- Rust workspace of 10 crates behind platform traits, Tauri 2 + Svelte 5 shell, 20 ADRs and an unedited engineering log. v1.2.1, my daily driver.

`Rust` `Tauri` `Svelte` `whisper.cpp` `ONNX` `SQLite`

### [Algomaxx](https://github.com/Majidraza12/Algomaxx)
DSA practice platform: 150-problem bank, in-browser editor with sandboxed grading, study tracks, per-pattern analytics, and an AI coach.
- All 150 problems auto-graded through Judge0, with structural adapters for linked lists, trees and graphs.
- AI weak-pattern analysis from hint reliance, difficulty split and solve rate; Stripe subscriptions with trial.
- Vitest unit tests plus a real-Python test harness, Playwright end-to-end tests.

`Next.js` `React` `Supabase` `Judge0` `Claude API` `Stripe` `Playwright`

### [Violence detection in video](https://github.com/Majidraza12/incident-detection-project)
CNN-LSTM (ResNet-18 → LSTM over 16 frames) classifying surveillance clips, built for a course and run like a real experiment.
- Fixed seeds, checkpoint selection by validation loss, results as mean ± std over 3 seeds.
- Controlled ablation found the LSTM **does not** beat simple frame averaging (89.9% vs. 90.6% test accuracy, within noise), reported as the headline finding.

`Python` `PyTorch` `Streamlit`

### More
- **[Orbitize](https://github.com/Majidraza12/Orbitize):** project management app for small teams with role-based permissions and a Git-style commit log per project. `Next.js` `Supabase` `TanStack Query`
- **[ratelimiter](https://github.com/Majidraza12/ratelimiter):** Spring Boot rate-limiting service with pluggable token-bucket and sliding-window strategies. `Java` `Spring Boot`

## Toolkit

<p>
  <img src="https://skillicons.dev/icons?i=ts,js,py,rust,java,postgres&perline=6" alt="TypeScript, JavaScript, Python, Rust, Java, PostgreSQL" /><br/>
  <img src="https://skillicons.dev/icons?i=nextjs,react,svelte,tauri,spring,tailwind&perline=6" alt="Next.js, React, Svelte, Tauri, Spring Boot, Tailwind CSS" /><br/>
  <img src="https://skillicons.dev/icons?i=supabase,pytorch,docker,githubactions,vercel,git&perline=6" alt="Supabase, PyTorch, Docker, GitHub Actions, Vercel, Git" />
</p>

**Languages:** TypeScript, Python, Rust, Java, SQL
**Web & backend:** Next.js, React, Svelte, Tauri, Spring Boot, Supabase (Postgres, Auth, RLS)
**AI / ML:** PyTorch, Claude API, whisper.cpp, scikit-learn, pandas
**Testing & infra:** Vitest, Playwright, GitHub Actions, Docker, Vercel, Stripe

## Now

- Building a held-out eval set for JobGate so its numbers mean something beyond the dev set.
- Finishing my CS degree at Illinois Tech (May 2027).

<br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Majidraza12/Majidraza12/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Majidraza12/Majidraza12/output/github-snake.svg" />
  <img alt="Contribution graph animation" src="https://raw.githubusercontent.com/Majidraza12/Majidraza12/output/github-snake.svg" />
</picture>
