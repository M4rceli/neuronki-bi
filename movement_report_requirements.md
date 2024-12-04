# Wymagania do raportu dotyczącego ruchu towarów w magazynach

Raport ma wspierać analizę ruchu towarów w magazynach oraz transferów między lokalizacjami, wykorzystując dane z tabeli `Fact.Movement` i powiązanych wymiarów. Poniżej przedstawiamy szczegółowe wymagania biznesowe i funkcjonalne.

---

## 1. Kluczowe potrzeby

### a) Informacje o ruchu towarów
- Data transakcji dotyczących przepływu towarów (`Date Key`).
- Typ transakcji (`Transaction Type Key`), np. przyjęcie, wydanie, przesunięcie wewnętrzne.
- Ilość przemieszczonych towarów (`Quantity`):
  - Pozytywne wartości dla przyjęć.
  - Negatywne wartości dla wydań.
- Identyfikacja zamówień i dostaw:
  - Numer faktury (`WWI Invoice ID`).
  - Numer zamówienia zakupu (`WWI Purchase Order ID`).

### b) Analiza transferów między lokalizacjami
- Szczegółowe informacje o dostawcach (`Supplier Key`) oraz klientach (`Customer Key`), jeśli dotyczy.
- Produkty podlegające ruchowi (`Stock Item Key`) i ich charakterystyka, np.:
  - Marka.
  - Opakowanie.
  - Wielkość.
- Porównanie ruchu towarów między różnymi lokalizacjami, z możliwością wizualizacji przepływów.

### c) Podział transakcji według typów
- Analiza ilości i wartości transakcji według typu (np. przyjęcie, wydanie, transfer).
- Identyfikacja najczęstszych typów ruchów towarów.

### d) Efektywność zarządzania zapasami
- Analiza trendów w ruchach towarów w różnych okresach (miesiąc, kwartał, rok).
- Identyfikacja produktów o największej częstotliwości ruchów magazynowych.
- Wskaźniki dotyczące zgodności z planowanymi terminami transakcji.

### e) Podsumowanie według dostawców i klientów
- Kluczowi dostawcy realizujący największy wolumen dostaw.
- Klienci odbierający największą liczbę towarów.

---

## 2. Funkcjonalności raportu

- **Filtrowanie danych**:
  - Daty.
  - Typy transakcji.
  - Produkty.
  - Dostawcy.
  - Lokalizacje.
- **Forma prezentacji danych**:
  - Wykresy (np. słupkowe, liniowe) i tabele ułatwiające analizę.
  - Wizualizacja przepływu towarów między lokalizacjami za pomocą map lub diagramów przepływu.
- **Eksport raportu**:
  - Możliwość eksportu do formatu Excel lub PDF.

---