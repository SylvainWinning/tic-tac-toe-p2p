# Tic‑Tac‑Toe+ (WebRTC • P2P)

Jeu Tic‑Tac‑Toe moderne, mobile‑first, thème auto, a11y, micro‑interactions, **mode en ligne sans serveur** via WebRTC (copier‑coller ou **liens d’invitation**).

## Jouer en ligne — pas à pas (liens recommandés)

### Rôle Hôte (X)
1. Ouvrir la page GitHub Pages : `https://<user>.github.io/<repo>/`
2. Cliquer **En ligne → Créer** puis **Créer une invitation (X)**.
3. Bouton **Copier lien** → envoyer ce lien à l’invité (ou **Partager** si dispo).

Le lien ressemble à :  
`https://<user>.github.io/<repo>/#offer=...`  
(il contient l’offre WebRTC encodée)

### Rôle Invité (O)
1. Ouvrir le **lien d’invitation** reçu.
   - La page s’ouvre directement sur l’onglet **Rejoindre**.
   - Le champ d’invitation est déjà prérempli (si le lien comporte `#offer=...`).
2. Cliquer **Générer ma réponse (O)**.
3. Bouton **Copier lien** (ou **Partager**) → renvoyer ce **lien de réponse** à l’hôte.

Le lien ressemble à :  
`https://<user>.github.io/<repo>/#answer=...`

### Finalisation pour l’Hôte
- Ouvrir le **lien de réponse** reçu.  
  L’onglet **Créer** s’ouvre et la réponse est **validée automatiquement**.  
  Statut **Connecté** → la partie commence.

> Astuce : si un lien est trop long pour votre messagerie, utilisez les **codes texte** juste au‑dessus des liens (copier/coller).

## Déploiement GitHub Pages
- Déposer `index.html`, `.nojekyll`, `assets/icon.svg`, `manifest.webmanifest`.
- **Settings → Pages** : *Deploy from a branch* → `main` / `(root)` → *Save*.
- URL : `https://<user>.github.io/<repo>/`.

## Détails techniques
- WebRTC DataChannel (STUN: `stun.l.google.com:19302`).
- Pas de TURN (si NAT très strict : possible échec → jouer en local).
- Persistance : `localStorage` (scores, préférences, état en cours).
- Accessibilité : ARIA live, progressbar, navigation clavier, focus trap modal.
- Partage : `navigator.share` si dispo, sinon copie robuste (Clipboard API + fallback).

## Licence
MIT
