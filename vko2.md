### Viikon 2 tehtävä
#### Miten GitHub Actionsia ja CI/CD-putkea voisi käyttää web-kehityksessä?

Yleisesti web-kehityksessä CI/CD-putkea voi käyttää muun muassa kehitys- ja julkaisutyön automatisointiin. GitHub Actionsia käyttäessä GitHubiin lisättävään workflow-tiedostoon voidaan määritellä komennot sovelluksen buildaamista, testaamista ja lopulta julkaisemista varten. Esimerkiksi voidaan määritellä, että jokaisen push-komennon jälkeen GitHub buildaa sovelluksen, alustaa ja ajaa testit testiympäristössä (esim. Playwright) ja lopulta julkaisee sovelluksen haluamassamme ympäristössä. Putkimaiseksi tästä tekee se, että mainitut toimet suoritetaan järjestyksessä ja tarvittaessa riippuvaisina toisistaan: mitään ei julkaista, jos testit eivät mene läpi, ja testeihin ei siirrytä, jos koko sovelluksen buildaus epäonnistuu.

GitHub Actions automatisoi Jekyll-sivun buildaamisen ja julkaisun, mikä on ehkä yksinkertaisin tapa hyödyntää Actionsia Jekyll-sivun kanssa. Actionsin kautta voimme lisäksi myös asentaa plugineja, jotka eivät ole oletusarvoisesti tuettuja, sekä käyttää repositorion salaisuuksia.

Muita CI/CD-teknologoita- ja työkaluja on muun muassa Jenkins ja Azure DevOps jatkuvaan integrointiin, Docker ja Kubernetes kontitukseen ja Prometheus sovelluksen monitorointiin. Kurssin harjoitustyössä GitHub Actionsia voisi käyttää myös repositorion salaisuuksien hallintaan esimerkiksi autentikoinnin ja tietokantayhteyksien osalta.

[Palaa takaisin etusivulle](index.md)