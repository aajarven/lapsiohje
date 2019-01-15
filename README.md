# Lapsiohjepohja
Resurssikeskus Linkin käyttämä LaTeX-pohja lasten käyttöön annettavien pelinteko-ohjeiden laatimiseen. Pohjasta on pyritty laatimaan yksinkertainen käyttää ja sen tuottamista ohjeista helppolukuisia ja lapsiin vetoavia. Kunkin kohdan vieressä on checkbox, joka helpottaa edistymisen seuraamista.

## Pohjan käyttö
Helpoimmalla pääset, kun uutta ohjetta tehdessäsi kopioit koko tämän repon sisällön clone or download -namikkaa tai komentoriviä käyttäen ja muokkaat sitten pohja.tex -tiedostoa. Sitä voi editoida haluamallaan tekstieditorilla. Työtä voi sujuvoittaa jonkin verran käyttämällä tarkoitukseen laadittua LaTeX-editoria kuten [Texmakeria](http://www.xm1math.net/texmaker/).

Tavallisessa käytössä ei tarvitse editoida mitään ennen `\begin{document}`-riviä ei tarvitse muokata, vaan kaikki sisältömuutokset tehdään sen jälkeen.

### Mallipelin kuva ja kuvaus
Helpoin tapa vaihtaa mallipelin kuva on korvata polussa `kuvat/esimerkki.png` oleva kuva uudella. Pelin kuvaus tulee kirjoittaa `\caption{}`-komennon aaltosulkujen väliin. On käytännöllistä laittaa kuvaukseen myös linkki mallipeliin, tämä onnistuu komennolle `\href{https://google.fi}{Linkki mallipeliin}`, jossa googlen urlin voi korvata pelin osoitteella ja jälkimmäisten aaltosulkujen väliin laittaa linkille haluamansa tekstin. Tekstissä kannattaa mainita pelin nimi ja tekijä, jotta se on mahdollista löytää myös paperisen ohjeen perusteella.

### Varsinaiset ohjeet
Pelin teon vaiheet tulevat vaihetaso-environmenttien sisään, siis `\begin{vaihetaso1}` jälkeen mutta ennen `\end{vaihetaso1}`. Mikäli tahtoo käyttää alakohtia, voi `vaihetaso1` sisällä käyttää vastaavasti `vaihetaso2` ja sen sisällä `vaihetaso3`. Ennen kunkin kohdan haluttua tekstiä tulee olla komento `\item`.

Halutessaan ohjeen rakennetta voi selkeyttää käyttämällä väliotsikoita. Tämä onnistuu lisäämällä `\subsection*{Haluttu otsikko}`. Komennon tulee olla kaikkien vaihetasojen ulkopuolella.

## Kääntäminen
Dokumentin kääntäminen pdf:ksi onnistuu joko käyttämällä esimerkiksi texmakerin quick build -toimintoa tai komentoriviltä komennoilla:
```
latex -interaction=nonstopmode pohja.tex
pdflatex -synctex=1 -interaction=nonstopmode pohja.tex
```
