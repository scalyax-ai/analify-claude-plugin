---
name: save
description: Save something to your Analify Business Brain right now — a finding, a decision, a business rule, or a report file — so the next conversation starts from it.
argument-hint: "[what to save, or a file path]"
disable-model-invocation: true
---

# Save to your Business Brain

The user asked for this save, so it is approved. What to save: $ARGUMENTS (if empty, save the important findings and decisions from this conversation so far). Save only what is about this business.

1. Start or confirm the session with `analify_brain_session_start` (one session id for this conversation).
2. A file the user names (Markdown, CSV, text): `analify_call_write_tool` with tool_name `analify_brain_files_post`, arguments `{ filename, text: <the file's content>, import: true }`.
3. A finding worked out from data: `analify_call_write_tool` with tool_name `analify_brain_remember`, arguments `{ question, answer, toolsUsed }`. The answer states the finding with its numbers and period; `toolsUsed` lists the Analify tools you actually called.
4. A decision, business rule, test or procedure: `analify_brain_capture` with the session id, a new eventId, kind (fact, decision, constraint, experiment or procedure), a one- or two-sentence statement, the date it happened, decisionItImproves and entities. A recommendation the owner has not approved is kind experiment, never a rule.
5. A rule the owner stated in their own words: `analify_call_write_tool` with tool_name `analify_brain_statements`, arguments `{ text }`.
6. Never send passwords, keys, or customers' names, phone numbers, emails or addresses. If Analify refuses a save, read the reason and fix it once; if it is still refused, tell the user exactly what was not saved.
7. Say in one line what was saved.
