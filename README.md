# 🚢 Logistyka Cierpienia: Analiza Danych Transatlantyckiego Handlu Niewolnikami

> **Projekt Data Science (EDA & Storytelling)** > Analiza historyczna oparta na zbiorze danych *Slave Voyages* (1500-1900).

## 📋 O Projekcie
Celem tego projektu nie jest tylko analiza liczb, ale opowiedzenie tragicznej historii poprzez dane. Projekt skupia się na **Exploratory Data Analysis (EDA)**, czyszczeniu brudnych danych historycznych oraz weryfikacji powszechnych przekonań dotyczących transportu niewolników (tzw. *Middle Passage*).

Analiza odpowiada na pytania:
* Jakie czynniki najbardziej wpływały na śmiertelność podczas rejsu?
* Czy "upchanie" ludzi na statku (zagęszczenie) było główną przyczyną zgonów?
* Jak wyglądały główne szlaki logistyczne tego procederu?

## 🛠️ Technologie i Narzędzia
* **Język:** Python 3.x
* **Biblioteki:**
    * `Pandas` & `NumPy`: Manipulacja danymi, czyszczenie (Data Cleaning).
    * `Matplotlib` & `Seaborn`: Wizualizacja statystyczna (Heatmapy, Scatter plots).
    * `GeoPandas`: Wizualizacja geoprzestrzenna (Mapowanie tras).

## 📊 Kluczowe Wnioski (Insights)

Po wyczyszczeniu danych (z 36 000 do ok. 15 000 wiarygodnych rekordów) i przeprowadzeniu analizy statystycznej, wyciągnięto następujące wnioski:

1.  **Śmiertelność:** Średnio **14.5%** zaokrętowanych ludzi nie przeżywało podróży. Istniały rejsy ze 100% śmiertelnością.
2.  **Czas a Śmiertelność:** Istnieje wyraźna dodatnia korelacja (**0.35**) między długością podróży a śmiertelnością. Im dłuższy rejs (rekord to ponad 300 dni), tym mniejsze szanse na przeżycie.
3.  **Mit Zagęszczenia:** Analiza wykazała **brak korelacji (-0.06)** między zagęszczeniem (ilość osób na tonę wyporności) a śmiertelnością. Sugeruje to, że główną przyczyną zgonów były epidemie (niezależne od tłoku) oraz długość trwania rejsu, a nie sam ścisk w ładowniach.
4.  **Geografia:** Głównymi odbiorcami nie była Ameryka Północna, lecz **Karaiby (Jamajka, Saint-Domingue)** oraz **Brazylia**.

## 📈 Wizualizacje

### 1. Mapa Głównych Szlaków Handlowych
Analiza geoprzestrzenna tras o największym natężeniu ruchu (TOP 10).
*(Tu wstaw swój zrzut ekranu z mapą, np. map_routes.png)*
`![Mapa Tras](map_routes.png)`

### 2. Macierz Korelacji
Badanie wpływu czasu i zagęszczenia na śmiertelność.
*(Tu wstaw swój zrzut ekranu z heatmapą)*
`![Heatmapa](heatmap.png)`

## ⚙️ Proces Analizy (Metodologia)

1.  **Data Cleaning:**
    * Usunięcie rekordów z brakującymi datami.
    * Filtracja błędnych danych ("sanity check"): usunięcie rejsów z ujemnym czasem trwania, zerowym tonażem lub zerową liczbą pasażerów.
2.  **Feature Engineering:**
    * Obliczenie `Mortality Rate` (Śmiertelność %).
    * Obliczenie `Density` (Osoby / Tonaż).
3.  **Analiza Statystyczna:** Wykorzystanie korelacji Pearsona do zbadania zależności między zmiennymi.
4.  **Geocoding:** Przypisanie współrzędnych geograficznych do historycznych nazw regionów (np. *Bight of Biafra*, *Saint-Domingue*) w celu stworzenia mapy przepływów.

## 📚 Źródło Danych
Dane pochodzą z projektu [SlaveVoyages.org](https://www.slavevoyages.org/), który gromadzi informacje o dziesiątkach tysięcy rejsów transatlantyckich.

---
*Autor: [Twoje Imię]*
