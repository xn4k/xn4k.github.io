---
title: "Boolesche Operatoren"
date: 2026-07-20
categories:
  - IHK
tags:
  - Python
  - Kontrollstrukturen
  - Boolesche Operatoren
  - if
  - Programmierung
learning_status: Completed
last_reviewed: 2026-07-20
---

# Boolesche Operatoren

## Was sind boolesche Operatoren?

Boolesche Operatoren verknüpfen Bedingungen miteinander oder kehren deren Ergebnis um.

Eine Bedingung liefert immer einen booleschen Wert:

- `True`
- `False`

Mit booleschen Operatoren können mehrere Bedingungen kombiniert oder negiert werden.

Die drei wichtigsten Operatoren sind:

- `and`
- `or`
- `not`

Diese werden häufig zusammen mit `if`-Anweisungen verwendet.

---

# Der Operator `and`

Der Operator `and` bedeutet:

> Beide Bedingungen müssen wahr sein.

Nur wenn beide Bedingungen `True` sind, ist das Gesamtergebnis ebenfalls `True`.

## Syntax

```python
if bedingung1 and bedingung2:
    print("Beide Bedingungen sind erfüllt.")
```

## Beispiel

```python
alter = 20
hat_ausweis = True

if alter >= 18 and hat_ausweis:
    print("Einlass erlaubt.")
```

Ausgabe:

```text
Einlass erlaubt.
```

---

# Der Operator `or`

Der Operator `or` bedeutet:

> Mindestens eine Bedingung muss wahr sein.

Sobald eine Bedingung `True` ist, wird die gesamte Bedingung ebenfalls `True`.

## Syntax

```python
if bedingung1 or bedingung2:
    print("Mindestens eine Bedingung stimmt.")
```

## Beispiel

```python
akku = 15
ladekabel = True

if akku < 20 or ladekabel:
    print("Gerät kann verwendet werden.")
```

Ausgabe:

```text
Gerät kann verwendet werden.
```

---

# Der Operator `not`

Der Operator `not` kehrt einen Wahrheitswert um.

| Vorher | Nachher |
|--------|---------|
| True | False |
| False | True |

## Syntax

```python
if not bedingung:
    print("Die Bedingung ist nicht erfüllt.")
```

## Beispiel

```python
eingeloggt = False

if not eingeloggt:
    print("Bitte anmelden.")
```

Ausgabe:

```text
Bitte anmelden.
```

---

# Wahrheitstabellen

## and

| A | B | A and B |
|---|---|----------|
| False | False | False |
| False | True | False |
| True | False | False |
| True | True | True |

---

## or

| A | B | A or B |
|---|---|---------|
| False | False | False |
| False | True | True |
| True | False | True |
| True | True | True |

---

## not

| A | not A |
|---|-------|
| True | False |
| False | True |

---

# Reihenfolge der Auswertung

Python berechnet Bedingungen schrittweise.

Beispiel:

```python
x = False
y = True

if not x and y:
    print("A")
```

Schrittweise Auswertung:

```text
not False
↓

True

True and True
↓

True

if True
↓

A
```

Python berechnet also zuerst den Ausdruck.

Erst danach entscheidet die `if`-Anweisung, welcher Block ausgeführt wird.

---

# Mehrere Beispiele

## Beispiel 1

```python
regen = False

if not regen:
    print("Spazieren gehen.")
```

Ausgabe:

```text
Spazieren gehen.
```

---

## Beispiel 2

```python
alter = 19
hat_ticket = False

if alter >= 18 and not hat_ticket:
    print("Ticket fehlt.")
```

Ausgabe:

```text
Ticket fehlt.
```

---

## Beispiel 3

```python
mitglied = False
gast = True

if not mitglied and gast:
    print("Gastzugang erlaubt.")
```

Ausgabe:

```text
Gastzugang erlaubt.
```

---

# Typische IHK-Fallen

## Fehler 1

`not` wird vergessen.

Falsch gedacht:

```text
not False

↓

False
```

Richtig:

```text
not False

↓

True
```

---

## Fehler 2

Mehrere Bedingungen werden nicht vollständig ausgewertet.

Falsch:

```python
if x and y
```

Nur auf `x` schauen.

Richtig:

Beide Bedingungen vollständig berechnen.

---

## Fehler 3

Die Reihenfolge wird verwechselt.

Python arbeitet immer nach diesem Schema:

1. Variablen einsetzen
2. `not` berechnen
3. `and` und `or` berechnen
4. Ergebnis ist `True` oder `False`
5. Erst jetzt entscheidet `if`

---
## Fehler 4
if benötigt keinen Vergleich

Viele Anfänger glauben, dass hinter if immer ein Vergleich stehen muss.

Zum Beispiel:

if alter >= 18:

Das stimmt jedoch nicht.

Eine if-Anweisung benötigt lediglich einen Wahrheitswert (True oder False).

Deshalb funktionieren auch folgende Beispiele:

if True:
print("A")
if False:
print("B")

Oder:

eingeloggt = False

if not eingeloggt:
print("Bitte anmelden.")

Python berechnet zuerst:

not False

↓

True

Anschließend entscheidet die if-Anweisung:

if True:

und führt den entsprechenden Code aus.

Merksatz:

Eine if-Anweisung prüft keinen Vergleich. Sie prüft nur, ob das Ergebnis True oder False ist.

# Prüfungsrelevanz

Boolesche Operatoren gehören zu den absoluten Grundlagen der Programmierung.

Sie werden benötigt für:

- Kontrollstrukturen
- Schleifen
- Funktionen
- Algorithmen
- Benutzereingaben
- Prüfungsaufgaben der IHK

---

# Wiederholungsfragen

- Wofür wird `and` verwendet?
- Wofür wird `or` verwendet?
- Was macht `not`?
- Wann liefert `and` den Wert `True`?
- Wann liefert `or` den Wert `False`?
- Was passiert zuerst: Ausdruck berechnen oder `if` ausführen?
- Warum ergibt `not False` den Wert `True`?

---

# Merksätze

- `and` → Beide Bedingungen müssen wahr sein.
- `or` → Mindestens eine Bedingung muss wahr sein.
- `not` → Kehrt den Wahrheitswert um.
- Python berechnet zuerst die Bedingung und entscheidet danach über den `if`-Block.
- Jede Bedingung endet immer mit einem Ergebnis: `True` oder `False`.

---

# Zusammenfassung

Boolesche Operatoren ermöglichen es, Bedingungen miteinander zu verknüpfen oder umzudrehen.

Die drei wichtigsten Operatoren sind:

- `and`
- `or`
- `not`

Vor jeder Entscheidung berechnet Python den gesamten Ausdruck. Erst wenn das Ergebnis `True` oder `False` feststeht, entscheidet die `if`-Anweisung, welcher Code ausgeführt wird.

Diese Operatoren gehören zu den wichtigsten Grundlagen der Programmierung und werden in nahezu jedem Programm verwendet.