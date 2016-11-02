# hyph_pl

licencja: Public Domain z wymogiem zachowania tekstów z nagłówków.

Plik hyph_pl.dic tylko dla ADE
==============================
(czytniki i PC) (data 15 I 2105)
 
### Czytniki e-ink PocketBook ###
(sprawdzone na fv 4.4 i 5.x)

W czytnikach PocketBook umieść plik hyph_pl.dic w 
`pamiećwewnętrzna:\system\fonts\adobe\hyphenDicts\`
folder "system" jest ukryty, wiec pod windows musisz trochę pokombinować by 
go zobaczyć  google: windows (wersja) pokaż ukryte foldery

### Czytniki e-ink Onyx ###
(Onyx Reader i Onyx Neo Reader)

`/system/adobe/resources/hyphenDicts`

Namawiam jednak byś wypróbował ten specjalny, i napisał czy działa.

(wymaga jakiegoś managera plików i roota)

### Czytniki e-ink inkBook ###
(InkBOOK: ONYX, Obsidian, 8; także Bouye i Icarus)

Wgraj do `/system/adobe/resources/hyphenDicts` jak nie działa to użyj _vanilla/hyph_pl.dic_ 

Wymaga roota

### ADE PC (komputer) ###
Jest duża szansa że musisz umieścić plik tutaj
`c:\Program Files (x86)\Adobe\Adobe Digital Editions 3.0\resources\hyphenDicts\`
bądź
`c:\Program Files (x86)\Adobe\Adobe Digital Editions 4.0\resources\hyphenDicts\`

### Inne czytniki na silniku ADE (RMSDK) ###
poszukaj na czytniku katalogu hyphenDicts w nim powinny być plik hyph_en.dic 
i kilka innych podobnie nazwanych, wgraj tam hyph_pl.dic dla PB, 
jeśli czytnik po otwarciu polskich książek będzie się wieszał (lub wychodził do 
ekranu powitalnego) skorzystaj z _vanilla/hyph_pl.dic_.

### appki typowo androidowe dla tabletów opartych na ADE ###
"/data/data/" może być jakimś innym katalogiem

Wszystkie poniższe wymagają praw roota

### mantano reader ###
(RMSDK 9.3.3 2013Nov01)

plik _mantano.reader/libhyph_pl.so_ wgrać do 
`/data/data/com.mantano.reader.android.lite/lib/`

### obrrey PocketBook ###
(RMSDK-9.3 .3?)

wgraj plik dla pb do 
`/data/data/com.obreey.reader/app_resources/hyphenDicts/`


Technikalia i po co ten plik a nie inny:
========================================
ADE dla czytników ma przykrą właściwość traktowania wielu znaków (twarda spacja, 
cudzysłowy) jako znaki należące do wyrazu go otaczającego - zamiast potraktować
je jako znaki białe. Przez takie zachowanie powstają błędne podziały, pomimo 
poprawnych reguł.

Plik bierze pod uwagę twarde spacje które polskie wydawnictwa lubują się 
wstawiać, by przeciwdziałać rozdzieleniu spójnika (i, do, ...) od wyrazu po nim,
tzw wiszące spójniki.


ku pamięci:
parzysta - zakaz; nieparzysta - przenoszenie; wygrywa wyższa cyfra


Ar't

PS W paru bardzo rzadkich sytuacjach podział nadal jest błędny, niestety wynika 
to z faktu traktowania przez ADE wielu znaków tj. nawiasy, średniki, cudzysłowy, itp 
jako części wyrazu z którym sąsiadują (zamiast jako znaki białe).

