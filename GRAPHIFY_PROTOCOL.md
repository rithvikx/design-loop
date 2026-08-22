# Graphify Integration Protocol

## Purpose

Graphify provides a persistent structural representation of the project's
codebase.

The Design Loop should use Graphify as a codebase-awareness layer rather than
treating the repository as a collection of unrelated files.

---

# 1. INITIAL GRAPH

At the beginning of a new project, determine whether Graphify is already
available.

If no graph exists and Graphify is installed:

run the platform-appropriate Graphify initialization.

For example:

/graphify .

Do not claim success unless the graph was actually generated.

---

# 2. CODEBASE AWARENESS

Before major architectural changes:

use Graphify when available to understand:

- dependency relationships
- component relationships
- route relationships
- service relationships
- data relationships
- affected code areas

Use the graph when the question spans multiple files or architectural layers.

---

# 3. FINALIZATION UPDATE

After the Design Loop reaches an accepted implementation state:

update the Graphify graph.

Preferred incremental operation:

/graphify . --update

Do not rebuild from scratch when an incremental update is sufficient.

---

# 4. WHEN TO UPDATE

Run a Graphify update after:

- a major feature implementation
- significant architecture changes
- component restructuring
- route restructuring
- backend changes
- database/schema changes
- final accepted implementation

Do not run a full graph rebuild after every trivial CSS change.

---

# 5. FINAL COMPLETION RULE

The final completion sequence is:

ACCEPT IMPLEMENTATION
→ VERIFY
→ UPDATE GRAPHIFY
→ VERIFY GRAPHIFY
→ RECORD STATE
→ COMPLETE

The project should not be reported as fully finalized until the Graphify state
is synchronized, unless Graphify is unavailable.

---

# 6. GRAPHIFY FAILURE

If Graphify fails:

1. record the failure
2. identify the error
3. attempt a reasonable recovery
4. if recovery fails, mark Graphify as NOT VERIFIED
5. do not fabricate successful synchronization

---

# 7. GRAPH MEMORY

The Design Loop may use Graphify to answer questions such as:

- Where is this component used?
- Which routes depend on this component?
- What will break if this API changes?
- Which files implement this feature?
- What architecture is currently present?

Do not assume inferred graph relationships are guaranteed.

Respect Graphify's distinction between extracted, inferred, and ambiguous
relationships.

# GAUNTLET CODEBASE AWARENESS

When the Gauntlet identifies a high-impact issue, use Graphify when available
to understand which components, routes, and dependencies may be affected by
the proposed fix.

Do not treat visual changes as isolated if they depend on shared architecture.

Before large changes:

inspect dependency relationships.

After accepted changes:

update Graphify.

This helps prevent a Gauntlet fix from creating hidden architectural
regressions.

---

# END OF GRAPHIFY PROTOCOL
