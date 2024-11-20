# Data Structures & Algorithms I

- [Data Structures \& Algorithms I](#data-structures--algorithms-i)
  - [Asymptotische Schranken](#asymptotische-schranken)
  - [Elementare Datenstrukturen](#elementare-datenstrukturen)
    - [Lineares Feld (Array)](#lineares-feld-array)
    - [Lineare Liste (Linked List)](#lineare-liste-linked-list)
    - [Stapel (Stack)](#stapel-stack)
    - [Schlange (Queue)](#schlange-queue)
  - [Sortierverfahren](#sortierverfahren)
    - [Divide \& Conquer](#divide--conquer)
    - [Insertion Sort](#insertion-sort)
    - [Merge Sort](#merge-sort)
    - [Quick Sort](#quick-sort)
    - [Radix Sort](#radix-sort)
  - [Suchverfahren](#suchverfahren)
    - [Sequentielle Suche](#sequentielle-suche)
    - [Selbstanordnende Felder](#selbstanordnende-felder)
    - [Binärsuche](#binärsuche)
    - [Interpolationssuche](#interpolationssuche)
    - [Quadratische Binärsuche](#quadratische-binärsuche)
    - [Fast Search](#fast-search)
  - [Binärbäume](#binärbäume)
    - [Auslesereihenfolgen](#auslesereihenfolgen)
    - [sortierte Binärbäume](#sortierte-binärbäume)
    - [balancierte Bäume](#balancierte-bäume)
    - [2-4 Bäume](#2-4-bäume)
    - [B-Sort](#b-sort)
  - [Halden (Heaps)](#halden-heaps)
    - [heapify](#heapify)
    - [build\_heap](#build_heap)
    - [Heap Sort](#heap-sort)
  - [Hash Tables](#hash-tables)
    - [Hashing](#hashing)
    - [Überläuferlisten](#überläuferlisten)
    - [Offene Adressierung](#offene-adressierung)
  - [Dynamische Arrays](#dynamische-arrays)
  - [Amortisierte Analyse](#amortisierte-analyse)

---

## Asymptotische Schranken

- generelle Methode Wachstum von Funktion abzuschätzen
- O(1) < O(log n) < O(√n) < O(n) < O(n log n) < O(n^x) < O(x^n) < O(n!)
- O-Notation -> asymptotische obere Schranke
  - Definition: O(g(n)) = f(n) | Ǝ c ∈ R+, n𝑜 ∈ N: f(n) <= c * g(n) ∀ n >= n𝑜
- Ω-Notation -> asymptotisch untere Schranke
  - Definition: Ω(g(n)) = f(n) | Ǝ c ∈ R+, n𝑜 ∈ N: f(n) >= c * g(n) ∀ n >= n𝑜
- Θ-Notation -> asymptotisch exakte Schranke
  - Definition: Θ(g(n)) = f(n) | Ǝ c1, c2 ∈ R+, n𝑜 ∈ N: c1 * g(n) <= f(n) <= c2 * g(n) ∀ n >= n𝑜
- Laufzeit best case:    T(n) = min{T(I): |I| = n}
- Laufzeit average case: T(n) = 1/(|I(n)|) ∑T(I) mit I(n) = {I: |I| = n}
- Laufzeit worst case:   T(n) = max{T(I): |I| = n}

## Elementare Datenstrukturen

|Operation            |Array|Linked List|Stack|Queue|
|---------------------|-----|-----------|-----|-----|
|Zugriff auf Element i|O(1) |O(i)       |     |     |
|Suchen               |O(n) |O(n)       |     |     |
|Einfügen             |O(n) |O(1)       |O(1) |O(1) |
|Entfernen            |O(n) |O(1)       |O(1) |O(1) |

### Lineares Feld (Array)

- fixe Größe
- Zugriff auf Element A[i] -> O(1)
- Suchen -> O(n)
- Einfügen -> O(n)
- Löschen -> O(n)

### Lineare Liste (Linked List)

- Zugriff auf Element A[i] -> O(i)
- Suchen -> O(n)
- Einfügen -> O(1)
- Löschen -> O(1)
  - mit Suchen -> O(n)

### Stapel (Stack)

- LIFO
- Hinzufügen nur an letzte Stelle
- Nur Entfernen des letzten Elements
- alle Operationen -> O(1)

### Schlange (Queue)

- FIFO
- Hinzufügen nur an letzte Stelle
- Nur Entfernen des ersten Elements
- alle Operationen -> O(1)

## Sortierverfahren

- in-place
  - Zahlen im Inputfeld umgeordnet
  - Zu jedem Zeitpunkt nur eine konstante Anzahl davon außerhalb zwischengespeichert
- stabil
  - Elemente mit identischen Sortierschlüsseln in In- & Output in gleicher Reihenfolge
- adaptiv
  - vorsortierte Folgen werden effizienter sortiert
  - bessere Laufzeit für fast sortierete Folgen
- worst-case optimal
  - Jede Eingabe wird in O(n log n) Zeit sortiert
- worst-case Verhalten -> längster Ast in Entscheidungsbaum
- Idealer Algorithmus -> vollständiger Binärbaum mit n! Blättern
- Höhe Binärbaum mit n! Blättern -> Ω(n log n)

|Algorithmus  |in-place|stabil|adaptiv|best-case |avg-case  |worst-case|
|-------------|--------|------|-------|----------|----------|----------|
|InsertionSort|✓       |✓     |✓      |O(n)      |O(n^2)    |O(n^2)    |
|MergeSort    |x       |✓     |x      |O(n log n)|O(n log n)|O(n log n)|
|QuickSort    |✓       |x     |x      |O(n log n)|O(n log n)|O(n^2)    |
|RadixSort    |x       |✓     |x      |O(d * n)  |O(d * n)  |O(d * n)  |
|HeapSort     |✓       |x     |x      |O(n log n)|O(n log n)|O(n log n)|
|B-Sort       |x       |x     |✓      |O(n log n)|O(n log n)|O(n log n)|

### Divide & Conquer

- Teile -> Problem in Anzahl von Teilproblemen aufteilen
- Herrsche -> Teilprobleme durch rekursive Aufrufe lösen
- Verbinde -> Teillösungen zu Gesamtlösung verbinden

### Insertion Sort

- best case:    Ω(n)
- average case: O(n^2)
- worst case:   O(n^2)
- Speicher:     Θ(1)
- in-place
- stabil
- adaptiv

```
INSERTIONSORT(A, n)
    FOR i <- 1 TO n-1 DO
        h <- A[i]
        j <- i-1
        WHILE j >= 0 AND h < A[j] DO
            A[j+1] <- A[j]
            j <- j-1
        A[j+1] <- h
    RETURN A
```

### Merge Sort

- Teile Feld in 2 Hälften
- Hälften rekursiv sortieren
- sortierte Teilfolgen zu sortierter Gesamtfolge verschmelzen
- best case:    Ω(n log n)
- average case: O(n log n)
- worst case:   O(n log n)
- Speicher:     Θ(n)
- stabil

```
MERGESORT(A, von, bis)
    IF von < bis THEN
        k <- floor((von+bis)/2)
        MERGESORT(A, von, k)
        MERGESORT(A, k+1, bis)
        VERSCHMELZE(A, von, k, bis)
```

### Quick Sort

- Zerlege Feld, dass Elemente links kleiner-gleich der Elemente rechts sind
- Zerlege Teilfelder rekursiv
- best case:    Ω(n log n)
- average case: O(n log n)
- worst case:   O(n^2)
- Speicher:     O(n)
- in-place

```
QUICKSORT(A, von, bis)
    IF von < bis THEN
        k <- PARTITION(A, von, bis)
        QUICKSORT(A, von, k)
        QUICKSORT(A, k+1, bis)
```

### Radix Sort

- nach k Durchläufen Zahlen, eingeschränkt auf die letzten k Ziffern, sortiert
- nur bei großen Datenmengen effizient
- hoher Speicheraufwand
- nicht vergleichsorientiert
- Streuphase
  - A nach i-ter Ziffer von hinten in Fächer einordnen
- Sammelphase
  - Fächer in aufsteigender Reihenfolge in A zusammenfassen

```
RADIXSORT(A, d)
    FOR i = 1 TO d
        {Streuphase}
        {Sammelphase}
```

## Suchverfahren

- ohne Vorsortierung
  - sequentielle Suche
  - selbstanordnende Felder
- mit Vorsortierung
  - Binärsuche
  - Interpolationssuche
  - Quadratische Binärsuche
  - Fastsearch
- Speicherbedarf
  - rekursive Algorithmen: proportional zur Laufzeit
  - iterative Algorithmen: O(1)

|Algorithmus|avg-case    |worst-case|
|-----------|------------|----------|
|SeqSearch  |Θ(n)        |Θ(n)      |
|BinSearch  |O(log n)    |O(log n)  |
|IntSearch  |O(log log n)|Θ(n)      |
|QuadSearch |O(log log n)|O(√n)     |
|FastSearch |O(log log n)|O(log n)  |

### Sequentielle Suche

- Feld von Anfang bis Ende durchsuchen
- average case: Θ(n)
- worst case:   Θ(n)
  - wenn jedes Element gleich oft gesucht
- Verbesserung durch Speichern der Elemente nach Zugriffswahrscheinlichkeit
  - Gleichverteilung:         O(n)
  - exponentielle Verteilung: O(1)

```
SEQSEARCH(A, x)
    i <- 0
    WHILE i < n DO
        IF A[i] = x THEN
            RETURN i
        i <- i+1
    RETURN NAN
```

### Selbstanordnende Felder

- Elemente, die häufiger gesucht werden nach vorne verschieben
- 3 Heuristiken
  - vertausche A[i] mit A[0]
  - vertausche A[i] mit A[i-1]
  - Zählen d. Zugriffe & dementsprechend umordnen

### Binärsuche

- Feld in 2 gleich große Hälften teilen
- Mit mittlerem Vergleichen
  - ident -> gefunden
  - ansonsten in linker (kleiner) / rechter (größer) Hälfte wiederholen
- average case: O(log n)
- worst case:   O(log n)

```
BINSEARCH(A, x)
    IF len(A) > 0 THEN
        m <- floor(len(A)/2)
        IF x = A[m] THEN
            RETURN m
        ELSE
            IF y < A[m] THEN
                RETURN BINSEARCH(A[0...m-1], x)
            ELSE
                RETURN BINSEARCH(m+1+A[m+1...len(A)-1], x)
    ELSE
        RETURN NAN
```

### Interpolationssuche

- Suche nicht in der Mitte, sondern dort wo Element "sein sollte"
  - unter Annahme, dass Werte linear steigen
- average case: O(log log n)
- worst case:   Θ(n)

```
INTSEARCH(von, bis, x)
    IF A[von] < A[bis] THEN
        t <- von + floor((bis-von)*((x-A[von])/(A[bis]-A[von])))
        IF x = A[t] THEN
            RETURN t
        ELSE
            IF x < A[t] THEN
                RETURN INTSEARCH(von, t-1, x)
            ELSE
                RETURN INTSEARCH(t+1, bis, x)
    ELSE
        IF x = A[von] THEN
            RETURN von
        ELSE
            RETURN NAN
```

### Quadratische Binärsuche

- Idee: verhindere worst-case d. Interpolationssuche durch Anwendung Interpolationssuche auf √n Teilfelder der Länge vn
  - Berechne Index t durch Interpolationssuche
  - Suche von t aus korrektes Teilfeld (in Sprüngen von √n) & suche von dort aus weiter
  - Identifizieren des korrekten Teilfelds in O(1) Zeit
- average case: O(log log n)
- worst case:   O(√n)

```
QUADSEARCH(von, bis, x)
    n <- bis-von+1
    IF A[von] < A[bis] THEN
        t <- von + floor((bis-von)*((x-A[von])/(A[bis]-A[von])))
        IF x = A[t] THEN
            RETURN t
        ELSE IF x < A[t] THEN
            REPEAT t <- t - floor(√n) UNTIL x >= A[t]
            RETURN QUADSEARCH(t, t + floor(√n)-1, x)
        ELSE
            REPEAT t <- t + floor(√n) UNTIL x <= A[t]
            RETURN QUADSEARCH(t - floor(√n)+1, t, x)
    ELSE IF x = A[von] THEN
        RETURN von
    ELSE
        RETURN NAN
```

### Fast Search

- Kombination Binärsuche & Interpolationssuche
- average case: O(log log n)
- worst case:   O(log n)

```
FASTSEARCH(von, bis, x)
    IF von <= bis THEN
        m(B) <- floor((von+bis)/2)
        m(I) <- von + floor((bis-von)*((x-A[von])/(A[bis]-A[von])))
        IF m(B) > m(I) THEN
            VERTAUSCHE(m(B), m(I))
        IF x = A[m(B)] THEN 
            RETURN m(B)
        ELSE IF x = A[m(I)] THEN
            RETURN m(I)
        ELSE IF x < A[m(B)] THEN
            RETURN FASTSEARCH(von, m(B)-1, x)
        ELSE IF x < A[m(I)] THEN
            RETURN FASTSEARCH(m(B)+1, m(I)-1, x)
        ELSE
            RETURN FASTSEARCH(m(I)+1, bis, x)
    ELSE
        RETURN NAN
```

## Binärbäume

- Wurzel -> ausgezeichneter Knoten ohne Parent (A[0])
- Blatt -> Knoten ohne Kinder
- Höhe h -> max Anzahl der Anwendungen von parent um von beliebigen Knoten zur Wurzel zu gelangen
- Jeder Knoten hat genau 1 Parent
- Jeder Knoten ist Parent von maximal 2 Kindern
- Jeder Knoten ist Wurzel eines Teilbaumes
- Ordnung Knoten: Anzahl seiner Kinder
- Ordnung Baum: maximale Ordnung aller Knoten
- Höhe Baum: Länge d. längsten Astes
- Voller Baum d. Ordnung K -> Jeder Knoten hat genau k Kinder oder ist ein Blatt
- Vollständiger Baum -> Voller Baum, bei dem jedes Blatt gleiche Tiefe hat
- grundlegende Operationen
  - Wurzel(B) -> Wurzelknoten d. Baumes
  - links(k) -> linkes Kind von k
  - rechts(k) -> rechtes Kind von k
  - Parent(k) -> Parentknoten von k
  - Wert(k) -> Wert in Knoten k

### Auslesereihenfolgen

- symmetrische Reihenfolge (SR)
  - in-order
  - linker Teilbaum in SR, Wurzel, rechter Teilbaum in SR
- Hauptreihenfolge (HR)
  - preorder
  - Wurzel, linker Teilbaum in HR, rechter Teilbaum in HR
- Nebenreihenfolge (NR)
  - postorder
  - linker Teilbaum in NR, rechter Teilbaum in NR, Wurzel

### sortierte Binärbäume

- in symmetrischer Reihenfolge sortiert
  - Knoten linker Teilbaum <= Wurzel <= Knoten rechter Teilbaum
- Suchen: O(h)
  - h -> Länge d. längsten Astes
- Einfügen: O(h)
- Minimum / Maximum: O(h)
- Aufbau
  - durch wiederholtes Einfügen (natürliche Bäume)
  - Binärbaum hängt von Reihenfolge d. Elemente ab
  - randomisiert Einfügen -> E[h] = Θ(log n)
- Nachfolger von k 
  - nächster Knoten in sortierter Reihenfolge (nächstgrößerer / gleicher Wert in Baum)
  - Laufzeit: O(h)
- Vorgänger von k
  - Vorgängerknoten in sortierter Reihenfolge
  - Laufzeit: O(h)
- Entfernen
  - a) k ist Blatt -> abhängen
  - b) k hat nur 1 Kind -> Teilbaum des Kindes als Parent(k) anhängen
  - c) k hat 2 Kinder
    - Finde k' -> nächster Knoten in sortierter Knotenfolge
    - Wert(k) = Wert(k')
    - Entferne k' (Fall a) oder b))
  - Laufzeit: O(h)
- Vorteil: dynamische Lösung d. Wörterbuchproblems
- Nachteil: Zeiten bis zu Θ(n) bei entarteten Bäumen

```
SEARCH(B, k)
    IF k = nil OR B = wert(k) THEN
        write k
    ELSE IF B < wert(k) then
        SEARCH(B, links(k))
    ELSE
        SEARCH(B, rechts(k))
```

```
INSERT(B, k)
    y <- nil
    x <- wurzel(B)
    WHILE x != nil DO
        y <- x
        IF wert(k) < wert(x) THEN
            x <- links(x)
        ELSE
            x <- rechts(x)
    parent(k) <- y
    IF y = nil THEN
        wurzel(B) <- k
    ELSE IF wert(k) < wert(y) THEN
        links(y) <- k
    ELSE rechts(y) <- k
```

### balancierte Bäume

- Bedingungen zur Erhaltung logarithmischer Baumhöhe:
  - Höhenbedingung
    - h(B) -> Höhe von B
    - Für jeden Knoten gilt: |h(B(links)) - h(B(rechts))| <= k
  - Gewichtsbedingung
    - g(B) -> # Blätter von B
    - Für jeden Knoten gilt: 1/𝛼 <= g(B(links))/g(B(rechts)) <= 𝛼
  - Strukturbedingung
    - Alle Blätter haben gleiche Tiefe, Ordnung d. Knoten (# Kinder) ist variabel

### 2-4 Bäume

- Alle Äste gleich lang
- max # Kinder pro Knoten ist 4
- innere Knoten haben >= 2 Kinder
- Blätter enthalten von links nach rechts Werte aufsteigend sortiert
- Jeder innere Knoten k mit 𝛼(k) Kindern (2 <= 𝛼(k) <= 4) speichert 𝛼(k)-1 Hilfsinformationen
  - wobei x(i) = größter Wert im Teilbaum d. i-ten Kindes von links
- Innere Knoten speichern Hilfsinformationen
- Höhe h: Θ(log n)
- Anzahl Blätter wird mit jeder Schicht
  - mindestens verdoppelt
  - maximal vervierfacht
- Anzahl Knoten bei n Blättern
  - \# Knoten <= 2n = O(n)
- Suchen: Θ(log n)
- Einfügen: O(log n)
  - 𝛼(k) <= 4 -> resultierender Baum ist wieder 2-4 Baum
  - 𝛼(k) = 5 -> Spalten von k
    - k an Bruder k' rechts von k geben
    - 2 rechtesten Kinder von k auf k' umhängen 
    - (muss evtl. für übergeordnete Knoten wiederholt werden)
- Entfernen: O(log n)
  - 𝛼(k) >= 2 -> resultierender Baum ist wieder 2-4 Baum
  - 𝛼(k) = 1 (k' -> direkter Bruder)
    - 𝛼(k') >= 3 -> stehlen eines Kindes von k'
    - 𝛼(k') = 2 -> verschmelzen von k mit k'
- Vorgenommene Umstrukturierungen amortisieren sich später 

### B-Sort

- adaptiv & worst-case optimal
- Zahlenfolge verkehrt (a(n) ... a(1)) in 2-4 Baum einfügen
- Innere Knoten speichert nur Maximum in Teilbaum
- Idee:
  - wenn f(i) klein, liegt w' tief
  - Bottom up einfügen
    - starte bei linkestem Blatt
    - laufe bis zu w' (1. Knoten mit max > a(i))
    - Füge a(i) in Teilbaum ein
  - -> Anhängen von a(i) in Θ(log f(i)) Zeit

## Halden (Heaps)

- A[i] >= max{A[2i+1], A[2i+2]}
- Zugriff auf Nachfolger / Vorgänger
  - links(i)  -> 2i+1
  - rechts(i) -> 2i+2
  - parent(i) -> floor((i-1)/2)
- A[0] -> Wurzel -> Maximum 
- Jeder Teilbaum wieder Halde
- Höhe h -> floor(ld n)

### heapify

- Voraussetzung
  - Teilbäume mit Wurzel links(i) & rechts(i) sind Halden
  - Element i verletzt Haldenbedingung
- Laufzeit: O(log n)

```
HEAPIFY(A, i)
    l <- links(i)
    r <- rechts(i)
    index <- i
    IF l < len(A) AND A[l] > A[i] THEN
        index <- l
    IF r < len(A) AND A[r] > A[index] THEN
        index <- r
    IF i != index THEN
        VERTAUSCHE(A[i], A[index])
        HEAPIFY(A, index)
```

### build_heap

- Blätter sind bereits triviale Halden
- Verhalde nur Elemente mit index i <= floor(n/2) - 1
- Verhalde bottom-up
- Laufzeit
  - Naive Analyse: O(n log n)
  - Aber: Element der Höhe h kann in O(n) verhaldet werden: O(n)

```
BUILD_HEAP(A)
    FOR i <- floor(n/2) - 1 DOWNTO 0 DO
        HEAPIFY(A, i)
```

### Heap Sort

- Idee
  - Vertausche A[0], A[n-1]
  - Verkleinere Halde um 1
  - -> A[0] ist nicht mehr Maximum
  - -> Datenstruktur muss umstrukturiert werden
- best case:    O(n log n)
- average case: O(n log n)
- worst case:   O(n log n)
- in-place

```
HEAPSORT(A)
    BUILD_HEAP(A)
    FOR i <- n-1 DOWNTO 1 DO
        VERTAUSCHE(A[0], A[i])
        N <- N-1 // N ist aktuelle Haldengröße
        HEAPIFY(A, 0)
```

## Hash Tables

- m -> Tabellengröße
- n -> Anzahl eingefügter Elemente
- 𝛼 -> Belegungsfaktor
  - n/m
  - 𝛼 > 1 -> Kollisionen unvermeidbar

### Hashing

- Anstatt zu suchen, berechne Datums-Adresse aus Schlüssel in O(1) Zeit
- gute Hashfunktion
  - h(w) soll effizient berechnet werden können
  - Jeder Index soll gleich wahrscheinlich sein, um Kollisionen zu verhindern
  - Ähnliche Werte sollen gut getrennt werden
  - h(w) soll unabhängig von Mustern in den Daten sein
- ideale Hashfunktion (theoretisches Konstrukt)
  - Verwendung zur Analyse
  - existiert in der Praxis nicht
- reale Hashfunktionen
  - Divisionsmethode
    - Dividiere Wert durch m & nimm Rest
    - h(w) = w mod m
    - Vorteil: schnell berechenbar
    - Nachteil nicht für alle m gut
  - Multiplikationsmethode
    - Multipliziere Wert mit fixer Konstante A & multipliziere gebrochenen Teil mit m
    - h(w) = floor(m*frac(w*A))
    - Vorteil: m ist unkritisch

### Überläuferlisten

- Bei Kollisionen Daten in verketteter Liste angelegt
- Einfügen: O(1)
- Suchen: O(1+𝛼)
- Löschen: O(1+𝛼)
- worst case: Θ(1+n)
  - für Suchen & Löschen

### Offene Adressierung

- Bei Kollision wird so lange neue Adresse berechnet, bis freier Platz gefunden
- Ideale Hashfunktion -> für jeden Wert ist h(w) mit Wahrscheinlichkeit 1/m! eine der m! Permutationen
- In der Praxis verwendete Näherungen
  - Linear Probing
    - h(w,i) = (h'(w)+1) mod m
    - Problem: benachbarte Felder wahrscheinlicher belegt (primary Clustering)
  - Quadratic Probing
    - h(w,i) = (h'(w)+f(i)) mod m
    - f(i) -> quadratische Funktion; bei Kollision weiterhin selbe Indexfolge (secondary Clustering)
  - Double Hashing
    - h(w,i) = ((h'(w)+ih''(w))) mod m
- Einfügen: O(1/(1-𝛼))
- Suchen: O(1/(1-𝛼))
- Löschen: O(1/(1-𝛼))

## Dynamische Arrays

- dynamische Größe
- Zugriff auf Element i in konstanter Zeit
- Hinzufügen am Ende in (amortisierter) konstanter Zeit
- Entfernen am Ende in (amortisierter) konstanter Zeit
- dynamisches Array is Tupel DA = (A, n)
  - A -> Array d. Größe n(cap)
  - n -> Anzahl gespeicherter Elemente
- Grundprinzip
  - Array von links nach rechts auffüllen
  - mehr als n(cap) Elemente -> größe verdoppeln
  - Array wird von rechts nach links geschrumpft
  - löschen & weniger als n(cap)/4 Elemente -> Größe halbieren
- Speicherverbrauch (n(cap)) -> Θ(n)
- worst case: Ω(n)
  - für Löschen & Hinzufügen (wenn erweitert / geschrumpft wird)
- Amortisierte Laufzeit
  - k aufeinanderfolgende add / delete Operationen in beliebiger Reihenfolge
  - -> Laufzeit der k Operationen: O(k)

```
ADD(DA, x)
    IF n < n(cap) THEN
        A[n] <- x
        RETURN (A, n+1)
    ELSE
        A_old <- A
        A = new array of size 2n(cap)
        A[0,...,n-1] <- A_old[0,...,n-1]
        free(A_old)
        RETURN ADD((A, n), x)
```

```
DELETE(DA)
    IF n > n(cap)/4 THEN
        RETURN (A, n-1)
    ELSE
        A_old <- A
        A = new array of size n(cap)/2
        A[0,...,n-1] <- A_old[0,...,n-1]
        free(A_old)
        RETURN DELETE((A, n))
```

## Amortisierte Analyse

- zeigt, dass m aufeinanderfolgende (verschiedene) Operationen effizient sind
- Beispiel 2-4 Baum
  - einfügen / entfernen benötigt nicht immer spalten / stehlen / ...
  - O(m log n) Umstrukturierungen nicht benötigt
  - m einfügen / entfernen Operationen benötigen nur O(m) Umstrukturierungen
- Beispiel dynamisches Array
  - add / delete hat im worst case Ω(n) Laufzeit
  - k add / delete Operationen braucht keine Ω(k^2) Laufzeit
  - Laufzeit für k Operationen eigentlich O(k)
- Abrechnungstechnik
  - Datenstruktur bekommt Konto
  - Jede Operation auf Datenstruktur wird Ein- / Auszahlung zugeordnet
  - Auszahlungen entsprechen typischerweise Laufzeit für Operation
  - Durch Konto können Aufwände in der Datenstruktur abgeschätzt werden
