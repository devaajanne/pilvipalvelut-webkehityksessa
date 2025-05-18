# Harjoitustyö: My Mocktail cabinet

## Yleisesti

My Mocktail Cabinet on sivusto, jonka kautta käyttäjät voivat etsiä uusia mocktaileja sekä tallentaa niitä omaan mocktailkaappiinsa. My Mocktail Cabinet on julkaistu täällä: [https://devaajanne.github.io/my-mocktail-cabinet/#/](https://devaajanne.github.io/my-mocktail-cabinet/#/)

Sivusto on rakennettu pääasiassa TypeScriptillä ja Reactilla. Käyttäjän autentikoinnissa on käytetty Firebasea. Käyttäjän oma mocktail-kaappi tallennetaan Firestore databaseen. Sivusto käyttää mocktail-reseptien hauessa [The Cocktail DB:n APIa](https://www.thecocktaildb.com/api.php).

Sivusto käyttää yhteinäistä ulkoasua kaikilla sivuillaan. Lisäksi sivuston saatavuutta on parannettu lisäämällä elementteihin ja komponentteihin aria-attribuutteja.

## Responsiivisuus

Responsiivisuutta on testattu eri kokoisilla selainikkunoilla desktopissa sekä mobiililla.

Desktopilla mocktail-korttien asettelu muuttuu selainikkunan koon mukaan: isoilla näytöillä kortteja on kolme rivillä, ja korttien määrä rivillä pienenee selainkkunaa piennettäessä.

Mobiililla selainkortit asettuvat yksi per rivi.

## Selaimet

Sivuston toimivuutta on testattu seuraavilla selaimilla:

- Edge v. 136.0.3240.76: Ei ongelmia, toiminnallisuudet kunnossa, elementit latautuvat oikein
- Chrome v. 136.0.7103.114: Ei ongelmia, toiminnallisuudet kunnossa, elementit latautuvat oikein
- Firefox v. 138.0.4: Ei ongelmia, toiminnallisuudet kunnossa, elementit latautuvat oikein. Tuntuu hieman nopeammalta kuin muut selaimet

## Latautumisajat

Sivusto latautuu sekä desktopilla että mobiililla seruaavasti:

Desktopilla sivusto latautuu varsin nopeasti

- First Contentful Paint: 0.5 s
- Largest Contentful Paint: 0.9 s
- Total Blocking Time: 140 ms
- Cumulative Layout Shift: 0.005
- Speed Index: 0.5 s

![desktop speed results](./desktop%20speed%20results.png)

Mobiililla sivusto lautautui hitaammin kuin selaimella. Tämä johtunee suuren datamäärän hakemisesta APIn kautta kirjautuessa sivustolla, mitä voisi lieventää esimerkiksi paginoimalla API-kutsun tuloksia.

- First Contentful Paint: 2.1 s
- Largest Contentful Paint: 2.1 s
- Total Blocking Time: 260 ms
- Cumulative Layout Shift: 0
- Speed Index: 2.1 s

![mobile speed results](mobile%20speed%20results.png)
