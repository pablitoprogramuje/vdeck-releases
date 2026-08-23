# VDeck — wydania

To repozytorium zawiera **wyłącznie gotowe binarki** VDeck (host Windows + klient) publikowane jako
[GitHub Releases](https://github.com/pablitoprogramuje/vdeck-releases/releases) — bez kodu źródłowego. Kod
źródłowy jest w prywatnym repozytorium.

Ten plik (`manifest.json`) jest odczytywany automatycznie przez mechanizm sprawdzania aktualizacji w
aplikacji VDeck (patrz `docs/11-wersjonowanie-i-aktualizacje.md` w głównym repo) — nie edytuj go ręcznie bez
powodu, appki na to reagują.

## Najnowsza wersja

Zobacz [Releases](https://github.com/pablitoprogramuje/vdeck-releases/releases/latest) — każdy release ma swoją
stronę z numerem wersji w notatkach, ale nazwy plików assetów **nie zawierają numeru wersji**, żeby dało się
linkować do "zawsze najnowszej" binarki bez ręcznej aktualizacji linku przy każdym wydaniu:

```
https://github.com/pablitoprogramuje/vdeck-releases/releases/latest/download/<nazwa-pliku>
```

GitHub przekierowuje ten adres na asset o danej nazwie z release'a aktualnie oznaczonego jako „Latest" —
strona WWW i `manifest.json` używają właśnie tej formy, więc nowy release (te same nazwy plików, nowy tag) nie
wymaga aktualizacji żadnego linku, tylko podmiany samych plików.

- **VDeck-Host.zip** — host na Windows (wypakuj, uruchom `VDeck.Host.App.exe`)
- **VDeck-Client-Setup.exe** — instalator klienta Windows (jeden plik, bez uprawnień administratora)
- **VDeck-Client.apk** — klient na Androida (podpisany kluczem debug — zainstaluj bezpośrednio z pobranego
  pliku, poza Google Play)

Klient na iOS nie jest jeszcze publikowany — build wymaga podpisu certyfikatem Apple Developer, którego jeszcze
nie skonfigurowano (patrz `docs/11-wersjonowanie-i-aktualizacje.md` w głównym repo). Android, iOS i Windows to
jeden i ten sam kod źródłowy Fluttera (`mobile/`) — dlatego mają zawsze tę samą wersję.
