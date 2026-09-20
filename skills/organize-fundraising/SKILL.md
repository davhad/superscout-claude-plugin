---
name: organize-fundraising
description: Use when a founder wants to turn known investors or programs into a private Superscout shortlist, record notes, track follows, or maintain fundraising preferences.
version: 1.0.0
---

# Organize fundraising

Use Superscout as the user's private decision workspace for known targets.
This plugin does not expose broad discovery or bulk database search.

## Workflow

1. Read the user's existing investment preferences and relevant lists before
   creating duplicates.
2. Clarify the shortlist purpose, such as current raise, accelerator options,
   regional targets, or follow-up queue.
3. Create or update one private list. Add only exact visible Superscout target
   IDs supplied by the user or returned by an authorized Superscout tool.
4. Keep concise decision notes on list items. Separate observed facts from the
   user's judgment.
5. Use `check_fit` only when the user names an exact investor or program and
   supplies the material company context.
6. Follow a target only when the user asks to retain that follow state.

Before any write, state the exact list, item, preference, follow, or private
organization record that will change. Create operations require a stable
`request_id`; reuse it only for an exact retry. Re-adding a list item preserves
its notes, so use `update_list_item` when the notes should change.

Never present a list as an endorsement, promise alerts that do not exist, or
claim that a private organization record changes Superscout's public data.
