# Rhizome: A Living Secure Network

An interactive design study of a secure, federated knowledge commons. This presentation explores individual data sovereignty, mutually authorized communities, privacy-preserving computation, changing historical perspectives, collective knowledge, and distributed reliability.

The presentation is intended for conversations with collaborators, researchers, designers, and community members. It explains sophisticated concepts through interactive examples, with an optional engineering lens.

## Open the presentation

1. Visit [the published presentation](https://gblongiu.github.io/rhizome-living-network/).
2. Select **Enter the network** to begin, or scroll to a chapter.
3. Use **Engineering lens** in the navigation bar for technical notes.

The presentation includes its CSS, JavaScript, and visualization library in `index.html`. No build step is required. You can open the file in a desktop browser or use the published HTTPS site. Some mobile file previewers do not execute JavaScript.

For local development, start a server from the repository directory:

```bash
python3 -m http.server 8000
```

Open `http://localhost:8000` in a browser. Modern browsers treat localhost as a secure context for Web Crypto.

## What you can explore

| Area | Interaction | Central question |
| --- | --- | --- |
| Principles | Scroll through the four core promises | Which kinds of authority must stay separate? |
| Federation | Independent, Introduction, Approved, Compromised | Who can connect, and what can they access? |
| Protection | Direct, Protected core, Delayed mix, relay failure | What network information is exposed? |
| Data sovereignty | Seal and unlock a sample thought | What can a storage operator read? |
| Private compute | Six computation patterns | How can communities collaborate without exporting raw datasets? |
| Knowledge | Perspective modes and evidence cutoff | What was knowable then, and what is understood now? |
| Classification | Community lens, year scrubber, Play history | How can interpretation change without changing past records? |
| Relationships | Shared questions, Complementary skills, Mentorship | How can introductions respect each person's consent? |
| Resilience | Healthy, Partition, Stale grant, Forked history | Which operations must stop when authorization is uncertain? |
| Diagnostics | Missing evidence, Privacy exposure, Bad synthesis | What failed, and what can be demonstrated? |
| Build | Small node, Laptop, Desktop | Which security functions are realistic on consumer hardware? |

All people, communities, votes, timelines, points, and feasibility positions shown in the diagrams are **synthetic**. They illustrate behavior and tradeoffs rather than reporting measured research findings.

## Repository contents

```text
rhizome-living-network/
  index.html
  README.md
  SHA256SUMS.txt
  docs/
    ARCHITECTURE.md
    INTERACTION_GUIDE.md
    SECURITY_BOUNDARIES.md
    THIRD_PARTY_NOTICES.md
    QA_REPORT.md
  licenses/
    D3_BSD_3_CLAUSE.txt
  previews/
    desktop.png
    relationship_consent.png
    mobile.png
  tools/
    verify_package.py
```

`index.html` serves the published website. The remaining files document the architecture, interactions, security boundaries, testing, and integrity checks.

## Security and privacy scope

This is a **design presentation, not a deployed Rhizome node or a production cryptographic system**.

- The sample vault uses browser-local AES-256-GCM with a temporary memory-resident key when Web Crypto is available.
- The relationship consent flow changes only local demonstration state. It does not contact another participant or issue real credentials.
- Multi-hop routes, private set intersection, encrypted AI computation, distributed authorization, and failure modes are **simulations**.
- No user data is intentionally transmitted or retained by this HTML. No analytics, remote scripts, or third-party fonts are included.
- Recipient copying, traffic correlation, compromised devices, and historical plaintext exposure remain important limitations.

Read [`docs/SECURITY_BOUNDARIES.md`](docs/SECURITY_BOUNDARIES.md) before treating any demonstration as an implementation guarantee.

## Design and accessibility

The seven-color palette encodes different concepts across the visualization system. Color is paired with labels and line styles in key security and policy diagrams. Motion is reduced when the operating system requests reduced animation. Some dense graphs can be explored by horizontal scrolling on narrow screens.

The document works best in a modern graphical browser with JavaScript enabled.

## Verify the files

From the repository root:

```bash
python3 tools/verify_package.py
```

The script checks SHA-256 hashes of the tracked project files using the Python standard library.

## Sharing and licensing

Share the published website for interactive viewing, or the repository for technical documentation.

The original material has no project-level reuse license. The embedded D3 library has a separate permissive license, documented in [`docs/THIRD_PARTY_NOTICES.md`](docs/THIRD_PARTY_NOTICES.md) and [`licenses/D3_BSD_3_CLAUSE.txt`](licenses/D3_BSD_3_CLAUSE.txt).
