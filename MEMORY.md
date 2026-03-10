# [NOM DU PROJET] — Mémoire (index)

> **Nouvelle session :** Lire d'abord `docs/CLAUDE_CONTEXT.md` si disponible.
> Charger les fichiers thématiques selon le mode actuel ci-dessous.

---

## 🔄 Mode actuel

**EXPLOITATION** — depuis [DATE]

→ Charger `memory/mode-exploitation.md` en priorité

> Pour basculer en MODE PROJET : mettre à jour cette section.
> Exemple : `**PROJET — Feature: [nom]** → Charger memory/mode-projet.md`

---

## 🏗️ Ce projet

| Quoi | Valeur |
|---|---|
| App prod | `https://[url-app]` |
| API prod | `https://[url-api]` (si applicable) |
| Projet local | `[/chemin/local/du/projet]` |
| GitHub | `git@github.com:Vortex-Support/[repo-name]` |
| Stack frontend | `[React / Vue / Flutter / Swift / Kotlin / ...]` |
| Stack backend | `[Express / NestJS / FastAPI / ...]` (si applicable) |
| Base de données | `[PostgreSQL / SQLite / MongoDB / ...]` (si applicable) |

---

## 📂 Fichiers thématiques

| Fichier | Contenu | Mode |
|---|---|---|
| `memory/mode-exploitation.md` | Runbook : checks, fixes, maintenance | EXPLOITATION |
| `memory/mode-projet.md` | Workflow : planning → implémentation → deploy | PROJET |
| `memory/architecture.md` | Stack, patterns, pièges techniques | Les deux |

> Ajouter d'autres fichiers selon les besoins du projet :
> `memory/integrations.md`, `memory/security.md`, `memory/roadmap.md`...

---

## Variables d'env — toutes configurées sur VPS, ne jamais re-demander

`[LISTE_DES_VARS_D_ENV]`

> Exemple : `JWT_SECRET` · `DATABASE_URL` · `BREVO_API_KEY` · `GROQ_API_KEY`

---

## ⚠️ Règles spécifiques à ce projet

> Ajouter ici les règles et décisions propres à ce projet au fil du développement.
> Exemple : "Ne jamais modifier X sans backup", "Pattern Y obligatoire pour les routes PDF", etc.
