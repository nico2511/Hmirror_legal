---
layout: default
title: Politique de confidentialité — Aura
---

# Politique de confidentialité — Aura (Heures miroirs)

**Dernière mise à jour :** 9 octobre 2026  
**Éditeur :** développeur de l’application Aura (`com.aura.mirror`)  
**Contact :** l’adresse e-mail indiquée sur la fiche Google Play de l’application Aura

Cette politique décrit les données traitées par l’application mobile **Aura** à partir de la version **1.5.10**. Elle s’applique à la version Android publiée sur Google Play.

## 1. Résumé

Aura est une application **locale d’abord**. Les contenus spirituels, le journal et le profil sont stockés **sur l’appareil**. Aucun compte Aura n’est créé. Le développeur ne collecte ni ne partage aucune donnée : il n’y a pas de serveur Aura, pas d’analyse d’audience, pas de publicité et pas d’outil de signalement de plantages dans l’application.

## 2. Données stockées sur l’appareil

| Donnée | Finalité | Stockage |
|--------|----------|----------|
| Entrées du journal d’éveil | Mémoriser vos réflexions | Appareil uniquement, chiffré (coffre Android) |
| Historique des synchronicités détectées | Afficher vos détections récentes | Stockage local |
| Profil (prénom optionnel, date de naissance optionnelle) | Numérologie personnelle et résonance avec les heures miroirs | Appareil uniquement, chiffré (coffre Android) |
| Préférences (notifications, langue, achat débloqué) | Fonctionnement de l’app | Stockage local |

Ces données **ne sont pas synchronisées** vers un cloud Aura. Elles sont exclues de la sauvegarde Android et du transfert vers un autre appareil. Elles sont perdues si vous désinstallez l’application (sauf restauration d’achat Play).

## 3. Achats in-app

L’achat unique `aura_full_unlock` est traité par **Google Play Billing**. Au démarrage et au retour au premier plan, Aura interroge Google Play pour vérifier les achats réellement possédés sur l’appareil (état payé, accusé de réception). Aucun jeton d’achat n’est envoyé au développeur. Un indicateur local sert uniquement si Play est injoignable, pour ne pas reverrouiller un achat déjà confirmé. Un remboursement ou une annulation retire l’accès dès que Play répond. Il n’y a pas de serveur Aura.

Google peut traiter des données de paiement selon sa propre politique :  
[https://policies.google.com/privacy](https://policies.google.com/privacy)

## 4. Notifications et alarmes

Pour vous signaler une heure miroir au **regard** (écran allumé encore verrouillé) ou au **déverrouillage**, Aura utilise :

- les notifications locales ;
- des événements système (allumage d’écran, déverrouillage, redémarrage) ;
- une alarme exacte au début de chaque minute miroir (permission `SCHEDULE_EXACT_ALARM`, que vous accordez), qui réveille l’app le temps de cette minute si l’écran est déjà allumé et verrouillé.

Ces mécanismes restent **sur l’appareil**. Ils servent uniquement à détecter les heures miroirs. Aucun contenu de notification n’est envoyé à un serveur Aura.

## 5. Liens externes

L’écran Ressources peut ouvrir des liens (YouTube, Amazon, pages auteurs) via le navigateur ou une application tierce. Ces services ont leurs propres politiques. Aura n’envoie pas votre journal à ces sites.

## 6. Polices et réseau

Les polices (Noto Serif, Plus Jakarta Sans) sont **embarquées** dans l’application. Aura ne les télécharge pas, et n’appelle plus Google Fonts. Les seuls échanges réseau sont Google Play Billing (achat et vérification) et les liens que vous ouvrez vous-même. Aucun serveur Aura n’est contacté.

## 7. Données personnelles sensibles

La **date de naissance**, si vous la renseignez, sert uniquement aux calculs de numérologie **locaux**. Elle n’est pas transmise au développeur. Le journal d’éveil et le profil (dont la date de naissance) sont stockés uniquement sur l’appareil et chiffrés avec une clé non exportable du coffre Android (Keystore). Ils sont exclus de la sauvegarde Android.

## 8. Conservation et suppression

Les données locales restent jusqu’à désinstallation ou effacement du stockage de l’app. La sauvegarde Android ne les copie pas. Pour supprimer vos données : désinstallez Aura, ou effacez les données de l’application dans les réglages Android.

## 9. Enfants

Aura n’est pas destinée aux enfants de moins de 13 ans (ou l’âge minimum local applicable). Ne renseignez pas de données d’un enfant.

## 10. Vos droits

Selon votre résidence (ex. RGPD en UE), vous pouvez demander l’accès ou la suppression de vos données. Le développeur n’en détient pas de copie : il n’y a pas de compte cloud. La suppression passe par l’effacement local ou la désinstallation. Pour toute question : utilisez l’e-mail indiqué sur la fiche Play Store.

## 11. Modifications

Cette politique peut évoluer. La date en tête de page sera mise à jour. Les changements importants pourront être signalés via la fiche Play Store ou une mise à jour de l’application.

## 12. English summary

From version 1.5.10, Aura stores journal entries, detection history, an optional profile (first name, birth date) and preferences **on your device**. The developer does not collect or share any data: there is no Aura server, no analytics, no advertising and no crash-reporting tool in the app. The journal and profile (including birth date) are encrypted with a non-exportable Android Keystore key and excluded from Android backup and device transfer. The one-time purchase `aura_full_unlock` is handled by Google Play Billing: the app asks Google Play whether the purchase is owned and does not send the purchase token to the developer. Fonts (Noto Serif, Plus Jakarta Sans) are bundled; the app does not download Google Fonts. Local notifications and exact alarms run on-device only to detect mirror hours and send nothing out. The only network calls are Google Play Billing and links you choose to open. Contact details: see the Play Store listing.
