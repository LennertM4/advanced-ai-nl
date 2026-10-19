# Build log

| Date | Version | What I did | Result | Errors or observations | Next step |
| --- | --- | --- | --- | --- | 
| 2026-09-24 | v1 | Created a fixed prompt for classifying Outlook emails. | Ready to run on T01–T05. | Not tested yet. | Run every input twice and record the labels. |
| 2026-09-24 | v1 | Ran T01 once in a fresh Codex conversation. | `lezen`, matching the expected label. | No error observed. | Run T01 a second time in a new conversation. |
| 2026-09-24 | v1 | Ran T01 a second time in a fresh Codex conversation. | `lezen`, matching the expected label again. | No variation between the two runs. | Run T02 with T01 as the earlier email. |
| 2026-09-24 | v1 | Ran T02 once in a fresh Codex conversation, with T01 supplied as the earlier email. | `herhaling`, matching the expected label. | No error observed. | Run T02 a second time in a new conversation. |
| 2026-09-24 | v1 | Ran T02 a second time in a fresh Codex conversation. | `herhaling`, matching the expected label again. | No variation between the two runs. | Run T03 twice. |
| 2026-09-24 | v1 | Ran T03 once in a fresh Codex conversation. | `doen`, matching the expected label. | No error observed. | Run T03 a second time in a new conversation. |
| 2026-09-24 | v1 | Ran T03 a second time in a fresh Codex conversation. | `doen`, matching the expected label again. | No variation between the two runs. | Run T04 twice. |
| 2026-09-24 | v1 | Ran T04 once in a fresh Codex conversation. | `negeren`, matching the expected label. | No error observed. | Run T04 a second time in a new conversation. |
| 2026-09-24 | v1 | Ran T04 a second time in a fresh Codex conversation. | `negeren`, matching the expected label again. | No variation between the two runs. | Run T05 twice. |
| 2026-09-24 | v1 | Ran T05 once in a fresh Codex conversation. | `lezen`, matching the expected label. | No error observed. | Run T05 a second time in a new conversation. |
| 2026-09-24 | v1 | Ran T05 a second time in a fresh Codex conversation. | `lezen`, matching the expected label again. | No variation between the two runs. | Summarise the first measurement. |
| 2026-09-24 | v1 | Completed the first measurement on T01–T05. | 10/10 correct runs; no variation observed. | Only five school-email inputs and one duplicate pair: too small to generalise. | Add five more varied inputs and test v2 in week 3. |
| 2026-10-17 | v2/v3 | Prepared the week-4 checkpoint files, extended the test set to ten inputs and documented the cost-measurement method. | Existing evidence is 9/10 for v2 and 1/1 for the targeted v3 rerun. | A full second run and exact `/context`/`/cost` readings are not available in this session. | Run T01–T10 again in fresh conversations and fill `kosten.md`. |
| 2026-10-19 | v3 | Reviewed the week-4 evidence and separated measured results from the cost example. | No invented token or dollar values added; the post remains within the required 500–800 words. | The external Codex session needed for `/context` and `/cost` is still unavailable here. | Record the real values and the complete second pass before submitting. |
| 2026-10-19 | v3 | Ran T01–T10 again in ten separate fresh Codex sessions. | 10/10 correct; no classification errors observed. | This is a second measurement of v3, not proof of long-term reliability. | Measure the run cost and update the post. |
| 2026-10-19 | v3 | Ran T01 in a new Codex session to measure token usage. | 14,784 input tokens (6,656 cached) and 10 output tokens; estimated cost €0.00080 using the course price assumption. | The reported model was `gpt-5.6-luna`, not the exact model name in the course table. | Keep the model and price assumption visible in the cost notes. |
