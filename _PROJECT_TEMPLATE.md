<!--
PROJECT README TEMPLATE
Copy the structure below into each project's README.md and fill it in as you build.
Keep it project-first: this describes a thing you built, not a lesson you took.
Delete this comment block when you start.
-->

# <Project Title>

> One-line description of what this project is and does.

**Status:** 🚧 In Progress
**Services:** `IAM` · `VPC` · `EC2` (list the AWS services used)
**Homelab tie-in:** (e.g. "Raspberry Pi acts as the on-prem backup source") — or remove if none.

---

## Architecture

<!-- Add a diagram. Until you have one, describe the flow in text.
     Tools: draw.io / Excalidraw / Mermaid. Save images to ../assets/ -->

```
[ describe or embed the architecture diagram here ]
```

---

## Problem it solves

The real need this design addresses — what would go wrong, cost more, or be insecure without it.

## What was built

A concrete list of the components and how they connect:

- Component A — role
- Component B — role
- Component C — role

## Key decisions

The reasoning behind the choices. This is what gets probed in interviews, so capture it:

- **Why X over Y?** — ...
- **Why this subnet/SG/policy design?** — ...
- **Trade-offs accepted** — ...

---

## Deploy it

Reproducible steps (CLI commands, console steps, or Terraform).

```bash
# example
aws sts get-caller-identity
```

## Verify it works

How to confirm the thing actually does what it should.

```bash
# example check
```

---

## Validation (proof I own this)

The point of this section: this project isn't a copied tutorial — I rebuilt it from scratch
with no instructions and can defend it. Fill in after a blind rebuild.

- ✅ **Rebuilt from scratch without notes** on <date>, in <sandbox/Pi>.
- 🔧 **One thing that broke during the blind rebuild and how I fixed it:** ...
  _(This is your best interview story — a real failure you debugged.)_
- 💬 **Two questions I can now answer about this:**
  1. _Q:_ ... — _A:_ ...
  2. _Q:_ ... — _A:_ ...

---

## Gotchas & cost notes

- ⚠️ Things that commonly trip people up.
- 💰 Anything that costs money / must be torn down to avoid charges.

## Teardown

Remove everything created, in the right order.

```bash
# delete resources here
```

---

## Skills demonstrated

`skill-one` · `skill-two` · `skill-three`

## References

- [Official doc used](https://docs.aws.amazon.com/)
