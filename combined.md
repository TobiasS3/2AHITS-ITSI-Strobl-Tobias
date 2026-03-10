# 2AHITS ITSI Übungen

[Fach-Homepage🌐](https://www.franzmatejka.at/htl/doc/_SJ_2025/2AHITS_ITSI.html)
# Arbeitsbericht vom 17.09.2025

- Name: Tobias Strobl
- Klasse: 2AHITS
- Gruppe: 2
- Fach: ITSI Übungen
- Thema: Umgang mit Replit und Einführungen in Markdown

# Überschrift 1
## Überschirft 2
### Überschrift 3
#### Überschrift 4

**Fett**
*Kursiv*
`Code`
z.b. für Dateinamen `250917.md`

Bei Übungen immer den Text der Übung ins Dokument mit aufnehmen

---

**Übung:** mit welchem Befehl kann der Inhalt eines Verzeichnisses angezeigt werden?

**Recherche:**

Information über ls in folgenden Web-Seiten:

-[Link auf HTL](https://htl-braunau.at/)

**Lösung:**

```sh
$ ls
```

**Ausgabe**:

```
250917.md
```
>Erkläre den Linux Befehl `ls`(ChatGPT)
![Bild Capybara](image.png)# Arbeitsbericht vom 01.10.25

- Name: Tobias Strobl
- Klasse: 2AHITS
- Gruppe 2
- ITSI Übungen
- Thema: File Befehle  in Linux

# Grundlagen

Shell: ist ein Programm das ein textorienterite Schnittstelle zum Betriebssystem zur Verfügung stellt.

Prompt:
```sh
~/workspace$
```

Einfacher Befehl:
```sh
$ date
```

Jeder Befehl hat Optionen über die das Verhalten gesteuert werden kan.
```sh
$ date -I
```

## Optionen:
- short-hand = 1 Buchstabe
- long-hand = Wort
```sh
&date --iso-8601
```

Quelle zu Informationen über einen Befehl:

- häufig: Option `--help`
- man pages (Manuel = Handbuch) `$ man date`, nicht in Replit aber in gänigen Linux Distributionen
- Internetsuche mit "man date"
- KI

## Argumente

Daten mit denen ein Befehl arbeitet:

```sh
$ echo Hallo Welt
```
`Hallo` ist hier das Argument.

mit Optionen

```sh
$ echo -n Hallo Welt
```
## Tastenkürel

- Pfeil nach oben/unten: Historie
- Tabulator: automatische File Vervollständigung.
- Strg-A: Anfang der Zeile
- Strg.C: Abbruch des aktullen Kommands

## File Befehle

cd,mkdir,ls,touch,pwd,rm
working directory(Arbeitsverzeichnis)

Unterschied aboluter und relativer Pfad 

Bedeutung von cd(ohne argument) und von ~

```sh 
$ clear
```
👉 Löscht den Terminalbildschirm, um eine leere Ansicht zu schaffen.
```sh 
$ ls 
```
👉 Listet die Dateien und Ordner im aktuellen Verzeichnis auf.
```sh 
$ pwd
```
👉 Zeigt den vollständigen Pfad (Arbeitsverzeichnis) an, in dem du dich gerade befindest.
```sh 
$ cd berichte
```
👉 Wechselt in das Unterverzeichnis "berichte".
```sh 
$ cd ..
```
👉 Geht eine Verzeichnisebene zurück, also ins übergeordnete Verzeichnis.
```sh 
$ ls -l
```
👉 Zeigt die Dateien und Ordner in Listenform mit Details (Größe, Datum, Berechtigungen).
```sh 
$ ls -a
```
👉 Listet alle Dateien und Ordner auf, auch versteckte (die mit . beginnen).
```sh 
$ mkdir xyz
```
👉 Erstellt ein neues Verzeichnis namens "xyz".
```sh 
& cd xyz
```
👉 Wechselt in das neu erstellte Verzeichnis "xyz".
```sh 
$ touch test.md
```
👉 Erstellt eine neue leere Datei namens "test.md" (oder aktualisiert das Änderungsdatum, falls sie schon existiert).
```sh 
$ rm test.md
```
👉 Löscht die Datei "test.md".
```sh 
$ rmdir abc/
```
👉 Löscht das leere Verzeichnis "abc". Funktioniert nicht, wenn es Dateien enthält.
```sh 
$ touch abc/test.md
```
👉 Erstellt im Verzeichnis "abc" die Datei "test.md".
⚠️ Voraussetzung: Das Verzeichnis abc muss bereits existieren.
```sh 
$ rm -r abc
```
👉 Löscht das Verzeichnis "abc" inklusive aller Inhalte (rekursiv).



### Absoluter Pfad
Beschreibt den vollständigen Weg vom Wurzelverzeichnis (/) bis zur Datei oder zum Ordner.
Beispiel:
```sh
/home/user/dokumente/bericht.txt
```
Immer eindeutig, egal wo du dich gerade im Dateisystem befindest.

### Relativer Pfad
Beschreibt den Weg ausgehend vom aktuellen Verzeichnis (Arbeitsverzeichnis).
Beispiel:
```sh
dokumente/bericht.txt
```

Hängt davon ab, wo du gerade bist (z. B. im Ordner `/home/user`).

### Bedeutung von cd ohne Argument

Wenn du nur cd eingibst, wechselst du in dein Home-Verzeichnis.

Das ist derselbe Effekt wie `cd ~`.

### Bedeutung von ~

Das Tilde-Zeichen ~ ist eine Abkürzung für dein Home-Verzeichnis.

Beispiel:
```sh
cd ~/Dokumente
```
wechselt in den Ordner Dokumente in deinem Home-Verzeichnis, z. B. 
home/user/Dokumente.`
# **Arbeitsbericht vom 15.10.25**

- **Name:** Tobias Strobl
- **Klasse:** 2AHITS
- **Gruppe:** 2
- **Fach:** ITSI Übungen
- **Thema:** Übungen Basics

---

## **Übung: date**

Recherchiere in der Manpage von `date`, wie folgende ISO-8601-Datumsausgabe erzeugt werden kann:

2023-11-07T08:43:53+00:00

yaml
Code kopieren

**Hinweis:**  
Die Option `-I` zeigt standardmäßig nur das Datum an.

### **Lösung**
$ date --iso-8601=seconds

---

## **Übung: Directories und Files**

Lege mit `mkdir` und `touch` folgende Verzeichnisstruktur an:

./
└── abcd/
├── first_dir/
│ ├── abcd.01.1.txt
│ ├── abcd.01.2.txt
│ └── abcd.01.3.txt
└── second_dir/
├── xyz.02.1.txt
├── xyz.02.2.txt
└── xyz.02.3.txt

shell
Code kopieren

### **Lösung**
$ mkdir abcd  
$ cd abcd  
$ mkdir first_dir  
$ cd first_dir  
$ touch abcd.01.1.txt abcd.01.2.txt abcd.01.3.txt  
$ cd ..  
$ mkdir second_dir  
$ cd second_dir  
$ touch xyz.02.1.txt xyz.02.2.txt xyz.02.3.txt  

---

### **Zusatzaufgabe**

Stelle das Arbeitsverzeichnis auf `abcd/second_dir` und erstelle ohne weiteres `cd` ein Unterverzeichnis `in_first_dir` in `first_dir` und darin die Datei `neu.txt`.

Endgültige Struktur:

./
└── abcd/
├── first_dir/
│ ├── in_first_dir/
│ │ └── neu.txt
│ ├── abcd.01.1.txt
│ ├── abcd.01.2.txt
│ └── abcd.01.3.txt
└── second_dir/
├── xyz.02.1.txt
├── xyz.02.2.txt
└── xyz.02.3.txt

yaml
Code kopieren

### **Lösung**
$ mkdir -p ../first_dir/in_first_dir  
$ touch ../first_dir/in_first_dir/neu.txt  

---

## **Übung: Befehle – Bewegen und Kopieren**

Informiere dich über die Befehle `rm`, `rmdir`, `cp` und `mv`. Probiere die Befehle aus und dokumentiere deine Erkenntnisse.

### **Lösung**

**rm**  
Mit `rm` werden Dateien gelöscht. Die Dateien werden ohne Rückfrage entfernt, daher ist Vorsicht notwendig.

**rmdir**  
`rmdir` löscht ausschließlich leere Verzeichnisse. Enthält ein Ordner Dateien, kann er damit nicht gelöscht werden.

**cp**  
`cp` wird zum Kopieren von Dateien und Verzeichnissen verwendet. Für das Kopieren ganzer Ordner ist die Option `-r` erforderlich.

**mv**  
Mit `mv` können Dateien oder Verzeichnisse verschoben oder umbenannt werden. Der Vorgang erfolgt ohne Bestätigung.

---

**Dies sind alle bearbeiteten Aufgaben, die ich im Unterricht erledigt habe.**# Arbeitsbericht vom 01.10.25

- Name: Tobias Strobl
- Klasse: 2AHITS
- Gruppe 2
- ITSI Übungen
- Thema: GIT-HUB


## GitHub Anmeldung & Verknüpfung

1. Einen Account bei GitHub erstellen.  
2. Zurück zu Replit wechseln.  
3. Einen neuen Tab öffnen und **Git** auswählen.  
4. Oben rechts auf das **Zahnrad** klicken und die **Einstellungen** öffnen.  
5. Mit dem erstellten GitHub-Account anmelden.  
6. Den Repository-Link bei **Remote** einfügen (Verbindung über **HTTPS**).  
7. Eine **Commit-Message** als Summary eingeben und auf **Commit** klicken.  
8. Anschließend **Sync Changes** auswählen.
 ![image](image_3.png)
9. Auf GitHub unter **Actions** überprüfen, ob die Änderungen übernommen wurden.  
10. Den fertigen Bericht als Link über Teams abgeben.
# Arbeitsbericht von 05.11.25

- Name: Tobias Strobl
- Klasse: 2AHITS
- Gruppe: 2
- Fach: ITSI Übungen
- Thema: stdin/stdout
---



## Arbeiten mit cat, echo, stdin und stdout

In Linux kann man mit ein paar einfachen Befehlen Texte ausgeben, Dateien anzeigen oder neue Dateien erstellen.  
Dabei gibt es zwei wichtige Begriffe:

- **stdin** = Standardeingabe (normal die Tastatur)  
- **stdout** = Standardausgabe (normal der Bildschirm)

---

## cat

Mit `cat` kann man sich Dateien anzeigen lassen oder neue Dateien erstellen.

**Beispiel:**
```sh
cat datei.txt
````

Zeigt den Inhalt von *datei.txt* auf dem Bildschirm an (stdout).

Wenn man eine neue Datei erstellen will:

```sh
cat > text.txt
```

Jetzt kann man Text eingeben.
Zum Speichern **Strg + D** drücken.

---

## echo

Mit `echo` kann man Text ausgeben.

**Beispiel:**

```sh
echo Hallo Welt
```

Zeigt „Hallo Welt“ auf dem Bildschirm an (stdout).

---

## Umleitungen

Mit `>` kann man die Ausgabe in eine Datei schreiben, statt sie auf dem Bildschirm zu sehen.

**Beispiel:**

```sh
echo Hallo Welt > hallo.txt
```

Schreibt „Hallo Welt“ in die Datei *hallo.txt*.
Wenn die Datei schon da ist, wird sie überschrieben.

Wenn man etwas **anhängen** will, nimmt man `>>`:

```sh
echo Noch was >> hallo.txt
```

Der Text wird hinten an die Datei angefügt.

---

## Kurz erklärt

| Zeichen / Begriff | Bedeutung                       |
| ----------------- | ------------------------------- |
| stdin             | Eingabe (meist Tastatur)        |
| stdout            | Ausgabe (meist Bildschirm)      |
| `>`               | Ausgabe in Datei (überschreibt) |
| `>>`              | Ausgabe an Datei anhängen       |

---

### Übung: Kopie mit cat

**Aufgabe:**  
Erstelle mit `cat` eine Kopie von `test.txt` in `test2.txt`.

**Lösung:**  
```sh
$ cat test.txt > test2.txt
$ cat test2.txt
```
---
### Übung: dirlist in File

**Aufgabe:**  
Schreibe den mit `ls` ermittelten Inhalt des Verzeichnisses `/etc`  
in die Datei `etcdir.txt`.

**Lösung:**  
```sh
$ ls /etc > etcdir.txt
$ cat etcdir.txt
```
---
### Übung: /etc/os-release

**Aufgabe:**  
Sieh dir die Datei `/etc/os-release` an.

**Lösung:**  
```sh
$ cat /etc/os-release
$ ls -l /etc/os-release
```
#### Infos:

Zeigt Name, Version und ID des Betriebssystems

Könnte einem Hacker helfen, weil er damit weiß, welche Schwachstellen er gezielt suchen kann

ls -l zeigt Rechte, Besitzer, Größe und Änderungsdatum der Datei

---
### Übung: Textdatei mit echo erstellen

**Aufgabe:**  
Erstelle die Datei `made_by_echoing.txt` nur mit `echo`-Befehlen.

**Lösung:**  
```sh
$ echo "=====================" > made_by_echoing.txt
$ echo "=    HTL BRAUNAU    =" >> made_by_echoing.txt
$ echo "=====================" >> made_by_echoing.txt
$ echo "= 2AHITS Gruppe 2   =" >> made_by_echoing.txt
$ echo "= 0 Schülerinnen   =" >> made_by_echoing.txt
$ echo "= 13 Schüler        =" >> made_by_echoing.txt
$ echo "=====================" >> made_by_echoing.txt
```
Kontrolle:
```sh
$ cat made_by_echoing.txt
```

---


## Übung: C-Programm "Hallo Welt" mit echo erstellen

**Aufgabe:**  
Erstelle nur mit `echo` die Datei `hello.cpp` mit folgendem Inhalt:

```cpp
#include <iostream>

int main() {
  printf("\n\t*** Hallo Welt ***\n");
  return 0;
}
````

**Lösung:**

```sh
echo '#include <iostream>' > hello.cpp
echo '' >> hello.cpp
echo 'int main() {' >> hello.cpp
echo '  printf("\n\t*** Hallo Welt ***\n");' >> hello.cpp
echo '  return 0;' >> hello.cpp
echo '}' >> hello.cpp
```

**Kompilieren:**

```sh
g++ -o hello hello.cpp
```

**Starten:**

```sh
./hello
```

**Tipp:**
Man kann auch **2 Befehle hintereinander** schreiben, getrennt mit `;`:

```sh
g++ -o hello hello.cpp; ./hello
```



                 # Arbeitsbericht von 19.11.25

- Name: Tobias Strobl
- Klasse: 2AHITS
- Gruppe: 2
- Fach: ITSI Übungen
- Thema: WGET
---


## Übungen – TOOLS

### Einleitung:

### Vorbereitung
- `wget` war im System zunächst nicht installiert
- Installation wurde über Nix angeboten und durchgeführt

### Überprüfung
- Installation mit `wget --version` erfolgreich geprüft
- `wget` zeigt bei fehlender URL eine korrekte Fehlermeldung

### Download
- Datei wurde über eine HTTPS-Adresse heruntergeladen
- `shopping.txt` erfolgreich gespeichert

### Ergebnis
- Datei befindet sich im Verzeichnis `~/workspace`
- `wget` ist nun einsatzbereit**

---

# Arbeitsbericht – Übung 3.1 (head)

## 1. Erste Zeilen von Systemdateien
Zeigt die ersten 5 Zeilen der Benutzerdatei `/etc/passwd` und die ersten 7 Zeilen der Gruppen-Datei `/etc/group` an.

```bash
$ head -n 5 /etc/passwd
$ head -n 7 /etc/group
````

```
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync

root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:
tty:x:5:
disk:x:6:
```

---

## 2. Negative Zahl bei head

Zeigt alle Zeilen von `/etc/passwd` **außer den letzten 5** an.

```bash
$ head -n -5 /etc/passwd
```

```
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
```

---

## 3. Datei zahlen.txt erstellen und anzeigen

Erstellt eine Datei `zahlen.txt` mit den Zahlen 1 bis 100, zeigt die ersten 10 Zeilen und dann alles außer den letzten 80 Zeilen.

```bash
$ seq 1 100 > zahlen.txt
```
```
$ head -n 10 zahlen.txt
```
```
1
2
3
4
5
6
7
8
9
10
```
```
$ head -n -80 zahlen.txt
```
```
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20

```

---

## 4. Erste 7 Zeilen in neue Datei schreiben

Speichert die ersten 7 Zeilen von `zahlen.txt` in `anfang.txt`.

```bash
$ head -n 7 zahlen.txt > anfang.txt
$ cat anfang.txt
```

```
1
2
3
4
5
6
7
```

---

## 5. Erste 8 Zeilen mehrerer Dateien gleichzeitig

Zeigt die ersten 8 Zeilen von `/etc/passwd` und `/etc/group` in einer Ausgabe an.

```bash
$ head -n 8 /etc/passwd /etc/group
```

```
==> /etc/passwd <==
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin

==> /etc/group <==
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:
tty:x:5:
disk:x:6:
lp:x:7:
```

---

## 6. Zeilen nummerieren und speichern

Nummeriert jede Zeile von `/etc/passwd` mit `nl` und speichert das Ergebnis in `passwd_numbered`; zeigt die ersten 12 Zeilen.

```bash
$ nl /etc/passwd > passwd_numbered
$ head -n 12 passwd_numbered
```

```
     1  root:x:0:0:root:/root:/bin/bash
     2  daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
     3  bin:x:2:2:bin:/bin:/usr/sbin/nologin
     4  sys:x:3:3:sys:/dev:/usr/sbin/nologin
     5  sync:x:4:65534:sync:/bin:/bin/sync
     6  games:x:5:60:games:/usr/games:/usr/sbin/nologin
     7  man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
     8  lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
     9  mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
    10  news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
    11  uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
    12  proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
```

---

## 7. Zahlen 1–30 mit _ getrennt

Erstellt eine Datei `zahlen2.txt` mit den Zahlen 1 bis 30, getrennt durch `_`, und zeigt die ersten 20 Zeichen, um die Zahlen 1–10 darzustellen.

```bash
$ seq -s "_" 1 30 > zahlen2.txt
$ head -c 20 zahlen2.txt
```

```
1_2_3_4_5_6_7_8_9_10
```
---

# Arbeitsbericht – Übung 3.2 (more / less)

## 1. Datei mit `more` anzeigen
Zeigt den Inhalt der Datei seitenweise an.

```bash
$ more /usr/share/common-licenses/LGPL-2.1
````

```
                  GNU LESSER GENERAL PUBLIC LICENSE
                       Version 2.1, February 1999

 Copyright (C) 1991, 1999 Free Software Foundation, Inc.
 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301  USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

[This is the first released version of the Lesser GPL.  It also count
s
 as the successor of the GNU Library Public License, version 2, hence
 the version number 2.1.]

                            Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
Licenses are intended to guarantee your freedom to share and change
free software--to make sure the software is free for all its users.

  This license, the Lesser General Public License, applies to some
specially designated software packages--typically libraries--of the
Free Software Foundation and other authors who decide to use it.  You
can use it too, but we suggest you first think carefully about whethe
r
this license or the ordinary General Public License is the better
strategy to use in any particular case, based on the explanations bel
ow.

  When we speak of free software, we are referring to freedom of use,
not price.  Our General Public Licenses are designed to make sure tha
t
you have the freedom to distribute copies of free software (and charg
e
for this service if you wish); that you receive source code or can ge
t
it if you want it; that you can change the software and use pieces of
it in new free programs; and that you are informed that you can do
these things.

  To protect your rights, we need to make restrictions that forbid
distributors to deny you these rights or to ask you to surrender thes
e
rights.  These restrictions translate to certain responsibilities for
you if you distribute copies of the library or if you modify it.

--More--(7%)
```

---

## 2. Datei mit `less` anzeigen

Zeigt den Inhalt der Datei seitenweise und interaktiv an.

```bash
$ less /usr/share/common-licenses/LGPL-2.1
```

```
Sehr langer Text
```


# Arbeitsbericht von 19.11.25

- Name: Tobias Strobl
- Klasse: 2AHITS
- Gruppe: 2
- Fach: ITSI Übungen
- Thema: 
---


## Übungen – C++ 

### Vorbereitung: Hello-World-Programm anlegen

Erstelle eine Datei **hello.cpp** mit folgendem Inhalt:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World!" << endl;
    return 0;
}
```
### 1. g++ Version anzeigen
```
g++ --version
````

### 2. C++-Datei kompilieren

```
g++ hello.cpp -o hello
```

### 3. Dateien im aktuellen Verzeichnis anzeigen

```
ls
```

### 4. Dateien mit Details anzeigen

```
ls -l
```

### 5. Programm ausführen

```
./hello
```

--- 



# Übung (C in/out)

## Aufgabe

Auch selbstgeschriebene C-Programme lesen von **stdin** und schreiben auf **stdout**.  
Dadurch kann die Dateiumleitung mit `<`, `>` oder `>>` verwendet werden.

1. Erstelle eine Datei **sum.cpp** und öffne sie im Replit-Editor.
2. Schreibe ein C-Programm, das:
   - zuerst eine ganze Zahl **n** einliest,
   - danach **n** weitere ganze Zahlen einliest,
   - die Summe dieser Zahlen berechnet,
   - am Ende **nur die Summe** ausgibt.
3. Beispielablauf:
```
3
5
4
2
11

````
4. Kompiliere das Programm mit:
```bash
g++ -o sum sum.cpp
````

5. Prüfe mit `ls`, ob die Datei **sum** erzeugt wurde, und führe sie danach aus:

   ```bash
   ./sum
   ```
6. Erstelle eine Textdatei mit Eingabedaten (z. B. *input.txt*) und leite diese in das Programm um:

   ```bash
   ./sum < input.txt > output.txt
   ```

---
# Challenge (C in/out)

## AufgabeE

Erweitere das Programm so, dass **die Anzahl der Zahlen nicht mehr eingegeben werden muss**.  
Das Programm soll so lange Zahlen einlesen, bis das **Ende der Eingabe (EOF)** erreicht ist.  

- EOF auf der Tastatur: **Ctrl+D** (Linux/macOS) oder **Ctrl+Z** (Windows)  
- Bei einer Eingabedatei wird das Ende automatisch erkannt.  

Das Programm soll danach die **Summe aller eingegebenen Zahlen** ausgeben.



Alles klar! Ich passe den Bericht so an, dass alle Shell-Befehle mit `$` beginnen, um das Prompt/Verzeichnis zu symbolisieren. Die Ausgabe (`find`-Ergebnisse usw.) bleibt normal. Hier ist die angepasste Version für **Übung 3.4 (find)**:

---

# Arbeitsbericht von 19.11.25

* Name: Tobias Strobl
* Klasse: 2AHITS
* Gruppe: 2
* Fach: ITSI Übungen
* Thema: Übung 3.4 (find)

---

## Übung – Linux `find` Befehl

### Vorbereitung: Arbeitsverzeichnis setzen

Setze das Arbeitsverzeichnis auf `~/workspace`:

```bash
$ cd ~/workspace
```

Führe einen einfachen Test aus:

```bash
$ find -name "*.md"
```

---

## Aufgabenstellungen & Lösungen

### 1. Suche nach dem Directory mit dem Namen `profiles` von `~` aus

```bash
$ find ~ -name "profiles"
```

**Lösung:**
*/home/runner/.local/state/nix/profiles*

---

### 2. Suche nach der Datei `.latest.json` von `~` aus

```bash
$ find ~ -type f -name ".latest.json"
```

**Lösung:**
*/home/runner/workspace/.cache/replit/env/latest.json*

---

### 3. Suche nach allen Dateien, die auf `.json` enden

```bash
$ find ~ -name "*.json"
```

**Lösung:**
*/home/runner/workspace/.cache/replit/env/latest.json
/home/runner/workspace/.cache/replit/nix/dotreplitenv.json
/home/runner/workspace/.cache/replit/toolchain.json
/home/runner/workspace/.local/state/replit/agent/.latest.json
/home/runner/workspace/.upm/store.json*

---

### 4. Suche nach allen Directories

```bash
$ find -type d
```

**Lösung:**
*.
./.cache
./.cache/replit
./.cache/replit/modules
./.cache/replit/env
./.cache/replit/nix
./.local
./.local/state
./.local/state/replit
./.local/state/replit/agent
./.git
./.git/info
./.git/hooks
./.git/refs
./.git/refs/heads
./.git/refs/tags
./.git/refs/replit
./.git/refs/remotes
./.git/refs/remotes/origin
./.git/objects
./.git/objects/pack
./.git/objects/info
./.git/objects/4b
./.git/objects/56
./.git/objects/b6
./.git/objects/ea
./.git/objects/bf
./.git/objects/c9
./.git/objects/fe
./.git/objects/61
./.git/objects/50
./.git/objects/25
./.git/objects/d3
./.git/objects/91
./.git/objects/0d
./.git/objects/e6
./.git/objects/06
./.git/objects/eb
./.git/objects/a3
./.git/objects/78
./.git/objects/2f
./.git/objects/82
./.git/objects/8b
./.git/objects/6f
./.git/objects/04
./.git/objects/19
./.git/objects/99
./.git/objects/21
./.git/objects/af
./.git/objects/51
./.git/objects/03
./.git/objects/63
./.git/objects/1e
./.git/objects/30
./.git/objects/29
./.git/objects/ca
./.git/objects/73
./.git/objects/70
./.git/objects/49
./.git/objects/8f
./.git/objects/93
./.git/objects/b1
./.git/objects/8c
./.git/objects/fd
./.git/objects/a9
./.git/objects/66
./.git/objects/34
./.git/objects/a0
./.git/objects/4e
./.git/objects/86
./.git/objects/5d
./.git/objects/ad
./.git/objects/5a
./.git/logs
./.git/logs/refs
./.git/logs/refs/heads
./.git/logs/refs/remotes
./.git/logs/refs/remotes/origin
./.upm
./berichte
./berichte/imagne
./xyz
./abcd
./abcd/first_dir
./abcd/first_dir/in_first_dir
./abcd/second_dir*

---

### 5. Suche nach allen Markdown-Files, die in den letzten 4 Wochen geändert wurden

```bash
$ find -type f -name "*.md" -mtime -28
```

**Lösung:**
*./berichte/251015.md
./berichte/260121.md
./berichte/051125.md
./berichte/251217.md
./berichte/251119.md
./berichte/260125.md*

---

### 6. Suche nach allen Directories, die in den letzten 4 Wochen geändert wurden

```bash
$ find -type d -mtime -28
```

**Lösung:**
*./.cache/replit
./.git
./.git/refs/heads
./.git/refs/remotes/origin
./.git/objects
./.git/objects/d3
./.git/objects/8b
./.git/objects/a9
./.git/objects/34
./.git/objects/a0
./.git/objects/4e
./.git/objects/86
./.git/objects/5d
./.git/objects/ad
./.git/objects/5a
./berichte
./berichte/imagne*

---

### 7. Suche nach allen Directories, die in den letzten 4 Wochen **nicht** geändert wurden

```bash
$ find -type d -mtime +28
```

**Lösung:**
*.
./.cache
./.cache/replit/modules
./.cache/replit/env
./.cache/replit/nix
./.local
./.local/state
./.local/state/replit
./.local/state/replit/agent
./.git/info
./.git/hooks
./.git/refs
./.git/refs/tags
./.git/refs/replit
./.git/refs/remotes
./.git/objects/pack
./.git/objects/info
./.git/objects/4b
./.git/objects/56
./.git/objects/b6
./.git/objects/ea
./.git/objects/bf
./.git/objects/c9
./.git/objects/fe
./.git/objects/61
./.git/objects/50
./.git/objects/25
./.git/objects/91
./.git/objects/0d
./.git/objects/e6
./.git/objects/06
./.git/objects/eb
./.git/objects/a3
./.git/objects/78
./.git/objects/2f
./.git/objects/82
./.git/objects/6f
./.git/objects/04
./.git/objects/19
./.git/objects/99
./.git/objects/21
./.git/objects/af
./.git/objects/51
./.git/objects/03
./.git/objects/63
./.git/objects/1e
./.git/objects/30
./.git/objects/29
./.git/objects/ca
./.git/objects/73
./.git/objects/70
./.git/objects/49
./.git/objects/8f
./.git/objects/93
./.git/objects/b1
./.git/objects/8c
./.git/objects/fd
./.git/objects/66
./.git/logs
./.git/logs/refs
./.git/logs/refs/heads
./.git/logs/refs/remotes
./.git/logs/refs/remotes/origin
./.upm
./xyz
./abcd
./abcd/first_dir
./abcd/first_dir/in_first_dir
./abcd/second_dir*

---

### 8. Suche nach allen Dateien mit der Berechtigung `644`

```bash
$ find -type f -perm 644
```

**Bedeutung der Berechtigung 644:**

* **Owner (Besitzer):** lesen + schreiben (`6 = 4+2`)
* **Group:** lesen (`4`)
* **Others:** lesen (`4`)

**Lösung:**
*./.cache/replit/modules/replit.res
./.cache/replit/modules/python-3.11.res
./.cache/replit/modules.stamp
./.cache/replit/env/latest
./.cache/replit/env/latest.json
./.cache/replit/toolchain.json
./.local/state/replit/agent/.agent_state_c9711c3025f8e0b09f4a7d9477c1469bde79db98.bin
./.local/state/replit/agent/.agent_state_25580d7e7559deadb90ab2ada285caeb6a8759e9.bin
./.local/state/replit/agent/repl_state.bin
./.local/state/replit/agent/.agent_state_main.bin
./.local/state/replit/agent/.latest.json
./.git/info/exclude
./.git/description
./.git/refs/heads/replit-agent
./.git/refs/heads/main
./.git/refs/replit/agent-ledger
./.git/refs/remotes/origin/HEAD
./.git/refs/remotes/origin/main
./.git/HEAD
./.git/logs/HEAD
./.git/logs/refs/heads/main
./.git/logs/refs/heads/replit-agent
./.git/logs/refs/remotes/origin/main
./.git/logs/refs/remotes/origin/HEAD
./.git/COMMIT_EDITMSG
./.git/FETCH_HEAD
./.git/config
./.git/index
./.replit
./README.md
./berichte/imagne/image_2.png
./berichte/250917.md
./berichte/251001.md
./berichte/hello.cpp
./berichte/251015.md
./berichte/260121.md
./berichte/051125.md
./berichte/251217.md
./berichte/251119.md
./berichte/260125.md
./abcd/first_dir/abcd.01.1.txt
./abcd/first_dir/abcd.01.2.txt
./abcd/first_dir/abcd.01.3.txt
./abcd/first_dir/in_first_dir/neu.txt
./abcd/second_dir/xyz.02.1.txt
./abcd/second_dir/xyz.02.2.txt
./abcd/second_dir/xyz.02.3.txt
./hallo.txt
./etcdir.txt
./made_by_echoing.txt
./hello.cpp
./input.txt
./output.txt
./sum.cpp
./shopping.txt
./anfang.txt
./zahlen.txt
./passwd_numbered
./zahlen2.txt*

---

### 9. Suche im `/usr` Verzeichnis nach allen Dateien größer als 2 MB

```bash
$ find /usr -type f -size +2M
```

**Lösung:**
*/usr/share/i18n/locales/iso14651_t1_common
/usr/share/i18n/locales/cns11643_stroke
/usr/lib/x86_64-linux-gnu/libcrypto.so.3
/usr/lib/x86_64-linux-gnu/libc.so.6
/usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.33
/usr/lib/x86_64-linux-gnu/libperl.so.5.38.2
/usr/lib/x86_64-linux-gnu/perl/5.38.2/auto/Encode/KR/KR.so
/usr/lib/x86_64-linux-gnu/perl/5.38.2/auto/Encode/CN/CN.so
/usr/lib/x86_64-linux-gnu/perl/5.38.2/auto/Encode/JP/JP.so
/usr/lib/x86_64-linux-gnu/perl/5.38.2/CORE/charclass_invlists.h
/usr/lib/locale/locale-archive
/usr/lib/git-core/git
/usr/bin/perl5.38.2
/usr/bin/perl
/usr/bin/git*

---

### 10. Unterverzeichnis erstellen, Dateien anlegen & kleine txt-Dateien löschen

```bash
$ mkdir -p ~/workspace/testdir
$ cd ~/workspace/testdir
$ echo "abc" > file1.txt
$ echo "12345678901" > file2.txt
$ echo "Hello World" > file3.md
$ echo "Test Markdown" > file4.md

# Lösche alle txt-Dateien kleiner als 10 Bytes
$ $ find . -type f -name "*.txt" -size -10c -exec rm {} \;
```

---

### 11. Inhalte aller `.md` Dateien zu einem neuen File zusammenfügen

```bash
$ find . -type f -name "*.md" -exec cat {} + > combined.md
```

**Lösung:**
*(Hier deine Lösung einfügen)*

---

### 12. Alle Dateien im `/var`, die `log` im Dateinamen haben, vollständig anzeigen

```bash
$ find /var -type f -name "*log*" -exec ls -l {} \;
```

**Beispielausgabe:**

```
-rw-r--r-- 1 root root 259 Apr 28  2024 /var/lib/dpkg/info/logsave.md5sums
-rw-r--r-- 1 root root 33 May 30  2024 /var/lib/dpkg/info/login.conffiles
-rwxr-xr-x 1 root root 174 May 30  2024 /var/lib/dpkg/info/login.postrm
```

**Lösung:**
*(Hier deine Lösung einfügen)*

---

Wenn du willst, kann ich jetzt schon die **fertige Vorlage für deine Lösungen** vorbereiten, so dass du nur noch die Ausgaben/Notizen einträgst.

Willst du, dass ich das mache?
Hello World
Test Markdown
