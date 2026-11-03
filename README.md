# 🐠 JBL ProScan Card — dépôt historique

> [!IMPORTANT]
> **JBL ProScan Card est désormais intégrée au code de l'[intégration JBL ProScan](https://github.com/AuroreVgn/JBL-ProScan).**
> Ce dépôt séparé n'est plus destiné à recevoir de nouvelles versions de la carte après publication et validation de son intégration. Il est conservé pour l'historique du projet, les anciennes versions et les captures d'écran.
>
> **La version de l'intégration incluant la carte n'est pas encore publiée.** En attendant, conservez votre installation actuelle de la carte indépendante.

## Installer la carte

Dès qu'une version de l'intégration incluant la carte sera publiée, installez ou mettez à jour **[AuroreVgn/JBL-ProScan](https://github.com/AuroreVgn/JBL-ProScan)** via HACS / Marketplace ou manuellement, puis redémarrez Home Assistant.

La ressource JavaScript est fournie par l'intégration :

```text
/jbl_proscan/jbl-proscan-card.js
```

L'intégration tente de l'enregistrer automatiquement. Si nécessaire, ajoutez-la dans **Paramètres → Tableaux de bord → Ressources** en tant que **Module JavaScript**.

Ajoutez ensuite une carte manuelle :

```yaml
type: custom:jbl-proscan-card
entity: sensor.bassin_historique
```

Remplacez `sensor.bassin_historique` par votre capteur d'historique JBL ProScan.

L'éditeur graphique, les graphiques historiques, les seuils de qualité de l'eau, les thèmes clair/sombre et les options de personnalisation sont conservés.

## Migration depuis l'installation séparée

1. Mettez à jour l'intégration JBL ProScan vers une **version publiée incluant la carte**.
2. Vérifiez que la ressource `/jbl_proscan/jbl-proscan-card.js` est accessible et enregistrée dans Lovelace.
3. Désinstallez l'ancienne carte `JBL-ProScan_card` installée séparément via HACS, si elle existe.
4. Supprimez uniquement son ancienne ressource JavaScript (par exemple `/hacsfiles/JBL-ProScan_card/jbl-proscan-card.js` ou `/local/jbl-proscan-card.js`), **pas** `/jbl_proscan/jbl-proscan-card.js`.
5. Actualisez le navigateur. Vos configurations `type: custom:jbl-proscan-card` restent valides.

Ne chargez pas simultanément les anciennes et nouvelles ressources : elles déclarent le même type de carte.

## Documentation et support

- [README complet, configuration et dépannage](https://github.com/AuroreVgn/JBL-ProScan#readme)
- [Instructions de migration](https://github.com/AuroreVgn/JBL-ProScan#toc-section-8)
- [Signaler un problème](https://github.com/AuroreVgn/JBL-ProScan/issues)
- [Captures d'écran historiques](assets/)

Merci aux utilisateurs et contributeurs de JBL ProScan Card !
