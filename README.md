# All-in-one skill set

This repository is a collection of installable agent skills. A skill is a folder with a `SKILL.md` file and the files that skill reads (references, scripts, and data). The skills are copied from public repositories and grouped by upstream, so each author's license stays with that author's files.

This is not one product and not one license. The file `LICENSE` at the root only says that. The code and instructions under `skills/` keep the license they shipped with.

Snapshot date of the copies: 14 November 2026. Each attribution row records the commit that was copied.

## Domains

| Namespace | Domain | Skills |
| --- | --- | --- |
| `mattpocock` | Engineering workflow, plus the published productivity and misc skills from the same repo | 31 |
| `addyosmani` | Software delivery lifecycle: spec, plan, build, test, review, ship | 25 |
| `nextlevelbuilder` | UI/UX design intelligence, plus the small companion skills shipped beside it | 6 |
| `emilkowalski` | Motion and design engineering | 19 |
| `wshobson` | Agent skills for development, review, testing, infrastructure, and security | 185 |
| `anthropics` | Skill format, MCP servers, frontend design, and webapp testing | 4 |
| `petrkindlmann` | QA catalog: automation, API, accessibility, performance, security, release | 50 |
| `coreyhaines31` | Marketing, SEO, AEO, and GEO | 53 |
| `aaron-he-zhu` | Social, influencer, and paid-social skills that Corey Haines does not already cover | 17 |

**390** skills in total.

Marketing search coverage lives in Corey Haines: `ai-seo` (AEO, GEO, and answer-engine citation), `seo-audit`, `schema`, `programmatic-seo`, and `site-architecture`. Aaron He Zhu's SEO/GEO tree was not copied, so this repo does not carry a second search library.

## Layout

```
skills/<namespace>/<skill>/SKILL.md
skills/<namespace>/LICENSE
skills/<namespace>/NOTICE          # Apache-2.0 namespaces
skills/<namespace>/support/        # files a skill links to that lived outside the skill folder
```

`support/` is not a skill. It holds benchmarks, tool notes, and scripts that the copied skills already pointed at. Those files keep their upstream relative path under `support/`.

Skill instructions were not rewritten. The only edits are path fixes required by this layout:

- `nextlevelbuilder/ui-ux-pro-max` runs its search script at `skills/nextlevelbuilder/ui-ux-pro-max/scripts/search.py` from the root of this repo. The script still finds its CSV data next to itself.
- `wshobson/review-agent-setup` ships the Cedar policy and `agents/review-policy-author.md` inside the skill folder, and the copy instructions point at those files.
- `wshobson/signed-audit-trails-recipe` links to `protect-mcp-setup` and `review-agent-setup` in this namespace instead of the upstream plugin directories.
- Aaron He Zhu links that targeted a skill we did not copy now point at that file on GitHub at the commit below. Links that targeted a file we did copy point at the file in this repo.

## Install into Cursor

One command, on Mac, Windows, or Linux. It needs Node.js. `-g` installs into your user folder so every project can see the skills. `-a cursor` targets Cursor. `--skill '*'` takes the whole catalog and skips the picker.

```bash
npx skills add tushar1599/all-in-one-skillset -g -a cursor -y --skill '*'
```

The `skills` CLI walks `skills/<namespace>/<skill>/SKILL.md`, which is this repo's layout. Two skills are both named `prototype` (Matt Pocock and Emil Kowalski). The installer keeps the first one it finds. Install the other under a second name:

```bash
npx skills add tushar1599/all-in-one-skillset -g -a cursor -y --skill prototype --rename design-prototype
```

Run that only if the first command did not install both. `--rename` changes the folder and the `name` field of the one skill it installs.

Cursor reads a skill from a folder that contains `SKILL.md`:

- This project: `.cursor/skills/<skill-name>/SKILL.md`
- Every project: `~/.cursor/skills/<skill-name>/SKILL.md` (`%USERPROFILE%\.cursor\skills` on Windows)

Drop `-g` to install into the current project only.

Corey Haines and Aaron He Zhu skills link to a `support/` folder next to the namespace. `npx skills` copies each skill folder and does not copy that sibling. On this machine those files were placed in `%USERPROFILE%\.cursor\support`, which is where `../support/...` resolves after a flat install into `%USERPROFILE%\.cursor\skills`.

The UI/UX search script needs Python 3 (`python` or `py -3`) and uses the standard library only. Inside this repo:

```bash
py -3 skills/nextlevelbuilder/ui-ux-pro-max/scripts/search.py "error summary validation" --domain ux
```

## Attribution

| Namespace | Upstream | Commit | License | Copyright notice | What was copied |
| --- | --- | --- | --- | --- | --- |
| `mattpocock` | [mattpocock/skills](https://github.com/mattpocock/skills) | `5863806dd4e15c63174bee4e7515a4256792ecfa` | MIT | Copyright (c) 2026 Matt Pocock | 31 skill folders from `skills/engineering`, `skills/productivity`, and `skills/misc`, plus `LICENSE` |
| `addyosmani` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) | `39b723ceebf81474d0557c1fecd01eddab585563` | MIT | Copyright (c) 2025 Addy Osmani | 25 skill folders under `skills/`, plus `LICENSE` |
| `nextlevelbuilder` | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | `6ae86f61f520d6ca229d2f40e070410638c908c5` | MIT | Copyright (c) 2024 Next Level Builder | `ui-ux-pro-max` (SKILL.md, `data/`, `scripts/`, `references/`) and five small companion skills that were already under `.claude/skills/`, plus `LICENSE` |
| `emilkowalski` | [emilkowalski/skills](https://github.com/emilkowalski/skills) | `0f2e23b32bb1265e84cff8d3e75785fec953fb1b` | MIT | Copyright (c) 2026 Emil Kowalski | 19 skill folders under `skills/`, plus `LICENSE` |
| `wshobson` | [wshobson/agents](https://github.com/wshobson/agents) | `9c61ab243def98f72da12abd41cfcf5bcd91af9d` | MIT | Copyright (c) 2024 Seth Hobson | 185 `SKILL.md` folders under `plugins/*/skills/`, plus `LICENSE`. `review-agent-setup` also includes that plugin's policy files and `agents/review-policy-author.md` |
| `anthropics` | [anthropics/skills](https://github.com/anthropics/skills) | `2c5958ecac7cee2b583967a2c4981d0f4a75c579` | Apache-2.0 | Copyright 2026 Anthropic, PBC, in three of the four skill notices | `skill-creator`, `mcp-builder`, `frontend-design`, `webapp-testing`, each with its own `LICENSE.txt`. See `skills/anthropics/NOTICE` |
| `petrkindlmann` | [petrkindlmann/qa-skills](https://github.com/petrkindlmann/qa-skills) | `62434253c2592f27b494609c27f224939c86346d` | MIT | Copyright (c) 2026 Petr Kindlmann | 50 skill folders under `skills/`, plus `LICENSE` |
| `coreyhaines31` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | `1f837447b20bb6f0e72d87b80ece1c221c362c7d` | MIT | Copyright (c) 2025 Corey Haines | 53 skill folders under `skills/`, the `tools/` notes those skills link to (`skills/coreyhaines31/support/tools/`), plus `LICENSE` |
| `aaron-he-zhu` | [aaron-he-zhu/aaron-marketing-skills](https://github.com/aaron-he-zhu/aaron-marketing-skills) | `2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4` | Apache-2.0 | Copyright 2024 Aaron He Zhu | 17 skill folders and the reference files they link to, under `support/`. Upstream had no NOTICE file. `skills/aaron-he-zhu/NOTICE` records the copy |

The MIT `LICENSE` files and the Apache-2.0 `LICENSE` / `LICENSE.txt` files are the upstream texts, unmodified. Copyright lines above are the lines in those files.

`frontend-design` is Apache License 2.0. Its `LICENSE.txt` is the Apache terms and does not include a filled copyright appendix. It was copied unchanged. The other three Anthropic skills state Copyright 2026 Anthropic, PBC.

Companion skills `banner-design`, `design`, and `design-system` say `license: MIT` in their frontmatter and name author `claudekit`. `brand` and `slides` do not have their own license file or license field. They were copied because they sit in the Next Level Builder MIT repository and have no contrary notice. `ui-styling` was not copied; see below.

## What was left out

### Not this collection

| Upstream | Why it is not here |
| --- | --- |
| [yaojingang/GEOHub](https://github.com/yaojingang/GEOHub) | Left out because it is AGPL-3.0. GEO coverage in this repo is Corey Haines `ai-seo`, not GEOHub. |
| `awesome-*` indexes (VoltAgent, ComposioHQ, spencerpauly, RankSpotAI, jqueryscript, and the rest) | Indexes point at other repos. Copying the README does not bring the skills, and the linked repos have their own licenses. |
| [sickn33/agentic-awesome-skills](https://github.com/sickn33/agentic-awesome-skills) | A large unreviewed catalog. It would duplicate the curated set. |
| [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) | Broad MIT library that overlaps Matt Pocock, Addy Osmani, and Corey Haines. Left out so this repo does not vendor the same engineering and marketing skills twice. |
| [obra/superpowers](https://github.com/obra/superpowers) | A second engineering workflow (brainstorm, TDD, review) beside Matt Pocock and Addy Osmani. |
| [pbakaus/impeccable](https://github.com/pbakaus/impeccable) and [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) | Not vendored. The UI source here is `ui-ux-pro-max` plus Emil Kowalski. |

### Skipped inside an included upstream

**License (skipped):**

- `nextlevelbuilder` skill `ui-styling`. `SKILL.md` says `license: MIT`. The folder's `LICENSE.txt` is the Apache License 2.0 template with the copyright line still reading `Copyright [yyyy] [name of copyright owner]`. The `canvas-fonts/` files are SIL Open Font License 1.1, which is not MIT or Apache-2.0. The skill was skipped. `ui-ux-pro-max` does not need it.

**Apache notices that were present:** the four Anthropic skills each have an Apache-2.0 `LICENSE.txt`. None of those four folders contained a NOTICE file. The upstream `THIRD_PARTY_NOTICES.md` attributes imageio, FFmpeg, and other components used by document and media skills that were not copied, so that file was not copied. `doc-coauthoring` has a `SKILL.md` and no `LICENSE.txt`; it was not requested and was not copied.

**Matt Pocock drafts:** `skills/in-progress/` was not copied (`chief-of-staff`, `claude-handoff`, `loop-me`, `setup-ts-deep-modules`, `software-factory`, `writing-beats`, `writing-fragments`, `writing-shape`). Those folders are unpublished drafts. The published engineering, productivity, and misc skills were copied.

**UI/UX trees the skill does not need:** `cli/`, `src/`, `stack/`, `gallery/`, `screenshots/`, `preview/`, `projects/`, and `docs/` from `ui-ux-pro-max-skill`. The running skill is `.claude/skills/ui-ux-pro-max/` (`data/`, `scripts/`, `references/`, `SKILL.md`).

**wshobson harness copies:** there was no second `SKILL.md` tree under `.cursor/`, `.agents/`, or per-plugin Codex/Claude adapter folders. Plugin `agents/*.md` and `commands/*.md` were not copied, except `review-policy-author.md`, which `review-agent-setup` tells the reader to open. Hooks and plugin manifests were not copied.

**Aaron He Zhu, to avoid a second marketing library.** Narrative, SEO/GEO, email, launch, and the protocol skills were not copied. Inside social, influencer, and paid ads, these were not copied because Corey Haines already covers that job:

| Aaron skill | Already covered by |
| --- | --- |
| `social-calendar-builder`, `social-creative-builder`, `short-video-scripter` | `social` (calendars, posts, short-form scripts) |
| `social-pulse-monitor` | `social` (listening) |
| `advocacy-program-designer` | `community-marketing` and `influencer-marketing` |
| `audience-mapper`, `fit-scorer`, `influencer-discovery`, `campaign-planner`, `brief-generator`, `budget-optimizer`, `outreach-manager`, `contract-helper` | `influencer-marketing` (vetting, briefs, pay, contracts) |
| `competitor-tracker` | `competitors` and `competitor-profiling` |
| `landing-optimizer` | `cro` |
| `performance-analyzer`, `roi-calculator`, `report-generator` | `influencer-marketing` (did the sponsorship work) |
| `campaign-architect`, `audience-segment-builder`, `bid-strategy-planner`, `budget-pacing-monitor` | `ads` |
| `ad-creative-builder` | `ad-creative` |
| `ad-test-designer` | `ab-testing` |
| `landing-experience-checker` | `cro` |
| `conversion-signal-qa`, `conversion-value-mapper` | `conversion-tracking` |
| `paid-measurement-loop` | `analytics` and `attribution` |
| `attribution-reconciler` | `attribution` |
| `search-term-miner`, `product-feed-optimizer` | Not social-paid (search terms and shopping feeds). `ads` covers Google and Meta campaign judgment |

Copied from Aaron instead: crisis response, dark social, share of voice, organic measurement, social quality audit, inbox, social selling, channel warmup, channel portfolio, voice dossier, platform norms, trend spotting, creator-content audit, content atomizing, placement exclusions, fatigue and frequency, and ad-account audit.

Links from those 17 skills to a skill in the table above point at the upstream commit, not at a local folder.

## How to add a skill later

1. Read that skill's `LICENSE` and any `NOTICE` in the upstream repo. Read the notice inside the skill folder when the repo has no root license.
2. If the license is missing, unclear, or not MIT or Apache-2.0, do not add the skill. Note the skip in this README.
3. Copy the skill folder to `skills/<namespace>/<skill>/`. Keep the upstream `LICENSE` in the namespace. Do not strip copyright notices.
4. For Apache-2.0, keep any `NOTICE` file and add a line to the namespace `NOTICE` that names the upstream, the commit, and the paths copied.
5. Copy files the skill links to that live outside its folder (scripts, references). Put them under `skills/<namespace>/support/` and change only the relative links that broke. Do not rewrite the instructions.
6. Do not copy a generated harness copy of a skill you already copied.
7. Add a row to the attribution table and the skill name to the index below.

## Index

<details>
<summary>mattpocock (31)</summary>

ask-matt, codebase-design, code-review, diagnosing-bugs, domain-modeling, git-guardrails-claude-code, grilling, grill-me, grill-with-docs, handoff, implement, implement-spec, improve-codebase-architecture, migrate-to-shoehorn, pr, prototype, research, retro, scaffold-exercises, setup-matt-pocock-skills, setup-pre-commit, tdd, teach, to-questionnaire, to-spec, to-tickets, triage, wait-what, wayfinder, wizard, writing-for-agents

</details>

<details>
<summary>addyosmani (25)</summary>

api-and-interface-design, browser-testing-with-devtools, ci-cd-and-automation, code-review-and-quality, code-simplification, constraint-driven-development, context-engineering, debugging-and-error-recovery, deprecation-and-migration, documentation-and-adrs, doubt-driven-development, frontend-ui-engineering, git-workflow-and-versioning, idea-refine, incremental-implementation, interview-me, observability-and-instrumentation, performance-optimization, planning-and-task-breakdown, security-and-hardening, shipping-and-launch, source-driven-development, spec-driven-development, test-driven-development, using-agent-skills

</details>

<details>
<summary>nextlevelbuilder (6)</summary>

banner-design, brand, design, design-system, slides, ui-ux-pro-max

</details>

<details>
<summary>emilkowalski (19)</summary>

animate, animate-expo, animation-performance, animation-vocabulary, apple-design, ask-sonner, break-ui, choreograph, emil-design-eng, find-animation-opportunities, gestures, improve-animations, learn-taste, mobile-native, pick-ui-library, prototype, remove-animations, review-animations, write-swift

</details>

<details>
<summary>wshobson (185)</summary>

accessibility-compliance, ai-debt-detector, airflow-dag-patterns, angular-migration, anti-reversing-techniques, api-design-principles, architecture-decision-records, architecture-patterns, async-python-patterns, attack-tree-construction, auth-implementation-patterns, avoid-ai-writing, backtesting-frameworks, bash-defensive-patterns, bats-testing-patterns, bazel-build-optimization, before-you-build, billing-automation, binary-analysis-patterns, block-no-verify-hook, brand-landingpage, changelog-automation, checkpoint-promotion, code-review-excellence, competitive-landscape, connectivity-triage, context-driven-development, cost-optimization, cqrs-implementation, database-migration, data-quality-frameworks, dataset-curation, data-storytelling, dbt-transformation-patterns, debugging-strategies, defi-protocol-templates, dependency-upgrade, deployment-pipeline-design, design-system-patterns, distributed-tracing, dotnet-backend-patterns, e2e-testing-patterns, embedding-strategies, employment-contract-templates, error-handling-patterns, eval-harness-first, evaluation-methodology, event-store-design, fastapi-templates, file-conversion, finetuning-method-selection, gdpr-data-handling, git-advanced-workflows, github-actions-templates, gitlab-ci-patterns, gitops-workflow, go-concurrency-patterns, godot-gdscript-patterns, grafana-dashboards, grounded-vault, grpo-rlvr-training, hads, helm-chart-scaffolding, hermes-tweet, hybrid-cloud-networking, hybrid-search-implementation, incident-runbook-templates, interaction-design, istio-traffic-management, javascript-testing-patterns, k8s-manifest-generator, k8s-security-policies, kpi-dashboard-design, langchain-architecture, linkerd-patterns, llm-evaluation, lora-qlora-recipes, market-sizing-analysis, memory-forensics, memory-safety-patterns, microservices-patterns, ml-pipeline-workflow, mobile-android-design, mobile-ios-design, modern-javascript-patterns, monorepo-management, mtls-configuration, multi-cloud-architecture, multi-reviewer-patterns, nextjs-app-router-patterns, nft-standards, nodejs-backend-patterns, nx-workspace-patterns, on-call-handoff-patterns, openapi-spec-generation, parallel-debugging, parallel-feature-development, paypal-integration, pci-compliance, postgresql-table-design, postmortem-writing, pptx-deck-context, pptx-quality-gates, pptx-reference-deck-analysis, pptx-slide-specification, pptx-visual-assets, preference-optimization, projection-patterns, prometheus-configuration, prompt-engineering-patterns, protect-mcp-setup, protocol-reverse-engineering, python-anti-patterns, python-background-jobs, python-code-style, python-configuration, python-design-patterns, python-error-handling, python-observability, python-packaging, python-performance-optimization, python-project-structure, python-resilience, python-resource-management, python-testing-patterns, python-type-safety, quantized-export, rag-implementation, react-modernization, react-native-architecture, react-native-design, react-state-management, recsys-pipeline-architect, responsive-design, review-agent-setup, risk-metrics-calculation, rust-async-patterns, saga-orchestration, sast-configuration, scan, screen-reader-testing, secrets-management, security-requirement-extraction, service-mesh-observability, session-guard, shellcheck-configuration, signed-audit-trails-recipe, similarity-search-patterns, slo-implementation, social-evidence-research, social-publishing, solidity-security, spark-environment-setup, spark-memory-thermal-ops, spark-optimization, spark-training-gotchas, sql-optimization-patterns, startup-financial-modeling, startup-metrics-framework, stride-analysis-patterns, stripe-integration, superself, tailwind-design-system, task-coordination-strategies, team-communication-protocols, team-composition-analysis, team-composition-patterns, temporal-python-testing, terraform-module-library, threat-mitigation-mapping, trace-to-training-data, track-management, turborepo-caching, typescript-advanced-types, unity-ecs-patterns, uv-package-manager, vector-index-tuning, vision-sft, visual-design-foundations, visual-edit-precision, wcag-audit-patterns, web3-testing, web-component-design, workflow-orchestration-patterns, workflow-patterns

</details>

<details>
<summary>anthropics (4)</summary>

frontend-design, mcp-builder, skill-creator, webapp-testing

</details>

<details>
<summary>petrkindlmann (50)</summary>

accessibility-testing, agentic-browser-testing, ai-bug-triage, ai-qa-review, ai-system-testing, ai-test-generation, analytics-tracking-testing, api-testing, bug-reproduction, chaos-engineering, ci-cd-integration, compliance-testing, contract-testing, coverage-analysis, cross-browser-testing, cypress-automation, database-testing, email-testing, exploratory-testing, mobile-testing, observability-driven-testing, payment-testing, performance-testing, playwright-automation, qa-dashboard, qa-do, qa-metrics, qa-project-bootstrap, qa-project-context, qa-report-humanizer, qa-start, quality-postmortem, release-readiness, risk-based-testing, security-testing, selector-drift-recovery, service-virtualization, shift-left-testing, synthetic-monitoring, test-case-management, test-data-management, test-environments, testing-in-production, test-migration, test-planning, test-reliability, test-strategy, test-suite-curation, unit-testing, visual-testing

</details>

<details>
<summary>coreyhaines31 (53)</summary>

ab-testing, ad-creative, ads, ai-seo, analytics, aso, attribution, churn-prevention, cold-email, co-marketing, community-marketing, competitor-profiling, competitors, content-strategy, conversion-tracking, copy-editing, copywriting, cro, customer-research, directory-submissions, emails, events, free-tools, image, influencer-marketing, launch, lead-magnets, link-building, marketing-council, marketing-ideas, marketing-loops, marketing-plan, marketing-psychology, offers, onboarding, paywalls, popups, pricing, product-marketing, programmatic-seo, prospecting, public-relations, referrals, reverse-engineer-marketing, revops, sales-enablement, schema, seo-audit, signup, site-architecture, sms, social, video

</details>

<details>
<summary>aaron-he-zhu (17)</summary>

ad-account-auditor, channel-portfolio-planner, content-amplifier, creator-content-auditor, crisis-response-planner, dark-social-attributor, engagement-inbox-manager, fatigue-frequency-manager, participation-warmup-planner, placement-exclusion-manager, platform-norm-profiler, share-of-voice-tracker, social-measurement-loop, social-quality-auditor, social-selling-planner, trend-spotter, voice-dossier-builder

</details>
