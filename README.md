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

## Aktualizácie

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
