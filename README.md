# Innovaatioprojekti CI/CD

## Actions

### Update repo on server

Pullaa uusimmat muutokset repon 'main' haarasta palvelimelle kun repoon tehdään muutoksia. Tehdään jotta saadaan uusimmat docker konttien rakennus ohjeet palvelimelle jota runnerit osaavat buildata kontit uusimpien ohjeiden mukaan.

### Deploy to server

EI AJANTASALLA

![alt text](https://github.com/ninopenttinen/Innovaatioprojekti-CI-CD/blob/main/Architecture%20pictures/Actions/deploy-to-server.png?raw=true)

### Build project

Projekti kohtaiset repot kutsuvat omaa projekti kohtaista build actioniaan, joka pullaa/kloonaa projektin lähdekoodit palvelimelle ja rakentaa projektin pohjalta docker imaget ja lopuksi kontit imagejen pohjalta. Docker imagejen rakennus ohjeet tehdään projektin omiin repoihin tarvittaessa CICD tiimin toimesta. Jos projekti pitää sisällään salaisuuksia, lähetetään ne inputteina build actionille.
ACTION VIELÄ TOISTAISEKSI TESTATTAVANA

![alt text](https://github.com/ninopenttinen/Innovaatioprojekti-CI-CD/blob/main/Architecture%20pictures/Actions/build-project.png?raw=true)
