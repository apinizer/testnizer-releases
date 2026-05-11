# Testnizer — Releases

This repository **hosts the official release artifacts** for
**[Testnizer](https://www.testnizer.com)** — the offline API client for teams
who can't paste tokens into the cloud.

> Testnizer is distributed as **pre-built binary installers only**. The
> source code is not publicly released. The "Source code" archives that
> GitHub auto-generates for every tag are a snapshot of *this* repo (i.e.
> just this README), not the application source.

> Testnizer is a **free** desktop application by
> [Apinizer](https://apinizer.com). Free to download and use — see the
> [End User License Agreement](https://www.testnizer.com/license) for terms.

## Download

Go to the **[Releases page](https://github.com/apinizer/testnizer-releases/releases/latest)**
and pick the installer for your platform:

| Platform | Architecture | Format |
|---|---|---|
| macOS | Apple Silicon (arm64) | `.dmg` |
| macOS | Intel (x64) | `.dmg` |
| Windows | x64 | NSIS installer (`.exe`) |
| Windows | arm64 | NSIS installer (`.exe`) |
| Linux | x64 | `.deb` (Debian/Ubuntu) |
| Linux | x64 | `.AppImage` |
| Linux | arm64 | `.deb` |
| Linux | arm64 | `.AppImage` |

All installers are free. No account required.

## Verify your download

Every release includes a `checksums.txt` file with SHA-256 hashes for every
artifact.

**macOS / Linux:**

```sh
shasum -a 256 Testnizer-1.3.0-arm64.dmg
```

**Windows (PowerShell):**

```powershell
Get-FileHash .\Testnizer-Setup-1.3.0-x64.exe -Algorithm SHA256
```

Compare the output against the matching line in `checksums.txt`. If they do
not match, do not install the file.

## What is Testnizer?

Testnizer is a fully offline desktop app for testing APIs:

- **HTTP / REST** — all methods, auth schemes, body modes, scripts, assertions
- **SOAP / WSDL** — WSDL import, manual envelope mode, WS-Security built in
- **WebSocket** — wss + custom headers + message timeline
- **GraphQL** — query, mutation, subscription, schema introspection
- **gRPC** — all four streaming modes, .proto import, server reflection
- **Server-Sent Events** — long-lived streams, Last-Event-ID resume
- **Socket.IO** — namespaces, auth, emit + subscribe, bidirectional timeline
- **MCP** — Streamable HTTP / SSE / stdio; list and invoke tools
- **AI Chat** — 14 providers + custom URL (vLLM, Ollama, LM Studio)

Everything runs locally. No login, no telemetry, no vendor server. Collections,
environments, history, certificates, and secrets live in a single SQLite
database on your machine.

Learn more at **[www.testnizer.com](https://www.testnizer.com)**.

## Air-gapped environments

1. Download the installer and `checksums.txt` on a connected machine
2. Verify the SHA-256 checksum
3. Transfer to the isolated machine via USB, SFTP, or your air-gap gateway
4. Install normally
5. Disable auto-update in **Settings → Updates** on the isolated machine

## Reporting issues

Bugs, feature requests, and questions:
[github.com/apinizer/testnizer-releases/issues](https://github.com/apinizer/testnizer-releases/issues)

For security vulnerabilities, please email **info@apinizer.com** instead of
opening a public issue.

## Enterprise support

Need paid support, response-time SLAs, on-premise deployment assistance,
training, or custom development? Contact **info@apinizer.com**.

## Documentation

Full documentation is available at
[www.testnizer.com/docs/getting-started](https://www.testnizer.com/docs/getting-started).

## License

Testnizer is **free** to download and use, but it is **not open source**.
The application is distributed as proprietary, pre-built binaries under the
[End User License Agreement](https://www.testnizer.com/license).
The "Testnizer" name and logo are project marks of Apinizer.
