# PrototypeKit

Deze prototypekit is geschreven ter ondersteuning van het bouwen van de verschillende prototypes voor deelvraag 8 van het onderzoek 'Machine learning voor de huisarts'.  Door de prototypes op de manier zoals in deze kit beschreven te bouwen krijgen alle prototypes dezelfde structuur. Hierdoor wordt het testen van alle prototypes makkelijker.



## Repository

Elk prototype wordt bewaard in een eigen repository binnen de organization HanNotSMachineLearning op GitHub. 

### Aanmaken repository

Volg de volgende stappen om een repository aan te maken voor het nieuwe prototype:

1. Maak een nieuw repository aan binnen de organization HanNotSMachineLearning en zorg hierbij voor het volgende:

   1. Geeft de repository een naam waarbij het duidelijk is dat het gaat om een prototype van een specifiek machine learning algoritme, bijvoorbeeld `DecisionTreePrototype ` of `DecisionForestPrototype`.
   2. Selecteer `HanNotSMachineLearning`  als owner.
   3. Selecteer de optie dat er een README.md wordt aangemaakt.
   4. Een .gitignore hoeft niet ingesteld te worden.
   5. Selecteer dat het repository valt onder de MIT License.

2. Voeg de volgende topics toe aan de repository: `deelvraag8` & `prototype`

3. Zorg ervoor dat het repository de volgende bestandsstructuur heeft (je kan hiervoor het een en ander uit dit repository kopiëren):

   ```
   repo
   |   README.md
   |   prototype.py
   |   requirements.txt
   |
   |---Data
   |	|   Dataset.csv
   ```

4. De repository is nu aangemaakt en ingericht!



## Prototype

Elk machine learning algoritme werkt op een andere manier, dus elk prototype werkt op een andere manier. Het is dus niet mogelijk om al helemaal vast te leggen hoe de applicatie er uit moet gaan zien.  Zorg  er in ieder geval voor dat de volgende zaken er in zitten:

- Maakt gebruik van tensorflow als machine learning framework.
- prototype.py is het hoofd bestand van de applicatie, door `python prototype.py` uit te voeren moet de applicatie dus opstarten.
- Maakt gebruik van de algemene dataset.
- Toont de accuraatheid van het getrainde algoritme.
- Toont de tijd die het kost om tot de voorspelling te komen.



#### Packages

Zorg ervoor dat je alle packages die je gebruikt toevoegd aan `requirements.txt` zodat alles in een keer te installeren is zoals in de documentatie template beschreven is. Zie het onderstaande voorbeeld:

```txt
tensorflow
csv
```

 

```
!-- LETOP --!
In deze prototypekit zitten al een aantal packages in requirements.txt van packages waarvan uit wordt gegaan dat deze in alle prototypes gebruikt worden.
Zorg ervoor dat deze er ook in zitten bij het prototype.
```



## Codevoorbeelden

Sommige onderdelen van het prototype worden waarschijnlijk in meerdere prototypes gebruikt, denk bijvoorbeeld aan het inlezen van de testdata. Om tijd te besparen staan een aantal van die functionaliteiten hieronder uitgewerkt.



### CSV inlezen

De onderstaande code leest het bestand met de dataset in en zet het om in een twee dimensionale array.

```python
import csv

with open('Data/Dataset.csv', 'r') as DataFile:
	dataset = list(csv.reader(DataFile))
```



### User input

Door middel van de onderstaande code is het mogelijk om via de console user input binnen te krijgen.

```python
userInput = input("")
```



## Documentatie

Om de documentatie van de verschillende prototypes consistent te houden moet deze voldoen aan het template dat terug te vinden is in deze kit. 

### Opstellen 

Volg voor het opstellen van de documentatie het volgende stappenplan:

1. Kopieer alles uit `template.md` naar `README.md` in het repository van het prototype. Dit is de basis voor de documentatie van het prototype.
2. Breid het hoofdstuk `Algoritme` uit. In dit hoofdstuk moet globaal duidelijk worden wat het algoritme is en hoe het werkt. Je kan hier waarschijnlijk ook stukken uit het onderzoeksrapport voor gebruiken.
3. Het hoofdstuk `Trainingsdata ` is in principe af. Het hoeft alleen uitgebreid te worden wanneer er wijzigingen aan de dataset plaatsvinden om 
4. Het hoofdstuk `Trainingsdata ` en `Afhankelijkheden` zijn als het goed is gelijk voor alle prototypes dus hier hoeft niks aangepast te worden.
5. Ook het hoofdstuk `Installatie` is grotendeels hetzelfde voor alle prototypes. Het enige dat in dit hoofdstuk verschillend kan zijn is de lijst met packages die door het prototype gebruikt worden. Werk deze lijst bij zodat het overeen komt met de door het prototype gebruikte packages.
6. Het hoofdstuk `Opstarten` hoeft alleen aangepast te worden wanneer het niet mogelijk is het prototype op de standaard gedefineerde manier op te starten.
7. In het laatste hoofstuk `Code` moet de code van het prototype beschreven en uitgelegd worden. Hieruit moet duidelijk worden wat bepaalde stukken code doen. Denk hierbij ook aan het toevoegen van stukken code om dit duidelijk te maken.
8. De documentatie van het prototype is nu up-to-date. Vergeet niet om het weer bij te werken als je iets veranderd aan het prototype.