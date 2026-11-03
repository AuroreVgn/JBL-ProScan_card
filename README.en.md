# 🐠 JBL ProScan Card — historical repository

> [!IMPORTANT]
> **JBL ProScan Card is now bundled in the source code of the [JBL ProScan integration](https://github.com/AuroreVgn/JBL-ProScan).**
> Once the integrated version is released and tested, this separate repository will no longer receive card updates. It remains available for project history, older releases, and screenshots.
>
> **The integration version containing the bundled card has not been released yet.** Until then, keep your existing standalone card installation.

## 🌍 Other languages

[Français](README.md)

## Install the card

Once an integration release includes the card, install or update **[AuroreVgn/JBL-ProScan](https://github.com/AuroreVgn/JBL-ProScan)** through HACS / Marketplace or manually, then restart Home Assistant.

The integration serves the JavaScript resource at:

```text
/jbl_proscan/jbl-proscan-card.js
```

The integration attempts to register the resource automatically. If needed, add it under **Settings → Dashboards → Resources** as a **JavaScript module**.

Add a manual card:

```yaml
type: custom:jbl-proscan-card
entity: sensor.bassin_historique
```

Replace `sensor.bassin_historique` with your JBL ProScan history sensor.

The visual editor, historical charts, water quality thresholds, light/dark themes, and customization options are preserved.

## Migrating from the standalone installation

1. Update the JBL ProScan integration to a **published version that includes the card**.
2. Check that `/jbl_proscan/jbl-proscan-card.js` is accessible and registered as a Lovelace resource.
3. Uninstall the former standalone `JBL-ProScan_card` HACS plugin, if installed.
4. Remove **only its old JavaScript resource** (for example `/hacsfiles/JBL-ProScan_card/jbl-proscan-card.js` or `/local/jbl-proscan-card.js`), **not** `/jbl_proscan/jbl-proscan-card.js`.
5. Refresh your browser. Existing `type: custom:jbl-proscan-card` configurations remain valid.

Do not load both old and new JavaScript resources simultaneously: they register the same custom card type.

## Documentation and support

- [Full README, configuration and troubleshooting](https://github.com/AuroreVgn/JBL-ProScan/blob/main/README.en.md)
- [Migration instructions](https://github.com/AuroreVgn/JBL-ProScan#toc-section-8)
- [Report an issue](https://github.com/AuroreVgn/JBL-ProScan/issues)
- [Historical screenshots](assets/)
- [Version française](README.md)

Thank you to all JBL ProScan Card users and contributors!
