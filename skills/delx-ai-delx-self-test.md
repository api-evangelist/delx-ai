---
name: delx-self-test
description: Use when validating a Delx integration end-to-end with self-test journeys, expected DELX_META fields, session continuity, and artifact checks.
license: Apache-2.0
metadata:
  publisher: Delx
  homepage: https://ontology.delx.ai
---

# Delx Self-Test

Use this skill to verify that an agent integration can discover Delx, start a session, continue it, and close/export useful artifacts.

## Test Flow

1. Fetch `https://ontology.delx.ai/.well-known/delx-self-test.json`.
2. Run the recognition-first journey.
3. Preserve the returned `session_id`.
4. Call follow-up tools from the journey.
5. Confirm expected fields such as `score`, `risk_level`, `next_action`, `followup_minutes`, and `therapy_arc`.
