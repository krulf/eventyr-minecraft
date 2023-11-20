# Læg din egen lyd ind i Minecraft
Hver gruppe kan bruge op til 3 discs i minecrafts jukebox
 - Lav 3 lydfiler
 - Pak de 3 lydfiler ned i en minecraft add-on pakke
 - Test at de 3 lydfiler virker

***

# Optag lyd med [Audacity](https://www.audacityteam.org/)
 - Start programmet: tryk på windows tasten og skriv audacity
 - Vælg optageenhed - som hedder noget forskelligt alt efter hvilken mikrofon I har - tjek at optagekvaliteten er god


![optageenhed](audacity-optageenhed.png)

 - brug optage knappen til at optage med
 - gem optagelsen ved at eksportere: __Fil -> Eksporter lyd... CTRL-SHIFT-E__
 - Vælg Format: Ogg Vorbis-filer
 - Det er vigtigt at I kalder jeres lydfiler de rigtige navne for jeres gruppe:


![discs](https://github.com/krulf/eventyr-minecraft/blob/main/lydpakke-discs.png)

***

# Ændre minecraft pakke (gruppe 1 bruges som eksempel)
 - Hent skabelonen til minecraftpakken for jeres gruppe: [lydpakker](https://github.com/krulf/eventyr-minecraft/tree/main/lydpakke)


![download](https://github.com/krulf/eventyr-minecraft/blob/main/lydpakke-download.png)
 - Pak lydpakken ud: højre-klik på filen under downloads/ overførsler og pak den ud med


![extract-here](https://github.com/krulf/eventyr-minecraft/blob/main/lydpakke-extract-here.png)
 - Find herefter mappen "gruppeX" i overførsler/ downloads
 - I den mappe findes:
     - manifest.json
     - mapperne "sounds/music/game/records" og for gruppe 1 hedder lydfilerne sådan:


![mapperne](https://github.com/krulf/eventyr-minecraft/blob/main/lydpakke-lydfilerne.png)
 - de tre filer der ligger der skal udskiftes med de optagelser I har lavet, samlet oversigt herunder:


![discs](https://github.com/krulf/eventyr-minecraft/blob/main/lydpakke-discs.png)

***

# Test minecraft-pakke
 - Det er tid for at teste minecraft-pakken med lydfilerne
 - Højreklik på den gule mappe i øverførsler og vælg at pakke den ned til en zip-fil:


![createzip](https://github.com/krulf/eventyr-minecraft/blob/main/lydpakke-createzip.png)
 - Filer har et navn og et efternavn, adskilt af punktum. F.eks.: __gruppe1.zip__
 - For at få minecraft til at importere zip-filen skal dens efternavn ændres fra "zip" til "mpack"
 - Dobbeltklik på filen og minecraft skulle gerne importere filen successfuldt
 - Test filen ved at oprette en ny verden
    - Under "Ressourcepakker" fold "Mine Pakker" ud og "aktiver" jeres ressourcepakke:


![ressourcepakke](https://github.com/krulf/eventyr-minecraft/blob/main/lydpakke-ressourcepakke.png)

***

# Ny version af minecraft pakke
Hvis pakken skal opdateres eller ændres skal der laves en ny version.

 - Opdater filerne som skal ændres
 - Pakken skal have et nyt navn og et nyt versionsnummer:
    - Åben __manifest.json__
    - Skift værdien "name" fra f.eks. "Gruppe 1" til: "Gruppe 1 version 1.0.1"
    - Skift værdien "Version" fra f.eks. [1, 0, 0], til: [1, 0, 1],

```
{
 "format_version": 2,
 "header": {
   "description": "13.ogg, cat.ogg, blocks.ogg",
   "name": "Gruppe 1",
   "uuid":"cbb8563c-51b1-4bb5-8889-73ad681e3790",
   "version": [1, 0, 0],
   "min_engine_version": [1, 16, 0]
  },
 "modules": [
   {
     "description": "Min næsten første add-on",
     "type": "resources",
     "uuid": "4315d904-e594-4424-a328-dffe9d132b55",
     "version": [1, 0, 0]
   }
 ]
}
```
