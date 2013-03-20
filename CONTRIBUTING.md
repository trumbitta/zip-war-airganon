# Come contribuire

1. forka il repository
2. crea una topic branch a partire da `master`
3. seguendo l'immagine del diagramma di flusso - http://i.imgur.com/xDanWtZ.jpg - aggiungi un pezzo di percorso mancante (e leggi il prossimo paragrafo)
4. mandami una pull request

Io darò uno sguardo, e se sarà tutto ok farò il merge da `master` a `gh-pages` in modo che http://trumbitta.github.com/zip-war-airganon/ ne risulti aggiornato!

## Come aggiungere un pezzo di percorso mancante

Aggiungere un pezzo di percorso mancante è facilissimo!  
Basta aggiungere un file JSON sotto `contents` ed eventualmente modificare uno dei precedenti perché punti al tuo!

### Mettiamo per esempio che tu voglia creare l'ultimo passo del diagramma di flusso.

 * crea `contents/invece-si.json`  
 * scrivine il contenuto come segue:

```json
{
  "titolo": "Invece sì!",
  "nota": "E te lo dimostreremo perché anche noi siamo entrati in possesso del...",
  "opzione1": [
      {
        "questa-opzione": "Attivazione Cross Checking",
        "ti-porta-a": "/attiva-cross-checking",
        "icona": "spinner"
      }
  ]
}
```
 * apri il file che descrive il passo precedente al tuo, modifica il `ti-porta-a` dell'opzione opportuna facendo sì che punti a `/invece-sì` (il tuo nuovo passo).

### Formato dei passi, commentato

`titolo`: è il titolo del passo  
`nota`: è la nota aggiuntiva sotto il titolo  
`opzione1`: è il primo bottone  
`opzione2`: se decidi di metterla, è il secondo bottone che compare a fianco del primo bottone  
`opzione3`: se decidi di metterla, è il terzo bottone che è molto più piccolo e compare al di sotto dei primi due

#### Per ciascuna opzione

`questa-opzione`: è il testo che compare all'interno del bottone  
`ti-porta-a`: è costituita da uno `/` seguito dal nome del passo a cui il bottone porta. (Es: `/attiva-cross-checking` porta al passo descritto in `attiva-cross-checking.json`)  
`icona`: se decidi di metterla, è il nome senza `icon-` di una icona presa da [Font Awesome](http://fortawesome.github.com/Font-Awesome/) (Es: l'icona `icon-spinner` va indicata con `spinner`)
