# Security Policy

## Reporting a vulnerability

**Please do not open a public issue.** Use GitHub's private vulnerability reporting on the
affected repository (the **Security** tab, then **Report a vulnerability**), which is visible
only to the maintainer.

Useful things to include, to whatever extent you have them: what an attacker gains, the
conditions under which it works, and the smallest sequence that shows it. A concrete
reproduction is worth more than a severity label.

## Scope, stated honestly

The Helios projects are pre-release and built in the open. Until a version is released, there
is no supported version; once releases exist, the supported version of each project is its most
recent release. This is a one-person project with no capacity to backport fixes to older
releases, and saying so plainly is better than implying a support window that will not be
honoured.

## What this software is

A BBS is a network service that accepts untrusted input over Telnet, SSH, HTTP, SMTP and FTP,
runs sysop-supplied scripts, executes external door programs, and exchanges mail with other
systems over store-and-forward networks. Several of those are trust boundaries, and they are
treated as such in the design rather than being hardened later: every feature brief carries its
threat model before any code exists.

## Anti-abuse

The load-test harness is deliberately not published. It drives the real Telnet, SSH, WebSocket
and API surfaces under configurable concurrent load, which also makes it a load generator
pointed at whatever host it is given. It stays private until the engine's abuse controls are
proven under it and the harness refuses to run against a board whose operator has not opted in.
