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
  - [Wymagania i konfiguracja SDL2](#wymagania-i-konfiguracja-sdl2)

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

---

## Wymagania i konfiguracja SDL2

Projekt został przygotowany do pracy z biblioteką **SDL2** zainstalowaną lokalnie w systemie. Zalecanym sposobem instalacji SDL2 na macOS jest użycie menedżera pakietów **Homebrew**.

Do poprawnej kompilacji projektu wymagane są:

- kompilator C/C++, np. `clang++`,
- biblioteka **SDL2**,
- narzędzie `sdl2-config`,
- środowisko uruchomieniowe zgodne z SDL2,
- opcjonalnie Visual Studio Code z przygotowaną konfiguracją w katalogu `.vscode`.

Zalecana instalacja SDL2 na macOS:

~~~bash
brew install sdl2
~~~

Projekt korzysta z systemowej instalacji SDL2, a nie z bibliotek dołączonych bezpośrednio do repozytorium. W praktyce oznacza to, że podczas kompilacji używane są ścieżki oraz flagi kompilatora zwracane przez polecenie:

~~~bash
sdl2-config --cflags --libs
~~~

Takie rozwiązanie jest bardziej stabilne i ogranicza problemy kompilacyjne wynikające z niezgodności wersji bibliotek, architektury procesora lub ścieżek do plików nagłówkowych.

W repozytorium mogą znajdować się katalogi lub pliki związane z SDL2, środowiskiem Code::Blocks albo wcześniejszymi próbami konfiguracji projektu. Należy traktować je jako **artefakty projektu** lub pozostałości konfiguracyjne, a nie jako główne źródło biblioteki wykorzystywanej podczas budowania programu.

Aktualny sposób uruchamiania projektu zakłada korzystanie z SDL2 zainstalowanego przez Homebrew. Dzięki temu konfiguracja jest prostsza, bardziej przenośna na macOS i mniej podatna na typowe błędy, takie jak:

- brak pliku nagłówkowego `SDL.h`,
- nieprawidłowe ścieżki include,
- konflikt między różnymi wersjami SDL,
- problem z linkowaniem biblioteki,
- niezgodność architektury bibliotek, np. Apple Silicon vs Intel.

Przykładowa komenda kompilacji:

~~~bash
mkdir -p build
clang++ -std=c++17 -g NAZWA_PLIKU.cpp -o build/NAZWA_PROGRAMU $(sdl2-config --cflags --libs)
~~~

Przykład dla konkretnego laboratorium:

~~~bash
mkdir -p build
clang++ -std=c++17 -g GK2026-LabX.cpp -o build/GK2026-LabX $(sdl2-config --cflags --libs)
~~~

Uruchomienie programu:

~~~bash
./build/GK2026-LabX
~~~

W powyższych komendach należy zastąpić `GK2026-LabX` właściwą nazwą projektu, np. `GK2026-Lab2`, `GK2026-Lab3` albo `GK2026-Lab4`.