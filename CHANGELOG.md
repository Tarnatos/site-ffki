Änderungen mit Firmwareversion 2016.2.7 basierend auf Gluon 2016.2.7
====================================================================

Freifunk Kiel spezifische Änderungen:
-------------------------------------

 * quickfix [1] verbesserung: der Grund für die ersten 5 Reboots wird jetzt reboot-sicher geloggt
 * Neu: Bei WR1043ND und WR740/841/2N/ND kann ist der WiFi Button deaktiviert und man kann diverse Funktionen im Config mode aktivieren [2]
 * Neu: gluon-ssid-changer 3] schaltet die SSID eines Routers auf "FF_Offline_Knotenname" wenn dieser 24h offline ist

 - [1] - https://github.com/Freifunk-Nord/eulenfunk-packages/tree/v2016.2.x/gluon-quickfix
 - [2] - https://github.com/rubo77/ffm-packages/tree/master/ffffm-button-bind
 - [3] - https://github.com/Freifunk-Nord/gluon-ssid-changer/

Release Note: https://github.com/freifunk-kiel/site-ffki/releases/tag/v2016.2.7

Offizielle Changelogs zum nachlesen:
------------------------------------

* https://gluon.readthedocs.io/en/v2017.1.x/releases/v2016.2.7.html

<br>

Änderungen mit Firmwareversion 2016.2.6.2 basierend auf Gluon 2016.2.6
======================================================================

Freifunk Kiel spezifische Änderungen:
-------------------------------------
 * ibss (AdHoc) wird deaktiviert. Der Übergang zu 802.11s-only ist vollbracht.

Release Note: https://github.com/freifunk-kiel/site-ffki/releases/tag/v2016.2.6.2

<br>

Änderungen mit Firmwareversion 2016.2.6.1 basierend auf Gluon 2016.2.6
======================================================================

Freifunk Kiel spezifische Änderungen:
-------------------------------------
 * roamguide löscht jetzt seine log-Dateien im /tmp Ordner
 * quickfix scannt mit niedrigerer Priorität
 * mesh (802.11s) und ibss (AdHoc) sind aktiviert, um den Übergang zu 802.11s-only vorzubereiten.
 
Generelle Änderungen an Gluon 2016.2.6
----------------------------
 * Der TP-Link TL-WR841N/ND v12 wird unterstützt
 * Fix: Wenn zwischen Clients, die am LAN Port angeschlossen sind und Clients im WLAN am selben Knoten Verbindungen aufrecht gehalten werden und dabei der Client im WLAN zu einem anderen Knoten "roamt", dann bleiben diese Verbindungen jetzt aufrecht erhalten (#1121).
 * **Offloader und andere Knoten mit einer x86er-Firmware benötigen mindestens diese Version, bevor sie auf einen späteren 2017.x release mit lede updaten**

Offizielle Changelogs zum nachlesen:
------------------------------------

* https://gluon.readthedocs.io/en/latest/releases/v2016.2.6.html

<br>

Änderungen mit Firmwareversion 2016.2.5.1 basierend auf Gluon 2016.2.5
================================================================

Freifunk Kiel spezifische Änderungen:
-------------------------------------
 * Der Eulenfunk-Patch startet frühesten nach einer Stunde den Router neu, wenn kein Gateway erreichbar ist.

<br>

Änderungen mit Firmwareversion 2016.2.5 basierend auf Gluon 2016.2.5
====================================================================

Freifunk Kiel spezifische Änderungen:
-------------------------------------
 * Texte im Config Mode überarbeitet
 * Der Knotenalarm auf unserer Webseite wird besser beworben
 * In der Anmelde-Email kann man sich gleich für den Knotenalarm anmelden
 
Generelle Änderungen an Gluon 2016.2.5
----------------------------
 * Ein Fehler wurde behoben, der nur batman-adv 15 betrifft, welches wir in Kiel nicht nutzen

Offizielle Changelogs zum nachlesen:
------------------------------------

* https://gluon.readthedocs.io/en/latest/releases/v2016.2.5.html

<br>

Änderungen mit Firmwareversion 2016.2.4 basierend auf Gluon 2016.2.4
===================================================================

Freifunk Kiel spezifische Änderungen:
-------------------------------------
 * Im Config Mode kann man jetzt das Pico Peering Agreement akzeptieren

Generelle Änderungen an Gluon 2016.2.4
----------------------------
 * Ein Problem mit batman-adv (compat 15) wurde behoben. Dieses führte dazu, dass Pakete einer bestimmten Größe nicht übertragen werden konnen (b7eeef9).
 Die Gluon Entwickler gehen davon aus, dass dies der Grund für hängende Autoupdateprozesse war.
 * Ein Problem beim kompilieren der Gluon Firmware wurde behoben (#1059).
 * Es wurde ein Fehler im Ladescript von respondd behoben, der zum einem Speicherüberlauf führte (9a0aeb9).
 * Die sysupgrade Files für x86 Systeme wurden repariert (41fd50d, ad37e2b).
 * Der Manifestgenerator erstellt nun Hashwerte mit dem SHA256 Algorithmus.

Probleme mit Gluon 2016.2.4
--------------------------------------
 * Beim Update von x86 Systemen kann es zum Verlust der Konfiguration kommen, wenn die Kernel Partition anwächst.
 * Wenn Mesh on WAN aktiviert ist, wird bei bestimmten Modellen die MAC Adresse des WAN Ports verändert. Dies kann in Umgebungen mit vorgeschalteten MAC Filterregeln zu Problemen führen.
 * Die TX Leistung der meisten Ubiquiti Geräte ist zu hoch eingestellt. Genaue Werte sind unbekannt. Es wird empfolen die Sendeleistung per Hand zu reduzieren.
 
Offizielle Changelogs zum nachlesen:
------------------------------------

* https://gluon.readthedocs.io/en/latest/releases/v2016.2.4.html

<br>

Änderungen mit Firmwareversion 2016.2.3 basierend auf Gluon 2016.2.3
====================================================================

Änderungen an Gluon 2016.2.3
----------------------------
 * respondd wird nun bei einem Fehler automatisch neu gestartet (#863)
 * autoupdater timeouts verändert, dies verhindert ein "hängen" des Autoupdaters beim Manifest-Download. Er wurde nun so verbessert, dass der wget Prozess jederzeit sicher beendet werden kann. (#987)
 * Änderung der WLAN-Länderkodierung wurde verbessert (#1001)
 
Mehr Routermodelle werden unterstützt
-------------------------------------

    ar71xx-generic
        TP-Link:    TL-WR940N v4, TL-WR1043ND v4
    ramips-rt305x
        Fonera:     20N

Offizielle Changelogs zum nachlesen:
------------------------------------

* https://gluon.readthedocs.io/en/latest/releases/v2016.2.3.html

<br>

Änderungen mit Firmwareversion 2016.2.2 basierend auf Gluon 2016.2.2
====================================================================

Änderungen an Gluon 2016.2.2
----------------------------
 * Bootprobleme auf mehreren QCA955x-basierenden Geräten behoben (z.B. OpenMesh OM5P AC v2) (#965)
 * Build-Prozess: Git Downloadprobleme von git.kernel.org auf Debian Wheezy behoben(#919)
 * Fix: RX Filter von Ubiquiti UAP Outdoor+ Geräten (d43147a8e03d)
 * Fix: vertauschtes WAN/LAN interface bei der CPE210 (59deb2064d54)
 * Deutliche Vverringerung der CPU Last durch die Steuerung der Signal LEDs (#897)
 * Fix: Netzwerk-Port des Ubiquiti UAP AC Lite (#911)
 * Build: /tmp Verzeichnis des Hosts wird nicht länger genutzt (f9072a36411b)
 * Fix: mesh interface type respondd/alfred announcements wenn VLANs über IBSS genutzt werden (#941)
 * Fix: next-node ebtables Regeln ohne next_node.ip4 (9dbe9f785d2b) 
 * x86-generic und x86-64 images haben nun PATA und MMC support.
 * Clean up opkg postinst scripts während der Imageerstellung.

Mehr Routermodelle werden unterstützt
-------------------------------------

    ar71xx-generic
        TP-Link:    CPE210/510 EU/US versions, TL-WA801N/ND v3, TL-WR841ND v11 EU/US versions 

Offizielle Changelogs zum nachlesen:
------------------------------------

* http://gluon.readthedocs.io/en/v2016.2.2/releases/v2016.2.2.html
