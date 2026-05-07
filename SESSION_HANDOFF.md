# RECONNECT MAP — SESSION HANDOFF

_Saved 2026-05-07 (avant compactage). État final : V8._

---

## OÙ EN EST LE PROJET

**Quiz/diagnostic interactif** pour marché AU anglophone, route vers **Pleasuary Elysia** (toggle `PRODUCT_CONFIG` en haut du JS pour basculer vers POPPY).

**Fichier principal** : [outputs/reconnect-map-v1/index.html](outputs/reconnect-map-v1/index.html) — 1839 lignes single-file vanilla, pas de deps externes (Chart.js retiré, remplacé par SVG custom).

**Brief stratégique complet** : [outputs/reconnect-map-v1/CONTENT_BRIEF_v2.md](outputs/reconnect-map-v1/CONTENT_BRIEF_v2.md) + [.html navigable](outputs/reconnect-map-v1/CONTENT_BRIEF_v2.html).

---

## DÉCISIONS STRATÉGIQUES VERROUILLÉES

### Hero (Schwartz Big Idea)
- **Titre** : *"There are 5 kinds of pleasure. Most women only ever experience two."*
- **Sub** : *"Find out which two are yours — and which three you've never met."*
- **Meta** : *"A 90-second test. Private. No email required."*
- **CTA** : *"Show me where I am →"*
- Centré vertical + horizontal, ornement doré sous CTA

### Audience + Architecture conditionnelle
Persona Sarah 50+ étendu à 18-65+ via Q1 âge → 5 paths :
- **A** 18-29 — Exploration / Discovery
- **B** 30-39 — Pressure / Reality (stress, kids, postpartum, career)
- **C** 40-49 — Transition / Perimenopause
- **D** 50-59 — Menopause + Resignation
- **E** 60+ — Repositioning / Late discovery

Total flow : Q1 âge + 3-4 path-specific + 8 communes = **12-13 questions**.

### Les 5 plaisirs (mappés aux 3 stims Elysia)
| Plaisir | Sensation | Stim Elysia |
|---------|-----------|-------------|
| **The Strike** | Focal, immediate peak | Clitoral pulses |
| **The Slow Burn** | Anticipation, build, presence | Parasympathetic + low-intensity multi |
| **The Tide** | Deep internal rolling waves | Back-and-forth interne |
| **The Hum** | Full-body, ambient, enveloping | Enveloping vibration |
| **The Echo** | Post-peak afterglow, integration | Émerge des 3 stim simultanées |

**Phrase-clé** : *"Most devices stimulate one zone. One zone gives you 1, maybe 2 of these. Reaching all five requires three coordinated stimulations simultaneously — which is exactly what Elysia is built for."*

### Verdict modulaire
**Composition** : Eyebrow + Headline ("You know The X") + Summary "2 yours / 3 missing" + Age opener (5 versions) + Spider radar SVG custom + Profile narrative (lead + body + 3 bullets icons) + Testimonial AU exact-match (matrix 5×5) + Mechanism universel + Bundle reco + Risk callout.

### Bundles (prix Pleasuary réels)
- **The Spark** ($89.99 was $194.99, Save $105) → Strike + Tide profiles
- **The Wildfire** ★ MOST POPULAR ($109.99 was $229.99, Save $120) → Slow Burn + Hum + Echo profiles
- Layout strike-left / price-right / save badge
- Includes Discreet Drawstring Pouch + (Wildfire) Ylang-Ylang Oil

### Soft exit (4 triggers)
1. **Already there** — 4-5/5 sélectionnés en K7 → "tu n'as pas besoin de produit"
2. **Relational** — Path D/E + signaux relationnels + low physio scores → 3 worksheets (conversation, doctor script, drift audit)
3. **Early literacy** — Path A + zero K7 + jamais lâché → "body literacy first"
4. **Health flag** — Path E + uncertainty/safety → AU practitioner directory (Jean Hailes, Australasian Menopause Society)

### Timer sticky
- 11 minutes
- Visible **uniquement sur la result page** (pas avant)
- Format `Limited release · Australia [11:00]`
- À expiration : countdown disparaît, label devient `Limited offer · Ending soon` (rouge)
- Persistance localStorage avec auto-reset si stale

### Flow d'urgence final (V8 ajout)
- Bundle CTA = **"Check availability →"** + sub `● Limited offer · Australia`
- Au clic → modal full-screen :
  - Loading 2.8s avec spinner + 4 messages séquentiels + progress bar
  - Reveal "Good news. Stock available in your area." + warning + 5 bénéfices
  - Final CTA terracotta : **"Claim my offer now →"** vers Pleasuary
  - Bouton "Not yet" pour fermer

---

## ANIMATIONS / VISUELS

**Décisions** :
- ❌ Animation top de page (sun rising / topo map / silhouette) — Alpha rejette tout
- ✅ **Constellation pentagone** sous les questions (5 dots qui s'illuminent en temps réel selon scores)
- ✅ **SVG custom radar** dans le verdict (Chart.js retiré) — 5 points pulsent individuellement, label dominant pulse aussi
- ✅ Icons SVG dans bullets : checkmark (have) / info (missing) / lightbulb (why)
- ✅ Hero ornement doré (line-dot-line) sous CTA

---

## VOCABULAIRE / ÉTHIQUE

- Marché AU anglophone uniquement
- Spelling : recognise / behaviour / colour / hot flushes
- Banlist : orgasm / orgasmic / sex drive / arousal / climax / spice things up / feel young again
- Disclosure footer : "paid models, verbatim composites from anonymous AU survey n=459"
- TGA-AU friendly : zero medical claim, soft exit health flag pour 60+ avec doute
- Persona Sarah file utilisée comme source de vérité : `C:\Users\Alpha Wolf\.claude\projects\C--\memory\elysia_persona_diagnostic.md`

---

## CE QUI RESTE À FAIRE

### Court terme (prochaine session)
1. **Audit 6 sous-agents en parallèle** sur le brief V2 — pas encore lancés. Personas-fit, sex-positive ethics, mechanism cohérence, conversion CRO, TGA-AU compliance, age-conditional flow auditor.
2. **Itération post-audit** sur questions / verdicts / soft exits.
3. **Backend email capture** : pas requis pour V1 (pas d'email gate). Pour V2 : Apps Script + Google Sheets ou MailerLite.
4. **Hosting** : décider GitHub Pages (comme Genesys-Website) ou autre.
5. **Décision animation top** : Alpha n'a aimé aucune option proposée. Status pending.

### Décisions ouvertes
- Test traffic : Meta cold AU $20/jour ? rerouting hemistone.com ? Reddit r/AusTRT ? attendre caméra YouTube + ads parallèles ?
- Toggle POPPY : Alpha a un projet POPPY landing v2 dormant. Switch quand prêt (1 ligne dans `PRODUCT_CONFIG`).
- 5-bar visual sur questions stage : déféré (constellation déjà en place).

---

## VERROUS DE BUILD (à respecter en future itération)

- ❌ Pas de Chart.js (retiré V7)
- ❌ Pas de bandeau visuel haut de page (Alpha rejette horizon/sun/topo/etc.)
- ❌ Pas de 6-minute test (max "90 seconds" perçu)
- ❌ Pas de "Begin the map" / "Start the map" CTA
- ❌ Pas de questions sur GP (utiliser "doctor")
- ❌ Pas d'âge mentionné en hero (universel)
- ✅ Toujours centré vertical sur stages
- ✅ Q1 âge sans numérotation (gating)
- ✅ Anglais AU strict
- ✅ Timer uniquement sur result page

---

## HISTORIQUE DES VERSIONS

- **V1** : Hemistone-style topo map + horizon → rejected
- **V2** : Sun rising → "looks like a bug" rejected
- **V3** : Hero centré + horizon viré → manque animation
- **V4** : 5 plaisirs Schwartz + paths conditionnels brief
- **V5** : Code complet client-facing 5 paths + 5 plaisirs
- **V6** : Prix corrigés + centrage + Q1 sans num + constellation + SVG radar custom + icons + 25 testimonials
- **V7** : Removed Chart.js dependency
- **V8** : Availability modal flow d'urgence (loading + reveal + claim)

---

## REPRENDRE LA SESSION SUIVANTE

1. Ouvrir [outputs/reconnect-map-v1/index.html](outputs/reconnect-map-v1/index.html) dans le navigateur
2. Tester les 5 paths d'âge (un par un) jusqu'au verdict
3. Vérifier le flow availability modal
4. Lancer les **6 sous-agents** sur le brief V2 (cf section 12 du brief HTML)
5. Itérer post-audit
