---
title: Definizioni relative alle versioni di aggiornamento
description: Questo articolo descrive i vari tipi di versioni di [!DNL Experience Manager] tra cui versioni complete, Feature Pack e Service Pack.
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: ce1026216ccb79a3c268b3f6b24698fa3a3388dc
workflow-type: ht
source-wordcount: '730'
ht-degree: 100%

---

# Definizioni relative alle versioni di aggiornamento di [!DNL Experience Manager]  {#update-release-vehicle-definitions}

Questo documento contiene informazioni dettagliate sui vari tipi di versioni di [!DNL Adobe Experience Manager], tra cui versioni complete, Feature Pack e Service Pack che [!DNL Adobe] distribuisce ai clienti.

>[!NOTE]
>
>Per la pianificazione delle versioni di aggiornamento di [!DNL Experience Manager], fai riferimento alla roadmap delle versioni di aggiornamento di [[!DNL Experience Manager] ](update-releases-roadmap.md)

## Versione completa {#full-release}

| Elementi | Descrizione |
|-------|------|
| Definizione | <ul> <li> Versione pianificata </li> <li> Supporta i percorsi di aggiornamento per versioni specifiche, definiti nelle note sulla versione </li> </ul> |
| Denominazione | <ul> <li> I numeri di versione per le release principali aumentano in base alla formula X+1.Y.Z. </li> <li> I numeri di versione per le release minori aumentano in base alla formula X.Y+1.Z </li> </ul> Dove X è il numero di versione principale, Y è il numero di versione secondario e Z il numero di patch. |
| Comprende | <ul> <li> Nuove funzioni </li> <li>  Miglioramenti </li> <li>  Correzioni di bug </li> </ul> |
| Documentazione | <ul> <li> Le note sulla versione sono disponibili nel portale della documentazione </li> <li> La documentazione su funzioni, miglioramenti e correzioni di bug è disponibile nel portale della documentazione </li> </ul> |
| Cadenza | Annuale |
| Disponibilità e installazione | <ul> <li> Fornito come programma di installazione autonomo </li> <li>  Disponibile dal sito web delle licenze e da Managed Services </li> <li> Il sito web delle licenze può richiedere la migrazione dell’archivio dei contenuti </li> </ul> |
| Livello di test | Completamente convalidato tramite QA |

## Service Pack {#service-pack}

| Elemento | Descrizione |
|-----|-----|
| Definizione | <ul> <li> Versione pianificata </li> <li> Attualmente non è possibile eseguire il rollback </li> </ul> |
| Denominazione | <ul> <li> Il numero di versione della patch è identificato da un numero a una cifra </li> <li> Dopo l’installazione, aumenterà la cifra del numero di versione della patch installata, in base alla formula X.Y.Z.SPx </li> </ul> Dove X è il numero di versione principale, Y è il numero di versione secondario e Z il numero di patch. x è il numero del service pack. |
| Comprende | <ul> <li> Nuove funzioni</li> <li>  Miglioramenti </li> <li> Correzioni di bug </li> <li> Feature Pack di interesse comune (se presenti) </li> </ul> |
| Documentazione | <ul> <li> Le note sulla versione sono disponibili nel portale della documentazione </li> <li> La documentazione su funzioni, miglioramenti, correzioni di bug si trova nel portale della documentazione </li> </ul> |
| Cadenza | Trimestrale |
| Disponibilità e installazione | <ul> <li> Consegnato come pacchetto </li> <li> Disponibile su Software Distribution</li> <li>  Richiede un’installazione esistente funzionante </li> </ul> |
| Livello di test | <ul> <li> Tutte le correzioni sono convalidate tramite QA </li> <li>  Integrità complessiva del pacchetto con esecuzioni in automazione </li> </ul> |

## Cumulative Fix Pack  {#cumulative-fix-pack-aem}

| Elemento | Descrizione |
|-----|-----|
| Definizione | <ul> <li> Modello di consegna singola delle correzioni rilasciate </li> <li> Pacchetto di contenuti aggregatore che comprende il pacchetto di contenuto di singoli componenti </li> <li>  I CFP comprendono gli hotfix ma non contengono miglioramenti delle funzioni.  </li> </ul> |
| Denominazione | X.Y.Z.CFPx <br> Dove X è il numero di versione principale, Y è il numero di versione secondaria e Z il numero della patch. x è il numero del Service Pack cumulativo. |
| Comprende | Il CFP è un fix pack cumulativo contenente le correzioni di tutti i componenti apportate in un periodo di tempo specificato. Ad esempio, se un cliente applica CFP3, allora CFP3 = CFP1 + CFP2. |
| Documentazione | Le note sulla versione sono disponibili nel portale della documentazione |
| Cadenza | Trimestrale |
| Disponibilità e installazione | <ul> <li> Consegnato come pacchetto </li> <li>  Disponibile su Software Distribution </li> <li>  A seconda dell’ultimo service pack rilasciato </li> <li>  Il CFP è indipendente. I clienti non devono preoccuparsi di trovare/risolvere le dipendenze. Il CFP deve essere installato sull’ultimo Service Pack rilasciato. </li> <li>  Il CFP può essere installato come pacchetto singolo, per una migliore esperienza del cliente.  </li> </ul> |
| Livello di test | Convalidato tramite QA a livello di integrazione e test di regressione |

## Sovrapposizione {#overlay}

| Elemento | Dettagli |
|-------|--------|
| Denominazione | overlay-&lt;ID ticket> |
| Comprende | Correzione di bug per un file JS o JSP |
| Documentazione | Nessuna |
| Cadenza | Secondo necessità |
| Disponibilità e installazione | <ul> <li> Fornito come pacchetto dall’Assistenza clienti di [!DNL Experience Manager]  </li> <li> Non necessariamente incluso nei service pack o nelle versioni complete </li> </ul> |
| Livello di test | Convalidato dall’Assistenza clienti |

## Feature Pack {#feature-pack}

| Elementi | Dettagli |
|--------|-----|
| Definizione | <ul> <li>I Feature Pack comprendono funzionalità aggiuntive e vengono forniti tramite Service Pack. Se per una versione di [!DNL Experience Manager] è stato rilasciato l’ultimo service pack, Adobe non fornirà più ulteriori feature pack. </li> <li> I FP contengono miglioramenti del prodotto, pianificati per essere inseriti in una versione successiva del prodotto, ma consegnati in anticipo in base alla decisione di [!DNL Adobe's] Product Management.</li> <li>  Le funzioni vengono sempre inserite nella versione principale successiva e quindi portate alla versione di [!DNL Experience Manager] richiesta dal cliente. </li> <li>  I feature pack di interesse comune e disponibilità generale (GA) vengono uniti nel service pack successivo.  </li> </ul> |
| Denominazione | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Comprende | <ul> <li> Nuove funzioni </li> <li> Miglioramenti </li> <li> Correzioni di bug (aggiornamenti di prodotto incrementali) </li> </ul> |
| Documentazione | La documentazione è disponibile su adobe.com. |
| Cadenza | Varia a seconda dell’area prodotto |
| Disponibilità e installazione | <ul> <li>Consegnato tramite Service Pack </li> <li> Disponibile su Software Distribution. I clienti accettano i Termini e Condizioni [!DNL Adobe's] attraverso Software Distribution. </li> </ul> |
| Livello di test | I pacchetti di funzioni per la disponibilità generale (GA) sono convalidati tramite QA. |

* 1: Le correzioni Oak non vengono distribuite come singoli hot fix. Tuttavia, sono incluse nel successivo hotfix cumulativo di OAK. Se necessario, è possibile mettere a disposizione una build diagnostica oltre al COFP più recente. La condizione preliminare è che il cliente disponga del COFP più recente e lo utilizzi. Le build diagnostiche forniscono solo lo stesso livello di garanzia qualità di un hotfix. Pertanto, non forniscono lo stesso livello di qualità di un Cumulative Fix Pack, di un Service Pack o di una versione del prodotto. La correzione definitiva viene fornita con il successivo CFP.
