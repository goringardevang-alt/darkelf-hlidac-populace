# Dark Elf — Hlídač populace

Userscript pro [darkelf.cz](https://www.darkelf.cz). Na mapě ti ukáže, ve kterých
zemích ti docházejí domy, takže se tam nevejde přírůstek obyvatel.

- 🔴 **červený puntík**: v zemi nemáš žádný volný dům,
- 🟠 **oranžový puntík**: volných domů je méně, než kolik obyvatel přibude příští kolo.

## Instalace

1. Nainstaluj si [Tampermonkey](https://www.tampermonkey.net/) (Chrome, Firefox, Edge).
2. Klikni na **[darkelf-hlidac-populace.user.js](https://raw.githubusercontent.com/goringardevang-alt/darkelf-hlidac-populace/main/darkelf-hlidac-populace.user.js)**. Tampermonkey nabídne instalaci.
3. Otevři ve hře mapu. V řadě tlačítek nad mapou přibude **dům tvé rasy**.

Nic dalšího není potřeba. **Aktualizace si Tampermonkey stahuje sám.** Ručně je
najdeš v Tampermonkey u skriptu pod „Check for updates".

## Použití

- **Klik na dům** hlídání zapne nebo vypne. Po instalaci je vypnuté, potom si skript
  pamatuje poslední nastavení.
- **Najetí myší na dům** vypíše země z obou skupin (i ty, které nejsou na vykreslené
  části mapy) a čas poslední kontroly.
- Podle ikony poznáš stav: šedá znamená vypnuto, průhlednější znamená, že se právě
  načítá, a červený nádech je chyba (důvod je v popisku).

Zapnutý hlídač kontroluje sám:
- po načtení mapy,
- po nákupu domů, verbu nebo propuštění vojska (v kterémkoli okně hry),
- po novém kole, pokud máš skript, který hlídá kola,
- když se vrátíš myší na mapu (nejvýš jednou za 20 s).

## Odkud bere data

- **`auto_domy.asp`** (hromadný nákup domů): volné domy a přírůstek obyvatel. Přírůstek
  skript sám nepočítá, bere ho hotový ze hry.
- **`map_export_json.asp`**: jen kvůli ikoně, aby ukázala dům tvé rasy. Stahuje se
  jednou po přihlášení.

Obě stránky jsou přehledy celého účtu. Skript nikdy neotevírá stránky jednotlivých
zemí, takže ti nepřepne „aktuální zem" ve hře a nákup ani útok neskončí v jiné zemi. Nic se neodesílá mimo hru.

Když máš nainstalované **Dark Elf - Core Utils**, skript ho použije. Bez něj
funguje stejně.

## Chyba nebo nápad

Napiš do [Issues](https://github.com/goringardevang-alt/darkelf-hlidac-populace/issues).
