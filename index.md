---
layout: default
title: Politique de confidentialité — Aura
---

# Politique de confidentialité — Aura (Heures miroirs)

**Dernière mise à jour :** 10 octobre 2026  
**Éditeur :** développeur de l’application Aura (`com.aura.mirror`)  
**Contact :** [dev@cmaboite.me](mailto:dev@cmaboite.me)

Cette politique décrit les données traitées par l’application mobile **Aura**, version **1.5.12** (code 17). Elle s’applique à la version Android publiée sur Google Play.

## 1. Résumé

Aura est une application **locale d’abord**. Les contenus spirituels, le journal, les pensées libres, l’humeur du jour et le profil sont stockés **sur l’appareil**. Aucun compte Aura n’est créé. Le développeur ne collecte ni ne partage aucune donnée : il n’y a pas de serveur Aura, pas d’analyse d’audience, pas de publicité et pas d’outil de signalement de plantages dans l’application.

## 2. Données stockées sur l’appareil

| Donnée | Finalité | Stockage |
|--------|----------|----------|
| Entrées du journal d’éveil, y compris les pensées libres | Mémoriser vos réflexions | Appareil uniquement, chiffré (coffre Android) |
| Humeur du jour (niveau de 1 à 5, note éventuelle) | Mémoriser votre humeur | Appareil uniquement, chiffré (coffre Android) |
| Historique des synchronicités détectées | Afficher vos détections récentes | Stockage local, **sans chiffrement** |
| Profil (prénom optionnel, date de naissance optionnelle) | Numérologie personnelle et résonance avec les heures miroirs | Appareil uniquement, chiffré (coffre Android) |
| Préférences (notifications, langue, achat débloqué, rappels d’humeur, demandes d’avis) | Fonctionnement de l’app | Stockage local, **sans chiffrement** |

Les pensées libres sont des entrées de journal enregistrées sans heure miroir. Elles suivent le même stockage chiffré que les autres entrées.

L’humeur du jour est chiffrée avant enregistrement, avec la même clé non exportable du coffre Android (Keystore) que le journal et le profil. Si le chiffrement ne peut pas aboutir, le texte reste sur l’appareil, en clair, et n’est pas envoyé.

L’historique des détections et les préférences restent en clair sur l’appareil. Les préférences comprennent notamment la langue des notifications, l’indicateur d’achat débloqué, les horaires des rappels d’humeur et les dates des demandes d’avis. Un nombre de chemin de vie, calculé sur l’appareil à partir de la date de naissance, est aussi recopié en clair dans ces préférences pour les notifications locales. La date de naissance elle-même reste dans le profil chiffré.

Ces données **ne sont pas synchronisées** vers un cloud Aura. Elles sont exclues de la sauvegarde Android et du transfert vers un autre appareil. Elles sont perdues si vous désinstallez l’application (sauf restauration d’achat Play).

Les statistiques (rythme du journal, séries, heures les plus présentes, moyennes et tendances d’humeur) sont calculées sur l’appareil à partir de ces données. Elles ne sont pas envoyées.

## 3. Achats in-app

L’achat unique `aura_full_unlock` est traité par **Google Play Billing**. Au démarrage et au retour au premier plan, Aura interroge Google Play pour vérifier les achats réellement possédés sur l’appareil (état payé, accusé de réception). Aucun jeton d’achat n’est envoyé au développeur. Un indicateur local sert uniquement si Play est injoignable, pour ne pas reverrouiller un achat déjà confirmé. Un remboursement ou une annulation retire l’accès dès que Play répond. Il n’y a pas de serveur Aura.

Google peut traiter des données de paiement selon sa propre politique :  
[https://policies.google.com/privacy](https://policies.google.com/privacy)

## 4. Notifications et alarmes

Pour vous signaler une heure miroir au **regard** (écran allumé encore verrouillé) ou au **déverrouillage**, Aura utilise :

- les notifications locales ;
- des événements système (allumage d’écran, déverrouillage, redémarrage) ;
- une alarme exacte au début de chaque minute miroir (permission `SCHEDULE_EXACT_ALARM`, que vous accordez), qui réveille l’app le temps de cette minute si l’écran est déjà allumé et verrouillé.

Pour l’humeur du jour, Aura peut aussi planifier des notifications locales : un rappel du matin, activé par défaut, et un rappel plus tard dans la journée seulement si vous l’activez et que l’accès complet est débloqué. Le texte de ces notifications est générique. Il ne contient ni votre niveau d’humeur ni votre note. L’appareil relit localement les humeurs déjà notées dans la journée uniquement pour savoir s’il doit encore afficher le rappel.

Ces mécanismes restent **sur l’appareil**. Aucun contenu de notification n’est envoyé à un serveur Aura.

## 5. Liens externes

L’écran Ressources peut ouvrir des liens (YouTube, Amazon, pages auteurs) via le navigateur ou une application tierce. Ces services ont leurs propres politiques. Aura n’envoie pas votre journal à ces sites.

Le profil peut ouvrir [boxproof.fr](https://boxproof.fr/?utm_source=aura&utm_medium=app&utm_campaign=profile) dans le navigateur. L’adresse contient des paramètres UTM (`utm_source=aura`, `utm_medium=app`, `utm_campaign=profile`). Aura n’intègre pas de traceur : elle n’ajoute pas d’outil d’analyse d’audience. Ce que le site fait ensuite de cette visite relève de ce site, pas d’Aura.

« Une idée ? Écris-moi » ouvre l’application de messagerie de votre appareil, avec le destinataire `dev@cmaboite.me` et un objet qui indique la version d’Aura. Aucun texte de journal, aucune humeur et aucune date de naissance n’est joint.

## 6. Export vers une IA, partage et avis

**Export vers une IA.** Si vous le demandez, Aura prépare sur l’appareil un texte (un prompt) à partir des données déjà présentes : journal, pensées libres, humeurs et détections. Aura n’envoie pas ce texte. Vous pouvez le copier dans le presse-papiers, ou le partager vers une application de votre choix par la feuille de partage du système. À partir de là, les données partent sous votre responsabilité et sous celle de l’IA ou de l’application que vous choisissez. La case « Inclure ma date de naissance et mon chemin de vie » est décochée par défaut : la date de naissance n’entre dans le prompt que si vous la cochez.

**Carte d’heure miroir.** « Partager cette heure » produit une image (l’heure, son titre, un extrait du texte de cette heure fourni par l’application, le nom Aura et le lien de la fiche Play) et la propose dans la feuille de partage. Cette carte ne contient pas votre prénom, votre date de naissance, votre journal ni votre humeur.

**Avis.** « Noter Aura » ouvre la fiche Google Play de l’application, via l’API In-App Review de Google. Séparément, après que vous quittez une page de signification ouverte depuis une notification, Aura peut demander à Google d’afficher le dialogue d’avis intégré (`requestReview`). Google décide d’afficher ou non ce dialogue et en gère le contenu. Aura n’envoie pas votre avis au développeur. Elle note seulement, sur l’appareil et sans chiffrement, les dates de ces demandes.

**Raccourcis du lanceur.** Deux raccourcis (nouvelle pensée, humeur du jour) ouvrent directement l’écran correspondant dans Aura. Ils ne transmettent rien.

## 7. Polices et réseau

Les polices (Noto Serif, Plus Jakarta Sans) sont **embarquées** dans l’application. Aura ne les télécharge pas, et n’appelle pas Google Fonts.

Aura ne contacte pas de serveur du développeur. Les échanges avec l’extérieur sont Google Play Billing, l’API d’avis Google Play, et les actions que vous lancez vous-même : liens (dont boxproof.fr), message `mailto`, copie ou partage du prompt, partage de la carte d’heure. Aucun outil d’analyse d’audience, de publicité ou de signalement de plantages n’est intégré à l’application.

## 8. Données personnelles sensibles

La **date de naissance**, si vous la renseignez, sert aux calculs de numérologie **locaux** et, seulement si vous cochez l’option dans l’export, au prompt préparé sur l’appareil. Elle n’est pas transmise au développeur. Le journal d’éveil (pensées libres comprises), l’humeur du jour et le profil sont stockés uniquement sur l’appareil et chiffrés avec une clé non exportable du coffre Android (Keystore). Ils sont exclus de la sauvegarde Android.

## 9. Conservation et suppression

Les données locales restent jusqu’à désinstallation ou effacement du stockage de l’app. La sauvegarde Android ne les copie pas. Pour supprimer vos données : désinstallez Aura, ou effacez les données de l’application dans les réglages Android.

## 10. Enfants

Aura n’est pas destinée aux enfants de moins de 13 ans (ou l’âge minimum local applicable). Ne renseignez pas de données d’un enfant.

## 11. Vos droits

Selon votre résidence (ex. RGPD en UE), vous pouvez demander l’accès ou la suppression de vos données. Le développeur n’en détient pas de copie : il n’y a pas de compte cloud. La suppression passe par l’effacement local ou la désinstallation. Pour toute question : [dev@cmaboite.me](mailto:dev@cmaboite.me).

## 12. Modifications

Cette politique peut évoluer. La date en tête de page sera mise à jour. Les changements importants pourront être signalés via la fiche Play Store ou une mise à jour de l’application.

## 13. English summary

Version 1.5.12 (version code 17) stores the journal, free thoughts (journal entries with no mirror hour), the mood of the day (a level from 1 to 5 and an optional note), and the optional profile (first name, birth date) **on your device**, encrypted with a non-exportable Android Keystore key. If encryption cannot complete, that text stays on the device in plain form and is not sent. Detection history and preferences are stored locally **without encryption**. Preferences include notification language, the unlock flag, mood-reminder times, in-app review request dates, and a life-path number copied in the clear for local notifications. The birth date itself stays in the encrypted profile. Statistics are calculated on the device. There is no Aura server, no analytics, no advertising and no crash-reporting tool in the app. Data is excluded from Android backup.

The one-time purchase `aura_full_unlock` is handled by Google Play Billing. The app asks Play whether the purchase is owned and does not send the purchase token to the developer. Local notifications and exact alarms detect mirror hours and, separately, can remind you to log a mood. Those reminders use generic text and do not include your mood. Fonts are bundled; the app does not download Google Fonts.

If you ask for an AI export, Aura builds the prompt on the device. You copy it to the clipboard or share it with an app you choose. Aura does not send it. From then on, the data is your responsibility and that of the AI you choose. The birth-date option is off by default and is included only if you turn it on. Sharing a mirror-hour card sends an image of the hour, its title, an excerpt of that hour’s text, the Aura name and the Play listing link — not your name, birth date, journal or mood. “Écris-moi” opens your mail app to dev@cmaboite.me with the app version as the subject and no journal attached. “Noter Aura” opens the Play listing through Google’s In-App Review API. After you leave a meaning page opened from a notification, the app may ask Google to show the in-app review dialog; Google decides whether to show it. The boxproof.fr link in the profile opens in the browser with UTM parameters; the app includes no tracker. Two launcher shortcuts only open screens inside the app. Contact: dev@cmaboite.me.
