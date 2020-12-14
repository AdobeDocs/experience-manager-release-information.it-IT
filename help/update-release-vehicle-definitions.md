---
title: Aggiorna definizioni veicolo di rilascio
description: Questo articolo descrive i vari tipi di rilasci  [!DNL Experience Manager] inclusi rilasci completi, pacchetti di funzioni e Service Pack.
contentOwner: AK
translation-type: tm+mt
source-git-commit: 11ff4f7d66038a80697afe5f104c560137e130f4
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 5%

---


# [!DNL Experience Manager] aggiornamento delle definizioni del veicolo  {#update-release-vehicle-definitions}

Questo documento contiene informazioni dettagliate sui vari tipi di [!DNL Adobe Experience Manager] rilasci, inclusi i rilasci completi, i pacchetti di funzioni e i service pack che [!DNL Adobe] distribuiscono ai clienti.

>[!NOTE]
>
>Per la pianificazione delle versioni di aggiornamento di [!DNL Experience Manager], fare riferimento alla tabella di marcia delle [[!DNL Experience Manager] versioni di aggiornamento](update-releases-roadmap.md)

## Versione completa {#full-release}

| Elementi | Descrizione |
|-------|------|
| Definizione | <ul> <li> Rilascio pianificato </li> <li> Supporta i percorsi di aggiornamento per versioni specifiche, definiti nelle note sulla versione </li> </ul> |
| Denominazione | <ul> <li> I numeri di versione per le release principali aumentano in base alla formula X+1.Y.Z. </li> <li> I numeri di versione per rilasci minori aumentano in base alla formula X.Y+1.Z </li> </ul> Dove X è il numero di versione principale, Y è il numero di versione secondario e Z il numero di patch. |
| Inclusioni | <ul> <li> Nuove funzioni </li> <li>  Miglioramenti </li> <li>  Correzioni di bug </li> </ul> |
| Documentazione | <ul> <li> Le note sulla versione sono disponibili nel portale della documentazione </li> <li> La documentazione su funzioni, miglioramenti e correzioni di bug è disponibile nel portale della documentazione </li> </ul> |
| Cadenza | Annuale |
| Disponibilità e installazione | <ul> <li> Fornito come programma di installazione autonomo </li> <li>  Disponibile dal sito Web delle licenze e da Managed Services </li> <li> Il sito Web delle licenze può richiedere la migrazione dell&#39;archivio dei contenuti </li> </ul> |
| Livello di test | Completamente convalidato da QA |

## Service Pack {#service-pack}

| Elemento | Descrizione |
|-----|-----|
| Definizione | <ul> <li> Rilascio pianificato </li> <li> Attualmente non è possibile eseguire il rollback </li> </ul> |
| Denominazione | <ul> <li> Numero di rilascio della patch: numero a una cifra </li> <li> Dopo l&#39;installazione, aumenterà la cifra della patch del numero di rilascio installata, in base alla formula X.Y.Z.SPx </li> </ul> Dove X è il numero di versione principale, Y è il numero di versione secondario e Z il numero di patch. x è il numero del service pack. |
| Inclusioni | <ul> <li> Nuove funzioni</li> <li>  Miglioramenti </li> <li> Correzioni di bug </li> <li> Pacchetti di funzioni di interesse comune (se presenti) </li> </ul> |
| Documentazione | <ul> <li> Note sulla versione disponibili nel portale della documentazione </li> <li> Documentazione su funzioni, miglioramenti, correzioni di bug nel portale della documentazione </li> </ul> |
| Cadenza | Trimestrale |
| Disponibilità e installazione | <ul> <li> Consegnato come pacchetto </li> <li> Disponibile su Distribuzione software</li> <li>  Richiede l&#39;installazione funzionale esistente </li> </ul> |
| Livello di test | <ul> <li> Tutte le correzioni QA convalidate </li> <li>  Integrità complessiva del pacchetto con le esecuzioni di automazione </li> </ul> |

## Cumulative Fix Pack  {#cumulative-fix-pack-aem}

| Elemento | Descrizione |
|-----|-----|
| Definizione | <ul> <li> Modello di consegna singola delle correzioni di rilascio </li> <li> Pacchetto di contenuti di aggregazione contenente il pacchetto di contenuti di singoli componenti </li> <li>  I CFP sono il rollover delle correzioni rapide e non ne fanno parte alcun miglioramento.  </li> </ul> |
| Denominazione | X.Y.Z.CFPx <br> Dove X è il numero di versione principale, Y è il numero di versione secondario e Z il numero della patch. x è il numero cumulativo del Service Pack. |
| Inclusioni | CFP è un fix pack cumulativo contenente correzioni di tutti i componenti per un periodo di tempo specificato. Ad esempio, se un cliente applica CFP3, CFP3 = CFP1 + CFP2. |
| Documentazione | Note sulla versione disponibili nel portale della documentazione |
| Cadenza | Trimestrale |
| Disponibilità e installazione | <ul> <li> Consegnato come pacchetto </li> <li>  Disponibile su Distribuzione software </li> <li>  A seconda dell&#39;ultimo service pack rilasciato </li> <li>  Il CFP dipende da se stesso. I clienti non devono preoccuparsi di trovare/risolvere dipendenze. Il CFP deve essere installato nell&#39;ultimo Service Pack rilasciato. </li> <li>  CFP può essere installato come pacchetto singolo, migliorando l&#39;esperienza dei clienti.  </li> </ul> |
| Livello di test | QA convalidato a livello di integrazione e test di regressione |

## Sovrapposizione {#overlay}

| Elemento | Dettagli |
|-------|--------|
| Denominazione | overlay-&lt;ID ticket> |
| Inclusioni | Correzione di bug per un file JS o JSP |
| Documentazione | Nessuno |
| Cadenza | Se necessario |
| Disponibilità e installazione | <ul> <li> Fornito come pacchetto dall&#39;Assistenza clienti [!DNL Experience Manager]  </li> <li> Non necessariamente incluso nei service pack o nelle versioni complete </li> </ul> |
| Livello di test | Convalidato dall&#39;Assistenza clienti |

## Feature Pack {#feature-pack}

| Elementi | Dettagli |
|--------|-----|
| Definizione | <ul> <li>I Feature Pack sono funzionalità aggiuntive e vengono forniti tramite Service Pack. Se una versione [!DNL Experience Manager] ha rilasciato l&#39;ultimo service pack,  Adobe non fornirà alcun feature pack per esso in futuro. </li> <li> I PQ contengono miglioramenti del prodotto, pianificati per una versione successiva del prodotto, ma consegnati in anticipo in base alla decisione di [!DNL Adobe's] Product Management.</li> <li>  Le funzioni vengono sempre unite alla versione principale successiva e quindi portate alla versione [!DNL Experience Manager] richiesta dal cliente </li> <li>  I pacchetti di funzioni di interesse comune e GA vengono uniti nel service pack successivo  </li> </ul> |
| Denominazione | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inclusioni | <ul> <li> Nuove funzioni </li> <li> Miglioramenti </li> <li> Correzioni di bug (aggiornamenti di prodotto incrementali) </li> </ul> |
| Documentazione | La documentazione è disponibile su adobe.com. |
| Cadenza | Varia con area prodotto |
| Disponibilità e installazione | <ul> <li>Consegnato tramite Service Pack </li> <li> Disponibile su Distribuzione software. I clienti accettano [!DNL Adobe's] Termini e Condizioni attraverso la distribuzione del software. </li> </ul> |
| Livello di test | I pacchetti di funzioni Disponibilità generale sono convalidati dal QA. |

* 1: Le correzioni OAK non vengono distribuite come singole correzioni rapide. Tuttavia, sono inclusi nella successiva correzione cumulativa per la quercia. Se necessario, è possibile mettere a disposizione una build diagnostica oltre al COFP più recente. La condizione preliminare è che il cliente abbia eseguito il COFP più recente. Le build diagnostiche forniscono solo lo stesso livello di garanzia qualità di una correzione rapida. Pertanto, non forniscono lo stesso livello di garanzia qualità di un fix pack cumulativo, service pack o release del prodotto. La correzione finale viene fornita con il successivo CFP.
