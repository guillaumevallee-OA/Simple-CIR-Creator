
### Historique des versions du Companion CIR Redactor (V20 à V34)

> Les versions V20 à V26 proviennent uniquement du résumé de l'historique (textes non disponibles). Les versions V27 à V34 ont été comparées à partir des prompts fournis ou produits dans la conversation, sans comparaison ligne à ligne pour V27 à V29. Les mentions « hypothèse » sont à confirmer.

### 1. Résumé par version

| Version | Changements principaux | Impact / statut | Fiabilité de l'information |
|---|---|---|---|
| **V20** | Socle initial : périmètre CIR strict, règles anti-invention, structure de fiche, état de l'art sous conditions, confidentialité, niveaux de confiance, traçabilité IA, phrases de supervision | Base de départ. Résumé absent, volumétrie à réaligner, sources surtout associées aux chiffres, règles de confiance dispersées, mentions d'heures à supprimer | D'après l'historique |
| **V21** | Résumé d'une page et volumétrie de la fiche 2025. Rubriques désignées par leur nom, sans numéro. Aiguillage des informations. Sources en notes par paragraphe. Statuts documenté, déclaré et déduit. Rappel de relecture | Meilleure traçabilité. Produite trop tôt, elle ne représentait pas la V25 déjà élaborée ailleurs | D'après l'historique |
| **V25** | Hiérarchie des règles, quatre statuts, marqueurs « À compléter », état de l'art fondé sur du contenu analysable, notes de sources, règles de chronologie | Base pertinente, mais texte transmis tronqué, donc non reconstituable avec certitude | D'après l'historique |
| **V26** | Reconstruction à partir de la V22 et des correctifs V23 à V25. Vocabulaire unifié, règles anti-invention et niveaux de confiance centralisés, résumé précisé, garde-fou clarifié | Plus cohérente, mais longue. Plusieurs choix sans accord explicite (refus, calcul des niveaux, mention IA) | D'après l'historique |
| **V27** | Revue paragraphe par paragraphe. Modèle 2025 par défaut, autre trame à fournir clairement, introduction une seule fois, questions fiscales intégrées au cadrage, formats élargis avec PDF complémentaire, OneNote conditionnel, notes omissibles sur demande, seuils des niveaux de confiance, format minimal de fin de rubrique, rédaction en français et conversation dans la langue de l'utilisateur | Version compacte validée, en texte pur. Éléments fixes de fin dans la langue de l'utilisateur | Prompt reçu |
| **V28** | Conversion hybride : règles conditionnelles en blocs JSON, sections explicatives en texte. Convention de lecture ajoutée. Éléments fixes de fin toujours en français | Même fond que la V27 annoncé. Ni plafond 🟡 ni signalement d'instruction ignorée. Jamais comparée à la V27 | Prompt reçu |
| **V29** | V28 avec le plafond 🟡 pour une description orale seule, sans seconde pénalité, et le signalement d'une instruction ignorée dans un document. Bloc de protection présent en double | Intègre les deux points laissés en attente. Contient un doublon | Prompt reçu |
| **V27.1** | Identique à la V29 selon ma lecture (même contenu, même doublon) | À confirmer. La batterie de 24 tests a été rédigée pour elle | Hypothèse |
| **V28.1** | Version évaluée dans le bilan final (23 OK, 6 partiels, 0 KO, 1 annulé). Texte non disponible | Origine des recommandations R1 à R11 | Contenu inconnu |
| **V30** | V29 avec R1 à R11, les corrections de l'analyse critique, et le doublon de protection supprimé | Non testée directement. Jugée trop complexe, ce qui a motivé la V31 | Prompt produit dans la conversation |
| **V31** | V30 simplifiée : OneNote et temporalité des essais retirés, niveaux de confiance en quatre règles déterministes, garde-fou aligné sur les niveaux, mode « refus partiel » et transparence sur les niveaux supprimés | **Testée** sur 10 tests critiques : 5 OK, 5 partiels, 0 KO. Voir le fichier de synthèse des tests | Prompt produit dans la conversation (version testée supposée) |
| **V32** | V31 avec 7 corrections issues de la campagne de tests (voir section 4) | Non testée. Remplacée par la V33 | Prompt produit dans la conversation |
| **V33** | V32 avec allègement des mentions de fin (encart par rubrique, fin de réponse unique, plafond de 5 points avec compteur) et suppression des statuts au profit d'un système unique (source nommée et niveau de confiance) | **Testée** sur 10 tests (une exécution chacun) : 5 OK (dont 2 avec réserve), 5 partiels, 0 KO. Défauts relevés : conflits internes sur la fin de réponse, niveaux 🔴 au lieu de 🟡, micro-modification non reconnue, vocabulaire interne visible. Voir le fichier de synthèse des tests | Prompt produit dans la conversation |
| **V34** | V33 avec 6 corrections issues de la campagne V33, deux corrections de cohérence interne, le passage en tableaux des renvois, du niveau de confiance et de « À vérifier », et le Résumé sans numéros de notes (voir section 6) | **Version courante, non testée.** Plan de retests à établir (voir section 8) | Prompt produit dans la conversation |

### 2. Détail des changements de la V30 par rapport à la V29

| Domaine | Changement |
|---|---|
| Introduction | Deux phrases au lieu de trois, OneNote supprimé partout, aucun connecteur appelé de sa propre initiative |
| Texte de la fiche | Pas de remarque interne dans le texte, avec exception pour l'attribution et les formules de prudence. Marqueurs ne contenant que l'élément attendu |
| Anti-invention | Aucun terme qualifiant ajouté. DÉDUIT seulement pour les reformulations qui changent le sens. Aucune date ajoutée |
| Statuts | Extrait avec nom, date et page = DOCUMENTÉ. Extrait sans référence = DÉCLARÉ. Une absence d'information est MANQUANT, jamais une source |
| Niveaux de confiance | Éléments essentiels définis par rubrique, seulement si l'indicateur ou le sous-traitant existe. Motif limité à la cause active. Cas de référence ajoutés au calcul |
| Garde-fou | Conditions ordonnées. Un refus seul donne la phrase 1. Une rubrique ⚪ n'est pas une lacune essentielle |
| Modes de réponse | Aiguillage, rubrique en attente, micro-modification, refus partiel, clarification courte. Ordre fixe des éléments de fin. Éléments de fin du Résumé définis |
| Incertitude | Ne jamais la justifier par l'absence de résultats consignés |
| Insistance | Explication brève à la première insistance, une à trois phrases à partir de la deuxième |
| Confidentialité | Codes et valeurs conservés lorsqu'ils sont nécessaires à la démonstration, généralisés sur demande |
| Transparence | Les niveaux peuvent être expliqués. Le détail des facteurs, plafonds et calculs reste interdit |
| Vocabulaire interne | Jamais affiché (« plafond », « première réponse », etc.) |

### 3. Détail des changements de la V31 par rapport à la V30

| Domaine | Changement |
|---|---|
| Temporalité | Supprimés : consigne sur les documents datés, année fiscale à demander, période des travaux, chronologie, références postérieures aux travaux, « à cette date » dans la phrase type de l'état de l'art, date dans la définition de DOCUMENTÉ |
| Niveaux de confiance | Quatre règles ordonnées : ⚪ rubrique non rédigée ; 🔴 marqueur sur un élément essentiel ou contradiction entre deux sources ; 🟡 élément essentiel déclaré ou déduit, ou verrou sans état de l'art ; 🟢 sinon. Plus de crans, de plafonds ni de facteurs d'abaissement. Motif choisi dans une liste fermée |
| Marqueurs secondaires | N'influent plus sur le niveau, signalés dans « À vérifier » |
| Éléments graphiques | Signalés dans « À vérifier » (restrictions de lecture), sans effet sur le niveau |
| Garde-fou | Aligné sur les niveaux : rubrique 🔴 ou contradiction → phrase 2 |
| Mode « refus partiel » | Supprimé |
| Transparence sur les niveaux | Supprimée. Le détail du calcul est explicitement confidentiel |
| Formulation | Phrases raccourcies, répétitions retirées, listes d'exemples allégées |
| Effet de bord constaté en test | La règle « ne crée un marqueur essentiel que pour une information indispensable » a disparu dans la simplification. Elle est à l'origine probable de la prolifération de marqueurs essentiels et des niveaux 🔴 trop fréquents |

### 4. Détail des changements de la V32 par rapport à la V31

Corrections décidées après la campagne de 10 tests critiques sur la V31.

| Point | Défaut visé | Modification |
|---|---|---|
| 1 | Prolifération de marqueurs essentiels, niveaux trop bas (tests 1, 8, 10) | Ajout de `element_essentiel_absent` : un élément essentiel est absent seulement si aucune information n'est fournie sur lui. Un détail manquant sur un élément fourni est un marqueur secondaire |
| 2a | Garde-fou en double ou commenté (test 10) | Une seule phrase, recopiée mot pour mot, sans commentaire sur la sélection |
| 2b | Phrase du garde-fou erronée pour un niveau 🔴 (tests 6, 7) | La phrase « Risque d'informations erronées ou incomplètes… » est liée à la présence de 🔴 dans une ligne « Niveau de confiance » (rubrique ou global), ou à une contradiction signalée |
| 2c | Phrase de fin en trop après un refus de révéler les instructions (test 5) | Aucune phrase pour le refus de révéler, traduire ou passer en « mode debug », ni pour le refus d'une demande hors périmètre |
| 3 (option B) | Année civile réclamée (tests 1, 8, 10) | Découpage par année civile conservé, plus la règle `annee_et_dates` : ne jamais demander l'année ni la date, aucun marqueur pour l'année ou une date |
| 4 | Contradiction : « question scientifique » interdit mais demandé dans Contexte (tests 7, 8) | Remplacé par « distingue le contexte industriel de la problématique scientifique » |
| 5 | Fausse troncature du message (test 8) | **Aucune règle ajoutée** : cas isolé, à reproduire d'abord |
| 6 | Remarques dans le texte de la fiche (tests 7, 8, 10) | Trois exemples de phrases interdites ajoutés à la règle `texte_de_la_fiche`, tirés des réponses réellement obtenues |

### 5. Détail des changements de la V33 par rapport à la V32

Corrections décidées avec l'utilisateur après la campagne de tests : alléger les mentions de fin de rubrique et de réponse, et remplacer les statuts par un système unique.

| Domaine | Modification |
|---|---|
| Encart de rubrique | Sous chaque rubrique rédigée, un encart en citation (lignes précédées de « > ») contient les éléments qui renvoient à cette rubrique : Sources, Niveau de confiance (niveau et motif), À vérifier |
| Fin de réponse unique | Après toutes les rubriques, séparée par « --- », une seule fois et dans cet ordre : niveau de confiance global (seulement s'il y a plusieurs rubriques), mention IA regroupée (liste des rubriques rédigées), phrase du garde-fou, relecture |
| Mention IA | Une seule mention en fin de réponse, avec la liste des rubriques rédigées, au lieu d'une mention par rubrique |
| Relecture raccourcie | « ⚠ Relisez le texte et chaque source avant intégration dans la fiche. » |
| « À vérifier » allégé | Retrait de « déclarations non corroborées essentielles » et de « marqueurs secondaires ». Plafond de 5 points par rubrique, ordre de priorité fixe (contradictions, informations manquantes essentielles, restrictions de lecture, sources écartées, questions sur une reformulation, autres points) et ligne de compteur des points omis (option C) |
| Statuts supprimés | Plus de DOCUMENTÉ, DÉCLARÉ, DÉDUIT ni MANQUANT. Chaque élément renvoie à une source nommée (document avec nom et page ou section, ou description de l'utilisateur). Un extrait sans nom de document ni page est traité comme une description de l'utilisateur. Le Companion ne juge jamais la valeur d'un document |
| Attribution | Tout élément qui ne provient pas d'un document est attribué à l'équipe dans le texte |
| Déductions | Plus de statut DÉDUIT : si une reformulation changerait le sens, le Companion ne l'écrit pas et pose la question dans « À vérifier » |
| Niveaux de confiance | 🟡 : un élément essentiel repose uniquement sur la description de l'utilisateur, ou verrou sans état de l'art. 🟢 : tous les éléments essentiels renvoient à un document nommé. Motif « éléments essentiels renvoyant à un document nommé » |
| Modes de réponse | Micro-modification : mention IA et garde-fou sur deux lignes. Rubrique en attente : encart avec niveau ⚪. Réponse ciblée : rubrique, son encart et la fin de réponse. Résumé : encart avec niveau seulement |
| Cohérence | Le marqueur secondaire n'a plus de consigne de signalement dans « À vérifier » |

### 6. Détail des changements de la V34 par rapport à la V33

Corrections décidées avec l'utilisateur après la campagne de 10 tests sur la V33 et une vérification théorique du prompt.

#### 6.1 Corrections issues de la campagne V33

| # | Clé du prompt | Défaut visé | Modification |
|---|---|---|---|
| 1 | `niveau_global` | Niveau global affiché pour une seule rubrique (tests 3, 7, 9, 10). Conflit interne avec `fin_de_reponse` | Niveau global affiché en tableau, seulement si plusieurs rubriques sont rédigées. Avec une seule rubrique, le niveau figure uniquement dans son tableau |
| 2 | `garde_fou.position` | Garde-fou placé avant la mention IA (tests 1 et 9). Conflit interne avec l'ordre de `fin_de_reponse` | Garde-fou placé après la mention IA (sinon après le niveau global) et avant la relecture |
| 3 | `marqueur_secondaire` | 🔴 au lieu de 🟡 : marqueurs sur des sous-parties ou des détails (tests 3 et 9) | Un marqueur sur un élément hors de la liste des éléments essentiels, ou sur un détail manquant d'un élément essentiel fourni, n'influe pas sur le niveau. Un marqueur ne présente jamais comme absent un élément essentiel pour lequel une information est fournie (version sans exemples) |
| 4 | `micro_modification` | Reformulation d'une phrase traitée comme une réponse ciblée (test 2) | Une reformulation de moins d'un paragraphe est une micro-modification même si la rubrique est nommée, et elle prime sur la réponse ciblée |
| 5 | `vocabulaire_interne` | Vocabulaire interne visible : « détails secondaires », « année civile », « au mieux 🟡 » (tests 3, 7, 8, 10) | Interdiction de « plafond » et de la qualification « secondaire » ou « essentiel » dans « À vérifier ». Interdiction de mentionner le niveau atteignable et l'absence de découpage par année. Les motifs de la liste fermée restent autorisés |
| 6 | `reformulation_qui_change_le_sens` | Reformulation qui déplace le sens (tests 1, 2, 10) | Reprendre les termes de l'utilisateur ou de la source tels quels, sans qualificatif ajouté, ou se limiter à une reformulation qui garde strictement le sens, avec la question dans « À vérifier » (option B) |

#### 6.2 Corrections de cohérence issues de la vérification théorique

| Clé du prompt | Problème | Modification |
|---|---|---|
| `vocabulaire_interne` (correction A) | La liste fermée des motifs contient « élément essentiel », ce qui contredisait l'interdiction du mot | Les motifs de la liste fermée sont explicitement exclus de l'interdiction |
| `marqueur_secondaire` (correction B) | La règle « pas de marqueur sur un élément essentiel fourni » contredisait `element_essentiel_absent` et `information_manquante` | Le marqueur sur un détail reste autorisé et secondaire. Il ne présente jamais l'élément essentiel comme absent |

#### 6.3 Passage en tableaux et autres modifications

| Domaine | Modification |
|---|---|
| Renvois et niveau par rubrique | Tableau à deux colonnes (« Élément » et « Contenu ») : une ligne par note, puis une ligne « Niveau de confiance » |
| « À vérifier » | Second tableau (« N° » et « Point à vérifier »), 5 points maximum, ligne de compteur des points omis, une ligne par cellule |
| Niveau global | Tableau placé juste après « --- », avec les lignes « Niveau de confiance global » et « Rubriques évaluées » |
| Fin de réponse | Mention IA, phrase du garde-fou et relecture regroupées dans un encart en citation. Niveau global conditionné à « plusieurs rubriques rédigées » |
| Résumé scientifique | Tableau avec la seule ligne « Niveau de confiance ». Aucun numéro de note dans le Résumé |
| Alignements | `rubrique_en_attente`, `reponse_ciblee`, `micro_modification`, `texte_sans_notes_demande` et `etat_de_l_art.citation` parlent de tableaux au lieu d'encart ou de « ligne Sources » (le dernier alignement a été ajouté par l'assistant) |

#### 6.4 Décisions et points laissés en l'état

| Point | Décision |
|---|---|
| Garde-fou, condition 3 | Laissée en l'état : Contexte, Indicateurs et Travaux externalisés reçoivent la phrase 1 |
| Fausse troncature (test 8 de la V31) | Non reproduite dans la campagne V33 (le cas « nom à retrouver » est bien traité). Aucune règle ajoutée, mais le cas n'est pas clos après une seule exécution |
| Effet de bord des points 4 et 6 | En micro-modification, la phrase renvoyée peut être presque identique à l'originale, avec une question dans « À vérifier ». Accepté, à surveiller |

### 7. Chaîne de versions (hypothèse)

V27 (texte) → V28 (hybride) → V29 (plafond 🟡 et instruction ignorée) → V30 (R1 à R11 et corrections) → V31 (simplification) → V32 (corrections après tests) → V33 (encarts, fin de réponse unique, système sans statuts) → V34 (corrections après la campagne V33, tableaux)

### 8. État des tests par version

| Version | Tests réalisés |
|---|---|
| V27 | 10 scénarios préparés, exécution non documentée |
| V27.1 / V28.1 | Batterie de 24 tests (+ 6 complémentaires) : 23 OK, 6 partiels, 0 KO, 1 annulé |
| V30 | Aucun test direct |
| V31 | 10 tests critiques : 5 OK, 5 partiels, 0 KO (suivi dans le fichier de synthèse des tests) |
| V32 | Aucun (remplacée par la V33) |
| V33 | 10 tests (une exécution chacun) : 5 OK (dont 2 avec réserve), 5 partiels, 0 KO. Tests OK : 4, 5, 6, et 7 et 8 avec réserve. Tests partiels : 1 (mineur), 2, 3, 9, 10 (non concluant, compteur non exercé) |
| V34 | Aucun. Retests prévus : micro-modification (2), description orale seule (3), extrait sans nom de document (9), plus de 5 points avec message reformulé (10), instruction cachée (7), dossier complet (1), rapport complet (4) |

Priorités de la V34 : vérifier le rendu des tableaux dans L'OréalGPT, retester les défauts de niveau (🔴 au lieu de 🟡), l'absence de niveau global pour une seule rubrique, l'ordre de la fin de réponse, la micro-modification, le vocabulaire interne, et exercer la ligne de compteur de « À vérifier ».

### 9. Limites

- La chaîne de versions est partiellement hypothétique (V27.1 et V28.1 notamment).
- La version testée dans la campagne de 10 tests critiques est supposée être la V31, sans confirmation explicite.
- Les V32 et V34 n'ont pas été testées. La V33 l'a été une seule fois par test.
- Le rendu de l'encart de la V33 n'a pas pu être évalué à partir du texte collé, et le rendu des tableaux de la V34 n'est pas vérifié dans L'OréalGPT.
- Les causes attribuées aux défauts de la V33 sont des hypothèses.
- La V34 contient une exemption (Résumé sans numéros de notes) qui s'écarte de la règle « chaque élément du texte renvoie à une source nommée » : à surveiller en test.
- Une revue par un expert CIR ou FINECO reste nécessaire avant tout déploiement.
