# AGORA

**A minimalist P2P communication suite by Foxen Studio.**
Secure. Serverless. Untraceable.

```
E2E ENCRYPTED  //  P2P  //  NO LOGS
```

No accounts. No message history sitting on someone else's server.
No central point of failure to compromise, subpoena, or leak. When
the room closes, the conversation is gone — not archived, not
backed up, just gone.

---

## Why Agora exists

Most group chat today runs through infrastructure you don't control
and can't fully trust. Agora takes the opposite approach: messages
and files are end-to-end encrypted and routed peer-to-peer, so the
only people who can ever read a conversation are the people in it.

## Core features

- **True end-to-end encryption** — RSA-2048 for key exchange,
  AES-256-GCM for message and file content. Every group message
  gets its own one-time AES key, individually encrypted for each
  recipient.
- **Serverless by design** — built on WebRTC via PeerJS. No central
  server stores or relays plaintext; a lightweight signaling layer
  only helps peers find each other.
- **Encrypted file transfer** — files are encrypted client-side
  before they ever leave your device, with size limits and
  integrity checks to prevent abuse.
- **Room roles** — Host, Admin, and Moderator tiers with kick, ban,
  pin, and ownership transfer controls.
- **Password-protected rooms** — protected with salted PBKDF2
  hashing (100,000 iterations) and brute-force lockout after failed
  attempts.
- **Burn-on-read messages** — set a timer and messages fade from
  the screen automatically.
- **Six visual themes** — Ghost, Terminal, Amber, Ice, Blood, and
  Snow Fox.
- **Zero persistence** — nothing is written to a database. Close
  the room, and it's as if it never existed.

## Quick start

1. Open Agora in your browser.
2. Pick a username and either **create** a room or **join** one
   with a room code.
3. Share the code with whoever you want in the room — that's the
   only "invite" that exists.
4. Talk freely. Send files. Set a burn timer if you want messages
   to disappear.
5. Close the tab to wipe the session completely.

## Commands

```
/help                     list available commands
/users                    show who's online + encryption status
/msg <user> <text>        send a private, separately encrypted DM
/burn <seconds> | off     enable/disable self-destructing messages
/mute <user>               mute a user locally (client-side only)

Moderator/Admin:
/kick <user>  /ban <user>  /unban <user>
/pin <text>   /unpin

Host only:
/set lock | unlock
/set pass <password> | 0
/set max <number>
/set roomcode <code> | r
```

Or skip the commands entirely — everything is also available
through the side drawer menu.

## Security notes

Agora doesn't ask you to trust it — it's built so there's nothing
to trust. That said, WebRTC does expose peer IP addresses by
design (it's how direct connections work), so a VPN is recommended
if full anonymity matters to you. This is disclosed on-screen every
time you create or join a room.

## Tech stack

`HTML` · `CSS` · `Vanilla JS` · `Web Crypto API` · `WebRTC` · `PeerJS`

No frameworks, no build step, no dependencies beyond a single CDN
script. One file, fully self-contained.

## Roadmap

- [ ] Community rooms with optional persistent history
- [ ] Voice channels
- [ ] Fabric/mod client integration

---

*Foxen Studio — building tools that don't watch you back.*

`Xsgdwh Vrrq.`
