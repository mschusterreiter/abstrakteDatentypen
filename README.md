# Übung 13 - Abstrakte Datentypen

# 1. Aufgabe

Folgendes Klassendiagramm soll umgesetzt werden:

<p align="center">
  <img src="/assets/images/UML1.png" alt="Bildbeschreibung" />
</p>

Bei dieser Aufgabe müssen sie das erste Mal zwei Klassen programmieren. Die Verbindung zwischen den beiden Klassen ist eine „Has a“-Beziehung. In diesem Fall `Sportwagen` has a `Person`. Die Raute ist immer bei der Klasse, wo die andere benötigt wird. Die Zahlen 0..2 geben an, dass die `Sportwagen` Klasse entweder 0, 1 oder 2 Personen hat. Genaueres zu 
den UML Diagrammen schauen wir uns nächste Woche an.

**Beschreibung der Klasse `Person`:**
- Eigenschaften: 
    - `vorname` und `nachname` dürfen nicht leer sein. 
    - `alter` darf nicht negativ sein.
    - `fuehrerschein` darf nur `true` sein, wenn die `Person` älter als 17 Jahre ist.
- Methoden:
    - `print()`: Gibt alle Eigenschaften einer `Person` aus. 
    - `boolean zahlen(int betrag)`: Die `Person` muss etwas bezahlen. Falls zu wenig Bargeld vorhanden ist, soll `false` zurückgegeben werden. Kann die Person den Betrag begleichen soll `true` zurückgegeben werden.

**Beschreibung der Klasse `Sportwagen`:**
- Eigenschaften: 
    - `marke` darf nicht leer sein. 
    - `ps` muss größer als `100` sein.
    - `verbrauch` muss größer als `8.0` und kleiner als `30.0` sein.
    - `fahrer` darf nicht `null` sein. (Ein `Sportwagen` kann nicht ohne Fahrer fahren, ohne Beifahrer jedoch schon)

- Methoden:
    - `print()`: Gibt alle Eigenschaften des Sportwagens aus. Auch die Eigenschaften der Personen im Wagen sollen angezeigt werden.
    - `schnellfahren(int betrag)`: Der Fahrer muss eine Strafe zahlen. Falls er nicht genug Geld hat, kann er entweder den Beifahrer nach einem Darlehen fragen, oder sich einen Zahlschein ausstellen lassen. Hat er Beifahrer auch nicht genügend Geld, bekommt der Fahrer auch einen Zahlschein. Es ist auch gestattet, dass Fahrer und Beifahrer „zusammenlegen“. Muss trotzdem ein Zahlschein ausgestellt werden, verliert der Fahrer seinen Führerschein.


Um Ihr Programm zu testen, erstellen Sie eine `Main`-Klasse, welche die `main`-Methode beinhaltet:
- `main(String[] args)`: Erstellen Sie dabei zuerst Instanzen jeder Klasse. Dies machen Sie wie gehabt mit dem Wort `new` und dann den Aufruf des Konstruktors. Um eine Instanz der `Sportwagen` Klasse zu erstellen, benötigen Sie zuerst mindestens eine Instanz der Person `Klasse`. Testen Sie Ihr Programm. 

## 2. Aufgabe

Folgendes Klassendiagramm soll umgesetzt werden:

<p align="center">
  <img src="/assets/images/UML2.png" alt="Bildbeschreibung" />
</p>

**Beschreibung der Klasse `USBStick`:**
- Eigenschaften: 
    - `kennzeichen` darf nicht leer sein. 
    - `groesseInMB` muss mindestens 512 sein.
    - `verkaufsPreisUSB` liegt zwischen `5` und `100`. 
- Methoden:
    - `printUSBStick()`: Gibt alle Eigenschaften des jeweiligen Sticks aus.

**Beschreibung der Klasse `Computer`:**
- Eigenschaften: 
    - `name` darf nicht leer sein. 
    - `verkaudsPreisComputer` muss größer als `200` sein.

- Methoden:
    - `printComputer()`: Gibt alle Eigenschaften des Sportwagens (inklusive der angesteckten USB-Sticks) aus.
    - `summeVerkaufsPreis()`: Summe aller Teile.

Um Ihr Programm zu testen, erstellen Sie eine `Main`-Klasse, welche die `main`-Methode beinhaltet:
- `main(String[] args)`: Testen Sie Ihr Programm. Gehen Sie dabei genauso wie in der ersten Aufgabe vor.


## 3. Aufgabe

Folgendes Klassendiagramm soll umgesetzt werden:

<p align="center">
  <img src="/assets/images/UML3.png" alt="Bildbeschreibung" />
</p>

**Beschreibung der Klasse `Baum`:**
- Eigenschaften: 
    - `name` darf nicht leer sein. 
    - `alter` muss größer-gleich `0` sein.
    - `hoehe` (in Meter) muss größer `0` und kleiner `150` sein.
    - `durchmesser` (in Meter) muss größer `0` und kleiner als ein Zehntel der `hoehe` sein. 
- Methoden:
    - `boolean zuFaellen()`:  Überprüft, ob der Baum gefällt werden muss. Ein Baum darf gefällt werden, wenn sein `alter` größer `40` oder seine `hoehe` größer `50` ist. Hat ihn eine Krankheit befallen muss er auch gefällt werden.
    - `double volumen()`: Liefert das Volumen eines Baums zurück – denken Sie sich den Baum als Zylinder.

**Beschreibung der Klasse `MiniWald`:**

- Methoden:
    - `Baum faellen()`: Gibt den gefällten `Baum` zurück. Falls keiner zu fällen ist, wird `null` zurückgegeben. Welche Methode können Sie hier anwenden? Wird ein `Baum` gefällt, wird seine Objektreferenz (b0, b1 oder b2) auf `null` gesetzt.
    - `pflanzen(Baum b)`: Eine Objektreferenz mit dem Wert `null` erhält ein neues `Baum`-Objekt. Falls kein Platz mehr ist, soll eine Fehlermeldung ausgegeben werden.
    - `int anzahlKrank()`: Gibt die Anzahl an kranken Bäumen zurück.
    - `double volumen()`: Gibt das Gesamtvolumen des MiniWalds zurück.


Um Ihr Programm zu testen, erstellen Sie eine `Main`-Klasse, welche die `main`-Methode beinhaltet:
- `main(String[] args)`: Testen Sie Ihr Programm. Gehen Sie dabei genauso wie in der ersten Aufgabe vor.
