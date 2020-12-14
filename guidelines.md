---
source-git-commit: 65c8c0b9940f9d2e20234ccc65b1d819971ea52e
workflow-type: tm+mt
translation-type: tm+mt
source-wordcount: '752'
ht-degree: 5%

---
# Linee guida per il contributo alla documentazione Adobe Experience Manager

## Filosofia della documentazione

Sappiamo che gli utenti Adobe Experience Manager lavorano in ambienti altamente competitivi, cercando di creare esperienze digitali che li distinguano dalla concorrenza. Pertanto, è fondamentale che, quando  Adobe offre nuovi strumenti avanzati in AEM, questi strumenti siano integrati da una documentazione accurata e chiara che consenta al cliente di sfruttare immediatamente il proprio investimento AEM e massimizzare il ROI.

L&#39;obiettivo della documentazione AEM è mettere la documentazione nelle mani degli AEM utenti il prima possibile. Pertanto, diamo priorità a una documentazione accurata e utilizzabile e ci impegniamo a aggiornarla e a migliorarla continuamente.

## Contributi alla documentazione

Al fine di migliorare continuamente AEM documentazione, l&#39;intera comunità di utenti AEM è benvenuta a contribuire alla documentazione. Sia attraverso richieste pull o problemi, i miglioramenti alla documentazione possono essere correzioni, chiarimenti, espansioni ed esempi aggiuntivi.

## Standard di documentazione

Pur accogliendo con favore i contributi alla documentazione, qualsiasi contributo alla documentazione AEM, sotto forma di richiesta di pull o di un problema, dovrebbe essere conforme ai nostri standard di contributo e documentazione.

I contributi che non soddisfano tali standard possono essere rifiutati.

### Documentiamo i casi di utilizzo standard.

AEM documentazione riguarda i casi di utilizzo standard. I casi di utilizzo che esulano dall&#39;ambito di installazione e utilizzo standard del prodotto non fanno parte della documentazione AEM.

### In genere non documentiamo i bug o le loro soluzioni.

AEM documentazione riguarda i casi di utilizzo standard. Per questo motivo, i bug, gli effetti causati da bug e le soluzioni alternative per i bug non sono generalmente documentati.

Le eccezioni a questa regola si applicano alle note sulla versione in cui possono essere elencati i problemi noti con possibili soluzioni approvate da AEM Product Management.

### I contributi alla documentazione non sono destinati a rispondere a domande tecniche.

Qualsiasi idea che potresti dover migliorare AEM documentazione è gradita come contributo. Tuttavia, commenti, problemi e richieste pull sono destinati solo a *contributi*. Non sono destinati a rispondere alle tue domande su come usare AEM, implementare il tuo progetto AEM o risolvere problemi tecnici.

Eventuali domande sull&#39;utilizzo di errori AEM o tecnici possono essere segnalate attraverso il normale processo di assistenza tramite il [ portale di assistenza Enterprise Support del Experience Cloud](https://helpx.adobe.com/it/contact/enterprise-support.ec.html) o discusse nella [ comunità Experienci Manager](https://forums.adobe.com/community/experience-cloud/marketing-cloud/experience-manager).

***AEM contributi alla documentazione non sostituiscono  Adobe*** Careale per i clienti e qualsiasi contributo di questo tipo alla ricerca di risposte alle domande relative al supporto verrà rifiutato.

### I contributi devono fare riferimento in modo chiaro alle pagine della documentazione interessate.

Se si crea un problema per suggerire miglioramenti alla documentazione, è necessario includere collegamenti alle pagine interessate. Se apri una segnalazione problema utilizzando il collegamento **Modifica pagina** di una pagina della documentazione, il problema verrà creato automaticamente con un collegamento alla pagina in questione.

Ciò non si applica alle richieste pull, in quanto le richieste pull per loro natura fanno riferimento alle pagine interessate.

## Linee guida sulla documentazione

Chiediamo che qualsiasi contributo alla nostra documentazione segua determinate linee guida di stile.

Seguendo queste linee guida è più semplice rivedere il proprio contributo e l&#39;integrazione nella documentazione è quindi più rapida.

### Lingua e stile

#### Lingua

* AEM documentazione è creata e mantenuta in inglese americano.
* Tenete delle frasi il più semplici possibile.
* Tenete la lingua chiara e concisa.

Ricordate, i lettori di AEM documentazione sono in tutto il mondo e non ci si può aspettare che siano madrelingua o parlanti inglesi fluenti. Evitare i colloquialismi e mantenere la lingua il più possibile chiara e semplice.

#### Segui il manuale di stile di Microsoft

[Il Manuale di ](https://docs.microsoft.com/en-us/style-guide/welcome/) Styleis Microsoft è una guida di stile della documentazione disponibile liberamente che si concentra sulla documentazione del software e AEM la documentazione segue questa guida quando possibile.

### Formattazione

| Elemento | Stile |
|---|---|
| Elemento o opzione dell&#39;interfaccia utente | **grassetto** |
| Nome file, percorso, input utente, valori-parametro | `monospaced` |
| Codice, riga di comando | ```Code Block``` |

### Schermate

Le schermate devono essere utilizzate in modo appropriato e solo quando una descrizione testuale è insufficiente.

Non devono essere utilizzati marcatori o altre annotazioni nelle schermate (come cornici rosse, frecce o testo). In questo modo le schermate sono più facili da riutilizzare o replicare nelle versioni localizzate della documentazione.

### Riferimenti specifici per le versioni

Cercate di evitare, quando possibile, riferimenti diretti a una versione specifica nel contenuto della documentazione. Questo rende la documentazione più flessibile ed estensibile per le versioni future.

### Utilizzo di Day, AEM, CQ, CRX

Il prodotto deve sempre essere indicato con il nome completo **Adobe Experience Manager** per la prima volta in un articolo e può essere successivamente denominato **AEM**.

Day, Day Software, CQ e CRX non devono essere utilizzati a meno che non sia inevitabile, ad esempio nei nomi di classe o che faccia riferimento alla cronologia dei AEM.