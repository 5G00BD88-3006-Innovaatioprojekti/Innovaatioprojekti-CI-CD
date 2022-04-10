# Innovaatioprojekti CI/CD

## Actions

### Deploy app

Workflown inputeissa määritellään asennettava sovellus, branchi ja kohde ympäristö. Asennettavan sovelluksen repo haetaan palvelimelle ja nyt etäkoneella sijaitsevan repon kopiossa vaihdetaan inputeissa määriteltyyn branchiin. Seuraavaksi workflow kutsuu sovellus kohtaista build actionia. Build action käyttää imagejen luomiseen .dockerfile tiedostoja jotka löytyvät sovelluskohtaisesta reposta. Nämä .dockerfilet tehdään tarvittaessa CI/CD tiimin toimesta. Vanhat ajossa olevat imaget uudelleen tagataan "ympäristö_previous" tagilla jota voidaan käyttää tarvittaessa rollbackin tekemiseen. Imagejen rakennuksen jälkeen sovellus käynnistetään CI/CD reposta löytyvän projekti ja ympäristö kohtaisen docker-compose tiedoston mukaisesti.

![alt text](https://github.com/ninopenttinen/Innovaatioprojekti-CI-CD/blob/main/README%20pictures/workflows/deploy-app.png?raw=true)

### Rollback

Kutsuu projektikohtaista rollback actionia, joka vaihtaa "ympäristö" ja "ympäristö_previous" tagit päittäin. Lopuksi kutsutaan projektikohtaista deploy actionia joka käynnistää sovelluksen uudestaan.

![alt text](https://github.com/ninopenttinen/Innovaatioprojekti-CI-CD/blob/main/README%20pictures/workflows/rollback.png?raw=true)
