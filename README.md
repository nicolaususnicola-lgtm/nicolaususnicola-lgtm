<p align="center">
  <img src="./assets/MyZubster_Profilo_N4K48.png" alt="N4K48 — MyZubster profile" width="100%">
</p>

<h1 align="center">N4K48</h1>

<p align="center">
  Open-source builder · AI-assisted product planning · MyZubster · Zorgax · Nicola Comics · Neon Plaza
</p>

<p align="center">
  <a href="https://dev.to/n4k48">DEV Community</a> ·
  <a href="https://github.com/nicolaususnicola-lgtm/myzubster">MyZubster</a> ·
  <a href="https://github.com/nicolaususnicola-lgtm/myzubster-mvp">N4K48 MVP</a> ·
  <a href="https://github.com/nicolaususnicola-lgtm/myzubster/blob/main/ROADMAP_N4K48_METAVERSE.md">Public roadmap</a>
</p>

## Servizi a Rimini — traslochi, autista e condivisione di competenze

Oltre allo sviluppo di MyZubster, metto a disposizione le mie capacità pratiche per servizi a pagamento e scambio di conoscenze.

- **Piccoli traslochi e trasporto di oggetti ingombranti:** possiedo un pickup con gancio traino, disponibile per trasporti compatibili con le caratteristiche e la capacità del mezzo.
- **Disponibilità come autista:** sono munito di **patenti B, C, CE e CQC merci**. Posso valutare incarichi di guida anche quando il cliente dispone già di un camion o di un mezzo adatto al trasloco.
- **Condivisione di conoscenze pratiche:** offro sessioni concordate per condividere la mia esperienza di autista, la preparazione di un trasloco e l'organizzazione pratica del trasporto. Si tratta di condivisione di esperienza, non di corsi abilitanti o rilascio di patenti e certificazioni.

**Zona:** Rimini e dintorni; altre destinazioni da concordare.  
**Disponibilità e preventivo:** da concordare in base a percorso, durata, oggetti da trasportare e mezzo utilizzato. Le sessioni di condivisione delle competenze possono essere concordate separatamente dal servizio di trasporto.

Per una richiesta, indica partenza, destinazione, data, oggetti da trasportare, disponibilità di un mezzo oppure l'argomento che vuoi approfondire.

**Contatto:** [nicolaususnicola@gmail.com](mailto:nicolaususnicola@gmail.com).  
Il [Marketplace MyZubster](https://www.myzubster.com/marketplace) è il canale previsto per presentare questi servizi; il link al singolo annuncio sarà aggiunto quando disponibile.

## What I am building now

I am connecting the **N4K48 / Nicola Comics pilot** to the wider **MyZubster + Zorgax** ecosystem.

The current pilot exposes a small, read-only comics catalog through an API. Zorgax can request the gallery, inspect a comic, identify the NFT candidate and explain the next verification steps without performing minting, wallet operations, payments or catalog mutations.

The integration is intentionally evidence-first: a comic is never described as minted unless verifiable on-chain proof exists, and rights remain `TO_VERIFY` until they are actually verified.

## Start here

- **Explore the technical MVP:** [N4K48 Project Planner AI/Zorgax](https://github.com/nicolaususnicola-lgtm/myzubster-mvp#n4k48-project-planner-aizorgax).
- **Run the MVP locally:** [Docker quick start](https://github.com/nicolaususnicola-lgtm/myzubster-mvp#avvio-rapido-con-docker).
- **Follow the Metaverse roadmap:** [N4K48 roadmap](https://github.com/nicolaususnicola-lgtm/myzubster/blob/main/ROADMAP_N4K48_METAVERSE.md).
- **Explore the visual identity:** [N4K48 profile](https://github.com/nicolaususnicola-lgtm/myzubster-mvp/blob/main/docs/N4K48.md).
- **Follow the comics pilot:** [Nicola Comics roadmap](https://github.com/nicolaususnicola-lgtm/myzubster-mvp/blob/main/docs/n4k48-comics/ROADMAP.md).

## N4K48 × MyZubster — Nicola Comics

Three AI-assisted comic pages tell the journey from a software idea to development and the future vision of Neon Plaza:

1. **Dall'idea software al metaverso** — current NFT candidate.
2. **Il software prende forma**.
3. **Verso Neon Plaza**.

The first comic is currently `NFT_CANDIDATE` / `PROPOSED_FOR_REVIEW`. Rights are still `TO_VERIFY`; contract address, token ID and transaction hash remain empty until a real verified mint exists.

[**Read the comic pages**](https://github.com/nicolaususnicola-lgtm/myzubster-mvp/tree/main/docs/n4k48-comics) · [Pilot roadmap](https://github.com/nicolaususnicola-lgtm/myzubster-mvp/blob/main/docs/n4k48-comics/ROADMAP.md) · [Zorgax adapter documentation](https://github.com/nicolaususnicola-lgtm/myzubster-mvp/blob/main/docs/nicola-comics/ZORGAX.md)

## Nicola Comics × Zorgax adapter

The pilot currently supports:

- `GET /api/comics` — public catalog.
- `GET /api/comics/{comic_id}` — comic detail/card.
- `POST /api/zorgax/ask` — read-only Zorgax adapter.
- Actions: `gallery`, `detail`, `candidate`, `next_steps`.
- Configurable public base URL through `NICOLA_COMICS_BASE_URL`.
- Docker propagation of the base URL without hardcoding a local PC address.

The local happy path has been manually verified with the Docker API healthy: gallery, detail, candidate and next-steps responses work as expected. The configurable base URL was also verified through Docker using a test URL, producing absolute comic detail URLs correctly.

The current environment does **not** contain `pytest`, so the automated comics test suite has not been rerun in the latest validation session. Historical test results are documented separately; current claims are limited to what was actually rechecked.

## Current integration milestone

Coordination with the public MyZubster project is tracked in **MyZubster-Ecosystem/myzubster issue #1176**.

The target public end-to-end flow is:

```text
Zorgax request
   ↓
Nicola Comics gallery
   ↓
Comic detail/card + image
   ↓
NFT candidate
   ↓
Rights verification
   ↓
Verified on-chain data only when it really exists
```

The pilot must be hosted on a public HTTPS endpoint separately from the local PC. Authentication secrets, if required by the public integration, belong in the hosting environment and must never be committed to the repository.

## Verified progress

- ✅ Persistent N4K48 character profile
- ✅ JWT-based authentication and authenticated Neon Plaza join flow
- ✅ Existing Metaverse automated verification: 4 suites / 22 tests passed locally on September 3, 2026
- ✅ Public N4K48 documentation, profile and visual identity
- ✅ Nicola Comics catalog with three comic entries
- ✅ `n4k48-comic-001` selected as NFT candidate without claiming a mint
- ✅ Read-only Zorgax adapter implemented
- ✅ Local Docker happy path manually verified
- ✅ Configurable `NICOLA_COMICS_BASE_URL` implemented and verified through Docker
- ✅ Public integration coordination opened as issue #1176
- 🚧 Public HTTPS deployment of the Nicola Comics pilot
- 🚧 Public Zorgax → pilot end-to-end integration
- 🚧 Rights verification and eventual on-chain proof

## Featured projects

### [N4K48 Project Planner AI/Zorgax](https://github.com/nicolaususnicola-lgtm/myzubster-mvp#n4k48-project-planner-aizorgax)

An experimental AI-guided project planner for turning one objective into clear activities, detecting mistakes and documenting verifiable progress.

### [MyZubster development fork](https://github.com/nicolaususnicola-lgtm/myzubster)

The public development fork containing the persistent N4K48 profile, JWT authentication, authenticated Neon Plaza flow, automated tests and project roadmap.

### [MyZubster MVP / Nicola Comics pilot](https://github.com/nicolaususnicola-lgtm/myzubster-mvp)

The technical MVP now includes the read-only Nicola Comics API and Zorgax adapter alongside Docker, observation APIs, local AI experiments with Ollama, Qdrant and retrieval-augmented generation.

## Working principles

```text
OBSERVE → DOCUMENT → BUILD → TEST → VERIFY → PUBLISH
```

Visuals and storytelling explain the direction. Code, tests, commits and evidence demonstrate what has actually been completed.

---

The projects shown here are experimental and under development. Public documentation, visuals and local test results do not by themselves demonstrate production deployment, commercial adoption, payment, partnership, verified intellectual-property rights or on-chain minting. Those claims are made only when supporting evidence exists.
