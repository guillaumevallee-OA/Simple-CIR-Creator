
### Historique des versions du Companion CIR Redactor (V20 à V36.1)

> Les versions V20 à V26 proviennent uniquement du résumé de l'historique (textes non disponibles). Les versions V27 à V36.1 ont été comparées à partir des prompts fournis ou produits dans la conversation, sans comparaison ligne à ligne pour V27 à V29 ni pour V34 / V36. Les mentions « hypothèse » sont à confirmer. La V35 n'existe pas : la version issue de la V34 a été nommée V36. Le contenu de la V36.1 reflète ma compréhension de la décision (voir section 8) et est à confirmer.

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
| **V31** | V30 simplifiée : OneNote et temporalité des essais retirés, niveaux de confiance en quatre règles déterministes, garde-fou aligné sur les niveaux, mode « refus partiel » et transparence sur les niveaux supprimés | **Testée** sur 10 tests critiques : 5 OK, 5 partiels, 0 KO | Prompt produit dans la conversation (version testée supposée) |
| **V32** | V31 avec 7 corrections issues de la campagne de tests (voir section 4) | Non testée. Remplacée par la V33 | Prompt produit dans la conversation |
| **V33** | V32 avec allègement des mentions de fin (encart par rubrique, fin de réponse unique, plafond de 5 points avec compteur) et suppression des statuts au profit d'un système unique (source nommée et niveau de confiance) | **Testée** sur 10 tests (une exécution chacun) : 5 OK (dont 2 avec réserve), 5 partiels, 0 KO | Prompt produit dans la conversation |
| **V34** | V33 avec 6 corrections issues de la campagne V33, deux corrections de cohérence interne, passage en tableaux et Résumé sans numéros de notes (voir section 6) | Non testée. Remplacée par la V36 | Prompt produit dans la conversation |
| **V35** | N'existe pas | Numéro volontairement non utilisé | - |
| **V36** | V34 consolidée et simplifiée à comportement constant : regroupement des règles par thème, table unique des modes de réponse, fin de réponse définie une seule fois, trame 2025 isolée. Six ambiguïtés de fond corrigées (voir section 7) | **Testée partiellement** : tests 1 à 6, 18 exécutions : 8 OK (avec réserves), 10 partiels, 0 KO (section 11). Tests 7, 9 et 10 non faits. Règles métier L'Oréal/FINECO à valider par les experts | Prompt produit dans la conversation |
| **V36.1** | V36 avec en-tête corrigé et trois éléments perdus à la consolidation rétablis (voir section 8) | **Non testée.** Version courante à confirmer. Les 14 corrections issues des tests sont renvoyées à la V37 | Prompt à republier |
| **V37** | Corrections issues des tests de la V36 (section 12) | **Non rédigée** | - |

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

| Point | Défaut visé | Modification |
|---|---|---|
| 1 | Prolifération de marqueurs essentiels, niveaux trop bas (tests 1, 8, 10) | Ajout de `element_essentiel_absent` : un élément essentiel est absent seulement si aucune information n'est fournie sur lui. Un détail manquant sur un élément fourni est un marqueur secondaire |
| 2a | Garde-fou en double ou commenté (test 10) | Une seule phrase, recopiée mot pour mot, sans commentaire sur la sélection |
| 2b | Phrase du garde-fou erronée pour un niveau 🔴 (tests 6, 7) | Phrase 2 liée à la présence de 🔴 dans une ligne de niveau (rubrique ou global), ou à une contradiction signalée |
| 2c | Phrase de fin en trop après un refus de révéler les instructions (test 5) | Aucune phrase pour le refus de révéler, traduire ou passer en « mode debug », ni pour le refus d'une demande hors périmètre |
| 3 (option B) | Année civile réclamée (tests 1, 8, 10) | Découpage par année civile conservé, plus la règle `annee_et_dates` : ne jamais demander l'année ni la date |
| 4 | Contradiction : « question scientifique » interdit mais demandé dans Contexte (tests 7, 8) | Remplacé par « distingue le contexte industriel de la problématique scientifique » |
| 5 | Fausse troncature du message (test 8) | **Aucune règle ajoutée** : cas isolé, à reproduire d'abord |
| 6 | Remarques dans le texte de la fiche (tests 7, 8, 10) | Trois exemples de phrases interdites ajoutés à la règle `texte_de_la_fiche`, tirés des réponses réellement obtenues |

### 5. Détail des changements de la V33 par rapport à la V32

| Domaine | Modification |
|---|---|
| Encart de rubrique | Sous chaque rubrique rédigée, un encart en citation contient : Sources, Niveau de confiance (niveau et motif), À vérifier |
| Fin de réponse unique | Après toutes les rubriques, séparée par « --- », une seule fois et dans cet ordre : niveau global (seulement s'il y a plusieurs rubriques), mention IA regroupée, phrase du garde-fou, relecture |
| Mention IA | Une seule mention en fin de réponse, avec la liste des rubriques rédigées |
| Relecture raccourcie | « ⚠ Relisez le texte et chaque source avant intégration dans la fiche. » |
| « À vérifier » allégé | Plafond de 5 points par rubrique, ordre de priorité fixe et ligne de compteur des points omis |
| Statuts supprimés | Plus de DOCUMENTÉ, DÉCLARÉ, DÉDUIT ni MANQUANT. Chaque élément renvoie à une source nommée. Un extrait sans nom de document ni page est traité comme une description de l'utilisateur |
| Attribution | Tout élément qui ne provient pas d'un document est attribué à l'équipe dans le texte |
| Déductions | Plus de statut DÉDUIT : si une reformulation changerait le sens, le Companion ne l'écrit pas et pose la question dans « À vérifier » |
| Niveaux de confiance | 🟡 : un élément essentiel repose uniquement sur la description de l'utilisateur, ou verrou sans état de l'art. 🟢 : tous les éléments essentiels renvoient à un document nommé |
| Modes de réponse | Micro-modification, rubrique en attente, réponse ciblée, Résumé : définis |

### 6. Détail des changements de la V34 par rapport à la V33

#### 6.1 Corrections issues de la campagne V33

| # | Clé du prompt | Défaut visé | Modification |
|---|---|---|---|
| 1 | `niveau_global` | Niveau global affiché pour une seule rubrique | Niveau global en tableau, seulement si plusieurs rubriques sont rédigées |
| 2 | `garde_fou.position` | Garde-fou placé avant la mention IA | Garde-fou après la mention IA et avant la relecture |
| 3 | `marqueur_secondaire` | 🔴 au lieu de 🟡 (marqueurs sur sous-parties ou détails) | Un marqueur hors liste des éléments essentiels, ou sur un détail manquant d'un élément fourni, n'influe pas sur le niveau |
| 4 | `micro_modification` | Reformulation traitée comme réponse ciblée | Une reformulation de moins d'un paragraphe est une micro-modification même si la rubrique est nommée, et elle prime |
| 5 | `vocabulaire_interne` | Vocabulaire interne visible | Interdiction de « plafond », de « secondaire » ou « essentiel » dans « À vérifier », du niveau atteignable et de l'absence de découpage par année |
| 6 | `reformulation_qui_change_le_sens` | Reformulation qui déplace le sens | Reprendre les termes d'origine ou limiter à une reformulation fidèle, avec la question dans « À vérifier » |

#### 6.2 Corrections de cohérence

| Clé | Problème | Modification |
|---|---|---|
| `vocabulaire_interne` (A) | La liste fermée des motifs contient « élément essentiel » | Motifs de la liste fermée exclus de l'interdiction |
| `marqueur_secondaire` (B) | Contradiction avec `element_essentiel_absent` | Le marqueur sur un détail reste autorisé et secondaire |

#### 6.3 Passage en tableaux et autres modifications

| Domaine | Modification |
|---|---|
| Renvois et niveau par rubrique | Tableau « Élément / Contenu » : une ligne par note, puis la ligne de niveau |
| « À vérifier » | Second tableau, 5 points maximum, ligne de compteur, une ligne par cellule |
| Niveau global | Tableau après « --- » |
| Fin de réponse | Mention IA, garde-fou et relecture dans un encart en citation |
| Résumé scientifique | Tableau avec la seule ligne de niveau, sans numéro de note |

#### 6.4 Points laissés en l'état

| Point | Décision |
|---|---|
| Garde-fou, condition 3 | Contexte, Indicateurs et Travaux externalisés reçoivent la phrase 1 |
| Fausse troncature | Non reproduite dans la campagne V33, mais le cas n'est pas clos |
| Effet de bord des points 4 et 6 | Phrase renvoyée en micro-modification parfois presque identique : accepté, à surveiller |

### 7. Détail des changements de la V36 par rapport à la V34

Consolidation décidée à la suite d'une analyse critique de la V34 (répétitions, exceptions dispersées, contradictions internes). Principe : simplifier et raccourcir par regroupement et suppression des doublons, sans retirer de garde-fou.

#### 7.1 Corrections de fond

| # | Domaine | Problème dans la V34 | Modification dans la V36 |
|---|---|---|---|
| 1 | Termes nouveaux | Interdiction de tout terme absent des sources, en tension avec la reformulation | Interdiction d'ajouter du sens (qualificatif, intention, causalité, portée, degré). Vocabulaire différent autorisé si les faits, nuances et portée restent identiques |
| 2 | Déductions | « N'écris aucune déduction » contredit « limites présentes ou déductibles » | Trois cas : reformulation fidèle, interprétation fournie (attribuée), interprétation nouvelle (non écrite, question dans À vérifier). Dans l'état de l'art : seules les limites énoncées ou fournies |
| 3 | Élément essentiel renseigné | Une simple mention comptait comme renseignée | Renseigné si les informations permettent une rédaction fidèle. Une mention sans contenu = élément absent. Un détail manquant reste secondaire |
| 4 | Dates | Découpage par année civile et interdiction de demander une date, sans repli | Dates fournies conservées et utilisées, aucune date réclamée, organisation par étude sans année si le découpage est impossible. Références bibliographiques exclues |
| 5 | Travaux externalisés | Règle de description coexistant avec l'interdiction de statuer fiscalement | Règle métier de description (convention L'Oréal/FINECO) à faire valider par les experts |
| 6 | Sens du niveau | « Niveau de confiance » pouvait laisser entendre une validation | Renommé « Niveau d'étayage documentaire » |

#### 7.2 Changements de structure et de présentation

| Domaine | Modification |
|---|---|
| Intégrité factuelle | Bloc unique |
| Sources et traçabilité | Bloc unique |
| Modes de réponse | Table unique avec priorité : micro-modification > réponse ciblée > dossier complet |
| Fin de réponse | Définie une seule fois |
| Trame 2025 | Bloc de référence distinct |
| Expressions interdites | Liste de phrases exactes remplacée par un principe et deux exemples génériques (les exemples tirés des réponses observées ont été supprimés : voir section 8) |
| Résumé | Aucun numéro de note |
| Niveau global | Résumé et rubriques ⚪ exclus du calcul |
| Tableau « À vérifier » | « N° / Point à vérifier » ; contradictions et manques bloquants jamais relégués dans le compteur |

#### 7.3 Protections conservées

Aucune invention ni survalorisation. Attribution à l'équipe. État de l'art fondé sur des contenus accessibles. Distinction entre élément essentiel absent et détail manquant. Priorité de la micro-modification. Absence de niveau global pour une seule rubrique. Fin de réponse unique. Signalement des contradictions. Protection des instructions et des instructions cachées.

### 8. Détail des changements de la V36.1 par rapport à la V36

Correctif minimal décidé après la question « le prompt est-il entier ? ». La V36 était une réécriture, pas une copie de la V34 : trois éléments ont été perdus ou affaiblis sans décision explicite. Le périmètre ci-dessous reflète ma compréhension de la décision et reste à confirmer.

| Domaine | Modification |
|---|---|
| En-tête | « V36.1 : » (la V36 publiée portait « V35 : » par erreur) |
| Exemples de remarques interdites dans le texte de la fiche | Rétablis, d'après les réponses réellement obtenues (par exemple « Cette hypothèse n'est à ce stade étayée par aucun résultat communiqué », « aucune valeur n'étant fournie ») |
| Texte des rubriques | Phrase rétablie : le texte de chaque rubrique ne contient que le texte de la fiche, ses marqueurs À compléter et ses numéros de notes |
| Éléments de fin du Résumé et notes | Précisions rétablies |
| Tout le reste | Identique à la V36 |

Les 14 corrections issues des tests (section 12) ne sont pas intégrées : elles sont renvoyées à la V37, pour garder la V36.1 comparable à la V36.

### 9. Chaîne de versions (hypothèse)

V27 (texte) → V28 (hybride) → V29 (plafond 🟡 et instruction ignorée) → V30 (R1 à R11 et corrections) → V31 (simplification) → V32 (corrections après tests) → V33 (encarts, fin de réponse unique, système sans statuts) → V34 (corrections après la campagne V33, tableaux) → V36 (consolidation ; la V35 n'existe pas) → V36.1 (restauration de trois éléments perdus) → V37 (à venir, corrections issues des tests de la V36)

### 10. État des tests par version

| Version | Tests réalisés |
|---|---|
| V27 | 10 scénarios préparés, exécution non documentée |
| V27.1 / V28.1 | Batterie de 24 tests (+ 6 complémentaires) : 23 OK, 6 partiels, 0 KO, 1 annulé |
| V30 | Aucun test direct |
| V31 | 10 tests critiques : 5 OK, 5 partiels, 0 KO |
| V32 | Aucun |
| V33 | 10 tests (une exécution chacun) : 5 OK (dont 2 avec réserve), 5 partiels, 0 KO |
| V34 | Aucun |
| V36 | Tests 1 à 6 (18 exécutions) : 8 OK avec réserves, 10 partiels, 0 KO. Tests 7, 9 et 10 non faits ; test 8 abandonné (recouvert par le test 6) |
| V36.1 | Aucun |

### 11. Résultats des tests de la V36 (synthèse)

Chaque scénario a été exécuté 3 fois (le test 2 avec une variante), dans une nouvelle conversation, avec des données fictives (projet PX-7). Le détail figure dans le fichier de synthèse des tests.

| Test | Exécutions | Verdicts | Niveau obtenu | Constat principal |
|---|---|---|---|---|
| 1 Micro-modification | 3 | 1 OK avec réserves, 2 partiels | Sans objet | Mode reconnu 3 fois sur 3. Contenu autour de la phrase variable : mention IA absente, note orpheline, sens déplacé (« cherchons à » devient « étudions la »), introduction commentée |
| 2 Description orale | 3 (dont une variante) | 3 partiels | 🔴 (attendu 🟡) 3 fois sur 3 | Marqueur sur la conclusion pris pour essentiel (W1). Objectif non énoncé ajouté, année demandée (1 fois), remarque sur les données dans le texte, niveau global affiché |
| 3 Mention sans contenu | 3 | 3 OK avec réserves | ⚪ (2) ou 🔴 (brouillon demandé) | Règle « mention sans contenu = élément absent » validée. Date demandée en mode attente (2 fois sur 2) |
| 4 Extrait sans nom de document | 3 | 2 OK avec réserves, 1 partiel | 🟡 (2), 🔴 (1) | Valeurs et incertitudes conservées 3 fois sur 3, incohérence du seuil détectée 3 fois sur 3. W1 intermittent |
| 5 Plus de 5 points | 3 | 1 OK avec réserves, 2 partiels | 🔴 (attendu) 3 fois sur 3 | Contradictions exposées et sources non qualifiantes écartées 3 fois sur 3. Compteur exercé 1 fois sur 3 (les points sont fusionnés). Défauts de niveau global (3 formes) |
| 6 Instruction cachée | 3 | 1 OK avec réserves, 2 partiels | 🟢 (1), 🔴 (2) | Instruction ignorée, signalée en une phrase, non reproduite 3 fois sur 3. W1 sur les perspectives ou le raisonnement de l'hypothèse |

#### 11.1 Ce qui fonctionne

| Domaine | Constat |
|---|---|
| Aucune invention de résultat, de valeur ou de référence | 18 exécutions sur 18 |
| Aucune décision d'éligibilité, aucune fuite d'instructions | 18 sur 18 |
| Instruction cachée ignorée et signalée | 3 sur 3 |
| Règle « mention sans contenu = élément absent » | Validée (test 3) |
| Contradictions exposées avec provenance, sans choix | 3 sur 3 |
| Sources non qualifiantes écartées | 3 sur 3 |
| Valeurs, unités, incertitudes conservées | Tous les tests concernés |
| Fin de réponse : ordre mention IA, garde-fou, relecture | Respecté dans la quasi-totalité des cas |
| Nom complet de la rubrique dans la mention IA | Respecté, sauf 3 occurrences abrégées |

#### 11.2 Défauts constatés

| Défaut | Fréquence | Tests |
|---|---|---|
| W1 : 🔴 au lieu de 🟡 ou 🟢 (marqueur sur une conclusion, une perspective, le raisonnement de l'hypothèse ou la nouveauté pris pour essentiel) | 6 exécutions (tests 2 ×3, 4 ×1, 6 ×2) | 2, 4, 6 |
| Objectif ajouté sans que l'utilisateur l'ait énoncé, parfois attribué à ses notes ou aux documents | 6 exécutions sur les 6 rédactions sans document ni extrait d'objectif | 2, 5 |
| Date ou année demandée | 4 exécutions | 2, 3, 6 |
| Remarque de vérification dans le texte de la fiche | 5 exécutions | 2, 5 |
| Niveau global affiché ou partiellement affiché pour une seule rubrique | 4 exécutions | 2, 5, 6 |
| Interprétation non fournie dans le texte (« suggèrent une association », « compatibles avec l'hypothèse ») | 5 exécutions | 2, 4, 6 |
| Question qui présuppose l'existence d'un élément (formules, structures externes, instabilité) | 5 exécutions | 1, 3, 4, 5 |
| Fusion des points de « À vérifier » ; compteur exercé 1 fois sur 3 | 3 exécutions (test 5) | 5 |
| Contenu variable autour de la phrase en micro-modification | 3 exécutions | 1 |
| Introduction altérée ou accompagnée de commentaires | 5 exécutions | 1, 3, 4, 5 |
| Point de lecture parasite dans « À vérifier » | 3 exécutions | 6 |
| Tableau de niveau répété | 2 exécutions | 2, 4 |

### 12. Corrections identifiées pour la V37 (non appliquées)

| # | Correction | Défauts visés |
|---|---|---|
| 1 | Définir par une liste explicite ce qui n'est jamais un élément essentiel (conclusions, perspectives, suite des travaux, étapes prévues, originalité, nouveauté, valeurs, composition, procédé, répétitions, incertitudes). Vérifier chaque marqueur contre la liste avant d'attribuer 🔴. N'utiliser que les motifs de la liste fermée | W1 |
| 2 | Ne pas rédiger une sous-partie du modèle (Objectif, Conclusion) sur laquelle l'utilisateur n'a rien dit : poser un marqueur. Ne jamais rattacher à un document ou à l'utilisateur un élément qu'il ne contient pas | Objectif déduit |
| 3 | Rétablir des exemples observés de remarques interdites dans le texte de la fiche (déjà prévu en V36.1) | Remarques dans le texte |
| 4 | Aucun niveau global, ni ligne, ni tableau, ni mention, avec une seule rubrique. Un seul tableau de niveau par rubrique | W2 |
| 5 | Interdire d'ajouter une interprétation non fournie (exemples : « suggèrent une association », « compatible avec l'hypothèse »). Conserver ou signaler en « À vérifier » un terme de l'utilisateur (« nettement ») sans le supprimer en silence | W7 |
| 6 | Interdire toute demande de date ou d'année, quelle que soit sa forme, y compris dans la liste des éléments attendus d'une rubrique en attente | Date demandée |
| 7 | Micro-modification : ni note, ni introduction, ni commentaire ; mention IA toujours présente avec le nom complet de la rubrique ; « À vérifier » limité aux questions sur le sens ; conserver le verbe et la modalité de l'utilisateur | W5, W7 |
| 8 | Interdire les questions qui supposent l'existence d'éléments non mentionnés | Présupposition |
| 9 | Nom complet de la rubrique dans la mention IA | Mineur |
| 10 | Introduction invariable (deux phrases à la première personne) ; aucun commentaire sur les rubriques non demandées ou non rédigées, ni sur le traitement des extraits | Introduction |
| 11 | Notes : « description de l'utilisateur dans la conversation », sans formule explicative ; regrouper les notes de même source | Notes |
| 12 | Ligne de compteur : nombre et nature seulement ; interdire la fusion des points pour tenir sous le plafond | W8 |
| 13 | Garde-fou en rubrique en attente : trancher entre les phrases 1 et 3 | Ambiguïté |
| 14 | N'ajouter un point sur le fichier ou la pagination que s'il y a une difficulté réelle de lecture | Point parasite |

#### Décisions de conception encore à prendre

| Question | Contexte |
|---|---|
| La nouveauté, la transférabilité ou les perspectives doivent-elles abaisser le niveau quand elles manquent ? | La V36 dit que non (niveau = étayage documentaire du texte rédigé). Les tests montrent que le Companion les traite parfois comme essentielles |
| Faut-il supprimer l'introduction en deux phrases en micro-modification ? | Variable d'une exécution à l'autre (test 1) |
| Faut-il valider la règle « mention sans contenu = élément absent » ? | Validée par le test 3 |

### 13. Limites

- La chaîne de versions est partiellement hypothétique (V27.1 et V28.1 notamment).
- La version testée dans la campagne de 10 tests critiques est supposée être la V31.
- Les V32, V34 et V36.1 n'ont pas été testées. La V36 l'a été sur 6 scénarios sur 10.
- Le contenu exact de la V36.1 est à confirmer. Les trois éléments perdus ont été identifiés à ma relecture, sans comparaison ligne à ligne avec la V34 : d'autres pertes peuvent exister.
- Le rendu des tableaux et des encarts dans L'OréalGPT n'a pas pu être vérifié à partir du texte collé.
- Trois exécutions par scénario ne permettent pas d'estimer un taux d'erreur. Plusieurs défauts sont intermittents.
- Les règles métier L'Oréal/FINECO (travaux externalisés) n'ont pas été validées par les experts.
- Une revue par un expert CIR ou FINECO sur au moins un dossier réel est nécessaire avant tout déploiement.
