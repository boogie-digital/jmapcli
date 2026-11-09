# jmapcli

**JMAP from the command line.** A fast, native macOS command-line client for [JMAP](https://jmap.io) and [Stalwart Mail Server](https://stalw.art) — send, read, search, sync and manage your mail straight from the terminal.

By [Boogie](https://boogie.digital) · made by KTP Digital.

➡️ **Website & docs: https://boogie.digital/cli/**

## Install

```sh
brew install boogie-digital/boogie/jmapcli
```

Upgrade later:

```sh
brew upgrade boogie-digital/boogie/jmapcli
```

Each release is also listed under [Releases](https://github.com/boogie-digital/jmapcli/releases) with the signed tarball and its `sha256`; the formula lives in the tap [`boogie-digital/homebrew-boogie`](https://github.com/boogie-digital/homebrew-boogie). This is the only publication path; the older `jasonhollis/boogie` tap is legacy (`brew untap jasonhollis/boogie`).

## Quick start

```sh
jmapcli login --url https://api.fastmail.com --username YOU@fastmail.com --oauth
jmapcli mailboxes                               # list your mailboxes
jmapcli list                                    # list the inbox
jmapcli read <id>                               # read a message
jmapcli send --to you@example.com \
             --subject "Hi" --body "Sent from the CLI"
```

`login --oauth` opens a browser (RFC 8252 loopback PKCE + RFC 7591 dynamic client registration) and stores access + refresh in the macOS Keychain (`jmap-oauth`). App-password (`--password`) and paste-token (`--token`) login still work. 1.5.0 is the first release with `--oauth`.

Everything is a subcommand — `send`, `list`, `read`, `mailboxes`, `move`, `trash`, `delete`, `alias`, … Run `jmapcli --help` or `jmapcli <command> --help` for the full set.

## What it is

- **Native** — a compiled Swift binary, not a script. Instant startup, no runtime to install.
- **Signed & notarised** — Developer-ID signed and notarised by KTP Digital, so macOS trusts it out of the box.
- **Standards-based** — speaks JMAP ([RFC 8620](https://www.rfc-editor.org/rfc/rfc8620) / [RFC 8621](https://www.rfc-editor.org/rfc/rfc8621)). Works with any JMAP server — e.g. Stalwart, Fastmail, Cyrus.
- **Private** — credentials live in the macOS Keychain. No account, no telemetry.
- **Free.**

jmapcli is the command-line companion to **Boogie**, the native JMAP email + calendar app for macOS, iOS, iPadOS and watchOS.

## Platform

macOS (Apple silicon).

## Source & issues

jmapcli ships as a closed-source, signed binary. This repository hosts the **documentation and issue tracker** — please file bug reports and feature requests here.

## Links

- Website / docs — https://boogie.digital/cli/
- Homebrew tap — https://github.com/boogie-digital/homebrew-boogie
- Releases — https://github.com/boogie-digital/jmapcli/releases
- Boogie app — https://boogie.digital

---

© KTP Digital Pty Ltd · ABN 85 648 755 980
