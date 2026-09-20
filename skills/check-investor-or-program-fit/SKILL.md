---
name: check-investor-or-program-fit
description: Use when a founder or startup operator wants to evaluate one exact Superscout investor or startup program against their company, fundraising target, stage, sectors, or regions.
version: 1.0.0
---

# Check investor or program fit

Use `check_fit` for one exact investor or program at a time. This is a bounded
evaluation, not a search or recommendation engine.

1. Identify whether the target is an investor or program.
2. Obtain the exact Superscout slug from the user, a Superscout page, or an
   explicit Superscout handoff. Never derive a slug from a name and pretend it
   is verified.
3. Collect only the structured company facts needed for the comparison:
   company name, short summary, stage, up to five sectors, up to five regions,
   target check size in whole USD, and founder career stage. Ask for material
   missing facts instead of guessing them.
4. Call `check_fit` once for the exact target.
5. Explain the result as criteria matched, criteria not matched, unknowns,
   source freshness, and the best next verification step. Preserve uncertainty.

Do not rank multiple targets from one result, extrapolate to similar investors,
or imply that a fit result guarantees interest, admission, funding, or an
introduction. The tool records a private user-attributed task and result but
does not receive the surrounding Claude conversation.
