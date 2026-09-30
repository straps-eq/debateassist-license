# debateassist-license

This repository holds one file, `revocations.json`: the signed list of withdrawn Debate Assistant licence keys.
The app downloads it from

    https://raw.githubusercontent.com/straps-eq/debateassist-license/main/revocations.json

and ignores it unless it carries a valid Ed25519 signature from the owner's signing key. It contains licence
ids only (8 hex characters), a reason, the minimum app version and an optional notice. Nothing in it is
secret. Don't edit it by hand: `python -m tools.license publish` in the DebateAssist repo writes it.
