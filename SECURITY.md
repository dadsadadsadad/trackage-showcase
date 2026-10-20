# Security

Please report security problems privately through [GitHub's private vulnerability reporting](https://github.com/dadsadadsadad/trackage-showcase/security/advisories/new), not in a public issue.

## How Trackage protects your data

- The collector is open source ([trackage-cli](https://github.com/dadsadadsadad/trackage-cli)), so anyone can check what it reads and sends.
- The collector builds uploads from an allow-list and checks them before sending; the server checks them again and rejects anything that looks like text.
- The collector only talks to the server over HTTPS and refuses plain HTTP to anything but your own computer.
- Session and file ids are HMACs keyed with a secret that never leaves your computer.
- Passwords are hashed with scrypt; device tokens, API keys, session tokens and email links are stored only as SHA-256 hashes.
- Email alerts and reports go only to confirmed addresses. Changing your password signs out your other browsers.
- Two-step sign-in with any authenticator app, with single-use recovery codes. Settings shows every browser signed in to your account.
- Two-step keys, Admin keys for bill matching and the push signing key are encrypted in the database with AES-256-GCM.
- Phone and browser alerts are end-to-end encrypted to your device (Web Push, RFC 8291), and only go to the browsers' own push services.
- Team members see each other's numbers only, never titles, prompts or files; invites are accepted only with the invited address.
- You get an email when your password changes, a computer is linked, or two-step sign-in is turned on or off.
- Traffic is encrypted with TLS. State-changing requests require our own origin and a custom header; webhooks are signature-checked.
- Plan limits are enforced on the server.
