# 8W Research

**AI for the fields it skipped.**

Not because the problems are easy, and not because nobody has tried. Because the
work needed to make them tractable is unglamorous: a decade of domain simulation
nobody wants to rewrite, spatial data in a dozen incompatible projections, and a
user who has a question rather than a dataset.

---

## Why these fields

The interesting gap is not model capability. Frontier models are already good
enough for most of what forestry, land management, agriculture and public
utilities actually need.

The gap is that in these fields **the answer does not exist until someone
computes it**. Ask which forest stands can supply a power plant at a workable
cost and no document contains the answer. It has to be produced — from terrain,
from road networks, from harvest economics, from fire risk — by models that take
minutes to hours to run, over data measured in hundreds of millions of rows.

So retrieval over documents fails. There is nothing to retrieve. What is needed
is retrieval over *computation*: precompute the expensive surfaces, index them
spatially, and let an agent compose them at conversational speed.

That is what we build.

The people who need these answers are planners, agency staff, cooperatives and
small operators. They do not have a GIS team. Today the answer costs a
consulting engagement and several weeks. It should cost a sentence.

---

## What we have built

**[FRED](https://biofred.us)** — conversational decision support for forest
biomass procurement in California. Ask where to site a facility, what it will
cost to feed it, and how much wildfire risk the harvest removes. Get a sited
location, a cost-optimal supply curve and a map, in about the time it takes to
read the question.

| | |
|---|---|
| Statewide harvest-cost predictions | **166 million** |
| Forest clusters indexed in PostGIS | **3.1 million** |
| Pre-computed truck routes | **445,000** |
| Cost surrogate accuracy | **R² 0.9965**, ~5,479× faster than the simulator |

That surrogate is the pattern in miniature. The underlying model, FRCS, is a
well-validated harvest-cost simulator that is far too slow to sit inside a
conversation. Learning it to R² 0.9965 turns a batch process into something a
person can interrogate — without discarding the domain science it encodes.

The architecture behind it, **Compositional Spatial RAG**, generalises past
forestry. Any field with expensive spatial models and non-technical decision
makers has the same shape.

---

## How we work

**Source-available, free for research.** Everything here is published under the
[PolyForm Noncommercial License](https://polyformproject.org/licenses/noncommercial/1.0.0).
Universities, public research organisations, government bodies and environmental
non-profits may use it freely, regardless of how their work is funded. Read it,
fork it, build on it, publish what you find.

Commercial use is a separate licence — that is what funds the free half.

**We write things down.** The methodology is documented in public at
[docs.biofred.us](https://docs.biofred.us), including where the models break.
A tool that hides its assumptions from the people relying on it is worse than
no tool.

---

## Who we are

We started as researchers in grad school, building things that answered a real
question for people who would never read the paper. The tools stayed in the lab.
The people who needed them kept paying consultants. 8W Research exists to close
that gap.

**Aunsh Bandivadekar** — *Lead*
Electrical and Computer Engineering, UC Davis · Built the spatial prediction
layers and the agent architecture behind FRED · [LinkedIn](https://linkedin.com/in/aunsh)

**VKL** — *Network Chief*
Computer Science · Keeps the network from falling over ·
[LinkedIn](https://linkedin.com/in/vkl)

**Parth** — *Chem Wizard*
Chemistry · Maintains that every hard problem is a chemistry problem, and is
usually right ·
[LinkedIn](https://linkedin.com/in/parth)

---

## Repositories

| | |
|---|---|
| [`fred`](https://github.com/eight-west/fred) | The agent, the spatial models and the interface |
| [`fred-docs`](https://github.com/eight-west/fred-docs) | Methodology and user documentation |
| [`fred-studio`](https://github.com/eight-west/fred-studio) | Content schema for the writing |

---

## Get in touch

Working on a decision problem with the same shape, or wanting to use this
commercially — **contact@biofred.us**.

If you are at a university or a public research organisation, you already have
what you need under the licence. Write anyway if you are building on the method.

<sub>Developed at the Merge.</sub>
