# PickACardUI


PickACardUI er et enkelt grafisk korttrekkingsprogram utviklet i C# med WPF.  
Programmet lar brukeren velge hvor mange spillkort som skal trekkes, 
og genererer deretter tilfeldige kort fra en standard kortstokk.

---

Prosjektet er laget som en øvelse i:
- objektorientert programmering i C#
- bruk av statiske metoder
- enkel GUI-programmering med WPF (XAML)
- samspill mellom UI og programlogikk

---

## Funksjonalitet


- Brukeren velger antall kort (1–15) ved hjelp av en slider
- Ved knappetrykk trekkes et tilsvarende antall tilfeldige kort
- Hvert kort består av:
  - én verdi (Ace–King)
  - én farge (Spades, Hearts, Clubs, Diamonds)
- Resultatet vises i en liste i brukergrensesnittet

---

## Prosjektstruktur

<pre> 
PickACardUI/ 
  ├── CardPicker.cs         // Programlogikk for tilfeldig korttrekking 
  ├── MainWindow.xaml       // Definisjon av brukergrensesnittet (WPF) 
  └── MainWindow.xaml.cs    // Kode-behind: kobler UI og logikk ``` 
</pre>

---

## Teknisk beskrivelse

### CardPicker.cs
- Inneholder all logikk for korttrekking
- Bruker én statisk `Random`-instans
- Metoden `PickSomeCards(int numberOfCards)` returnerer et array med kort på tekstform
- Verdier og farger genereres via egne private hjelpemetoder

### MainWindow.xaml
- Definerer UI med:
  - Slider for valg av antall kort
  - Button for å starte korttrekk
  - ListBox for visning av resultat
- Layout bygget med Grid og StackPanel

### MainWindow.xaml.cs
- Håndterer knappetrykk (`Button_Click`)
- Kaller `CardPicker.PickSomeCards`
- Oppdaterer ListBox med de trukne kortene

---

## Hvordan kjøre programmet

### Alternativ 1: Visual Studio (anbefalt)
1. Åpne løsningen (`.sln`) i Visual Studio
2. Sørg for at prosjektet er satt som Startup Project
3. Trykk **Run (F5)**

### Alternativ 2: Ferdig bygget program
Hvis en ferdig `.exe` er tilgjengelig:
1. Last ned build
2. Kjør `PickACardUI.exe`

---

## Eksempel på output

<pre>
Ace of Spades
7 of Hearts
King of Diamonds
3 of Clubs
</pre>

---

## Status

Prosjektet er ferdig og fungerer som tiltenkt.
