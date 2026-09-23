# Contributing

Thank you for wanting to help. Read the repository's `CONSTITUTION.md` first; it is short and
it is what every change is measured against.

## How work happens

Every change starts as a feature brief in `features/`, owned by the maintainer. The
specifications in `docs/spec/` are derived from the briefs, and code is derived from the
specifications. A pull request that does not trace back to a feature has nothing to attach to.

Work is tracked in GitHub Issues, using the issue form, which asks for the files, the exact
change, the reason, whether the change is security-sensitive, and a plan. Pull requests target
`development`, close their issue, and merge through the merge queue once the required checks
pass. `make check` in the repository is the one definition of green.

## What is useful

- **Issues.** Feature requests, questions about intended behaviour, and notes from running
  VBBS, VADV or any other classic system that we should know about before a design is settled.
  A well-argued "this is how it actually worked, and here is why it mattered" is worth more
  than a patch at this stage.
- **The spin-off projects**, which are real repositories and are not gated on the engine. The
  Door Kit in particular is a wire protocol meant for other BBS software to implement, and it
  is permissively licensed for exactly that reason.

## Licensing of contributions

By opening a pull request you offer your contribution under the terms in that repository's
`LICENSE` (and `LICENSE.exception` where one exists). There is no separate contributor licence
agreement.

**Scripts and themes you write for your own board are yours.** The engine's Scripting API
Exception exists so that sysop-authored Lua that reaches the engine only through the public
`bbs.*` API is not a derivative work of the engine. You are not contributing those by writing
them, and you never owe anyone their source.

## Security

Do not open a public issue for a vulnerability. See `SECURITY.md`.
