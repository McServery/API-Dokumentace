# Dokumentace k API
### Co api umí? 
- Zobrazení všech veřejně dostupných informací o serveru
- Seznam hráčů hlasujících pro server za posledních 30 dní
- Aktuální počet hlasů

## Jak api použít? 
### Získání klíče
Pro pužívání api je nutné vygenerovat api key který vám zajistí přístup k informacím pro server se kterým je klíč navázaný. Klíč vygenerujete po přihlášení k účtu který je spojený s daným serverem. Je nutné být přihlášený na http://mcservery.eu/login.php

Pro vygenerování klíče si zobrazte seznam vašich serverů 

![api1](https://github.com/McServery/API-Dokumentace/blob/master/img/api1.JPG)


Otevřete detail požadovaného serveru

![api2](https://github.com/McServery/API-Dokumentace/blob/master/img/api2.jpg?raw=true)


Vygenerujte api klíč

![api3](https://github.com/McServery/API-Dokumentace/blob/master/img/api3.JPG)


Zkopírujte svůj api klíč

![api4](https://github.com/McServery/API-Dokumentace/blob/master/img/api4.JPG)

### Informace o serveru
> GET http://api.mcservery.eu/?api_key=vášklíč

`
{ "Name": "API Testovací server", "Description": "Testovací záznam pro zkoušku API", "Adress": "mc.hypixel.net", "Port": "25565", "Web": "http://api.mcservery.eu", "Discord": "", "Tag1": "", "Tag2": "", "Tag3": "", "Votes": "1", "VRD": "2020-08-25 15:39:03" }
`
*VRD = Votes Reset Date - Hlasy se resetují jednou za 30 dní od přidání serveru, vždy při resetu se nastaví aktuální čas kdy byl reset proveden*

### Hlasující hráči za posledních 30 dní
> GET http://api.mcservery.eu/players/?api_key=vášklíč

`
{ "username": "ArtyomCZ", "time": "2020-08-25 18:38:00" }
`

### Počet hlasů
> GET http://api.mcservery.eu/votes/?api_key=vášklíč

`
{ "Votes": "1" }
`
