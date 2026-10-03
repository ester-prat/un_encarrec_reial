# Un encàrrec reial

Web app del joc de pistes «Un encàrrec reial», pel recorregut de la muralla medieval de Granollers. Porta les pistes d'àudio de cada prova i ajuda els jugadors a trobar on han d'anar.

Funciona al navegador del mòbil i es pot posar a la pantalla d'inici com una app. Un cop carregada amb internet, les pistes es guarden al mòbil i es poden escoltar sense connexió.

## Què fa

- Reprodueix les pistes d'àudio: dues d'introducció i tres per cada una de les 7 proves (l'encàrrec, saber-ne més i encàrrec complert).
- Marca les pistes que ja s'han escoltat.
- Té una guia per no perdre's: amb la ubicació del mòbil diu a quants metres és la prova i cap a on s'ha d'anar, amb una fletxa i un mapa senzill. Aquesta guia no necessita internet.
- Té un botó per obrir el lloc al mapa del mòbil (Google Maps o Apple Maps). Aquest sí que necessita internet.

## Fitxers

- `index.html`: tota la pàgina (aspecte, dades de les proves i guia).
- `sw.js`: guarda els fitxers al mòbil perquè funcioni sense internet.
- `manifest.json`: dades per instal·lar-la com a app.
- `audio/`: les pistes en mp3 (`intro1`, `intro2`, `p1a`... `p7c`).
- `fonts/`: la tipografia Barlow, amb la seva llicència.
- `margarida.png`, `margarida-cara.png`, `icon-192.png`, `icon-512.png`: imatges.

## Com canviar-hi coses

**Llocs i coordenades.** A `index.html`, busca la llista `PUNTS`. Cada prova té el nom del lloc, el detall (la capella, si n'hi ha) i les coordenades.

**Noms de les activitats i durades.** A `index.html`, busca la llista `DATA`.

**Pistes d'àudio.** Substitueix el fitxer de la carpeta `audio/` pel nou, amb el mateix nom.

**Important després de qualsevol canvi.** Perquè els mòbils que ja tenen la web guardada rebin els canvis, cal canviar el número de versió (`encarrec-v3`, `encarrec-v4`...) a dos llocs: a `sw.js` (la línia `const CACHE`) i a `index.html` (la línia `const CACHE`). Han de ser iguals.

## Publicació

La web es publica a Netlify: https://unencarrecreial.netlify.app

## Tipografia

Barlow, de The Barlow Project Authors, amb llicència SIL Open Font License 1.1. La llicència és a `fonts/OFL-Barlow.txt`.

## Crèdits

Joc de pistes de Roca Umbert Fàbrica de les Arts i Ajuntament de Granollers.
