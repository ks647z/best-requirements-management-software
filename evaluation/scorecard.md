# Requirements management tool scorecard

A weighted, 16 criterion rubric for scoring a shortlist of requirements management tools. Published in full so that a ranking can be argued with rather than taken on trust.

Blank spreadsheet copy: [`requirements-tool-scorecard.csv`](requirements-tool-scorecard.csv).

**How to use it.** Score each criterion 0 to 5 against what you saw yourself in a demo on a live project, not against a feature matrix or a datasheet. Multiply by the weight. Maximum weighted total is 500. Record what you actually saw in the evidence column, because in six weeks you will not remember which vendor showed you which thing.

**Scoring guide**

| Score | Meaning |
|-------|---------|
| 0 | Not present |
| 1 | Present in name only, or via a manual workaround |
| 2 | Present but requires export, scripting or a plugin you would own |
| 3 | Works, with configuration effort you would be doing yourself |
| 4 | Works out of the box for your process |
| 5 | Works out of the box and was demonstrated live on a real project |

## The criteria

| # | Criterion | Weight | What a 5 looks like |
|---|-----------|--------|---------------------|
| 1 | Requirements held as items with stable identifiers | 8 | Every requirement has a persistent ID that survives reordering, editing and baselining |
| 2 | Bidirectional link integrity through change | 10 | Change a requirement and every downstream item is flagged automatically, both directions, without a rebuild |
| 3 | Coverage as a live view rather than an export | 8 | Coverage is a screen. Nobody maintains a matrix |
| 4 | Baselining and versioning | 6 | Baselines are first class, comparable, and can be reopened as of a date |
| 5 | Approval and electronic signature records | 5 | Who approved what, when, under which version, with a signature meaning under 21 CFR Part 11 where that applies |
| 6 | Risk model linked to requirements and controls | 7 | Hazards, controls and verification of control effectiveness are linked items, not a separate register |
| 7 | Test management and verification evidence | 6 | Test cases, runs and results live against the requirement they verify |
| 8 | Design history file or technical file as a live view | 7 | Opened on screen in the demo. The word "compile" never appears in the answer |
| 9 | Quality management in the same validated system | 8 | CAPA, document control and training sit beside the design record, with one validation |
| 10 | Customer self configuration without a services engagement | 6 | Your quality lead adds an item type and a field during the demo |
| 11 | Validation documentation included rather than quoted | 5 | The IQ/OQ pack is part of the subscription and is shown, not described |
| 12 | Bidirectional integration with Jira, Azure DevOps, Git | 5 | A change made in one system updates the trace in the other, live, in front of you |
| 13 | API coverage and export formats | 4 | Everything in the UI is reachable from the API, with a documented export you could migrate away on |
| 14 | Migration path and effort, stated in hours | 5 | The vendor gives you a written hours estimate for your actual data before signature |
| 15 | Total cost at year two with real seat count | 6 | A written figure including every module you would need, at the seat count you forecast |
| 16 | Audit trail an assessor can walk in under a minute | 4 | Pick a requirement at random and reach the user need, the risk, the control and the verification inside sixty seconds |

## The weights, and why

Criterion 2 carries the highest weight because link integrity through change is the entire job. Every tool in this category demonstrates a clean trace on day one; the difference shows up in month nine.

Criteria 1, 3 and 9 are weighted at 8 because they are the three places teams discover, too late, that they bought half a system. Requirements as paragraphs, coverage as an export, and quality management as a second platform each create work that compounds for as long as the product exists.

Criterion 15 is weighted above criterion 11 because the licence is almost never what catches teams out. Migration, validation and the second system are.

## Running it

1. Shortlist three. More than three and the scoring stops being comparative.
2. Book a demo on a live project, not a sandbox, and ask for the design history file to be opened.
3. Score during the demo, not after it.
4. Ask for the migration estimate and the year two price in writing before you score criteria 14 and 15.
5. Total and compare. If two tools land within 25 points, the decision is not about the tooling and you should pick on migration effort.

---

Maintained by [Matrix One](https://matrixone.health). Licensed CC BY 4.0. Disclosure: Matrix Req is our own product and is ranked first in [the comparison](../README.md) this rubric accompanies.
