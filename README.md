# Innovaatioprojekti CI/CD

## Actions

### Update repo on server

Pullaa uusimmat muutokset repon 'main' haarasta palvelimelle kun repoon tehdään muutoksia. Tehdään jotta saadaan uusimmat docker konttien rakennus ohjeet palvelimelle jota runnerit osaavat buildata kontit uusimpien ohjeiden mukaan.

### Deploy to server

Deploy action ottaa yhteyden TAMKin palvelimella pyörivään github runneriin, joka ajaa komennot projektin hakemiseksi/päivittämiseksi reposta ja käynnistää "Build project" actionin.

![alt text](https://github.com/ninopenttinen/Innovaatioprojekti-CI-CD/blob/main/Architecture%20pictures/Actions/deploy-to-server.png?raw=true)

### Build project

Projekti kohtaiset build actionit.

![alt text](https://github.com/ninopenttinen/Innovaatioprojekti-CI-CD/blob/main/Architecture%20pictures/Actions/build-project.png?raw=true)
