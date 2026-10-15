# Luma Capture

Moderný editor snímok obrazovky pre Windows 10 (2004+) a Windows 11, x64.

## Stiahnuť

[Stiahnuť Luma.exe](https://github.com/enthilza/Luma-Screenshots/releases/latest/download/Luma.exe) · [Všetky vydania](https://github.com/enthilza/Luma-Screenshots/releases)

Samostatné EXE obsahuje .NET runtime. Stačí ho uložiť do priečinka, kde máš právo zapisovať, a spustiť.

## Ovládanie

- **Ctrl+Alt+S:** nový obdĺžnikový výrez obrazovky.
- **Ctrl+Alt+D:** snímka vybraného monitora. Skratky sa dajú zmeniť v Nastaveniach.
- Šípky, obdĺžniky, elipsy, pero, text, farby a presúvateľné objekty; Ctrl+Z/Ctrl+Y.
- **Výber oblasti (V):** po pustení myši sa výrez vrátane anotácií skopíruje do schránky; rámček krátko zasvieti a zmizne. Pri chybe kopírovania výber zostane.
- **Shift pri pustení myši:** ponechať výber na uloženie alebo orezanie.
- **Ctrl+V:** vložiť obrázok zo schránky ako presúvateľný objekt do aktuálnej snímky. **Ctrl+Shift+V:** vložiť do novej záložky.
- Najviac **20 záložiek**. Pri otvorení ďalšej sa najstaršia automaticky zatvorí **bez uloženia**, aj s úpravami.
- Zavretie okna skryje aplikáciu k hodinám; pravé tlačidlo na ikone → Ukončiť Luma.

## Prehliadač obrázkov

Dvojklik na asociovaný obrázok otvorí prehliadač bez rámu s jemným tieňom a priehľadným panelom. Neotvára editor ani nepridáva záložky.

- Názov súboru a počítadlo; šípky na klávesnici aj paneli prechádzajú celý priečinok.
- Triedenie podľa názvu (prirodzene 1, 2, 10) alebo vytvorenia, vzostupne/zostupne.
- Pamätá si monitor; po presunutí a pustení myši sa vycentruje na novom monitore. Obrázok s panelom sa zmestí do 90 % pracovnej plochy, so zachovanými proporciami.
- Dvojklik alebo Enter otvorí obrázok v editore; Esc zatvorí iba prehliadač.
- Otočenie o 90° a vodorovné zrkadlenie sa automaticky uložia. Späť / Ctrl+Z obnoví presný predchádzajúci súbor. História platí počas otvorenia prehliadača, aj po prechode medzi obrázkami.
- JPEG používa EXIF orientáciu bez prekompresie; PNG, BMP a jednostranový TIFF bezstratové otočenie pixelov. GIF sa prehráva bez možnosti prepísania; viacstranový TIFF ukazuje prvú stranu bez úprav. ICO je iba na prezeranie.
- Podporované prípony: JPG/JPEG/JPE, PNG, BMP, GIF, TIF/TIFF, ICO. WebP/HEIC zatiaľ nie.

V Nastaveniach klikni **Otvárať obrázky v Lume…**, potom potvrď predvolené formáty vo Windows. Prehliadač otvoríš aj ikonou obrázka hore alebo cez menu pri hodinách. Registrácia neobchádza ochranu Windows UserChoice.

## Aktualizácie

Od verzie 1.4.1 sa kontrola, sťahovanie s percentami a overovanie zobrazujú v samostatnom okne. Sťahovanie možno zrušiť; sieť a kontrolný súčet neblokujú obsluhu okna. Nový priebeh sa prejaví až po nainštalovaní 1.4.1, pri ďalšom spustení aktualizácie.

Tlačidlo **Aktualizovať** v editore alebo rovnaká položka v menu pri hodinách vyhľadá najnovšie stabilné vydanie. Aplikácia overí digitálny podpis popisu vydania (RSA/SHA-256) voči zabudovanému verejnému kľúču a následne SHA-256 aj veľkosť EXE. Pred výmenou a reštartom sa opýta; neuložené záložky treba najprv uložiť.

Prvý prechod zo starších verzií bez aktualizátora vyžaduje manuálne nahradenie EXE. Ďalšie vydania možno inštalovať priamo z aplikácie.

Každé vydanie obsahuje `Luma.exe`, `SHA256SUMS.txt`, `update.json` a `update.sig`. Kontrolný súčet možno manuálne porovnať príkazom PowerShellu:

```powershell
Get-FileHash .\Luma.exe -Algorithm SHA256
```

Samotný kontrolný súčet overuje zhodu dát. Pôvod aktualizácie aplikácia overuje podpisom; nejde o Windows Authenticode podpis EXE a Windows môže pri prvom spustení zobraziť SmartScreen.

## Súkromie

Obrázky sa spracúvajú lokálne. Pri bežnom snímaní sa automaticky neukladajú na disk. Kontrola aktualizácií kontaktuje GitHub; obrázky sa pri nej neodosielajú. Nastavenia sú v `%LOCALAPPDATA%\LumaCapture`.

Tento repozitár obsahuje distribučné súbory a informácie o vydaniach.


