<p align="center">
  <img src="./assets/MyZubster_Profilo_N4K48.png" alt="N4K48 — MyZubster profile" width="100%">
</p>

<h1 align="center">N4K48</h1>

<p align="center">
  Building verifiable experiments across AI, APIs, digital identity, comics and MyZubster.
</p>

<p align="center">
  <a href="https://www.myzubster.com">MyZubster</a> ·
  <a href="https://github.com/nicolaususnicola-lgtm/myzubster-mvp">Nico Comics MVP</a> ·
  <a href="https://dev.to/n4k48">DEV Community</a>
</p>

## 👋 About me

I'm Nicola, building **N4K48**: an experimental path connecting software development, AI-assisted workflows, **MyZubster**, **Zorgax**, **Nico Comics** and the longer-term **Neon Plaza** vision.

My working principle is simple:

```text
OBSERVE → DOCUMENT → BUILD → TEST → VERIFY → PUBLISH
```

I try to keep public claims evidence-first: a feature is described as working when it has been tested, and blockchain/NFT claims are made only when verifiable on-chain evidence exists.

## 🚀 What I'm building now

### Nico Comics × MyZubster

The current public pilot turns three N4K48 comic boards into a small read-only catalog and API that can be queried by Zorgax-style clients.

**Public demo:** https://myzubster-mvp.onrender.com

Current capabilities:

- `GET /api/comics` — public comics catalog
- `GET /api/comics/{comic_id}` — comic detail
- `POST /api/zorgax/ask` — read-only adapter
- Actions: `gallery`, `detail`, `candidate`, `next_steps`
- Docker deployment and GitHub Actions verification
- Configurable `NICOLA_COMICS_BASE_URL`

The first board, `n4k48-comic-001`, is currently an **NFT candidate proposed for review**. Its rights status remains `TO_VERIFY`; no mint is claimed without contract address, token ID and transaction evidence.

### MyZubster real-world handover pilot

I also tested a real **hand-delivery workflow** in MyZubster using a kefir handover.

The verified application lifecycle reached:

```text
HAND_DELIVERY → HANDED_OVER → RECEIVED → RECORDED
```

The final application record reported `success: true`, `paymentRequired: false` and `onchainRecorded: false`.

That distinction matters: **RECORDED is a MyZubster digital record, not a blockchain claim.**

The test also surfaced a role-permission HTTP 403 during the recipient flow. Instead of bypassing it, we documented the error and continued only through the action enabled for the correct role.

## 🧪 Verified engineering progress

- ✅ Public Nico Comics HTTPS deployment
- ✅ Three-board N4K48 comics catalog
- ✅ Read-only Zorgax adapter
- ✅ `gallery`, `detail`, `candidate`, `next_steps` actions
- ✅ Docker verification
- ✅ GitHub Actions CI
- ✅ Public API smoke testing
- ✅ Evidence-first NFT candidate state
- ✅ Real MyZubster handover reaching `RECORDED`
- 🚧 Public MyZubster Zorgax → Nico Comics end-to-end bridge
- 🚧 Rights/provenance verification before any NFT mint claim
- 🚧 Broader Neon Plaza integration

## 🎨 Nico Comics

The first three AI-assisted N4K48 comic boards are:

1. **Dall'idea software al metaverso**
2. **Il software prende forma**
3. **Verso Neon Plaza**

[Explore the comic pilot](https://github.com/nicolaususnicola-lgtm/myzubster-mvp/tree/main/docs/n4k48-comics) ·
[Read the roadmap](https://github.com/nicolaususnicola-lgtm/myzubster-mvp/blob/main/docs/n4k48-comics/ROADMAP.md) ·
[Zorgax adapter docs](https://github.com/nicolaususnicola-lgtm/myzubster-mvp/blob/main/docs/nicola-comics/ZORGAX.md)

## 🛠 Tech & workflow

`GitHub` · `Docker` · `Python` · `Flask` · `REST APIs` · `GitHub Actions` · `Render` · `AI-assisted development`

I use AI as a development and documentation assistant while keeping tests, commits, API responses and deployment evidence as the source of truth.

## 📌 Featured work

### [Nico Comics / MyZubster MVP](https://github.com/nicolaususnicola-lgtm/myzubster-mvp)

Public API, Docker deployment, Zorgax adapter, automated verification and the Nico Comics pilot.

### [MyZubster development fork](https://github.com/nicolaususnicola-lgtm/myzubster)

Development work around the N4K48 profile, MyZubster experiments, authentication, Neon Plaza and project documentation.

## 🌐 Follow the build

- [Public Nico Comics demo](https://myzubster-mvp.onrender.com)
- [DEV Community](https://dev.to/n4k48)
- [MyZubster](https://www.myzubster.com)

---

**N4K48 × MyZubster — Pilot 2026**

> Build it. Test it. Verify it. Then publish it.

The projects shown here are experimental and under development. Public documentation and application records do not by themselves demonstrate commercial adoption, verified intellectual-property rights, blockchain transactions or NFT minting.
