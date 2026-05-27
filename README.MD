# GK2026-Lab2

Projekt laboratoryjny z przedmiotu **Grafika komputerowa**.  
Repozytorium zawiera program napisany w C/C++ z użyciem biblioteki **SDL2**, którego celem jest demonstracja podstawowych operacji przetwarzania obrazu rastrowego, takich jak konwersja do skali szarości, progowanie oraz dithering.

Autor: **Kacper Lelito**  
Przedmiot: **Grafika komputerowa**  
Laboratorium: **Lab 2**

---

## Spis treści

- [GK2026-Lab2](#gk2026-lab2)
  - [Spis treści](#spis-treści)
  - [Opis projektu](#opis-projektu)
  - [Funkcjonalności](#funkcjonalności)
  - [Sterowanie](#sterowanie)
    - [Wczytywanie obrazów](#wczytywanie-obrazów)
    - [Uruchamianie funkcji](#uruchamianie-funkcji)
  - [Struktura projektu](#struktura-projektu)

---

## Opis projektu

Program służy do wizualizacji wybranych metod przetwarzania obrazu rastrowego.  
Aplikacja otwiera okno graficzne SDL2, umożliwia wczytanie przykładowych obrazów BMP oraz uruchamianie kolejnych funkcji przetwarzających obraz za pomocą klawiszy.

Projekt obejmuje między innymi:

- odczyt koloru pojedynczego piksela,
- zapis koloru pojedynczego piksela,
- konwersję obrazu RGB do skali szarości,
- progowanie obrazu czarno-białego,
- dithering z użyciem tablic Bayera,
- dithering metodą Floyd–Steinberga,
- progowanie składowych RGB.

---

## Funkcjonalności

Program zawiera zestaw funkcji uruchamianych z klawiatury:

| Funkcja | Opis |
|---|---|
| `Funkcja1()` | Konwersja obrazu do skali szarości oraz proste progowanie czarno-białe |
| `Funkcja2()` | Dithering uporządkowany z użyciem tablicy Bayera 2x2 |
| `Funkcja3()` | Dithering uporządkowany z użyciem tablicy Bayera 4x4 |
| `Funkcja4()` | Dithering metodą Floyd–Steinberga |
| `Funkcja5()` | Progowanie każdej składowej RGB osobno |
| `Funkcja6()` | Kolorowy dithering z użyciem tablicy Bayera 4x4 |
| `Funkcja7()` | Miejsce na kolejną funkcję laboratoryjną |
| `Funkcja8()` | Miejsce na kolejną funkcję laboratoryjną |
| `Funkcja9()` | Miejsce na kolejną funkcję laboratoryjną |

---

## Sterowanie

### Wczytywanie obrazów

| Klawisz | Obraz |
|---|---|
| `A` | `obrazek1.bmp` |
| `S` | `obrazek2.bmp` |
| `D` | `obrazek3.bmp` |
| `F` | `obrazek4.bmp` |
| `G` | `obrazek5.bmp` |
| `H` | `obrazek6.bmp` |

### Uruchamianie funkcji

| Klawisz | Działanie |
|---|---|
| `1` | Uruchamia `Funkcja1()` |
| `2` | Uruchamia `Funkcja2()` |
| `3` | Uruchamia `Funkcja3()` |
| `4` | Uruchamia `Funkcja4()` |
| `5` | Uruchamia `Funkcja5()` |
| `6` | Uruchamia `Funkcja6()` |
| `7` | Uruchamia `Funkcja7()` |
| `8` | Uruchamia `Funkcja8()` |
| `9` | Uruchamia `Funkcja9()` |
| `B` | Czyści ekran na czarno |
| `ESC` | Zamyka program |

---

## Struktura projektu

```text
GK2026-Lab2/
├── .vscode/              # Konfiguracja Visual Studio Code
├── SDL2/                 # Pliki/biblioteki SDL2 używane w projekcie
├── bin/Debug/            # Katalog wynikowy środowiska Code::Blocks
├── build/                # Katalog kompilacji dla VS Code/macOS
├── GK2026-Lab2.cpp       # Główny plik źródłowy programu
├── GK2026-Lab2.cbp       # Plik projektu Code::Blocks
├── GK2026-Lab2.depend    # Plik zależności Code::Blocks
├── GK2026-Lab2.layout    # Układ projektu Code::Blocks
├── obrazek1.bmp          # Przykładowy obraz testowy
├── obrazek2.bmp          # Przykładowy obraz testowy
├── obrazek3.bmp          # Przykładowy obraz testowy
├── obrazek4.bmp          # Przykładowy obraz testowy
├── obrazek5.bmp          # Przykładowy obraz testowy
└── obrazek6.bmp          # Przykładowy obraz testowy