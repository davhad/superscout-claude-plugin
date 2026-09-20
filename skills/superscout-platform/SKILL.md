---
name: superscout-platform
description: Use when a user wants to inspect, summarize, or safely change their own Superscout profile, personas, Scout declaration, investment preferences, private lists, follows, or private organization records.
version: 1.0.0
---

# Superscout Platform

Use the Superscout Platform tools when the user asks to inspect or change their
own Superscout workspace. The connected OAuth identity is always the actor.
Never ask for, infer, or send an owner ID.

Start with the smallest read that establishes current state. When the request
spans several areas, build a concise workspace overview from the profile,
personas, Scout declaration, investment preferences, lists, follows, and
private organizations that are relevant to the user's goal. Do not fetch every
collection by default.

Before a write, state the exact record and fields that will change. Treat
profile fields as potentially public when the returned profile reports
`public_fields_changed`. Keep investment ticket amounts as whole major currency
units and always use the record's ISO currency code. Use the opaque cursor from
the previous response to continue a list operation.

Create operations require a stable `request_id`. Reuse the same value only for
an exact retry of the same operation and payload. `PUT` tools set a desired
state and are safe to retry. For list items, re-adding an existing target keeps
its current notes. Use the dedicated update tool when notes should change.

Do not imply that a persona or Scout declaration grants a verified role,
investment authority, admin access, or any paid entitlement. Following a target
only changes the user's following state. It does not promise alerts or
notifications.

The connector does not provide broad people, investor, or startup search. Do
not claim that it searched Superscout's full database. Exact investor and
program fit checks use the separate `check_fit` workflow. Canonical profile
editing, publication, approval, billing, operator research, and bulk export are
outside this plugin.
