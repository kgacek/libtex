% $Id: readme.txt,v 1.0 2005-04-15 11:00:52+02 myszka Exp myszka $
-------------------------------------------------------------
Dodatki do pakietu beamer udające prezentację zgodną z Księgą
Logotypu
-------------------------------------------------------------
Wersja 0.05 (alfa)

Autor: Wojciech Myszka  <wojciech.myszka@pwr.wroc.pl>

1. Instalacja

Należy zainstalować pakiet beamer wraz ze wszystkim czego
potrzebuje.

Plik "dystrybucyjny" rozpakować w osobnym katalogu.

Pakiet został przetestowany w zakresie takim jak widać to w pliku
test_prez.tex

2. Co nie działa

   + Nie ma możliwości wyboru języka
   + Nie ma możliwości wyboru ,,paska'' po lewej na stronie
     tytułowej
   + menu nawigacji na stronie tytułowej

3. Uwagi

Pakiet beamer ma dosyć rozbudowana strukturę. Do pierwszej
przymiarki wybrałem tematy domyślne (color, inner, font) oraz
sidebar (outer) i zmodyfikowałem TYLKO to co było niezbędne do
osiągnięcia efektu wizualnego. Stąd obecność w dystrybucji plików
beamer-*-theme-default.sty

4. Postulaty

Można przesyłać na mój adres (najlepiej z propozycją rozwiązania)

5. Do zrobienia

   + Opcje pozwalające na zmianę języka
   + Opcje pozwalające na zmianę paska
   + Font używany do wyświetlania adresów poleceniem \url{}


Zmiany:
-------
14 kwietnia 2005

+ Tytuły zrobione fontem półgrubym (jak we wzorcu)

+ Kolor odsyłaczy (okropny!) - jak we wzorcu.


Uwagi ogólne:
-------------
Uzyskanie fontu o wielkości zbliżonej do tej we wzorcu wymaga
następującego użycia pakietu beamer:

\documentclass[17pt]{beamer}

Czy litery powinny być tak wielkie - nie mam przekonania...

19 kwietnia 2005

Po instalacji fontów (również http://www.immt.pwr.wroc.pl/logotyp/)
użycie w preambule polecenia
\renewcommand{\sfdefault}{jtrr} wydaje się "załatwiać" sprawę fontów.
\renewcommand{\sfdefault}{jtrr}

24 kwietnia 2005, 7 maja 2005

1. Pierwsza sensowna wersja działająca tak jak powinna.

2. Przed instalacją należy skasować WSZYSTKIE pliki z wersji
poprzedniej!

3. Użycie pakietu wymaga instalacji fontu MS Trebuchet.

4. Zawartość archiwum:
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


5. Pliki z archiwum należy rozpakować we "właściwe miejsce". Układ
plików zbliżony do układu pakietu beamer. Najlepiej wszystkie pliki
skopiować (czyli rozpakować archiwum w kartotece) do drzewa
texmf-local. Można (na własną odpowiedzialność) skopiować
(rozpakować w) do texmf.

Następnie należy odświeżyć zawartość bazy danych.

5. Pakiet definiuje temat pwr; użycie \usetheme{pwr}

6. Do zrobienia:
+ parametryzacja (pasek po lewej na stronie tytułowej, wersja
angielska, obecność paska nawigacji, rozdzielczość ekranu).
+ fonty w \url!
+ wszechstronne testy
+ dokumentacja

7. Błędy:
+ pasek nawigacji na stronie tytułowej

7 maja 2005

  Dodano plik readme w kodowaniu iso-8859-2 (readme_l2.tex)


10 maja 2005

Polecenie \usetheme{pwr} może być teraz wywoływane z dodatkowymi
parametrami określającymi ,,ozdobę'' na stronie tytułowej (pasek)
oraz język (lang).

pasek=pasek1 na stronie tytułowej będzie pasek "szaro-biały"
pasek=pasek2 na stronie tytułowej będzie pasek "różowy"
pasek=<każda_inna_wartosc> - na stronie tytułowej umieszczony
zostanie plik graficzny dostarczony przez użytkownika; wymiary pliku
powinny być takie, żeby dobrze mieścił się w polu o szerokości 23 mm
i wysokości 73 milimetrów (plik będzie przeskalowany do tych
wymiarów!)

Uwaga: Jeżeli w kartotece bieżącej znajdzie się plik graficzny o
nazwie pasek[12].{png|jpg|pdf} zostanie on użyty jako ozdoba na
stronę tytułową zamiast pliku dostarczonego!

Parametr lang może przyjmować wartości pl lub en co spowoduje
umieszczenie znaku Politechniki Wrocławskiej w odpowiednim języku.

Dodatki wymagają zainstalowania na komputerze fontów lm (Latin Modern).

19 maja 2010

Dodana dodatkowa opcja fonty mogąca pzyjąć dwie wartości jtrr i trebuchet
w zalezności od sposobu zainstaloowania font podstawowego (,,ręczna'' -- jtrr
pakiet msfonts -- trebuchet). Wbudowana jest pewna inteligencja pozwalająca
rozstrzygnąć to automatycznie. Gdy system stwierdza, że font trebuchet nie
jest zainstalowany korzysta ze standardowego fontu cmss.

31 lipca 2012

W końcu szablon strony tytułowej honoruje wartość opcji acpectratio, który 
może przyjmować wartości
43   -- 4x3 (standard)
54   -- 5x4
169  -- 16x9
1610 -- 16x10
149  -- 14x9
32   -- 3x2
Szablon zakłada, że logo zawsze ma wymiary 23mm

