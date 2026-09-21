# Superscout Platform plugin for Claude

The Superscout Platform plugin gives founders, startup operators, scouts,
angels, and VCs guided workflows in Claude for:

- checking one exact investor or startup program against a company
- organizing a private fundraising shortlist
- maintaining a private scouting thesis and investment preferences
- managing Superscout profile, persona, list, follow, and private organization
  data

It connects Claude to the existing, directory-approved, OAuth-protected
Superscout Platform MCP at `https://platform.superscout.co/mcp`.

It contains no credentials or database logic. Installation starts Superscout
OAuth, and tool discovery is filtered to the scopes granted by the connected
account. Customer tools operate only on that account's own workspace data.
Operator research, editorial, canonical synchronization, admin, billing, and
publication workflows are intentionally absent from this package's guidance.

## Included skills

- `superscout-platform`: safely inspect or change the connected user's own
  Superscout workspace
- `check-investor-or-program-fit`: run a bounded fit check for one exact
  Superscout investor or program
- `organize-fundraising`: turn known targets into a private shortlist with
  decision notes
- `manage-venture-scouting`: maintain a Scout declaration, personal investment
  preferences, private organizations, lists, and follows

## Example prompts

- "Check whether the investor at this Superscout page fits my pre-seed company."
- "Create a private shortlist for my current raise and add these Superscout targets."
- "Review my scouting profile and investment preferences for inconsistencies."
- "Show my Superscout profile, personas, lists, and follows."

## Install directly from GitHub

In Claude Code, add the public Superscout marketplace and install the plugin:

```text
/plugin marketplace add davhad/superscout-claude-plugin
/plugin install superscout-platform@superscout-platform
```

After community-directory approval, users can install Superscout Platform from
Claude's plugin directory in Claude, Claude Desktop, Cowork, or Claude Code.

The public distribution repository for this Claude-only package is
`davhad/superscout-claude-plugin`. The Superscout Platform server and packages
for other AI platforms are maintained separately in Superscout's private
monorepo.

## Privacy and safety

Superscout receives only the inputs sent in explicit tool calls, not the
surrounding Claude conversation. OAuth fixes the actor to the connected account,
and every tool is limited to the scopes that user approves. The plugin does not
support broad people, investor, or startup database export.

- Documentation: https://platform.superscout.co/docs
- Support: https://platform.superscout.co/support
- Privacy: https://new.superscout.co/privacy
- Terms: https://new.superscout.co/tos
