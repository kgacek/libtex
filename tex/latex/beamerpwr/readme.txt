% $Id: readme.txt,v 1.0 2005-04-15 11:00:52+02 myszka Exp myszka $
-------------------------------------------------------------
Dodatki do pakietu beamer udaj�ce prezentacj� zgodn� z Ksi�g�
Logotypu
-------------------------------------------------------------
Wersja 0.05 (alfa)

Autor: Wojciech Myszka  <wojciech.myszka@pwr.wroc.pl>

1. Instalacja

Nale�y zainstalowa� pakiet beamer wraz ze wszystkim czego
potrzebuje.

Plik "dystrybucyjny" rozpakowa� w osobnym katalogu.

Pakiet zosta� przetestowany w zakresie takim jak wida� to w pliku
test_prez.tex

2. Co nie dzia�a

   + Nie ma mo�liwo�ci wyboru j�zyka
   + Nie ma mo�liwo�ci wyboru ,,paska'' po lewej na stronie
     tytu�owej
   + menu nawigacji na stronie tytu�owej

3. Uwagi

Pakiet beamer ma dosy� rozbudowana struktur�. Do pierwszej
przymiarki wybra�em tematy domy�lne (color, inner, font) oraz
sidebar (outer) i zmodyfikowa�em TYLKO to co by�o niezb�dne do
osi�gni�cia efektu wizualnego. St�d obecno�� w dystrybucji plik�w
beamer-*-theme-default.sty

4. Postulaty

Mo�na przesy�a� na m�j adres (najlepiej z propozycj� rozwi�zania)

5. Do zrobienia

   + Opcje pozwalaj�ce na zmian� j�zyka
   + Opcje pozwalaj�ce na zmian� paska
   + Font u�ywany do wy�wietlania adres�w poleceniem \url{}


Zmiany:
-------
14 kwietnia 2005

+ Tytu�y zrobione fontem p�grubym (jak we wzorcu)

+ Kolor odsy�aczy (okropny!) - jak we wzorcu.


Uwagi og�lne:
-------------
Uzyskanie fontu o wielko�ci zbli�onej do tej we wzorcu wymaga
nast�puj�cego u�ycia pakietu beamer:

\documentclass[17pt]{beamer}

Czy litery powinny by� tak wielkie - nie mam przekonania...

19 kwietnia 2005

Po instalacji font�w (r�wnie� http://www.immt.pwr.wroc.pl/logotyp/)
u�ycie w preambule polecenia
\renewcommand{\sfdefault}{jtrr} wydaje si� "za�atwia�" spraw� font�w.
\renewcommand{\sfdefault}{jtrr}

24 kwietnia 2005, 7 maja 2005

1. Pierwsza sensowna wersja dzia�aj�ca tak jak powinna.

2. Przed instalacj� nale�y skasowa� WSZYSTKIE pliki z wersji
poprzedniej!

3. U�ycie pakietu wymaga instalacji fontu MS Trebuchet.

4. Zawarto�� archiwum:
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


5. Pliki z archiwum nale�y rozpakowa� we "w�a�ciwe miejsce". Uk�ad
plik�w zbli�ony do uk�adu pakietu beamer. Najlepiej wszystkie pliki
skopiowa� (czyli rozpakowa� archiwum w kartotece) do drzewa
texmf-local. Mo�na (na w�asn� odpowiedzialno��) skopiowa�
(rozpakowa� w) do texmf.

Nast�pnie nale�y od�wie�y� zawarto�� bazy danych.

5. Pakiet definiuje temat pwr; u�ycie \usetheme{pwr}

6. Do zrobienia:
+ parametryzacja (pasek po lewej na stronie tytu�owej, wersja
angielska, obecno�� paska nawigacji, rozdzielczo�� ekranu).
+ fonty w \url!
+ wszechstronne testy
+ dokumentacja

7. B��dy:
+ pasek nawigacji na stronie tytu�owej

7 maja 2005

  Dodano plik readme w kodowaniu iso-8859-2 (readme_l2.tex)


10 maja 2005

Polecenie \usetheme{pwr} mo�e by� teraz wywo�ywane z dodatkowymi
parametrami okre�laj�cymi ,,ozdob�'' na stronie tytu�owej (pasek)
oraz j�zyk (lang).

pasek=pasek1 na stronie tytu�owej b�dzie pasek "szaro-bia�y"
pasek=pasek2 na stronie tytu�owej b�dzie pasek "r�owy"
pasek=<ka�da_inna_wartosc> - na stronie tytu�owej umieszczony
zostanie plik graficzny dostarczony przez u�ytkownika; wymiary pliku
powinny by� takie, �eby dobrze mie�ci� si� w polu o szeroko�ci 23 mm
i wysoko�ci 73 milimetr�w (plik b�dzie przeskalowany do tych
wymiar�w!)

Uwaga: Je�eli w kartotece bie��cej znajdzie si� plik graficzny o
nazwie pasek[12].{png|jpg|pdf} zostanie on u�yty jako ozdoba na
stron� tytu�ow� zamiast pliku dostarczonego!

Parametr lang mo�e przyjmowa� warto�ci pl lub en co spowoduje
umieszczenie znaku Politechniki Wroc�awskiej w odpowiednim j�zyku.

Dodatki wymagaj� zainstalowania na komputerze font�w lm (Latin Modern).

19 maja 2010

Dodana dodatkowa opcja fonty mog�ca pzyj�� dwie warto�ci jtrr i trebuchet
w zalezno�ci od sposobu zainstaloowania font podstawowego (,,r�czna'' -- jtrr
pakiet msfonts -- trebuchet). Wbudowana jest pewna inteligencja pozwalaj�ca
rozstrzygn�� to automatycznie. Gdy system stwierdza, �e font trebuchet nie
jest zainstalowany korzysta ze standardowego fontu cmss.

31 lipca 2012

W ko�cu szablon strony tytu�owej honoruje warto�� opcji acpectratio, kt�ry 
mo�e przyjmowa� warto�ci
43   -- 4x3 (standard)
54   -- 5x4
169  -- 16x9
1610 -- 16x10
149  -- 14x9
32   -- 3x2
Szablon zak�ada, �e logo zawsze ma wymiary 23mm

