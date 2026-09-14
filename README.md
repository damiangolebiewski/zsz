# RUSZKOWSKI: ZDAJ ALBO POWTARZAJ

Gra na Dzień Programisty 2026 w ZSZ im. Jana Ruszkowskiego w Pułtusku.

## Pliki

- `index.html` — cały kod, style i dźwięki, bez zależności.
- `assets/damian.png`
- `assets/uczen.png`
- `assets/logo.png`
- `assets/bg.png`

## Uruchomienie lokalne

Rozpakuj paczkę i otwórz `index.html` w przeglądarce. Nie potrzeba serwera ani instalacji. Brakujące grafiki zastępują kształty. Pierwsza interakcja uruchamia dźwięk.

## GitHub Pages

Wgraj `index.html` i folder `assets/` do głównego katalogu repozytorium. Wybierz Settings → Pages → Deploy from branch → main → / (root) → Save. Poczekaj na zakończenie publikacji i otwórz adres pokazany przez GitHub.

## Sterowanie

- ← / → albo A / D — ruch.
- Enter — start / dalej / zatwierdzenie postaci; także powrót z pauzy.
- P — pauza; R — restart klasy; M — wyciszenie.
- Telefon: przytrzymaj lewą lub prawą połowę canvasu. Dotknij karty, aby wybrać postać. Dotknięcie pozostałych menu działa jak Enter.
- Przyciski w prawym górnym rogu: pauza i dźwięk. Utrata aktywności okna pauzuje grę.

## Zasady i konfiguracja

Promocja wymaga 8 piątek w Klasie 1, 12 w Klasie 2 i 16 w Klasie 3. Trzy jedynki oznaczają powtarzanie klasy. Logo daje 5 sekund tarczy i magnesu. Sprawdzian liczy się jak jedynka. Każda piątka daje 100 punktów, sekunda aktywnej gry 1 punkt, klasa bez jedynki 500 punktów premii. Powtórka lub R cofają punkty do początku klasy. Rekord dotyczy ukończonych rozgrywek i pozostaje w pamięci do odświeżenia strony.

Parametry trzech klas są w tabeli `LEVELS` na początku skryptu. Prędkości i promień magnesu używają logicznego canvasu 1280×720, skalowanego proporcjonalnie do ekranu.

## Stan grafiki ucznia i weryfikacja

Dołączony `uczen.png` ma niestety 1254×1254 i zapisane tło z szachownicą (RGB), mimo żądania przezroczystości i próby poprawki. Przed pokazem należy podmienić go na PNG 1024×1024 z prawdziwym kanałem alfa. Kod nie wymaga zmiany. Pozostałe nazwy plików zostały dopasowane do wymaganej struktury.

Przeszły testy składni i logiki: przejścia klas, reset, rekord, booster, ruch 60/120 Hz oraz wywołania renderowania bez obrazów. Pełny test wizualny i dźwiękowy w rzeczywistej przeglądarce, w tym iOS, pozostaje do wykonania.

## Trudniejszy wariant

Oceny spadają o 20% szybciej, a odstępy między nimi są o 15% krótsze. W Klasie 3 szansa skosu wynosi 70%, a 35% złych ocen to sprawdziany. HUD pokazuje liczbę piątek i cel bieżącej klasy.
