# Upload Guide

## 1. Create the repository

Recommended name:

`jtec-network-engineering-labs`

Set it to Public if you want recruiters to view it.

## 2. Copy these folders

Upload the contents of this package to the repository root.

## 3. Add your Packet Tracer files

For each lab, copy your real `.pkt` file into:

`lab-XX-.../packet-tracer/`

Example:

`lab-10-lacp-etherchannel/packet-tracer/JTEC-Lab-10-EtherChannel.pkt`

## 4. Add screenshots

Use the screenshot naming convention:

```text
01-topology.png
02-configuration.png
03-verification.png
04-troubleshooting.png
05-final-test.png
```

Place them inside each lab's `screenshots` directory.

## 5. Replace example configurations with your final configs

The configuration files supplied here contain documented examples based on the known JTEC lab design.

Where your final Packet Tracer running-config differs, use the actual final configuration.

Do not invent command output.

## 6. Commit

```bash
git add .
git commit -m "Add JTEC networking labs 02-10 portfolio documentation"
git push
```

## 7. Pin the repository

Pin the JTEC repository to your GitHub profile so it is visible immediately.

## 8. Final quality check

Before sharing the repository:

- Every lab has a README.
- Every completed lab has its `.pkt` file.
- Screenshots are readable.
- Configuration is searchable text.
- Troubleshooting explains symptom → investigation → root cause → resolution → verification.
- No passwords or secrets are exposed.
- Lab status is accurate.
