# Budapest · 25–28 listopada 2026
Mobilny przewodnik na podstawie dostarczonego planu z 10.11.2026. Czysty HTML/CSS/JS, bez budowania i bez backendu.

Funkcje: cztery dni planu, checklisty i postęp, następny punkt, filtrowanie, mapy, oficjalne linki biletowe, notatki, lokalny adres noclegu, eksport/import, druk wszystkich dni i cache offline.

Dane użytkownika przechowuje localStorage. Nie ma automatycznej synchronizacji między urządzeniami. Eksport JSON zawiera notatki i wpisany adres noclegu — traktuj go jako prywatny. Publiczne pliki nie zawierają adresu noclegu ani danych rezerwacji. Godziny i informacje są z planu, bez ponownej weryfikacji organizatorów.

## Lokalnie
`python3 -m http.server 8765` w katalogu projektu, potem http://localhost:8765.

## GitHub Pages
Wgraj zawartość tego katalogu do nowego repozytorium z gałęzią `main`. W Settings → Pages wybierz Source: GitHub Actions. Workflow `.github/workflows/pages.yml` publikuje stronę po pushu. Alternatywnie wybierz Deploy from a branch → main → / (root); żadne budowanie nie jest potrzebne.

Strona offline działa po pierwszym pełnym otwarciu przez HTTPS (lub localhost). Zewnętrzne mapy, bilety i fonty wymagają internetu; bez fontów strona korzysta z fontów systemowych. W nowej wersji zmień nazwę cache w sw.js. Bez geolokalizacji — Google Maps może samodzielnie poprosić o lokalizację.

## Aktualizacja 12.11.2026
Plan dla dwojga: spokojne wieczory, dziewięć propozycji jedzenia/kawy/deserów, filtry według dnia i lokalne zapisy „Chcemy spróbować”. Dane lokali i linki źródłowe w food.js. Środa uwzględnia zameldowanie od 15:00 oraz przechowanie 1 walizki i 2 plecaków. Przechowalnia, stoliki i bilety pozostają propozycjami bez rezerwacji. Nowe pozycje zachowują stare identyfikatory planu; usunięty punkt wieczorny nie jest zaliczany do nowej propozycji romantycznej.

## Street food i widoki
Dodano Mama Goulash, Retró Lángos Vécsey, Simon’s Burger Flagship oraz Pizza Me Astoria. Zakładka Widoki zawiera 7 miejsc z dopasowaniem do dni, pory światła, filtrami i lokalnie zapisywaną listą. Źródła: oficjalne strony lokali, Budapest Info i strona bazyliki. Powiązania miejsc z planem są w food.js i views.js. Dane sprawdzono 12.11.2026; rekomendowane godziny są propozycjami, nie rezerwacją.
