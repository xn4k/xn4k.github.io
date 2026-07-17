---
title: "Kontrollstrukturen"
layout: knowledge-article
categories: [ihk]
tags:
  - python
  - algorithmen
  - kontrollstrukturen
knowledge: true
knowledge_category: IHK
difficulty: Beginner
learning_status: Learning
last_reviewed: 2026-07-17
---

# Kontrollstrukturen

## Was sind Kontrollstrukturen?

Kontrollstrukturen bestimmen den Ablauf eines Programms. Sie entscheiden, welcher Code ausgeführt wird und welcher nicht.

Mit Kontrollstrukturen können Programme auf unterschiedliche Situationen reagieren und Anweisungen wiederholen.

---

# if

Mit `if` wird eine Bedingung geprüft.

Ist die Bedingung **wahr (`True`)**, wird der eingerückte Code ausgeführt.

```python
x = 8

if x > 5:
    print("Hallo")
```

Ausgabe:

```
Hallo
```

Da `8 > 5` wahr ist, wird der Code innerhalb des `if` ausgeführt.

---

# if / else

Mit `else` kann festgelegt werden, was passieren soll, wenn die Bedingung **falsch (`False`)** ist.

```python
x = 3

if x > 5:
    print("A")
else:
    print("B")
```

Ausgabe:

```
B
```

Da `3 > 5` falsch ist, wird der `else`-Block ausgeführt.

---

# if / elif / else

Mit `elif` können weitere Bedingungen geprüft werden.

Das Programm arbeitet die Bedingungen **von oben nach unten** ab.

Sobald eine Bedingung wahr ist, werden alle weiteren Bedingungen übersprungen.

```python
x = 7

if x > 10:
    print("A")
elif x > 5:
    print("B")
elif x > 0:
    print("C")
else:
    print("D")
```

Ausgabe:

```
B
```

Obwohl `7 > 0` ebenfalls wahr ist, wird `C` **nicht** ausgegeben, da bereits die zweite Bedingung erfüllt wurde.

---

# Mehrere unabhängige if-Anweisungen

Mehrere `if`-Anweisungen sind unabhängig voneinander.

Jede Bedingung wird einzeln geprüft.

```python
x = 12

if x > 10:
    print("A")

if x > 5:
    print("B")
```

Ausgabe:

```
A
B
```

Beide Bedingungen sind wahr, daher werden beide Blöcke ausgeführt.

---

# Vergleich

## if / elif / else

```python
x = 12

if x > 20:
    print("A")
elif x > 10:
    print("B")
else:
    print("C")
```

Ausgabe:

```
B
```

Es wird **maximal ein Block** ausgeführt.

---

## Mehrere if

```python
x = 12

if x > 10:
    print("A")

if x > 5:
    print("B")
```

Ausgabe:

```
A
B
```

Es können **mehrere Blöcke** ausgeführt werden.

---

# Vergleichsoperatoren

| Operator | Bedeutung |
|----------|-----------|
| `==` | gleich |
| `!=` | ungleich |
| `>` | größer als |
| `<` | kleiner als |
| `>=` | größer oder gleich |
| `<=` | kleiner oder gleich |

---

# Ablauf eines if-Statements

1. Variable besitzt einen Wert.
2. Die Bedingung wird geprüft.
3. Ergibt die Bedingung `True`, wird der zugehörige Block ausgeführt.
4. Ergibt sie `False`, wird der nächste `elif` oder `else` geprüft.

---

# Merksätze

- `if` prüft eine Bedingung.
- `else` wird ausgeführt, wenn keine vorherige Bedingung wahr ist.
- `elif` bedeutet "ansonsten, falls".
- Ein `if`/`elif`/`else`-Block führt **maximal einen** Zweig aus.
- Mehrere `if`-Anweisungen werden unabhängig voneinander geprüft.
- Python erkennt Codeblöcke an der Einrückung.

---

# Typische IHK-Fallen

- `elif` mit mehreren `if` verwechseln.
- `=` und `==` verwechseln.
- `>` und `>=` verwechseln.
- Falsche Einrückung verwenden.
- Vergessen, dass nach einem erfolgreichen `elif` keine weiteren Bedingungen mehr geprüft werden.

---

# Eigene Beispiele

## Beispiel 1

```python
x = 8

if x < 5:
    print("A")
else:
    print("B")
```

Ausgabe:

```
B
```

---

## Beispiel 2

```python
x = 15

if x > 10:
    print("A")

if x > 20:
    print("B")

if x > 5:
    print("C")
```



# Zusammenfassung

Kontrollstrukturen steuern den Ablauf eines Programms.

Mit `if`, `elif` und `else` können Entscheidungen getroffen werden.

Mehrere `if`-Anweisungen werden unabhängig voneinander ausgeführt, während bei `if`/`elif`/`else` höchstens ein Zweig ausgeführt wird.

Dieses Thema bildet die Grundlage für Schleifen, Funktionen und komplexe Algorithmen und gehört zu den wichtigsten Grundlagen für die IHK-Abschlussprüfung.
1. if prüft eine Bedingung. Ist sie wahr, läuft der if-Block. Ist sie falsch, kann der else-Block ausgeführt werden.
2. Ein if-else if-else-Block wird von oben nach unten geprüft. Sobald eine Bedingung wahr ist, werden alle weiteren 
Bedingungen übersprungen.
3. 
| Schreibweise       | Verhalten                                                                           |
| ------------------ | ----------------------------------------------------------------------------------- |
| `if / elif / else` | Es wird maximal **ein** Block ausgeführt.                                           |
| Mehrere `if`       | Jede Bedingung wird unabhängig geprüft. Es können mehrere Blöcke ausgeführt werden. |



## Eigene Beispiele

## Prüfungsrelevanz

Dieses Thema ist Grundlage für:

- Algorithmen
- Schleifen
- Funktionen
- Pseudocode
- Struktogramme
- Codeanalyse
- Fehleranalyse