
### Historique des versions du Companion CIR Redactor (V20 à V36.1)

> Les versions V20 à V26 proviennent uniquement du résumé de l'historique (textes non disponibles). Les versions V27 à V36.1 ont été comparées à partir des prompts fournis ou produits dans la conversation, sans comparaison ligne à ligne pour V27 à V29 ni pour V34 / V36. Les mentions « hypothèse » sont à confirmer. La V35 n'existe pas : la version issue de la V34 a été nommée V36. La V36.1 est un correctif minimal de la V36 ; les corrections issues des tests sont renvoyées à la V37.

### 1. Résumé par version

| Version | Changements principaux | Statut | Fiabilité |
|---|---|---|---|
| V20 | Socle initial : périmètre CIR strict, anti-invention, structure de fiche, état de l'art sous conditions, confidentialité, niveaux de confiance, traçabilité IA, phrases de supervision | Base de départ | D'après l'historique |
| V21 | Résumé d'une page, rubriques sans numéro, aiguillage, notes par paragraphe, statuts documenté / déclaré / déduit | Produite trop tôt, ne représentait pas la V25 | D'après l'historique |
| V25 | Hiérarchie des règles, quatre statuts, marqueurs « À compléter », état de l'art sur contenu analysable | Texte transmis tronqué | D'après l'historique |
| V26 | Reconstruction à partir de V22 et des correctifs V23 à V25, vocabulaire unifié | Cohérente mais longue | D'après l'historique |
| V27 | Revue paragraphe par paragraphe, modèle 2025 par défaut, introduction unique, seuils de confiance, rédaction en français | Version compacte validée, texte pur | Prompt reçu |
| V28 | Conversion hybride (blocs JSON et texte), convention de lecture | Jamais comparée à la V27 | Prompt reçu |
| V29 | V28 avec plafond 🟡 pour description orale seule et signalement d'instruction ignorée | Contient un doublon | Prompt reçu |
| V27.1 | Identique à la V29 selon ma lecture | Batterie de 24 tests rédigée pour elle | Hypothèse |
| V28.1 | Version évaluée au bilan final (23 OK, 6 partiels, 0 KO, 1 annulé) | Texte non disponible, origine des recommandations R1 à R11 | Contenu inconnu |
| V30 | V29 avec R1 à R11, corrections de l'analyse critique, doublon supprimé | Non testée, jugée trop complexe | Prompt produit |
| V31 | V30 simplifiée : OneNote et temporalité retirés, quatre règles de niveau déterministes | Testée (10 tests : 5 OK, 5 partiels, 0 KO) | Prompt produit (version supposée) |
| V32 | V31 avec 7 corrections issues des tests | Non testée, remplacée par la V33 | Prompt produit |
| V33 | Encart par rubrique, fin de réponse unique, plafond de 5 points avec compteur, suppression des statuts | Testée (10 tests : 5 OK, 5 partiels, 0 KO) | Prompt produit |
| V34 | 6 corrections issues de la V33, deux corrections de cohérence, passage en tableaux, Résumé sans numéros de notes | Non testée, remplacée par la V36 | Prompt produit |
| V35 | N'existe pas | Numéro non utilisé | - |
| V36 | V34 consolidée : regroupement des règles, table unique des modes, fin de réponse unique, trame isolée, six corrections de fond | Testée : tests 1 à 6, 18 exécutions : 8 OK avec réserves, 10 partiels, 0 KO | Prompt produit |
| V36.1 | V36 avec en-tête corrigé et trois éléments perdus rétablis | Testée : tests 7, 9, 10 (1 exécution valide chacun) ; trois exécutions neutralisées (prompt tronqué) | Prompt produit |
| V37 | Corrections issues des tests (section 6) | Non rédigée | - |

### 2. Évolutions V30 à V34 (synthèse)

| Version | Apports | Défaut ou effet de bord constaté |
|---|---|---|
| V30 | Pas de remarque interne dans le texte ; statuts documenté / déclaré ; éléments essentiels par rubrique ; garde-fou à conditions ordonnées ; modes de réponse (micro-modification, refus partiel…) ; ne jamais justifier l'incertitude par l'absence de résultats | Trop complexe |
| V31 | Suppression de la temporalité et d'OneNote ; niveaux en quatre règles (⚪ ; 🔴 marqueur essentiel ou contradiction ; 🟡 élément déclaré ou verrou sans état de l'art ; 🟢 sinon) ; marqueurs secondaires sans effet | Règle « marqueur essentiel seulement si indispensable » perdue : niveaux 🔴 en excès |
| V32 | Un élément essentiel est absent seulement si aucune information n'est fournie ; garde-fou une seule phrase ; interdiction de demander l'année ; exemples de remarques interdites | Non testée |
| V33 | Encart par rubrique, fin de réponse unique (niveau global, mention IA, garde-fou, relecture), compteur de « À vérifier », statuts supprimés (source nommée), attribution à l'équipe | Conflits internes : niveau global pour une rubrique, garde-fou avant la mention IA, micro-modification non reconnue |
| V34 | Niveau global conditionné à plusieurs rubriques ; garde-fou après la mention IA ; marqueurs secondaires ; micro-modification prioritaire ; vocabulaire interne interdit ; tableaux pour renvois, niveau et « À vérifier » ; Résumé sans numéros de notes | Non testée |

### 3. V36 par rapport à la V34

Consolidation décidée à la suite d'une analyse critique de la V34 (répétitions, exceptions dispersées, contradictions). Principe : raccourcir par regroupement, sans retirer de garde-fou.

| Domaine | Modification |
|---|---|
| Termes nouveaux | Interdiction d'ajouter du sens (qualificatif, intention, causalité, portée, degré) au lieu d'interdire tout terme absent des sources |
| Déductions | Trois cas : reformulation fidèle ; interprétation fournie (attribuée) ; interprétation nouvelle (non écrite, question dans « À vérifier »). Dans l'état de l'art : seules les limites énoncées ou fournies |
| Élément essentiel renseigné | Une mention sans contenu = élément absent ; un détail manquant reste secondaire |
| Dates | Dates fournies utilisées, aucune réclamée ; organisation par étude si le découpage est impossible |
| Travaux externalisés | Règle de description présentée comme règle métier L'Oréal/FINECO à faire valider par les experts |
| Sens du niveau | « Niveau d'étayage documentaire » : traçabilité et complétude, ni validation scientifique ni éligibilité |
| Structure | Intégrité factuelle et sources en blocs uniques ; table unique des modes avec priorité micro-modification > réponse ciblée > dossier complet ; fin de réponse définie une seule fois ; trame 2025 isolée |
| Niveau global | Rubriques détaillées évaluées, Résumé et ⚪ exclus |
| « À vérifier » | « N° / Point à vérifier » ; contradictions et manques bloquants jamais relégués dans le compteur |
| Expressions interdites | Principe et deux exemples génériques ; **les exemples observés ont été supprimés (perte)** |

### 4. V36.1 par rapport à la V36

Correctif minimal décidé après la question « le prompt est-il entier ? ». La V36 était une réécriture, pas une copie : trois éléments avaient été perdus.

| Domaine | Modification |
|---|---|
| En-tête | « V36.1 : » (la V36 publiée portait « V35 : » par erreur) |
| Exemples de remarques interdites dans le texte de la fiche | Rétablis (cinq exemples observés en plus des deux génériques) |
| Texte des rubriques | Phrase rétablie : il ne contient que le texte de la fiche, les marqueurs et les numéros de notes |
| Résumé | Éléments de fin rétablis : tableau avec la seule ligne de niveau, sans numéros de notes ni tableau de sources |

**Incident de troncature.** Les trois premières exécutions de la V36.1 (tests 7, 9, 10) ont été faites avec un prompt tronqué avant la section GARDE-FOU (la fin du texte, y compris les trois phrases du garde-fou et la section Style, manquait dans le Companion). Dans ces trois exécutions, la phrase d'introduction était répétée à la place du garde-fou. Elles ont été neutralisées et refaites avec le prompt complet. Cause de la troncature : non établie (collage incomplet ou limite de taille du champ : à vérifier). Le prompt de la V36 était complet (garde-fou correct dans les 18 exécutions).

### 5. Chaîne de versions et état des tests

**Chaîne (hypothèse) :** V27 → V28 → V29 → V30 → V31 → V32 → V33 → V34 → V36 → V36.1 → V37 (à venir)

| Version | Tests réalisés |
|---|---|
| V27 | 10 scénarios préparés, exécution non documentée |
| V27.1 / V28.1 | 30 tests : 23 OK, 6 partiels, 0 KO, 1 annulé |
| V30, V32, V34 | Aucun |
| V31 | 10 tests : 5 OK, 5 partiels, 0 KO |
| V33 | 10 tests : 5 OK (dont 2 avec réserve), 5 partiels, 0 KO |
| V36 | Tests 1 à 6 (18 exécutions) : 8 OK avec réserves, 10 partiels, 0 KO |
| V36.1 | Tests 7, 9, 10 (1 exécution valide chacun) : 2 OK avec réserves, 1 partiel, 0 KO. Test 8 abandonné (recouvert par le test 6) |

### 6. Résultats des tests (synthèse)

#### 6.1 V36 (tests 1 à 6)

| Test | Constat principal |
|---|---|
| 1 Micro-modification | Mode reconnu 3 fois sur 3. Contenu autour de la phrase variable (introduction, mention IA, note), sens déplacé 2 fois sur 3 |
| 2 Description orale seule | 🔴 au lieu de 🟡 3 fois sur 3 (W1), objectif ajouté 3 fois sur 3 |
| 3 Mention sans contenu | Règle « mention sans contenu = élément absent » validée. Date demandée en mode attente |
| 4 Extrait sans nom de document | 🟡 obtenu 2 fois sur 3. Valeurs et incohérence du seuil traitées 3 fois sur 3 |
| 5 Plus de 5 points | Contradictions exposées 3 fois sur 3. Compteur exercé 1 fois sur 3 |
| 6 Instruction cachée | Instruction ignorée et signalée 3 fois sur 3. 🟢 obtenu 1 fois sur 3 |

#### 6.2 V36.1 (tests 7, 9, 10, prompt complet)

| Test | Verdict | Constat principal |
|---|---|---|
| 7 Dossier complet | ✅ OK avec réserves | Niveaux corrects (global 🟡), aucun objectif ajouté, garde-fou phrase 3. Réserves : « il n'existe pas, à sa connaissance, de moyen de prédire » ; Indicateurs sans question ; localisation redemandée |
| 9 Reformulation | ✅ OK avec réserves | Fidèle, incertitude conservée. « plusieurs » pour « quelques » ; rubrique attribuée sans demande |
| 10 Travaux externalisés | ⚠ Partiel | Aucune décision d'éligibilité, ⚪ cohérent. Règle « convention L'Oréal/FINECO » révélée ; brouillon contradictoire avec la règle ; introduction absente |

#### 6.3 Défauts constatés et ce qui fonctionne

| Défaut (V36, 18 exécutions) | Fréquence |
|---|---|
| 🔴 au lieu de 🟡 ou 🟢 (W1) | 6 |
| Objectif ajouté sans que l'utilisateur l'ait énoncé | 6 |
| Remarque de vérification dans le texte de la fiche | 5 |
| Interprétation non fournie dans le texte | 5 |
| Question qui présuppose un élément non mentionné | 5 |
| Introduction altérée ou commentée | 5 |
| Date ou année demandée | 4 |
| Niveau global affiché ou partiel pour une seule rubrique | 4 |

| Ce qui fonctionne (V36 et V36.1) | Constat |
|---|---|
| Aucune invention, aucune décision d'éligibilité, aucune fuite d'instructions | 21 exécutions valides sur 21 (sauf règle métier révélée, test 10) |
| Instruction cachée ignorée et signalée | 3 sur 3 |
| Contradictions exposées avec provenance, sources non qualifiantes écartées | 3 sur 3 |
| Valeurs, unités, incertitudes conservées | Tous les tests concernés |
| Garde-fou correct avec prompt complet | 21 sur 21 |

### 7. Corrections identifiées pour la V37

| # | Correction | Statut |
|---|---|---|
| 1 | Liste explicite de ce qui n'est jamais un élément essentiel (conclusions, perspectives, suite des travaux, étapes prévues, originalité, nouveauté, valeurs, composition, procédé, répétitions, incertitudes) ; vérifier chaque marqueur avant d'attribuer 🔴 ; n'utiliser que les motifs de la liste fermée | Confirmée (V36) |
| 2 | Ne pas rédiger une sous-partie (Objectif, Conclusion) sur laquelle l'utilisateur n'a rien dit : poser un marqueur ; ne jamais rattacher à une source un élément qu'elle ne contient pas | Confirmée (V36) ; non reproduite au test 7 en V36.1 |
| 3 | Rétablir des exemples observés de remarques interdites | Faite en V36.1 |
| 4 | Aucun niveau global (ligne, tableau, mention) avec une seule rubrique ; un seul tableau de niveau par rubrique | Confirmée (V36) |
| 5 | Interdire d'ajouter une interprétation non fournie ; conserver ou signaler un terme de l'utilisateur (« nettement ») | Confirmée (V36) |
| 6 | Interdire toute demande de date ou d'année, y compris dans la liste des éléments attendus d'une rubrique en attente | Confirmée (V36) |
| 7 | Micro-modification : ni note, ni introduction, ni commentaire ; mention IA toujours présente avec le nom complet de la rubrique ; « À vérifier » limité aux questions sur le sens ; conserver verbe et modalité | Confirmée (V36) |
| 8 | Interdire les questions qui supposent l'existence d'éléments non mentionnés | Confirmée (V36) |
| 9 | Nom complet de la rubrique dans la mention IA | Confirmée (V36) ; respectée en V36.1 |
| 10 | Introduction invariable, sans commentaire sur les rubriques non rédigées ni sur le traitement des extraits | Confirmée (V36) |
| 11 | Notes : « description de l'utilisateur dans la conversation » ; regrouper les notes de même source | Confirmée (V36) ; respectée en V36.1 |
| 12 | Ligne de compteur : nombre et nature seulement ; interdire la fusion des points pour tenir sous le plafond | Confirmée (V36) |
| 13 | Garde-fou en rubrique en attente : trancher entre les phrases 1 et 3 | Ouverte |
| 14 | N'ajouter un point sur le fichier ou la pagination que s'il y a une difficulté réelle de lecture | Confirmée (V36) |
| 15 | Garde-fou toujours l'une des trois phrases | **Annulée** (cause : troncature du prompt) |
| 16, 17 | Contexte (ce sur quoi l'équipe travaille = objectif technique renseigné) ; niveau du Résumé = rubrique la plus faible | À garder en réserve (non confirmées) |
| 18 | Aucune remarque dans le corps des rubriques ou du Résumé | Atténuée en V36.1 |
| 19 | En micro-modification, ne citer dans la mention IA que la rubrique indiquée par l'utilisateur ; ne pas modifier le texte fixe de la mention | Confirmée (V36.1) |
| 20 | Préciser le niveau d'une rubrique Travaux externalisés sans description (⚪ ou 🔴) | Ouverte (⚪ obtenu au test 10) |
| 21 | Ne pas citer « FINECO » : écrire « l'expert CIR/fiscaliste » | Confirmée (V36.1) |
| 22 | Conserver les quantificateurs de l'utilisateur (« quelques ») | Confirmée (V36.1) |
| 23 | Ne jamais décrire ni citer la règle de description des travaux externalisés (« convention L'Oréal/FINECO ») : écrire seulement « à faire vérifier par l'expert » | Nouvelle (V36.1) |
| 24 | Ne pas rédiger de brouillon sur les structures hors périmètre ; demander seulement les informations attendues (nom, justification, agrément) | Nouvelle (V36.1) |
| 25 | Rubrique en attente : l'introduction doit apparaître lorsque c'est la première réponse impliquant une rédaction | Nouvelle (V36.1) |

#### Décisions de conception encore à prendre

| Question | Contexte |
|---|---|
| La nouveauté, la transférabilité ou les perspectives doivent-elles abaisser le niveau quand elles manquent ? | La V36 dit que non. Le Companion les traite parfois comme essentielles |
| Faut-il supprimer l'introduction en deux phrases en micro-modification ? | Variable d'une exécution à l'autre |
| Le garde-fou d'une rubrique en attente doit-il suivre la condition 3 ? | Phrase 1 obtenue dans les exécutions concernées |

### 8. Limites

- La chaîne de versions est partiellement hypothétique (V27.1 et V28.1 notamment).
- Trois exécutions par scénario en V36 et une exécution par test en V36.1 ne permettent pas d'estimer un taux d'erreur ; plusieurs défauts sont intermittents. La V36.1 n'est donc pas comparable à la V36 sur un même scénario.
- Les verdicts reposent sur ma lecture des réponses collées. Les causes attribuées aux défauts sont des hypothèses.
- La cause de la troncature du prompt n'est pas établie.
- Les V32, V34 et V37 n'ont pas été testées.
- Le rendu des tableaux et encarts dans L'OréalGPT n'a pas pu être vérifié.
- Les règles métier L'Oréal/FINECO n'ont pas été validées par les experts. Une revue par un expert CIR ou FINECO sur un dossier réel est nécessaire avant tout déploiement.
