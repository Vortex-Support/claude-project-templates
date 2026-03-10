# Mode Projet — [Projet]

> Ce fichier est chargé en priorité quand `## Mode actuel` dans MEMORY.md indique **PROJET**.

---

## 🗺️ Workflow standard d'une feature

```
1. COMPRENDRE     → Lire les fichiers concernés AVANT de proposer quoi que ce soit
2. PLANIFIER      → EnterPlanMode — plan écrit, validé par Daniel, AVANT toute ligne de code
3. IMPLÉMENTER    → Suivre le plan étape par étape, une tâche à la fois (TodoWrite)
4. VÉRIFIER       → TypeScript check + preview tools (jamais "ça devrait marcher")
5. DÉPLOYER       → git push (CI/CD) → vérifier en prod
6. DOCUMENTER     → CLAUDE_CONTEXT.md + MEMORY.md + commit docs séparé
7. BASCULER       → Repasser en MODE EXPLOITATION dans MEMORY.md
```

---

## 📋 Checklist avant de coder

- [ ] Lire `docs/CLAUDE_CONTEXT.md` (état actuel du projet)
- [ ] Charger les fichiers thématiques pertinents (`memory/architecture.md`, etc.)
- [ ] Identifier les fichiers à modifier (lire leur contenu avant de proposer)
- [ ] Plan validé par Daniel
- [ ] Backup DB si migration : `ssh vps-vortex "/opt/[project]-backups/backup.sh"`

---

## 🛠️ Checklist après chaque commit

- [ ] `npx tsc --noEmit` → 0 erreurs TypeScript
- [ ] Build prod `npm run build` → pas d'avertissements bloquants
- [ ] Preview tools → vérifier visuellement le résultat
- [ ] `git push origin main` (CI/CD prend le relai)
- [ ] Vérifier en prod : `curl https://[url-api]/health`
- [ ] Mettre à jour `docs/CLAUDE_CONTEXT.md` (roadmap ✅ + état deploy)
- [ ] Commit docs : `docs: mise à jour CLAUDE_CONTEXT après [feature]`

---

## 🧩 Skills à utiliser selon le type de tâche

| Type de tâche | Skills à invoquer |
|---|---|
| Nouveau composant UI | `frontend-design` → `senior-frontend` |
| Optimisation React | `react-best-practices` |
| Nouvelle feature complexe | `brainstorming` → `writing-plans` |
| Revue après implémentation | `code-reviewer` |
| Nouvelle architecture | `senior-architect` |
| Nouvel agent maintenance | Lire `docs/AGENTS_MAINTENANCE_TEMPLATE.md` si disponible |
| Debugging | `systematic-debugging` |
| Diagram / récap | `visual-explainer` |

---

## 📐 Règles d'implémentation

- **Lire avant de modifier** — jamais de changements sur un fichier non lu
- **Expliquer avant d'agir** — toujours décrire ce qui va changer et pourquoi
- **Une tâche à la fois** — TodoWrite pour tracker, marquer ✅ immédiatement
- **Pas de sur-engineering** — minimum viable, pas de code pour des cas hypothétiques
- **Sécurité systématique** — toute nouvelle route : auth + validation + rate limit
- **UUID sur les routes** — valider avant d'envoyer à la DB (évite les 500 type mismatch)

---

## 🔄 Triggers de bascule vers MODE EXPLOITATION

Basculer vers `mode-exploitation.md` quand :
- Feature déployée et vérifiée en prod
- Hotfix appliqué
- Session terminée sans feature en cours

**Pour basculer :**
1. Mettre à jour `## Mode actuel` dans `MEMORY.md`
2. Vérifier que `docs/CLAUDE_CONTEXT.md` est à jour
3. La prochaine session démarre en MODE EXPLOITATION
