% $Id: readme.txt,v 1.0 2005-04-15 11:00:52+02 myszka Exp myszka $
-------------------------------------------------------------
Dodatki do pakietu beamer udaj¹ce prezentacjê zgodn¹ z Ksiêg¹
Logotypu
-------------------------------------------------------------
Wersja 0.05 (alfa)

Autor: Wojciech Myszka  <wojciech.myszka@pwr.wroc.pl>

1. Instalacja

Nale¿y zainstalowaæ pakiet beamer wraz ze wszystkim czego
potrzebuje.

Plik "dystrybucyjny" rozpakowaæ w osobnym katalogu.

Pakiet zosta³ przetestowany w zakresie takim jak widaæ to w pliku
test_prez.tex

2. Co nie dzia³a

   + Nie ma mo¿liwoœci wyboru jêzyka
   + Nie ma mo¿liwoœci wyboru ,,paska'' po lewej na stronie
     tytu³owej
   + menu nawigacji na stronie tytu³owej

3. Uwagi

Pakiet beamer ma dosyæ rozbudowana strukturê. Do pierwszej
przymiarki wybra³em tematy domyœlne (color, inner, font) oraz
sidebar (outer) i zmodyfikowa³em TYLKO to co by³o niezbêdne do
osi¹gniêcia efektu wizualnego. St¹d obecnoœæ w dystrybucji plików
beamer-*-theme-default.sty

4. Postulaty

Mo¿na przesy³aæ na mój adres (najlepiej z propozycj¹ rozwi¹zania)

5. Do zrobienia

   + Opcje pozwalaj¹ce na zmianê jêzyka
   + Opcje pozwalaj¹ce na zmianê paska
   + Font u¿ywany do wyœwietlania adresów poleceniem \url{}


Zmiany:
-------
14 kwietnia 2005

+ Tytu³y zrobione fontem pó³grubym (jak we wzorcu)

+ Kolor odsy³aczy (okropny!) - jak we wzorcu.


Uwagi ogólne:
-------------
Uzyskanie fontu o wielkoœci zbli¿onej do tej we wzorcu wymaga
nastêpuj¹cego u¿ycia pakietu beamer:

\documentclass[17pt]{beamer}

Czy litery powinny byæ tak wielkie - nie mam przekonania...

19 kwietnia 2005

Po instalacji fontów (równie¿ http://www.immt.pwr.wroc.pl/logotyp/)
u¿ycie w preambule polecenia
\renewcommand{\sfdefault}{jtrr} wydaje siê "za³atwiaæ" sprawê fontów.
\renewcommand{\sfdefault}{jtrr}

24 kwietnia 2005, 7 maja 2005

1. Pierwsza sensowna wersja dzia³aj¹ca tak jak powinna.

2. Przed instalacj¹ nale¿y skasowaæ WSZYSTKIE pliki z wersji
poprzedniej!

3. U¿ycie pakietu wymaga instalacji fontu MS Trebuchet.

4. Zawartoœæ archiwum:
tex
`-- latex
    `-- beamer
        |-- art
        |   |-- logopwrpl.eps
        |   |-- logopwrpl.pdf
        |   |-- logopwrplm.eps
        |   |-- logopwrplm.png
        |   |-- pasek.eps
        |   |-- pasek.png
        |   |-- pasek2.eps
        |   `-- pasek2.png
        |-- demo
        |   |-- sample.mov
        |   |-- test_prez.pdf
        |   |-- test_prez.tex
        |   |-- zz.eps
        |   |-- zz.pdf
        |   |-- zz_.eps
        |   |-- zz_.png
        |   `-- zz__.png
        |-- pwr.prj
        |-- pwr.prj.bak
        |-- readme.txt
        |-- readme_l2.txt
        `-- themes
            |-- color
            |   |-- beamercolorthemepwr.sty
            |   `-- beamercolorthemepwr.sty.bak
            |-- font
            |   `-- beamerfontthemepwr.sty
            |-- inner
            |   |-- beamerinnerthemepwr.sty
            |   `-- beamerinnerthemepwr.sty.bak
            |-- outer
            |   |-- beamerouterthemepwr.sty
            |   `-- beamerouterthemepwr.sty.bak
            `-- theme
                |-- beamerthemepwr.sty
                `-- beamerthemepwr.sty.bak


5. Pliki z archiwum nale¿y rozpakowaæ we "w³aœciwe miejsce". Uk³ad
plików zbli¿ony do uk³adu pakietu beamer. Najlepiej wszystkie pliki
skopiowaæ (czyli rozpakowaæ archiwum w kartotece) do drzewa
texmf-local. Mo¿na (na w³asn¹ odpowiedzialnoœæ) skopiowaæ
(rozpakowaæ w) do texmf.

Nastêpnie nale¿y odœwie¿yæ zawartoœæ bazy danych.

5. Pakiet definiuje temat pwr; u¿ycie \usetheme{pwr}

6. Do zrobienia:
+ parametryzacja (pasek po lewej na stronie tytu³owej, wersja
angielska, obecnoœæ paska nawigacji, rozdzielczoœæ ekranu).
+ fonty w \url!
+ wszechstronne testy
+ dokumentacja

7. B³êdy:
+ pasek nawigacji na stronie tytu³owej

7 maja 2005

  Dodano plik readme w kodowaniu iso-8859-2 (readme_l2.tex)


10 maja 2005

Polecenie \usetheme{pwr} mo¿e byæ teraz wywo³ywane z dodatkowymi
parametrami okreœlaj¹cymi ,,ozdobê'' na stronie tytu³owej (pasek)
oraz jêzyk (lang).

pasek=pasek1 na stronie tytu³owej bêdzie pasek "szaro-bia³y"
pasek=pasek2 na stronie tytu³owej bêdzie pasek "ró¿owy"
pasek=<ka¿da_inna_wartosc> - na stronie tytu³owej umieszczony
zostanie plik graficzny dostarczony przez u¿ytkownika; wymiary pliku
powinny byæ takie, ¿eby dobrze mieœci³ siê w polu o szerokoœci 23 mm
i wysokoœci 73 milimetrów (plik bêdzie przeskalowany do tych
wymiarów!)

Uwaga: Je¿eli w kartotece bie¿¹cej znajdzie siê plik graficzny o
nazwie pasek[12].{png|jpg|pdf} zostanie on u¿yty jako ozdoba na
stronê tytu³ow¹ zamiast pliku dostarczonego!

Parametr lang mo¿e przyjmowaæ wartoœci pl lub en co spowoduje
umieszczenie znaku Politechniki Wroc³awskiej w odpowiednim jêzyku.

Dodatki wymagaj¹ zainstalowania na komputerze fontów lm (Latin Modern).

19 maja 2010

Dodana dodatkowa opcja fonty mog¹ca pzyj¹æ dwie wartoœci jtrr i trebuchet
w zaleznoœci od sposobu zainstaloowania font podstawowego (,,rêczna'' -- jtrr
pakiet msfonts -- trebuchet). Wbudowana jest pewna inteligencja pozwalaj¹ca
rozstrzygn¹æ to automatycznie. Gdy system stwierdza, ¿e font trebuchet nie
jest zainstalowany korzysta ze standardowego fontu cmss.

31 lipca 2012

W koñcu szablon strony tytu³owej honoruje wartoœæ opcji acpectratio, który 
mo¿e przyjmowaæ wartoœci
43   -- 4x3 (standard)
54   -- 5x4
169  -- 16x9
1610 -- 16x10
149  -- 14x9
32   -- 3x2
Szablon zak³ada, ¿e logo zawsze ma wymiary 23mm

