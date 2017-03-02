# Lapsiohjepohja
Resurssikeskus Linkin käyttämä LaTeX-pohja lasten käyttöön annettavien pelinteko-ohjeiden laatimiseen. Pohjasta on pyritty laatimaan yksinkertainen käyttää ja sen tuottamista ohjeista helppolukuisia ja lapsiin vetoavia. Kunkin kohdan vieressä on checkbox, joka helpottaa edistymisen seuraamista.

## Pohjan käyttö
Tavallisessa käytössä ei tarvitse editoida mitään ennen `\begin{document}`-riviä ei tarvitse muokata, vaan kaikki sisältömuutokset tehdään sen jälkeen.

### Mallipelin kuva ja kuvaus
Helpoin tapa vaihtaa mallipelin kuva on korvata polussa `kuvat/esimerkki.png` oleva kuva uudella. Pelin kuvaus tulee kirjoittaa `\caption{}`-komennon aaltosulkujen väliin. On käytännöllistä laittaa kuvaukseen myös linkki mallipeliin, tämä onnistuu komennolle `\href{https://google.fi}{Linkki mallipeliin}`, jossa googlen urlin voi korvata pelin osoitteella ja jälkimmäisten aaltosulkujen väliin laittaa linkille haluamansa tekstin. Tekstissä kannattaa mainita pelin nimi ja tekijä, jotta se on mahdollista löytää myös paperisen ohjeen perusteella.
