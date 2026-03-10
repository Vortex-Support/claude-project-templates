# Claude Project Templates

Templates mémoire génériques pour démarrer rapidement un nouveau projet avec Claude Code.

## Utilisation

Au début de la **première session** d'un nouveau projet, dire à Claude :

> "Nouveau projet. Initialise la mémoire depuis le template GitHub."

Claude se charge de tout :
1. Cloner ce repo
2. Copier les fichiers dans le bon dossier mémoire du projet
3. Remplir les placeholders avec les infos du projet

## Contenu

| Fichier | Rôle |
|---|---|
| `MEMORY.md` | Index projet — mode actuel, URLs, stack, env vars |
| `mode-exploitation.md` | Runbook maintenance (checks, fixes, hotfix) |
| `mode-projet.md` | Workflow développement (plan → implémentation → deploy) |

## Complément permanent

Ces templates fonctionnent avec `~/.claude/CLAUDE.md` (profil Daniel permanent) qui est
chargé automatiquement sur tous les projets et contient : infra VPS, intégrations
(Brevo, Groq, n8n, Stripe), règles deploy, style de travail.
