<!-- GENERATED FILE: run `python3 scripts/generate-system-docs.py --write`; do not edit. -->

# System Architecture

This is the generated human view of [`references/system-catalog.json`](../references/system-catalog.json). The JSON catalog is authoritative.

- Architecture contract: `20.2.0`
- Bundle version: `20.2.0`
- Catalog digest: `sha256:42dd426e3a858d03e2d6ee8cae2cacd39a95d1058a1d114d45f2e38473609535`
- Shape: **112 discipline skills across 7 disciplines + 8 protocol skills = 120 skills; 8 commands**

## Runtime Capability Profiles

The capability matrix is delegated to [`references/capability-profiles.json`](../references/capability-profiles.json) (`sha256:a1bb5825bc677a4a5a452254f5d0b87a5fc21efb8ddc1dcecf31107f1318bc40`), preserving **Lite ⊂ Pro ⊂ Governed** without duplicating it in the system catalog.

Universal overlays applied to every profile: `consent` · `claims` · `pii-secrets` · `external-mutation` · `audit-verdict` · `release-provenance`.

| Profile | Rank | Capability count | Adds at this tier |
|---|---:|---:|---|
| **Lite** | 0 | 5 | `authored-workflows` · `auto-routing` · `deterministic-scoring` · `inline-delivery` · `canonical-state-read` |
| **Pro** | 1 | 7 | `connectors` · `audit-persistence` |
| **Governed** | 2 | 16 | `working-memory-write` · `registry-write` · `run-evidence` · `context-planning` · `runtime-controller` · `workflow-execution` · `workflow-loop` · `audit-loop` · `owner-capability` |

## Four Layers

| Layer | Purpose | Disciplines | Cadence |
|---|---|---|---|
| **L1 · Strategy** | what we say and who we are | narrative | always-on |
| **L2 · Channels** | always-on engines that express strategy | seo-geo → social → email → ad → influencer | always-on |
| **L3 · Orchestration** | time-boxed moments coordinated across channels | launch | episodic |
| **L4 · Protocol** | truth registries, governance, and working memory | protocol | continuous |

Canonical logical order: **narrative → seo-geo → social → email → ad → influencer → launch → protocol**.

## Discipline Topology

| Discipline | Layer | Framework | Loop | Skills |
|---|---|---|---|---:|
| **Brand Narrative** | L1 | TALE | Trace -> Architect -> Land -> Evaluate | 16 |
| **SEO/GEO** | L2 | CORE-EEAT + CITE | Survey -> Implement -> Tune -> Evaluate | 16 |
| **Organic Social** | L2 | ECHO | Explore -> Craft -> Host -> Observe | 16 |
| **Email Marketing** | L2 | SEND | Setup -> Engage -> Nurture -> Deliver | 16 |
| **Paid Ads** | L2 | ROAS | Research -> Orchestrate -> Activate -> Scale | 16 |
| **Influencer Marketing** | L2 | STAR | Scout -> Target -> Activate -> Report | 16 |
| **Product Launch** | L3 | RAMP | Research -> Assemble -> Mobilize -> Prove | 16 |

### Brand Narrative

- **trace:** [`narrative-baseline-mapper`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/trace/narrative-baseline-mapper/SKILL.md) · [`category-narrative-mapper`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/trace/category-narrative-mapper/SKILL.md) · [`audience-belief-mapper`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/trace/audience-belief-mapper/SKILL.md) · [`positioning-truth-tracer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/trace/positioning-truth-tracer/SKILL.md)
- **architect:** [`strategic-narrative-designer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/architect/strategic-narrative-designer/SKILL.md) · [`message-system-architect`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/architect/message-system-architect/SKILL.md) · [`brand-language-codifier`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/architect/brand-language-codifier/SKILL.md) · [`story-bank-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/architect/story-bank-builder/SKILL.md)
- **land:** [`narrative-cascade-planner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/land/narrative-cascade-planner/SKILL.md) · [`pitch-narrative-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/land/pitch-narrative-builder/SKILL.md) · [`narrative-enablement-kit`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/land/narrative-enablement-kit/SKILL.md) · [`proof-point-packager`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/land/proof-point-packager/SKILL.md)
- **evaluate:** [`narrative-quality-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/evaluate/narrative-quality-auditor/SKILL.md) · [`message-test-designer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/evaluate/message-test-designer/SKILL.md) · [`narrative-resonance-monitor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/evaluate/narrative-resonance-monitor/SKILL.md) · [`narrative-drift-monitor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/evaluate/narrative-drift-monitor/SKILL.md)

### SEO/GEO

- **survey:** [`keyword-research`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/survey/keyword-research/SKILL.md) · [`competitor-analysis`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/survey/competitor-analysis/SKILL.md) · [`serp-analysis`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/survey/serp-analysis/SKILL.md) · [`content-gap-analysis`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/survey/content-gap-analysis/SKILL.md)
- **implement:** [`content-writer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/implement/content-writer/SKILL.md) · [`geo-content-optimizer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/implement/geo-content-optimizer/SKILL.md) · [`serp-markup-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/implement/serp-markup-builder/SKILL.md) · [`page-play-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/implement/page-play-builder/SKILL.md)
- **tune:** [`content-quality-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/tune/content-quality-auditor/SKILL.md) · [`technical-seo-checker`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/tune/technical-seo-checker/SKILL.md) · [`on-page-seo-checker`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/tune/on-page-seo-checker/SKILL.md) · [`site-structure-optimizer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/tune/site-structure-optimizer/SKILL.md)
- **evaluate:** [`domain-authority-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/evaluate/domain-authority-auditor/SKILL.md) · [`rank-tracker`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/evaluate/rank-tracker/SKILL.md) · [`performance-monitor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/evaluate/performance-monitor/SKILL.md) · [`offsite-signal-analyzer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/evaluate/offsite-signal-analyzer/SKILL.md)

### Organic Social

- **explore:** [`channel-portfolio-planner`](../../channel-portfolio-planner/SKILL.md) · [`voice-dossier-builder`](../../voice-dossier-builder/SKILL.md) · [`platform-norm-profiler`](../../platform-norm-profiler/SKILL.md) · [`participation-warmup-planner`](../../participation-warmup-planner/SKILL.md)
- **craft:** [`social-calendar-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/social/craft/social-calendar-builder/SKILL.md) · [`social-creative-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/social/craft/social-creative-builder/SKILL.md) · [`short-video-scripter`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/social/craft/short-video-scripter/SKILL.md) · [`advocacy-program-designer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/social/craft/advocacy-program-designer/SKILL.md)
- **host:** [`social-quality-auditor`](../../social-quality-auditor/SKILL.md) · [`engagement-inbox-manager`](../../engagement-inbox-manager/SKILL.md) · [`social-selling-planner`](../../social-selling-planner/SKILL.md) · [`crisis-response-planner`](../../crisis-response-planner/SKILL.md)
- **observe:** [`social-pulse-monitor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/social/observe/social-pulse-monitor/SKILL.md) · [`share-of-voice-tracker`](../../share-of-voice-tracker/SKILL.md) · [`dark-social-attributor`](../../dark-social-attributor/SKILL.md) · [`social-measurement-loop`](../../social-measurement-loop/SKILL.md)

### Email Marketing

- **setup:** [`deliverability-qa`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/setup/deliverability-qa/SKILL.md) · [`list-segment-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/setup/list-segment-builder/SKILL.md) · [`list-growth-designer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/setup/list-growth-designer/SKILL.md) · [`list-hygiene-monitor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/setup/list-hygiene-monitor/SKILL.md)
- **engage:** [`email-creative-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/engage/email-creative-builder/SKILL.md) · [`subject-line-lab`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/engage/subject-line-lab/SKILL.md) · [`email-render-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/engage/email-render-builder/SKILL.md) · [`dynamic-content-personalizer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/engage/dynamic-content-personalizer/SKILL.md)
- **nurture:** [`email-sequence-designer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/nurture/email-sequence-designer/SKILL.md) · [`newsletter-monetization-planner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/nurture/newsletter-monetization-planner/SKILL.md) · [`preference-frequency-manager`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/nurture/preference-frequency-manager/SKILL.md) · [`reactivation-specialist`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/nurture/reactivation-specialist/SKILL.md)
- **deliver:** [`email-quality-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/deliver/email-quality-auditor/SKILL.md) · [`send-experiment-designer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/deliver/send-experiment-designer/SKILL.md) · [`inbox-placement-monitor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/deliver/inbox-placement-monitor/SKILL.md) · [`cold-outbound-sequencer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/deliver/cold-outbound-sequencer/SKILL.md)

### Paid Ads

- **research:** [`campaign-architect`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/research/campaign-architect/SKILL.md) · [`audience-segment-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/research/audience-segment-builder/SKILL.md) · [`search-term-miner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/research/search-term-miner/SKILL.md) · [`product-feed-optimizer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/research/product-feed-optimizer/SKILL.md)
- **orchestrate:** [`ad-creative-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/orchestrate/ad-creative-builder/SKILL.md) · [`ad-test-designer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/orchestrate/ad-test-designer/SKILL.md) · [`bid-strategy-planner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/orchestrate/bid-strategy-planner/SKILL.md) · [`landing-experience-checker`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/orchestrate/landing-experience-checker/SKILL.md)
- **activate:** [`ad-account-auditor`](../../ad-account-auditor/SKILL.md) · [`conversion-signal-qa`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/activate/conversion-signal-qa/SKILL.md) · [`placement-exclusion-manager`](../../placement-exclusion-manager/SKILL.md) · [`conversion-value-mapper`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/activate/conversion-value-mapper/SKILL.md)
- **scale:** [`paid-measurement-loop`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/scale/paid-measurement-loop/SKILL.md) · [`attribution-reconciler`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/scale/attribution-reconciler/SKILL.md) · [`budget-pacing-monitor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/scale/budget-pacing-monitor/SKILL.md) · [`fatigue-frequency-manager`](../../fatigue-frequency-manager/SKILL.md)

### Influencer Marketing

- **scout:** [`audience-mapper`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/scout/audience-mapper/SKILL.md) · [`trend-spotter`](../../trend-spotter/SKILL.md) · [`influencer-discovery`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/scout/influencer-discovery/SKILL.md) · [`fit-scorer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/scout/fit-scorer/SKILL.md)
- **target:** [`competitor-tracker`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/target/competitor-tracker/SKILL.md) · [`campaign-planner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/target/campaign-planner/SKILL.md) · [`brief-generator`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/target/brief-generator/SKILL.md) · [`budget-optimizer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/target/budget-optimizer/SKILL.md)
- **activate:** [`outreach-manager`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/activate/outreach-manager/SKILL.md) · [`creator-content-auditor`](../../creator-content-auditor/SKILL.md) · [`contract-helper`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/activate/contract-helper/SKILL.md) · [`content-amplifier`](../../content-amplifier/SKILL.md)
- **report:** [`landing-optimizer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/report/landing-optimizer/SKILL.md) · [`performance-analyzer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/report/performance-analyzer/SKILL.md) · [`roi-calculator`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/report/roi-calculator/SKILL.md) · [`report-generator`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/report/report-generator/SKILL.md)

### Product Launch

- **research:** [`positioning-mapper`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/research/positioning-mapper/SKILL.md) · [`launch-tier-planner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/research/launch-tier-planner/SKILL.md) · [`launch-window-planner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/research/launch-window-planner/SKILL.md) · [`early-access-designer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/research/early-access-designer/SKILL.md)
- **assemble:** [`message-house-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/assemble/message-house-builder/SKILL.md) · [`launch-asset-packager`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/assemble/launch-asset-packager/SKILL.md) · [`pricing-packaging-planner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/assemble/pricing-packaging-planner/SKILL.md) · [`sales-enablement-kit`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/assemble/sales-enablement-kit/SKILL.md)
- **mobilize:** [`launch-readiness-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/mobilize/launch-readiness-auditor/SKILL.md) · [`launch-day-conductor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/mobilize/launch-day-conductor/SKILL.md) · [`community-launch-runner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/mobilize/community-launch-runner/SKILL.md) · [`press-media-relations`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/mobilize/press-media-relations/SKILL.md)
- **prove:** [`launch-monitor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/prove/launch-monitor/SKILL.md) · [`launch-feedback-synthesizer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/prove/launch-feedback-synthesizer/SKILL.md) · [`launch-retro-analyzer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/prove/launch-retro-analyzer/SKILL.md) · [`momentum-planner`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/prove/momentum-planner/SKILL.md)

## Protocol Layer

The protocol layer contains 8 skills: [`entity-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/entity-registry/SKILL.md) · [`creator-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/creator-registry/SKILL.md) · [`offer-claims-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/offer-claims-registry/SKILL.md) · [`consent-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/consent-registry/SKILL.md) · [`launch-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/launch-registry/SKILL.md) · [`channel-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/channel-registry/SKILL.md) · [`narrative-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/narrative-registry/SKILL.md) · [`memory-management`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/memory-management/SKILL.md).

### Truth Registries

| Registry | Owner | Canonical stream | Projection | State machine |
|---|---|---|---|---|
| `entities` | [`entity-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/entity-registry/SKILL.md) | `memory/events/entities.ndjson` | `memory/projections/entities.json` | — |
| `creators` | [`creator-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/creator-registry/SKILL.md) | `memory/events/creators.ndjson` | `memory/projections/creators.json` | — |
| `claims` | [`offer-claims-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/offer-claims-registry/SKILL.md) | `memory/events/claims.ndjson` | `memory/projections/claims.json` | — |
| `consent` | [`consent-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/consent-registry/SKILL.md) | `memory/events/consent.ndjson` | `memory/projections/consent.json` | — |
| `launches` | [`launch-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/launch-registry/SKILL.md) | `memory/events/launches.ndjson` | `memory/projections/launches.json` | initial draft; draft→concept, concept→alpha, alpha→beta, beta→general-availability, general-availability→archived, archived→terminal |
| `channels` | [`channel-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/channel-registry/SKILL.md) | `memory/events/channels.ndjson` | `memory/projections/channels.json` | initial proposed; proposed→warming/retired, warming→active/paused/retired, active→paused/retired, paused→warming/retired, retired→terminal |
| `narrative` | [`narrative-registry`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/protocol/narrative-registry/SKILL.md) | `memory/events/narrative.ndjson` | `memory/projections/narrative.json` | — |

## Auditor Gates

| Auditor | Framework | Exclusive sink | Standalone contract |
|---|---|---|---|
| [`narrative-quality-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/narrative/evaluate/narrative-quality-auditor/SKILL.md) | TALE | `memory/audits/narrative/` | generated `references/auditor-runtime.md` |
| [`content-quality-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/tune/content-quality-auditor/SKILL.md) | CORE-EEAT | `memory/audits/content/` | generated `references/auditor-runtime.md` |
| [`domain-authority-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/evaluate/domain-authority-auditor/SKILL.md) | CITE | `memory/audits/domain/` | generated `references/auditor-runtime.md` |
| [`social-quality-auditor`](../../social-quality-auditor/SKILL.md) | ECHO | `memory/audits/social/` | generated `references/auditor-runtime.md` |
| [`email-quality-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/deliver/email-quality-auditor/SKILL.md) | SEND | `memory/audits/email/` | generated `references/auditor-runtime.md` |
| [`ad-account-auditor`](../../ad-account-auditor/SKILL.md) | ROAS | `memory/audits/ad/` | generated `references/auditor-runtime.md` |
| [`creator-content-auditor`](../../creator-content-auditor/SKILL.md) | STAR | `memory/audits/influencer/` | generated `references/auditor-runtime.md` |
| [`launch-readiness-auditor`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/mobilize/launch-readiness-auditor/SKILL.md) | RAMP | `memory/audits/launch/` | generated `references/auditor-runtime.md` |

## L1 Dependency

The seven core downstream builders must carry `narrative_canon_id`, `narrative_canon_version`, `claims_projection_offset`, `dependency_status`; `dependency_status` is exactly `verified | approved-fallback | blocked`.

- [`content-writer`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/seo-geo/implement/content-writer/SKILL.md)
- [`social-creative-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/social/craft/social-creative-builder/SKILL.md)
- [`email-creative-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/email/engage/email-creative-builder/SKILL.md)
- [`ad-creative-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/ad/orchestrate/ad-creative-builder/SKILL.md)
- [`brief-generator`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/influencer/target/brief-generator/SKILL.md)
- [`message-house-builder`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/assemble/message-house-builder/SKILL.md)
- [`launch-asset-packager`](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/2b9076d58d72d0ed86f5d4527ae0bfe06e9c43f4/launch/assemble/launch-asset-packager/SKILL.md)

## Symmetry Contract

Every discipline satisfies each column or cites a licensed deviation (see below); `check-architecture.py` enforces conform-or-declared and fails stale deviations.

| Discipline | Loop | Command | Registry | Gate(s) | Score surface |
|---|---|---|---|---|---|
| **Brand Narrative** | TALE (Trace -> Architect -> Land -> Evaluate) | `/narrative --phase trace\|architect\|land\|evaluate` | `narrative` (DEV-HUMANVIEW-NARRATIVE) | `narrative-quality-auditor` | profiles-only |
| **SEO/GEO** | SITE (Survey -> Implement -> Tune -> Evaluate) | `/seo-geo --phase survey\|implement\|tune\|evaluate` | `entities` | `content-quality-auditor` · `domain-authority-auditor` | Comparable overall (weighted-arithmetic-mean) · Default diagnostic (weighted-arithmetic-mean) |
| **Organic Social** | ECHO (Explore -> Craft -> Host -> Observe) | `/social --phase explore\|craft\|host\|observe` | `channels` | `social-quality-auditor` | profiles-only |
| **Email Marketing** | SEND (Setup -> Engage -> Nurture -> Deliver) | `/email --phase setup\|engage\|nurture\|deliver` | `consent` | `email-quality-auditor` | EQS (weighted-arithmetic-mean) |
| **Paid Ads** | ROAS (Research -> Orchestrate -> Activate -> Scale) | `/ad --phase research\|orchestrate\|activate\|scale` | `claims` | `ad-account-auditor` | RQS (weighted-arithmetic-mean) |
| **Influencer Marketing** | STAR (Scout -> Target -> Activate -> Report) | `/influencer --phase scout\|target\|activate\|report` | `creators` | `creator-content-auditor` | SQS (weighted-arithmetic-mean) |
| **Product Launch** | RAMP (Research -> Assemble -> Mobilize -> Prove) | `/launch --phase research\|assemble\|mobilize\|prove` | `launches` (DEV-HUMANVIEW-LAUNCHES) | `launch-readiness-auditor` | profiles-only |

### Licensed Deviations

| ID | Rule | Scope | Since | Rationale |
|---|---|---|---|---|
| `DEV-HUMANVIEW-LAUNCHES` | `SYM-09-human-view` | `registry:launches` | 18.0.0 | memory/launch/<skill>/ is the launch discipline's working-notes namespace, and the dossier/calendar view predates v18 in end-user projects; renaming the human view would orphan user state. (source: `references/skill-contract.md`) |
| `DEV-HUMANVIEW-NARRATIVE` | `SYM-09-human-view` | `registry:narrative` | 18.0.0 | memory/narrative/<skill>/ is the narrative discipline's working-notes namespace, and canon.md/versions.md predate v18 in end-user projects; renaming the human view would orphan user state. (source: `references/skill-contract.md`) |

## Distribution Profiles

| Profile | Shared root references | Executable runtime | Auditor contract |
|---|---|---|---|
| `repository` | True | True | root references plus typed scorer |
| `standalone-skill` | False | False | generated immutable references/auditor-runtime.md |
| `npx-skills` | False | host-dependent | skill directory including generated references |

Generated from the typed catalog; edit the JSON source and regenerate.
