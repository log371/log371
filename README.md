<!-- GitHub profile README · log371 -->

```text
log371@github:~$ whoami
Julien L. | Systems Developer / Local AI Engineering

log371@github:~$ cat /etc/engineering-principles
local-first · least privilege · reproducibility · maintainability
```

I build practical software around **local AI, Linux systems, backend engineering and security-conscious design**.

My focus is simple: keep systems understandable, data under control and dependencies justified. I prefer a small working prototype with documented limits over a large collection of promises.

```text
~/focus
├── local-ai/       Ollama · RAG · on-premise inference
├── backend/        Python · FastAPI · APIs · automation
├── systems/        Linux · Docker · offline workflows
└── assurance/      tests · permissions · traceability
```

## Selected work

### [`Skillbook`](https://github.com/log371/Skillbook) — controlled tools for local AI

A reproducible laboratory for deterministic tool permissions, signed offline updates, environment inventories and audit traces. The policy engine—not the LLM—decides which operations are allowed.

**Evidence:** documented offline demo, automated tests, explicit trust boundaries and known limitations.

### [`LocalProof`](https://github.com/log371/localproof) — inspect AI regressions locally

A local-first evaluation workbench that compares structured outputs, records test provenance and exposes differences for inspection. Includes an Ollama integration and a deterministic mock mode.

**Evidence:** reproducible runs, exportable reports, backend and frontend tests, and a clearly labeled real-model example.

### [`SentinelIA`](https://github.com/log371/sentinel1.2) — document intelligence with traceable citations

A FastAPI document-RAG demonstration with file ingestion, source-linked answers and interchangeable LLM providers, including local Ollama and a deterministic mock.

**Evidence:** documented API, local setup instructions, tests and explicit non-production constraints.

## How I work

- **Verify, don't assume.** Document what a test actually establishes.
- **Security by boundaries.** Validate inputs, restrict capabilities and minimize privileges.
- **Offline when appropriate.** Make network and model dependencies explicit.
- **Build for maintenance.** Prefer readable architectures and reproducible environments.

```text
log371@github:~$ contact --public
portfolio: https://julienl.dev
location:  Aix–Marseille, France
```

> Open to engineering opportunities in backend systems, local AI and on-premise integrations.
