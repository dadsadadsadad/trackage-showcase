# Security

Please report security problems privately through [GitHub's private vulnerability reporting](https://github.com/dadsadadsadad/trackage-showcase/security/advisories/new), not in a public issue.

## How Trackage protects your data

- The collector builds uploads from an allow-list and checks them before sending; the server checks them again and rejects anything that looks like text.
- Session and file ids are HMACs keyed with a secret that never leaves your computer.
- Passwords are hashed with scrypt; device tokens, API keys and session tokens are stored only as SHA-256 hashes.
- Traffic is encrypted with TLS. State-changing requests require our own origin and a custom header; webhooks are signature-checked.
- Plan limits are enforced on the server.
