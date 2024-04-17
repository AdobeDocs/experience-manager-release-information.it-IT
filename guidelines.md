---
source-git-commit: 437dad5fffe71592b6f9f9b4099a253e3a55b0c8
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 47%

---
# Linee guida per contribuire alla documentazione di Adobe Experience Manager

## Filosofia della documentazione

Gli utenti di Adobe Experience Manager lavorano in ambienti altamente competitivi per creare esperienze digitali che li distinguano dalla concorrenza. Pertanto, quando Adobe offre nuovi strumenti avanzati nell’AEM, questi sono integrati da una documentazione accurata e chiara che consente ai clienti di applicare immediatamente il proprio investimento nell’AEM e massimizzare il ROI.

Per la documentazione di AEM, l’obiettivo è renderla disponibile agli utenti della soluzione il prima possibile. Viene quindi creata una documentazione accurata e fruibile, continuamente aggiornata e migliorata.

## Contributi alla documentazione

Al fine di migliorare continuamente la documentazione di AEM, apprezziamo il contributo dell’intera comunità di utenti AEM. I miglioramenti apportati alla documentazione, che derivino da richieste o segnalazioni di problemi, possono essere correzioni, chiarimenti, ampliamenti e altri esempi.

## Standard della documentazione

I contributi alla documentazione sono accolti con favore; qualsiasi contributo alla documentazione AEM, sotto forma di richiesta o segnalazione di un problema, deve essere conforme agli standard in materia di contributi e documentazione di Adobe.

I contributi che non soddisfano tali standard possono essere rifiutati.

### Adobe documenta i casi d’uso standard.

La documentazione di AEM riguarda i casi di utilizzo standard. I casi di utilizzo che esulano dall’ambito di installazione e utilizzo standard del prodotto non rientrano nella documentazione di AEM.

### In genere, l’Adobe non documenta i bug o le relative soluzioni.

La documentazione di AEM riguarda i casi di utilizzo standard. Per questo motivo, i bug, gli effetti causati dai bug e le soluzioni alternative per i bug non sono documentati.

Fanne eccezione le note sulla versione, in cui possono essere elencati i problemi noti con possibili soluzioni approvate dal team AEM Product Management.

### I contributi alla documentazione non devono essere usati per rispondere a domande tecniche.

È gradita come contributo qualsiasi idea che punti al miglioramento della documentazione di AEM. Tuttavia, commenti, problemi e richieste sono intesi per *contributi* solo. L’obiettivo non è quello di rispondere a domande su come utilizzare l’AEM, implementare un progetto AEM o risolvere problemi tecnici.

Eventuali domande sull’utilizzo di AEM o su errori tecnici possono essere segnalate attraverso il normale processo di assistenza tramite il [portale di assistenza Enterprise Support di Experience Cloud](https://experienceleague.adobe.com/?support-solution=General&amp;lang=it#support) o discusse nella [community di Experience Manager](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community?lang=it).

***I contributi alla documentazione AEM non sostituiscono, ad Adobe, l’Assistenza clienti*** e tutti i contributi che richiedono risposte a domande correlate al supporto sono respinti.

### I contributi devono fare riferimento in modo chiaro alle pagine della documentazione interessate.

Se apri una segnalazione per suggerire miglioramenti alla documentazione, devi includere i collegamenti alle pagine interessate. Se si crea un problema utilizzando **Modifica questa pagina** su una pagina della documentazione, il problema viene creato automaticamente con un collegamento alla pagina.

Ciò non si applica alle richieste pull, che per loro natura fanno riferimento alla pagina o alle pagine interessate.

## Linee guida per la documentazione

Qualsiasi contributo alla documentazione deve seguire determinate linee guida di stile.

L’aderenza a queste linee guida semplifica la revisione del contributo e velocizza quindi l’integrazione nella documentazione.

### Lingua e stile

#### Lingua

* La documentazione di AEM è creata e mantenuta in inglese americano.
* Usa frasi quanto più semplici possibile.
* Usa un linguaggio chiaro e conciso.

Ricorda che i lettori della documentazione dell’AEM sono di tutto il mondo e non ci si può aspettare che siano di madrelingua inglese o che parlino inglese correntemente. Evita i colloquialismi e usa un linguaggio chiaro e semplice.

#### Segui il Manuale di stile di Microsoft®

[Manuale di stile di Microsoft®](https://learn.microsoft.com/en-us/style-guide/welcome/) è una guida di stile per la documentazione disponibile gratuitamente, specifica per la documentazione di software. La documentazione AEM segue questa guida quando possibile.

### Formattazione

| Elemento | Stile |
|---|---|
| Elemento o opzione dell’interfaccia utente | **grassetto** |
| Nome file, percorso, input utente, valori di parametri | `monospaced` |
| Codice, riga di comando | ```Code Block``` |

### Schermate

Le schermate devono essere utilizzate con cautela e solo quando una descrizione testuale è insufficiente.

Nelle schermate non devono essere utilizzati marcatori o altre annotazioni (come riquadri rossi, frecce o testo). In questo modo le schermate possono essere riutilizzate o replicate più facilmente nelle versioni localizzate della documentazione.

### Riferimenti a specifiche versioni

È meglio evitare, quando possibile, riferimenti diretti a una versione specifica nel contenuto della documentazione. In tal modo la documentazione sarà più flessibile e potrà essere estesa anche a versioni future.

### Utilizzo di Day, AEM, CQ, CRX

Fai sempre riferimento al prodotto con il suo nome completo **Adobe Experience Manager** per la prima volta in un articolo, successivamente, può essere chiamato **AEM**.

Day, Day Software, CQ e CRX non devono essere utilizzati a meno che non sia inevitabile, ad esempio nei nomi di classi o in riferimenti specifici a versioni storiche di AEM.