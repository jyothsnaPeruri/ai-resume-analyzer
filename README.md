# AI Resume Analyzer

Upload a resume and get an ATS score, strengths and gaps, a keyword match against any job ad, rewritten bullet points and a tailored cover letter. No sign-up and no API key needed.

**Live demo:** https://jyothsnaperuri.github.io/ai-resume-analyzer/

## Features

- **Overview:** overall, ATS and impact scores, detected skills, strengths and specific improvements
- **Job match:** match percentage, matched and missing keywords, and three concrete edits to tailor the resume
- **Rewrites:** the four weakest bullet points rewritten with stronger verbs (never invents numbers; uses `[X]` placeholders)
- **Cover letter:** 250–320 words, built only from facts in the resume, with copy and download
- **PDF upload:** text is extracted in the browser with pdf.js, or paste plain text

## How it works

```
Browser (this repo, GitHub Pages)          Server (FastAPI on Render)                Groq
index.html ── POST /resume/analyze ──────► validates input, rate-limits per visitor ─► gpt-oss-120b
            ◄── JSON result ──────────────  builds the prompt, parses JSON reply  ◄── (falls back to gpt-oss-20b)
```

- The **AI key stays on the server**, so visitors never need one.
- **Prompts live on the server**, so the endpoint can only analyse resumes and can't be used as a free general-purpose LLM.
- **Each results tab loads the first time it's opened**, which keeps waiting time and token usage low on the free tier.
- **Per-visitor rate limiting** (24 requests per 10 minutes), input size limits, and a retry when the model returns malformed JSON.
- If the main model is rate-limited, the server retries on a smaller model, which has its own quota.

The backend endpoint lives in [`Research-Agent/research-agent/resume.py`](https://github.com/jyothsnaPeruri/Research-Agent/blob/master/research-agent/resume.py).

## Tech

- **Frontend:** HTML, CSS, vanilla JavaScript, pdf.js; no build step
- **Backend:** Python, FastAPI, Pydantic validation
- **AI:** Groq (`openai/gpt-oss-120b`, JSON mode)
- **Hosting:** GitHub Pages (frontend), Render free tier (API)

## Run locally

```bash
git clone https://github.com/jyothsnaPeruri/ai-resume-analyzer.git
cd ai-resume-analyzer
python3 -m http.server 8000     # then open http://localhost:8000
```

The page calls the hosted API by default. To use your own backend, change `API_BASE` near the top of the script in `index.html`.

## Notes

- The API runs on Render's free tier, which sleeps when idle, so the first request can take up to a minute. The page pings the server on load and shows its status.
- Resumes are sent to the API only to generate the analysis and are not stored.

---

Built by **Jyothsna (Jo) Peruri** · [Portfolio](https://jyothsnaperuri.github.io/Jyothsna-portfolio/) · [LinkedIn](https://www.linkedin.com/in/jyothsna-jo-peruri/) · [GitHub](https://github.com/jyothsnaPeruri)
