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
learning_status: Completed
last_reviewed: 2026-07-18
---

# Kontrollstrukturen

## Was sind Kontrollstrukturen?

Kontrollstrukturen bestimmen den Ablauf eines Programms. Sie entscheiden, welcher Code ausgeführt wird und welcher nicht.

Mit Kontrollstrukturen können Programme auf unterschiedliche Situationen reagieren und Anweisungen abhängig von Bedingungen ausführen.

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

Da `8 > 5` wahr ist, wird der Code innerhalb des `if`-Blocks ausgeführt.

---

# if / else

Mit `else` wird festgelegt, was passieren soll, wenn die Bedingung **falsch (`False`)** ist.

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

Die Bedingungen werden **von oben nach unten** ausgewertet.

Sobald eine Bedingung wahr ist, wird der entsprechende Block ausgeführt und alle weiteren Bedingungen werden übersprungen.

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

Obwohl `7 > 0` ebenfalls wahr ist, wird `C` **nicht** ausgegeben, da bereits die vorherige Bedingung erfüllt wurde.

---

# Mehrere unabhängige if-Anweisungen

Mehrere `if`-Anweisungen werden unabhängig voneinander geprüft.

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

Beide Bedingungen sind wahr und werden deshalb beide ausgeführt.

---

# Unterschied zwischen if/elif/else und mehreren if

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

➡️ Es wird **maximal ein Block** ausgeführt.

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

➡️ Jede Bedingung wird unabhängig geprüft. Es können mehrere Blöcke ausgeführt werden.

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

1. Eine Variable besitzt einen Wert.
2. Die Bedingung wird ausgewertet.
3. Ergibt die Bedingung `True`, wird der eingerückte Code ausgeführt.
4. Ergibt die Bedingung `False`, wird der nächste `elif` oder der `else`-Block geprüft.

---

# Merksätze

- `if` prüft eine Bedingung.
- `else` wird ausgeführt, wenn keine vorherige Bedingung wahr ist.
- `elif` bedeutet „ansonsten, falls“.
- Ein `if`/`elif`/`else`-Block führt **maximal einen** Zweig aus.
- Mehrere `if`-Anweisungen werden unabhängig voneinander geprüft.
- Python erkennt Codeblöcke ausschließlich anhand der Einrückung.

---

# Typische IHK-Fallen

- `=` und `==` verwechseln.
- `>` und `>=` verwechseln.
- `elif` mit mehreren `if` verwechseln.
- Falsche Einrückung verwenden.
- Vergessen, dass nach einem erfolgreichen `elif` keine weiteren Bedingungen geprüft werden.

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

Ausgabe:

```
A
C
```

---

# Prüfungsrelevanz

Kontrollstrukturen gehören zu den wichtigsten Grundlagen der Programmierung und sind regelmäßig Bestandteil der IHK-Abschlussprüfung.

Sie werden unter anderem benötigt für:

- Algorithmen
- Schleifen
- Funktionen
- Pseudocode
- Struktogramme
- Codeanalyse
- Fehleranalyse

---

# Wiederholungsfragen

1. Was macht ein `if`?
2. Wann wird ein `else` ausgeführt?
3. Was ist der Unterschied zwischen `if`/`elif`/`else` und mehreren `if`?
4. Welche Vergleichsoperatoren gibt es?
5. Warum ist die Einrückung in Python wichtig?

---

# Lernstatus

**Status:** ✅ Abgeschlossen

## Behandelte Inhalte

- [x] if
- [x] else
- [x] elif
- [x] mehrere unabhängige if-Anweisungen
- [x] Vergleichsoperatoren
- [x] typische IHK-Fallen
- [x] eigene Beispiele

## Nächstes Thema

- [ ] Boolesche Operatoren (`and`, `or`, `not`)

---

# Zusammenfassung

Kontrollstrukturen steuern den Ablauf eines Programms.

Mit `if`, `elif` und `else` können Entscheidungen getroffen werden. Mehrere `if`-Anweisungen werden unabhängig voneinander ausgeführt, während bei `if`/`elif`/`else` höchstens ein Zweig ausgeführt wird.

Dieses Thema bildet die Grundlage für Schleifen, Funktionen und komplexe Algorithmen und gehört zu den wichtigsten Grundlagen der IHK-Abschlussprüfung.