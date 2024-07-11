---
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 54%

---
# Linee guida per contribuire alla documentazione di Adobe Experience Manager

## Filosofia della documentazione

Gli utenti di Adobe Experience Manager lavorano in ambienti altamente competitivi per creare esperienze digitali che li distinguano dalla concorrenza. Pertanto, quando Adobe introduce nuovi strumenti avanzati nell’AEM, fornisce una documentazione accurata e chiara. Questo approccio consente ai clienti di utilizzare immediatamente il proprio investimento AEM e massimizzare il ROI.

Per la documentazione di AEM, l’obiettivo è renderla disponibile agli utenti della soluzione il prima possibile. Viene quindi creata una documentazione accurata e fruibile, continuamente aggiornata e migliorata.

## Contributi alla documentazione

Al fine di migliorare continuamente la documentazione di AEM, apprezziamo il contributo dell’intera comunità di utenti AEM. I miglioramenti apportati alla documentazione, che derivino da richieste o segnalazioni di problemi, possono essere correzioni, chiarimenti, ampliamenti e altri esempi.

## Standard della documentazione

L’Adobe accoglie con favore i contributi alla documentazione. Qualsiasi contributo alla documentazione dell’AEM, sia esso una richiesta pull o un problema, deve essere conforme agli standard in materia di contributi e documentazione di Adobe.

I contributi che non soddisfano tali standard possono essere rifiutati.

### Adobe scrive sui casi d’uso standard.

La documentazione di AEM riguarda i casi d’uso standard. I casi di utilizzo che esulano dall’ambito di installazione e utilizzo standard del prodotto non rientrano nella documentazione di AEM.

### In genere Adobe non documenta i bug o le relative soluzioni.

La documentazione di AEM riguarda i casi d’uso standard. Per questo motivo, i bug, gli effetti causati dai bug e le soluzioni per ovviare ai bug non sono documentati.

Fanno eccezione le note sulla versione, in cui possono essere elencati i problemi noti con possibili soluzioni approvate dal team di gestione del prodotto AEM.

### I contributi alla documentazione non devono essere usati per rispondere a domande tecniche.

È gradita come contributo qualsiasi idea che punti al miglioramento della documentazione di AEM. Tuttavia, commenti, problemi e richieste sono intesi per *contributi* solo. L’obiettivo non è quello di rispondere a domande su come utilizzare l’AEM, implementare un progetto AEM o risolvere problemi tecnici.

Segnala eventuali domande sull’utilizzo dell’AEM o errori tecnici utilizzando [Portale di supporto Experience Cloud Enterprise](https://experienceleague.adobe.com/i?support-solution=General#support). Oppure, utilizza [community Experienci Manager](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community?lang=it).

***I contributi alla documentazione di AEM non sostituiscono l’Assistenza clienti di Adobe***. Pertanto, verranno rifiutati tutti i contributi che richiedono risposte a domande correlate al supporto.

### I contributi devono fare riferimento in modo chiaro alle pagine della documentazione interessate.

Se apri una segnalazione problema per suggerire miglioramenti alla documentazione, includi i collegamenti alle pagine interessate. Se si crea un problema utilizzando **Modifica questa pagina** su una pagina della documentazione, il problema viene creato automaticamente con un collegamento alla pagina.

Questo processo non si applica alle richieste pull, che per loro natura fanno riferimento alla pagina o alle pagine interessate.

## Linee guida per la documentazione

Qualsiasi contributo alla documentazione deve seguire determinate linee guida di stile.

L’aderenza a queste linee guida semplifica la revisione del contributo e velocizza quindi l’integrazione nella documentazione.

### Lingua e stile

#### Lingua

* La documentazione di AEM è creata e mantenuta in inglese americano.
* Usa frasi quanto più semplici possibile.
* Usa un linguaggio chiaro e conciso.

Ricorda che la documentazione di AEM viene letta in tutto il mondo da persone che potrebbero non essere di madrelingua inglese o non parlare inglese correntemente. Evita le espressioni colloquiali e usa un linguaggio chiaro e semplice.

#### Segui il manuale di stile di Microsoft®

[Il manuale di stile di Microsoft®](https://learn.microsoft.com/it-it/style-guide/welcome/) è una guida di stile per la documentazione disponibile gratuitamente, specifica per la documentazione di software. La documentazione di AEM segue questa guida quando possibile.

### Formattazione

| Elemento | Stile |
|---|---|
| Elemento o opzione dell’interfaccia utente | **grassetto** |
| Nome file, percorso, input utente, valori di parametri | `monospaced` |
| Codice, riga di comando | ```Code Block``` |

### Schermate

Le schermate vanno utilizzate in modo non eccessivo e solo quando una descrizione testuale è insufficiente.

Nelle schermate non devono essere utilizzati marcatori o altre annotazioni (come riquadri rossi, frecce o testo). In questo modo le schermate possono essere riutilizzate o replicate più facilmente nelle versioni localizzate della documentazione.

### Riferimenti a specifiche versioni

Se possibile, evita riferimenti diretti a una versione specifica in tutto il contenuto della documentazione. Questo approccio rende la documentazione più flessibile ed estensibile per le versioni future.

### Utilizzo di Day, AEM, CQ, CRX

Quando citi il prodotto per la prima volta in un articolo, utilizza sempre il suo nome completo, **Adobe Experience Manager**. Dopodiché, potrai fare riferimento a essa come **AEM**.

Day, Day Software, CQ e CRX non devono essere utilizzati a meno che non sia inevitabile, ad esempio nei nomi di classi o in riferimenti specifici a versioni storiche di AEM.