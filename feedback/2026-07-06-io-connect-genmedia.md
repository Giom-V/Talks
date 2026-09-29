# Feedback & Coaching Critique — Google I/O Connect '26

* **Date :** 6 juillet 2026
* **Événement :** Google I/O Connect 2026 (Berlin)
* **Talk :** *Build creative apps with the GenMedia suite (I/O Connect ‘26)*
* **Speaker :** Guillaume Vernade (Developer Relations Engineer, Google DeepMind)
* **Captation officielle :** [YouTube Google for Developers](https://www.youtube.com/watch?v=nRLZqaNOrwQ) (26m35s)
* **Support Slides :** [Slides PDF (16 slides)](../2026-07-06%20-%20Build%20creative%20apps%20with%20the%20GenMedia%20suite.pdf) • [Cookbook Notebook (`Book_illustration.ipynb`)](https://github.com/google-gemini/cookbook/blob/main/examples/Book_illustration.ipynb)
* **Contexte important :** Ce créneau avait été initialement conçu et préparé comme un **workshop interactif pour développeurs**, avant d'être présenté sous forme de talk sur scène.
* **Type d'analyse :** Revue vidéo multimodale native (Gemini 3.1 Pro), posture sans complaisance ("sans gants").

---

## 🎯 Synthèse Globale : Le Syndrome du "Workshop Déguisé en Talk"

Le projet présenté — prendre un livre du domaine public (*The Wind in the Willows*) et enchaîner toute la suite GenMedia (Gemini, Imagen / Nano Banana, Veo, Lyria, TTS, Omni) pour créer un livre interactif — est **techniquement brillant** et offre un fil rouge narratif hyper cohérent.

Mais sur le plan scénique, **ce n'est pas un keynote : c'est un "scroll de notebook" sur grand écran.** Parce que la session avait été pensée comme un workshop hands-on, le format tente de faire rentrer au chausse-pied un tutoriel pas-à-pas dans une conférence unidirectionnelle de 26 minutes. Résultat : la présence scénique est sacrifiée derrière le pupitre au profit du défilement de cellules Colab.

---

## 1. 🧍‍♂️ Présence Scénique & Langage Corporel

* **Le bunker du pupitre (Syndrome du DJ) :** Dès **`[02:38]`**, tu te réfugies derrière le pupitre pour piloter ton notebook Colab. C'est la mort de la présence scénique : pendant 24 minutes, une barrière physique te sépare de la salle et tu deviens le commentateur e-sport de ton propre écran.
* **Ancrage & Swaying :** Sur les 2 premières minutes debout hors pupitre, on retrouve le balancier chronique (*swaying*) d'une jambe sur l'autre et l'hésitation des mains (clicker, poche).
* **Regard & Connexion :** Une fois derrière le MacBook, ton regard est happé à **80% par l'écran**. Tu lèves les yeux ponctuellement, mais tu parles à ton code plutôt qu'aux développeurs dans la salle.
* **Voix, Débit & Phobie du silence :** Tu es en apnée parce que tu veux couvrir toute la matière d'un workshop en 26 minutes. Le débit est mitraillette, sans **aucun silence stratégique**, et les respirations sont comblées par des mots de remplissage (*"so"*, *"like"*, *"basically"*, *"um"*).

---

## 2. 🛠️ Ce qui marche vs Ce qui souffre du Format Workshop

### ❌ Ce qui souffre sur une scène de conférence
* **`[03:05]` Setup & Clé API / `[03:41]` Paramètre `retry` :** Vital dans un atelier où les participants codent en direct ; soporifique en keynote.
* **`[08:16]` Scroll dans l'output JSON brut :** Faire défiler un long tableau JSON généré par Gemini pour extraire les personnages casse le rythme visuel. Il fallait une slide schématique propre : *Livre $\rightarrow$ JSON structuré $\rightarrow$ Prompt Imagen*.

### 🌟 Ce qui sauve le talk
* **Le fil conducteur (*The Wind in the Willows*) :** Au lieu d'aligner un catalogue froid d'APIs déconnectées, chaque modèle (Gemini $\rightarrow$ Imagen $\rightarrow$ Veo $\rightarrow$ Lyria $\rightarrow$ TTS) vient enrichir le même objet créatif.
* **L'honnêteté intellectuelle du dev :** Quand un modèle hallucine un détail rigolo (`[14:08]` le rat avec le marteau dans Veo, ou une voix TTS inattendue), tu ne le caches pas sous le tapis : tu en ris et tu expliques pourquoi. Cela crée une crédibilité immédiate auprès d'un public d'ingénieurs.

---

## 3. 🖥️ Rendu Visuel : Slides, Code & Démos

* **L'interface Colab sur grand écran :** Le thème sombre est agréable, mais la police du code est trop petite pour le fond de la salle, et l'UI de Colab (barres de scroll, menus, logs d'exécution) pollue l'image.
* **Le péché visuel majeur (Assets coincés dans des cellules) :** Quand Imagen génère de superbes illustrations **`[09:34]`** ou que Veo anime les personnages **`[14:08]`**, ces médias sont enfermés dans de petites cellules d'output Jupyter et tu scrolles déjà vers la suite ! **Ces résultats doivent exploser en plein écran pendant 5 secondes** pour laisser la salle admirer la qualité des modèles.

---

## 4. ⏱️ Autopsie Minutée des Moments Clés

* **`[00:04]` Intro :** Présentation rapide, léger swaying. Il manque un *hook* visuel immédiat : montrer dès la 1re minute le livre multimédia finalisé (avec voix, musique et vidéo) pour faire saliver la salle avant d'ouvrir le capot.
* **`[02:18]` Le QR Code du Cookbook :** Bascule officielle en mode tutoriel Colab.
* **`[05:22]` File API & Context Caching :** Explication très claire de l'intérêt du caching sur un livre entier pour économiser des tokens.
* **`[08:16]` Extraction JSON des personnages :** Trop brut à l'écran.
* **`[09:34]` Générations Imagen / Nano Banana :** Très beaux visuels, mais scrollés beaucoup trop vite.
* **`[14:08]` Animation Veo :** Superbe démo et excellente blague spontanée sur le rat au marteau.
* **`[15:54]` Musique Lyria :** Pendant l'écoute audio, l'écran reste figé sur une cellule de code avec un mini player HTML. Il fallait afficher le prompt musical et les paroles en grand.
* **`[19:12]` Bedtime Story multi-voix (Gemini TTS) :** Le meilleur moment conceptuel du talk — l'orchestration multi-speakers donne vie au texte.
* **`[24:16]` Démo Gemini Omni (Perroquet & Licorne) :** Très drôle, réveille immédiatement la salle, même si la transition avec le livre est un peu abrupte.
* **`[26:12]` Conclusion :** Expédiée en 15 secondes (*"Voilà, merci"*). Manque une phrase de clôture forte et 3 secondes d'ancrage avant de quitter la scène.

---

## 5. 📈 Évolution entre I/O Connect '26 (Juillet) et dotAI Paris (Septembre)

| Dimension | I/O Connect '26 (06/07/2026) | dotAI Paris (17/09/2026) | Bilan de progression |
| :--- | :--- | :--- | :--- |
| **Posture sur scène** | 🔴 Enfermé 24 min derrière le pupitre (mode live-coding). | 🟢 **100% hors pupitre**, face à la salle en format keynote pur. | **Progrès majeur (+2 pts)** |
| **Mise en valeur des démos** | 🔴 Médias coincés dans de petites cellules Colab scrollées vite. | 🟢 Vidéos (SIMA, QA) intégrées directement dans les slides. | **Progrès net (+1.5 pt)** |
| **Lisibilité des slides** | 🟠 Scroll de code et de JSON brut dans Colab. | 🟡 Mieux structuré, mais encore pollué par des screenshots bruts et petits textes *(erreur imputable au coach IA qui a généré les slides !)*. | **À corriger côté Coach IA** |
| **Ancrage corporel** | 🟠 Swaying dès qu'il sort du pupitre. | 🟠 Swaying toujours présent sur scène. | **Défaut persistant (=)** |
| **Débit & Silences** | 🔴 Débit rapide, zéro silence, *"so / basically / like"*. | 🔴 Débit toujours trop rapide, punchlines enchaînées sans pause de 3s. | **Priorité #1 du prochain talk** |

---

## 6. 💡 Le Playbook de Survie quand un "Workshop sur Scène" est Imposé

Quand un organisateur impose un format atelier/workshop sur un grand amphithéâtre ou une scène principale (contrainte fréquente en conférence tech), le speaker ne peut pas simplement dire non. En revanche, il peut éviter le piège du "bunker" grâce à 4 règles strictes :

1. **L'arme secrète dans Google Colab : Le raccourci `Alt + V`** :
   * En pleine démo, `Alt + V` bascule la cellule courante ou son résultat (image Imagen, clip vidéo Veo, output audio) en **mode focus / plein écran**.
   * Cela évite à 500 personnes de plisser les yeux sur un carré de 200px perdu au milieu des barres de menus de Colab.
2. **Le "Podium Breakout" (La Règle des 3 Postures)** :
   * **Posture 1 (Le Setup Clavier, ≤ 20s)** : Derrière le laptop uniquement pour lancer l'exécution.
   * **Posture 2 (Le Décrochage Immédiat)** : Dès que la cellule tourne (inférence IA qui prend 5 à 15s), **interdiction de regarder l'écran**. Faire 3 pas en avant vers le bord de scène, regarder la salle dans les yeux et expliquer le concept sous le capot.
   * **Posture 3 (La Révélation `Alt + V`)** : Revenir taper `Alt + V`, projeter l'output en grand et commenter le résultat face à l'audience, jamais face au MacBook.
3. **Setup Machine Pré-Talk (Stage Readiness)** :
   * Zoom navigateur à **125% - 150%**.
   * Masquage complet de la barre latérale (Table des Matières).
   * Thème à contraste adapté au projecteur de la salle.
4. **Filet de Sécurité Anti-Latence (Pre-baked Outputs)** :
   * Conserver systématiquement les sorties déjà exécutées en cache dans le notebook ou sur des slides de secours pour parer aux défaillances du Wi-Fi de scène.

