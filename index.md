# Politique de Confidentialité de Causali

**Dernière mise à jour :** 7 novembre 2026  
**Date d'entrée en vigueur :** 7 novembre 2026  

**Causali** est une application de journal alimentaire et de suivi de symptômes hors ligne pour Android, développée par **Hugo EYNARD** (développeur indépendant).

---

## Résumé rapide

- **100 % hors ligne :** Causali ne possède aucun serveur distant, aucune base de données cloud et aucun compte utilisateur.
- **Aucune collecte de données :** Vos entrées alimentaires, vos symptômes et vos données de santé ne quittent jamais votre appareil. Le développeur ne peut ni consulter, ni accéder à, ni récupérer vos données.
- **Confidentialité et sécurité totales :** Vos données sont chiffrées au repos, exclues des sauvegardes cloud non chiffrées et sous votre contrôle exclusif.

---

## 1. Architecture 100 % hors ligne

- **Aucun serveur distant :** Causali ne communique avec aucun serveur externe ni service cloud.
- **Aucun accès à Internet :** Causali ne demande ni ne possède les autorisations réseau Android (INTERNET ou ACCESS_NETWORK_STATE). Le système d'exploitation Android empêche strictement l'application d'envoyer des données hors de votre appareil.
- **Aucun suivi tiers :** Causali ne contient aucun SDK publicitaire, aucun traceur d'analyse (analytics) et aucun service distant de rapport de plantage. Les composants de télémétrie en arrière-plan inclus transitivement par certaines bibliothèques locales sont désactivés dans le manifeste de l'application.

---

## 2. Informations traitées sur votre appareil

Toutes les informations que vous enregistrez sont stockées localement dans l'espace privé (sandbox) de l'application sur votre appareil :

- **Repas et nutrition :** Noms des repas, horodatages, poids des portions en grammes, valeurs nutritionnelles (calories, macronutriments, micronutriments), classifications FODMAP, ainsi que les aliments personnalisés ou recettes que vous créez.
- **Symptômes et santé :** Symptômes que vous choisissez de suivre (tels que ballonnements, douleurs abdominales, crampes, nausées, diarrhée, constipation, maux de tête ou fatigue), niveaux d'intensité (Léger, Modéré, Sévère) et horodatages.
- **Objectifs et préférences :** Objectifs quotidiens en calories et macronutriments, horaires de repas par défaut, repas prédéfinis et paramètres d'affichage.
- **Corrélations :** Calculs statistiques (risque relatif, intervalles de confiance à 95 %, coefficient Phi et valeurs p) effectués directement sur votre appareil pour vous aider à identifier les associations entre vos aliments et vos symptômes.

---

## 3. Autorisations de l'appareil

### Appareil photo (Optionnel)
- **Finalité :** Utilisé uniquement pour scanner les codes-barres de produits alimentaires (EAN-13, EAN-8, UPC-A, UPC-E) afin de les rechercher dans la base de données alimentaire hors ligne.
- **Traitement en mémoire en temps réel :** Les images de la caméra sont analysées temporairement dans la mémoire vive (RAM) de l'appareil via Google ML Kit et supprimées immédiatement après l'analyse.
- **Aucune photo ni vidéo :** Causali ne capture, n'enregistre, ne stocke et ne transmet jamais de photos ou de séquences vidéo.
- **Accès facultatif :** Vous pouvez refuser ou révoquer l'autorisation d'accès à l'appareil photo à tout moment et rechercher ou saisir vos aliments et codes-barres manuellement.

---

## 4. Sécurité et stockage local

- **Chiffrement de la base de données :** La base de données de votre journal (repas, aliments, recettes et symptômes) est chiffrée au repos à l'aide de SQLCipher (AES-256).
- **Chiffrement des paramètres :** Les repas par défaut enregistrés dans les paramètres de l'application sont chiffrés au repos à l'aide d'AES-256-GCM.
- **Clés protégées par le matériel :** Les clés de chiffrement sont générées et protégées par l'Android KeyStore avec isolation matérielle (TEE ou StrongBox) lorsque votre appareil le permet.
- **Exclusion des sauvegardes cloud :** Les règles de sauvegarde automatique Android (Auto Backup) et de transfert d'appareil à appareil sont configurées pour exclure la base de données de votre journal, vos paramètres et vos clés de chiffrement de tout envoi vers Google Drive ou transfert non chiffré.

---

## 5. Contrôle et suppression de vos données

- **Exportation des données :** Vous pouvez exporter à tout moment l'intégralité de votre journal, vos aliments personnalisés, vos recettes et vos paramètres sous forme de fichier JSON non chiffré ou d'archive ZIP chiffrée (AES-256) protégée par mot de passe via le sélecteur de fichiers système d'Android. Une fois le fichier exporté, vous êtes responsable de sa protection à l'emplacement choisi.
- **Importation des données :** Vous pouvez restaurer ou fusionner des sauvegardes précédentes à partir de fichiers stockés sur votre appareil.
- **Suppression d'entrées :** Vous pouvez modifier ou supprimer des entrées individuelles directement dans le journal à tout moment.
- **Effacement de toutes les données :** Vous pouvez supprimer définitivement toutes les données locales et les clés cryptographiques en effaçant le stockage de l'application dans les paramètres Android ou en désinstallant Causali. Aucune donnée n'existant sur des serveurs externes, la suppression locale est complète et irréversible.

---

## 6. Droits internationaux en matière de confidentialité

### Espace économique européen et Royaume-Uni (RGPD / UK GDPR)
- **Responsable du traitement :** Hugo EYNARD est le développeur de Causali. L'application fonctionnant entièrement hors ligne et ne transmettant aucune donnée, le développeur n'a aucun accès à vos données personnelles.
- **Catégories particulières de données (Article 9) :** Les données relatives à la santé et à l'alimentation sont traitées localement sur votre appareil sur la base de votre consentement explicite lorsque vous les saisissez dans l'application.
- **Exercice de vos droits :** Vous pouvez exercer vos droits d'accès, de rectification, d'effacement et de portabilité des données directement et à tout moment grâce aux fonctionnalités de consultation, de modification, de suppression et d'exportation intégrées à l'application.

### Californie (CCPA / CPRA)
- Causali ne collecte, ne vend, ne loue ni ne partage aucune information personnelle ou sensible, et ne pratique aucun suivi comportemental inter-contexte.

---

## 7. Confidentialité des mineurs

Causali ne s'adresse pas aux personnes de moins de 13 ans (ou de moins de 16 ans dans l'EEE et au Royaume-Uni) et ne collecte d'informations personnelles auprès de personne.

---

## 8. Avertissement médical et de santé

**Causali n'est pas un dispositif médical et ne fournit aucun diagnostic médical, avis clinique ou plan de traitement.**  
Les données nutritionnelles, classifications FODMAP et corrélations statistiques sont fournies uniquement à des fins d'information et de suivi personnel. Consultez toujours un médecin qualifié, un gastro-entérologue ou un diététicien-nutritionniste diplômé avant de prendre toute décision médicale ou d'entamer un régime d'éviction.

---

## 9. Modifications de cette politique de confidentialité

Toute révision de cette Politique de Confidentialité sera publiée à l'adresse https://hugogo22.github.io/causali-privacy-policy/ et résumée dans les notes de version de l'application.

---

## 10. Contact

Pour toute question ou remarque concernant cette Politique de Confidentialité, vous pouvez contacter :

- **Développeur :** Hugo EYNARD  
- **E-mail :** hugo.eynard.dev@gmail.com  
