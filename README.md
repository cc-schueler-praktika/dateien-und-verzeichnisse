# Dateien und Verzeichnisse

*Dateien* beinhalten Informationen verschiedenster Art (Text, Programmcode, Bildinformationen, …).
Ein *Verzeichnis* beinhaltet eine Menge von Dateien.

## Verzeichnisstruktur 🌳

Dateien und Verzeichnisse befinden sich unter Linux in einer *baumartigen Struktur*. Das Verzeichnis der höchsten Ebene wird *Rootverzeichnis* genannt. Dargestellt wird es meisten durch `/`. Alle anderen Verzeichnisse in Linux sind über das Rootverzeichnis zugreifbar und in einer hierarchischen Struktur angeordnet.

```
/bin						# wichtige Programme die immer verfügbar sein müssen
/etc						# Konfigurationsdateien
/home						# darunter liegen Benutzerverzeichnisse
/home/testuser 	# Benutzerverzeichnis für den Benutzer "testuser"
/media					# Verzeichnisse von Speichermedien (USB-Stick, Festplatten, ...)
...
```

*Hinweis:* Auf einem Mac Computer können die Verzeichnisnamen abweichen. So gibt es beispielsweise statt `/media` das Verzeichnis `/Volumes` und statt `/home` das Verzeichnis `/Users`.

Eine Beschreibung der Dateiverzeichnisstruktur kann mit dem Befehl `man hier` angezeigt werden. `hier` steht für "file system *hier*archy".



## Dateipfade 🔍

Um eine Dateien oder ein Verzeichnis anzusprechen wird der Pfad zu eben diesem benötigt. Der Pfad gibt an, wo die Datei oder das Verzeichnis innerhalb der Verzeichnisstruktur zu finden ist.

Man unterscheidet dabei zwei Arten von Pfaden: *relative* und *absolute*

**absoluter Pfad** - Der vollständige Pfad beginnend beim Rootverzeichnis (`/`)
**relativer Pfad** - Pfad der das aktuelle Verzeichnis als Ausgangspunkt nimmt

Ein Beispiel für einen *absoluten* Pfad wäre: `/home/testuser/beispiele/notizen.txt`

Wenn wir uns im Benutzerverzeichnis des Benutzers `testuser` befinden würde der *relative* Pfad zu dieser Datei wie folgt aussehen: `beispiele/notizen.txt`



## Dateien 📄

Dateien dürfen unter Linux Namen mit einer Länge von bis zu 255 Zeichen haben. Dabei wird zwischen Groß- und Kleinschreibung unterschieden. So sind `beispielDatei` und `beispieldatei` zwei verschiedene Dateien.

*Hinweis:* Für Mac Computer gilt das standardmäßig *nicht*!

Ein Punkt gilt als normales Zeichen für einen Dateinamen. Beginnt eine Datei jedoch mit einem Punkt, so handelt es sich um eine *versteckte* Datei die in der Regel nicht angezeigt wird. Zum Beispiel: `.versteckteEinstellungen`

Man unterscheidet verschiedene *Dateiarten*. Darunter fallen:

- **normale Dateien** - mit einem `-` gekenntzeichnet
- **Verzeichnisse** - mit einem `d` gekenntzeichnet

Dabei wird deutlich, das Verzeichnisse letztlich auch nur Dateien sind, die andere Dateien auflisten.

Mit dem Befehl `ls -l` kann man sich alle Dateien innerhalb eines Verzeichnisses und deren Eigenschaften ansehen.

```
07:44 $ ls -l
total 8
-rw-r--r--  1 beni  staff  15  6 Mai 07:46 beispieldatei
drwxr-xr-x  2 beni  staff  64  6 Mai 07:46 weitereBeispiele
```

Hier zeigt das aller erste Zeichen in jeder Zeile die **Dateiart** an. Dabei sieht man, dass es sich bei der Datei `weitereBeispiele` um ein Verzeichnis handelt (`d`).

Eine Datei gehört immer dem Benutzer, der sie erstellt hat. Dieser ist **Eigentümer** der Datei. Im Beispiel zu sehen an dem Wort `beni`.



## Dateimanager vs. Kommandozeile 🤷‍♂️

Das Verwalten von Dateien und Ordnern über die Kommandozeile ist meist schneller, erfordert aber gleichzeitig Kenntnis über weitere Befehle zum Anzeigen, Öffnen und Editieren.

Dagegen bietet ein Dateimanager eine grafische und damit optisch meist zugänglichere Alternative. Diese Variante wird deshalb gerade für Einsteiger als intuitiver betrachtet.



## Thanks! 👏

[1] https://www.selflinux.org/selflinux/html/verzeichnisse_unter_linux01.html

[2] https://wiki.ubuntuusers.de/Verzeichnisstruktur/

[3] https://www.pks.mpg.de/~mueller/docs/suse10.3/opensuse-manual_de/manual/sec.new.fs.html

[4] https://www.pks.mpg.de/~mueller/docs/suse10.3/opensuse-manual_de/manual/sec.new.bash.fildir.html

[5] https://www.ernstlx.com/linux90linux.html
