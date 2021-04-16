# Ovidijus Vaštakas, 2oji užduotis "Pažymių skaičiuoklė"


## Funkcijos
Vartotojas gali/turi:
* Pasirinkti ar generuoti duomenis ir nuskaityti automatiškai ar įvesti studento duomenis pačiam, nuskaityti iš failo
* Pasirinkus įvesti pačiam, prašoma įvesti studento vardą ir pavardę
* Pasirinkti ar žino atliktų namų darbų skaičių (t/n forma)
* Pasirinkti ar namų darbų rezultatus sugeneruoti atsitiktine tvarka ar įvesti pačiam
* Įvesti egzamino rezultatą
* Pasirinkti ar pridėti kitą studentą
* Pasirinkti galutinio pažymio skaičiavimo būdą (vidurkis arba mediana)
* Rikiavimas pagal studento pavardę
* Programa išveda gautus rezultatus panašiu pavidalu: 
```
Vardas      Pavarde            Galutinis Vid.(arba Mediana)
------------------------------------------------------------
Ovidijus    Bulka              5.00
Justas      Vairuotojas        7.49
Antanas     Programuotojas     6.33 
```
## Įdiegimo ir naudojimo instrukcija
* Įdiegimas ir naudojimas
  * Iš skilties "releases" pasirinkti norimą programos versiją ir atsisiųsti
  * Atsisiųstą kodą sukompiliuoti per komandinę eilutę (CMD) arba naudojamu IDE
  ```
  g++ -o programa main.cpp functions.cpp
  ```
  * Paleisti gautą vykdomąjį failą (.exe)
  ```
  ./programa
  Arba tiesiog atidaryti .exe failą tame aplanke kur atsisiuntėte programą
  ```
* Naudojimas
  * Paleidus failą iš pradžių pasirinkti ar norima sugeneruoti duomenis automatiškai ir nuskaityti ar įvesti duomenis pačiam, nuskaityti iš failo
  * Jei pasirinkta generuoti ir nuskaityti automatiškai, pasirenkama kokį kiekį studentų norima generuoti
  * Jei pasirinkta duomenis nuskaityti iš failo galima atsisiųsti kelis šablonus, norimą nuskaityti failą pervadinti į "kursiokai.txt"
  * Pasirinkus įvesti pačiam, įvesti studento vardą ir pavardę
  * Toliau atsakyti į programos užklausas įvedant t- TAIP, n- NE
  * Įvesti namų darbų ar egzamino rezultatus dešimtbalėje sistemoje
  * Pasirinkti ar norime, jog galutinis pažymis būtų skaičiuojamas kaip mediana - t, jei norime jog būtų išvestas vidurkis - n

## Programos veikimo sparta

|               | 1000     | 10000    | 100000   | 1000000  | 10000000 |
| ------------- |----------| ---------|----------|----------|----------|
| **Vector**    |          |          |          |          |          |
| Nuskaitymas   | 0.018s   | 0.109s   | 1.19s    | 9.42s    | 69.171s  |
| Rūšiavimas    | 0.134s   | 0.01s    | 0.071s   | 0.856s   | 8.964s   |
| **List**      |          |          |          |          |          |
| Nuskaitymas   | 0.014s   | 0.148s   | 1.232s   | 7.529s   | 87.119s  |
| Rūšiavimas    | 0.001s   | 0.009s   | 0.079s   | 0.661s   | 6.954s   |
| **Deque**     |          |          |          |          |          |
| Nuskaitymas   | 0.012s   | 0.102s   | 1.113s   | 8.552s   | 87.766s  |
| Rūšiavimas    | 0.001s   | 0.009s   | 0.071s   | 0.606s   | 6.246s   |

Specifikacija: CPU I7-7700HQ 4Core 2.8GHz, RAM DDR4 2400MHz 16GB, SSD 

## Programos veikimo spartos dvejomis strategijomis palyginimas

|                      | 1000     | 10000    | 100000   | 1000000  | 10000000 |
| -------------------- |----------| ---------|----------|----------|----------|
| **Vector**           |          |          |          |          |          |
| Dviejų konteinerių   | 0.152s   | 0.119s   | 1.261s   | 10.276s  | 78.135s  |
| Vieno konteinerio    | 0.07s    | 5.404    | 0.071s   | 0.856s   | 8.964s   |
| **List**             |          |          |          |          |          |
| Dviejų konteinerių   | 0.015s   | 0.157s   | 1.311s   | 8.19s    | 94.073s  |
| Vieno konteinerio    | 0.013s   | 0.123s   | 1.281s   | 12s      | 6.954s   |
| **Deque**            |          |          |          |          |          |
| Dviejų konteinerių   | 0.013s   | 0.111s   | 1.184s   | 9.158s   | 94.012s  |
| Vieno konteinerio    | 0.038s   | 2.41s    | 0.071s   | 0.606s   | 6.246s   |

## Versijos
[v0.1](https://github.com/OvidijusV/2Uzduotis-OOP/tree/v0.1) Vardo, pavardės ir pažymių įvestis, atsakymai į programos užklausas, galutinio pažymio skaičiavimas(vidurkis arba mediana)\
[v0.2](https://github.com/OvidijusV/2Uzduotis-OOP/tree/v0.2) Pridėta galimybe nuskaityti rezultatus iš failo, pridėtas automatinis rikiavimas pagal pavardes\
[v0.3](https://github.com/OvidijusV/2Uzduotis-OOP/tree/v0.3) Atliktas kodo reorganizavimas, pagrindinis failas išskirtas į antraščių ir funkcijų failą, pridėti keli pranešimai nepavykus įvykdyti programos\
[v0.4](https://github.com/OvidijusV/2Uzduotis-OOP/tree/v0.4) Pridėtas automatinis duomenų generavimas ir nuskaitymas iš failo, studentų rūšiavimas pagal galutinį vidurkį ir išvedimas į du atskirus failus\
[v0.5](https://github.com/OvidijusV/2Uzduotis-OOP/tree/v0.5) Pridėta programos spartos matavimo galimybė naudojant vector, list arba deque konteinerius

