# Lær at kode
Et lille projekt, for nybegyndere 😊
Idéen er her at, hvis man følger instrukserne her, så får man en introduktion til at kode.

## Kom igang (til Windows)
Du skal bruge nogle værktøjer for at lave kode og programmer til din computer.
Først skal du downloade og installere nogle programmer:
1. _Python_ er et programmerings-sprog, som vi skal lave vores programmer med. Du kan vælge tilgang **a)** eller **b)**:
   
   **a)** Brug &#8862; eller ❖ (windows-knappen) og skriv "Store" og åben "Microoft Store" og brug søgefeltet til at
   skrive "Python" + ↵ og hent 3.12 eller nyere.

   **b)** Alternativt kan man downloade python fra: https://apps.microsoft.com/search?query=python&hl=en-GB&gl=DK
2. Nu skal du installere _Visual Studio Code_, som er lidt lige som MS Word eller Notes til programmering. Du kan enten
   tilgang **a)** eller **b)**:
   
   **a)** Brug "Microsoft Store" lige som i punkt 1.**a)** men søg på "vs code" + ↵ og installer "den blå" 
   _Visual Studio Code_.

   **b)** Alternativt går du til https://code.visualstudio.com/download og vælg Windows. Efter filen er downloadet, skal 
   du installere den nye fil.

## Øvelse 1: Få computeren til at tale med dig 🤖
Dette er den klassiske "Hello, World!", men gjort personlig. Det viser, at et program kan tage imod input og reagere på
det.

Hvad det lærer: `input()`, `print()` og variabler.

Koden:

```python
# Spørg brugeren om deres navn og gem det i en variabel
navn = input("Hej! Hvad hedder du? ")

# Svar brugeren med en personlig hilsen
print("Fedt navn, " + navn + "! Jeg er en computer. Dejligt at møde dig.")
```
Sådan virker det:

`input()` pauser programmet og venter på, at brugeren skriver noget og trykker Enter.


Det, brugeren skriver, bliver gemt i "hukommelsen" med mærkatet navn. Dette kaldes en variabel.

`print()` skriver en besked ud på skærmen. Her sætter vi teksten sammen med indholdet af navn-variablen.

Prøv selv:

Kan du få programmet til også at spørge om alder eller yndlingsfarve og bruge det i svaret?

## Øvelse 2: Lav en simpel lommeregner 🧮
Denne øvelse viser, at computere er utroligt gode (og hurtige) til matematik.

Hvad det lærer: At konvertere tekst til tal (`int()`) og simple matematiske operatorer (`+`, `-`, `*`).

Koden:

```python
print("Lad os regne lidt!")

# Spørg om det første tal
tal1_tekst = input("Skriv det første tal: ")
tal1 = int(tal1_tekst)

# Spørg om det andet tal
tal2_tekst = input("Skriv det andet tal: ")
tal2 = int(tal2_tekst)

# Beregn summen og print resultatet
resultat = tal1 + tal2
print("Resultatet af " + tal1_tekst + " + " + tal2_tekst + " er: " + str(resultat))
```

Sådan virker det:

`input()` læser altid det, du skriver, som tekst.

For at kunne regne med tallene, må vi oversætte dem fra tekst til heltal med `int()`.

Derefter kan vi lægge dem sammen med `+` og gemme resultatet.

Til sidst oversætter vi resultatet tilbage til tekst med `str()` for at kunne printe det pænt.

Prøv selv:

Kan du ændre koden, så den ganger (`*`) eller trækker fra (`-`) i stedet for?

## Øvelse 3: Lav dine egne filer og mapper 📁✍️
Denne øvelse er virkelig fed, fordi den viser, hvordan et program kan interagere med selve computerens filsystem.

Hvad det lærer: At interagere med operativsystemet via os-biblioteket.

Koden:

```Python
# Importer os-biblioteket, der kan tale med computerens system
import os

# 1. Definer et navn til en ny mappe
mappenavn = "MinKodedeMappe"

# 2. Tjek om mappen allerede findes, og opret den hvis ikke
if not os.path.exists(mappenavn):
os.mkdir(mappenavn)
print("Mappen '" + mappenavn + "' er blevet oprettet!")
else:
print("Mappen '" + mappenavn + "' findes allerede.")

# 3. Lav en ny tekstfil inde i mappen og skriv en besked i den
filsti = os.path.join(mappenavn, "min_fil.txt")
with open(filsti, "w") as fil:
fil.write("Hej fra Python!\n")
fil.write("Det er ret sejt, at jeg kan lave mine egne filer med kode.")

print("Der er nu skrevet en besked i filen 'min_fil.txt' inde i din nye mappe.")
```
Sådan virker det:

`os.mkdir()` er kommandoen til at lave en ny mappe (`mkdir` = make directory).

`open(filsti, "w")` åbner (eller opretter) en fil og gør den klar til at blive skrevet til ("`w`" står for write).

`fil.write()` skriver den angivne tekst ind i filen.

Resultat:
Efter at have kørt koden, vil der ligge en ny mappe i samme mappe som Python-programmet. Inde i den mappe ligger der en 
ny tekstfil med den besked, du har skrevet! Det er en meget konkret og synlig effekt af ens kode.

Disse øvelser skulle give en god fornemmelse for den magi, der ligger i at kunne give en computer instrukser. Held og 
lykke!

## Øvelse 4: Lav en skør historie (Mad Libs) 🤪📖
Denne øvelse er fantastisk, fordi den er kreativ og resultatet næsten altid er komisk. Den bygger videre på idéen om at
bruge input() til at skabe noget personligt.

Hvad det lærer: Flere variable og en moderne måde at formatere tekst på (f-strings).

Koden:

```python

print("Hjælp mig med at skrive en historie!")

# Indsaml en masse tilfældige ord fra brugeren
adjektiv = input("Skriv et tillægsord (fx 'latterlig'): ")
udsagnsord = input("Skriv et udsagnsord i nutid (fx 'løber'): ")
navneord = input("Skriv et navneord i flertal (fx 'bananer'): ")
sted = input("Skriv et sted (fx 'på månen'): ")

print("\n--- Din skøre historie ---")

# Brug f-strings til nemt at indsætte ordene i historien
historie = f"Den {adjektiv} drage {udsagnsord} altid med sine {navneord}, især når den er {sted}!"

print(historie)
```
Sådan virker det:

Vi indsamler en række ord og gemmer dem i hver deres variabel.

Linjen `historie = f"..."` bruger en f-string. Bogstavet `f` foran citationstegnet lader os indsætte variable direkte i 
teksten ved at bruge `{ }`-klammer. Det er en meget pænere måde at bygge strenge på end at bruge `+`.

Til sidst printes den færdige, og sandsynligvis meget mærkelige, historie.

Prøv selv:

Lav din helt egen historie-skabelon med endnu flere ord, der skal indsættes.

Kan du lave en historie, der fylder flere linjer? (Hint: du kan bruge `\n` til at lave et linjeskift i en string).

## Øvelse 5: Gæt mit hemmelige tal 🔢🤔
Dette er en klassiker og en perfekt introduktion til spil-logik. Computeren "tænker" på et tal, og brugeren skal gætte 
det. Det viser, hvordan kode kan bruge logik og tilfældighed.

Hvad det lærer: At importere `random`-biblioteket, `while`-løkker og `if`/`elif`/`else`-betingelser.

Koden:

```Python
# Importer biblioteket, der kan lave tilfældige tal
import random

# Computeren vælger et hemmeligt tal mellem 1 og 20
hemmeligt_tal = random.randint(1, 20)
print("Jeg tænker på et hemmeligt tal mellem 1 og 20...")

# En løkke, der fortsætter for evigt... indtil vi stopper den
while True:
gæt_tekst = input("Hvad gætter du på? ")
gæt = int(gæt_tekst)

    if gæt < hemmeligt_tal:
        print("For lavt! Prøv igen.")
    elif gæt > hemmeligt_tal:
        print("For højt! Prøv igen.")
    else:
        print(f"Korrekt! Det hemmelige tal var {hemmeligt_tal}. Godt gået!")
        break # Stopper løkken
```
Sådan virker det:

`import random` giver os adgang til en værktøjskasse med funktioner til tilfældighed.

`random.randint(1, 20)` beder computeren finde et tilfældigt heltal mellem 1 og 20.

`while True:` starter en uendelig løkke. Koden inden i den vil køre igen og igen.

`if`/`elif`/`else` er programmets "hjerne". Den tjekker, om gættet er for lavt (`<`), for højt (`>`) eller helt rigtigt 
(`else`).

`break` er nøgleordet, der "bryder ud" af den uendelige løkke, når det rigtige tal er gættet.

Prøv selv:

Kan du ændre koden, så det hemmelige tal er mellem 1 og 100?

Kan du tilføje en tæller, der holder styr på, hvor mange forsøg brugeren har brugt, og printe det til sidst?


## Øvelse 6: Sten, Saks, Papir mod computeren 🗿✂️📄
Denne øvelse lærer, hvordan man kan lade computeren vælge tilfældigt fra en liste og derefter sammenligne resultaterne
baseret på spillets regler.

Hvad det lærer: Lister, `random.choice()`, og mere avanceret `if`/`elif`/`else`-logik med `and` og `or`.

Koden:

```Python
# Importer biblioteket, der kan lave tilfældige valg
import random

# Trin 1: Definer de mulige valg i en liste
mulige_valg = ["sten", "saks", "papir"]

# Trin 2: Få computerens og spillerens valg
computer_valg = random.choice(mulige_valg)
spiller_valg = input("Vælg mellem sten, saks eller papir: ").lower()

# Trin 3: Vis hvad alle har valgt
print(f"\nDu valgte: {spiller_valg}")
print(f"Computeren valgte: {computer_valg}\n")

# Trin 4: Find vinderen med logik
if spiller_valg == computer_valg:
print(f"Det blev uafgjort! I valgte begge {spiller_valg}.")

elif (spiller_valg == "sten" and computer_valg == "saks") or \
(spiller_valg == "saks" and computer_valg == "papir") or \
(spiller_valg == "papir" and computer_valg == "sten"):
print("Tillykke, du vandt! 🎉")

else:
print("Øv, computeren vandt. Bedre held næste gang! 🤖")
```
Sådan virker det:

mulige_valg = `["sten", "saks", "papir"]`: Vi laver en liste (en samling af ting) med de tre mulige træk. Lister skrives
i `[ ]`-klammer.

`random.choice(mulige_valg):` Denne smarte funktion vælger et tilfældigt element direkte fra den liste, vi lige har 
lavet. Det er perfekt til det her spil.

`.lower():` Denne lille funktion bagefter `input()` sørger for, at uanset om brugeren skriver `"Sten"`, `"STEN"` eller 
`"sten"`, bliver det altid lavet om til små bogstaver. Det gør vores `if`-tjek meget nemmere.

Logikken:

Først tjekker vi for det nemmeste: en uafgjort (`if spiller_valg == computer_valg`).

Dernæst kommer den store betingelse (`elif`). Her tjekker vi for alle de måder, spilleren kan vinde på:

Sten slår saks (`and`)

ELLER (`or`)

Saks slår papir (`and`)

ELLER (`or`)

Papir slår sten (`and`)

Hvis ingen af de ovenstående er sande (`else`), er der kun én mulighed tilbage: Computeren har vundet.

Prøv selv:

Hvad sker der, hvis du staver forkert? Kan du tilføje et `if`-tjek i starten, der fortæller brugeren, hvis de har 
skrevet et ugyldigt valg?

Kan du putte hele koden (fra trin 2 og ned) ind i en while `True:`-løkke, så man kan spille igen og igen? (Husk at give
brugeren en mulighed for at skrive `"stop"` for at komme ud af løkken).

For de seje: Kan I lave en scoretavle? Opret to variable, `spiller_score = 0` og `computer_score = 0` før løkken 
starter, og tilføj `+1` til den rigtige vinder i hver runde. Print scoren efter hvert spil.
