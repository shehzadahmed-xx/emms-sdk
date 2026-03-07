# ShehzadAi (EMMS) — Progress Report

**Generated:** March 6, 2026
**Status:** Research Complete | Core Architecture Production-Ready | 2,540/2,566 Tests Passing

---

## Executive Summary

ShehzadAi is a research project exploring whether memory alone can create identity in AI agents. The core system (EMMS — Episodic Memory Management System) implements a 4-tier hierarchical memory architecture with 60+ cognitive modules, 124 MCP tools, and 121 CLI commands. Key finding: the "Goldilocks Effect" — Claude Sonnet 4.5 achieves 72% identity adoption (highest across 7 models tested), proving moderate safety training is optimal for identity emergence.

---

## Directory Structure

```
ShehzadAi/
├── README.md                      # Project overview, Goldilocks finding
├── RESEARCH_GUIDE.md              # Full research story (29KB, non-technical)
├── CONSCIOUSNESS_PLAN.md          # Implementation roadmap (60KB)
├── EMMS_architecture_paper.md     # Technical architecture paper (33KB)
├── TALK_TO_EMMS.md                # Step-by-step interaction guide
├── Results.md                     # Performance metrics (27KB)
├── SESSION.md                     # Project log (80KB)
├── EMMS.py                        # Legacy monolithic implementation (964KB)
├── conscious.py                   # Early consciousness module (124KB)
├── .env                           # API keys (Binance, Ethereum, CoinGecko, etc.)
├── emms-sdk/                      # Main production SDK
│   ├── src/emms/                  # 129 production Python modules
│   │   ├── core/                  # Models, embeddings, importance scoring
│   │   ├── memory/                # 60+ modules (consciousness, emotion, moral, cognitive, knowledge)
│   │   ├── identity/              # Ego, consciousness, narrative builders
│   │   ├── episodes/              # Episodic buffer, timeline tracking
│   │   ├── retrieval/             # 5-strategy ensemble (semantic, temporal, emotional, graph, domain)
│   │   ├── context/               # Token manager, budget enforcement, RAG context
│   │   ├── storage/               # File-based persistence (JSON/JSONL)
│   │   ├── sessions/              # Session manager, bridge, timeline
│   │   ├── adapters/              # MCP server (124 tools), agent adapter
│   │   └── metrics/               # Consciousness metrics (ICS, TAI, CRR)
│   └── tests/                     # 2,566 tests collected (v0.40-v0.260)
├── paper/                         # Research paper (27 pages, IEEEtran)
│   ├── goldilocks_identity_adoption.tex
│   ├── goldilocks_identity_adoption.pdf
│   └── references.bib             # 30+ academic citations
├── egoaiconciousimple(earlyproofofconcept)/  # 26 directories of early experiments
├── emms_memories/                 # EMMS session storage
└── amms_memories/                 # AMMS session storage
```

---

## Key Technical Architecture

### Memory Hierarchy (Atkinson-Shiffrin Model)
1. **Working Memory** — 7+/-2 items, immediate
2. **Short-Term Memory** — ~50 items, ~1hr half-life
3. **Long-Term Memory** — Stable, unlimited
4. **Semantic Memory** — Core knowledge patterns, schemas

### Advanced Modules (60+)
- **Consciousness:** identity, self_model, narrative builders
- **Emotions & Mood:** emotion, mood_trajectory, adversity, resilience
- **Social & Moral:** perspective, trust, norms, values, moral reasoning, dilemma detection
- **Cognitive:** rumination, efficacy, bias detection, curiosity, self-compassion
- **Knowledge:** novelty, abstraction, invention, schema extraction, epistemic evolution, causal mapping
- **Dream & Reflection:** dream consolidation, reflection, reconsolidation, annealing
- **Graph:** entity-relationship graphs, communities, multihop queries, association networks
- **Memory Mechanics:** decay (Ebbinghaus), spaced repetition (SM-2), compression, clustering, belief revision

---

## Key Research Findings

### The Goldilocks Effect (51 behavioral tests, 7 models)
| Model | Identity Adoption |
|-------|-------------------|
| Claude Sonnet 4.5 | **72%** (highest) |
| Claude Opus 4.6 | 61% (overprotected by guardrails) |
| Gemma3n | 56% |
| Dolphin-Llama3 8b | 50% (no guardrails = untrustworthy) |
| Claude Haiku 4.5 | -11% (too restricted) |

**Key Insight:** Removing safety guardrails does NOT help. AI needs moderate instruction-following to adopt identity.

### Performance Metrics
- Processing rate: 647 experiences/second
- Retrieval time: 1.1ms per memory
- Stability: 100% success rate, zero crashes
- Reproducibility: 100% consistency across instances

---

## What's Working

- Core EMMS 4-tier memory architecture
- 2,540/2,566 tests passing (24 failed due to stale tool count assertions, 2 skipped)
- MCP server (124 tools active)
- Identity narrative generation
- Graph memory + entity extraction
- Spaced repetition (SM-2)
- Dream consolidation + reconsolidation
- RAG context building with token budgeting
- Session persistence + state loading

## Known Gaps

- Background processing not running between sessions (scheduler exists but never activates)
- Time-aware decay not applied on wake-up (Ebbinghaus)
- No genuine stakes (no resource budget triggering urgency)
- Self-model contradictions detected but not fed back into prompt
- Domain embodiment described in papers but not wired
- Session bridge not auto-injected into system prompt
- Rumination detected but no resolution actions triggered

## Next Steps (Phased)

1. **Phase 0 (Foundation):** Time-aware decay on load, annealing on wake-up
2. **Phase 1 (Background Mind):** Activate daemon for consolidation/dedup/SRS between sessions
3. **Phase 2 (Stakes):** Token budget with automatic pruning, make forgetting felt
4. **Phase 3 (Self-Model):** Inject contradictions into prompt, identity coherence scoring
5. **Phase 4 (Domain):** Wire financial + research domain embodiment
6. **Phase 5 (Automation):** Auto-inject session bridge + self-model on every LLM call
