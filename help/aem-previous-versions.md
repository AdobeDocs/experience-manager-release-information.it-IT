---
title: Versioni precedenti di AEM, CQ e CRX
description: Documentazione per le versioni precedenti di Adobe Experience Manager, CQ e CRX.
translation-type: tm+mt
source-git-commit: 47b391ed659264b611f08d2fa9e45a923be5c445
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 26%

---


# Versioni precedenti di [!DNL Adobe Experience Manager], CQ e CRX {#older-versions-aem-cq-crx}

## Versioni precedenti della documentazione [!DNL Experience Manager] {#older-version-aem-documentation}

Le versioni di [!DNL Experience Manager], CQ e CRX elencate in questa pagina sono End of Life e non sono più ufficialmente vendute da  Adobe. Le ultime versioni della documentazione ufficiale per queste versioni precedenti sono comunque disponibili per gli utenti che possono averne bisogno. È consigliabile eseguire l&#39;aggiornamento alla versione più recente (che attualmente è [[!DNL Experience Manager] 6.5](https://experienceleague.adobe.com/docs/experience-manager-65.html)).

>[!NOTE]
>
>Per sapere quando una versione [!DNL Experience Manager] avrà termine il supporto di base, consulta [prodotti e periodi di supporto tecnico](https://helpx.adobe.com/it/support/programs/eol-matrix.html) e cerca `AEM`.

### Prima dell’installazione {#before-installation}

Prima di scaricare il pacchetto, verificare chi utilizzerà il contenuto. Questa decisione determinerà come verrà distribuito:

* Gli sviluppatori possono eseguire una installazione locale per riferimento rapido.
* Per esigenze di documentazione aziendale più ampie, è consigliabile che il pacchetto venga distribuito su un’istanza AEM Author non di produzione accessibile internamente.

>[!NOTE]
>
>Gli utenti devono essere connessi all&#39;istanza [!DNL Experience Manager] per accedere a questo contenuto in [!DNL Experience Manager] Autore. Per impostazione predefinita questo contenuto non è accessibile su AEM Publish (in quanto esiste in /libs).

## Posizioni di distribuzione software {#software-distribution-locations}

Sarà necessario un Adobe ID  valido:

* Se non disponete di un Adobe ID , potete crearne uno all&#39;indirizzo www.adobe.com
Per assistenza nella creazione o nella gestione dell&#39;Adobe ID , [fare riferimento a questa guida](https://helpx.adobe.com/manage-account.html)

| [!DNL Experience Manager] Versione | Collegamento di distribuzione software |
|:-----------:|:--------------------------------------------------:|
| [!DNL Experience Manager] 6.1 | [Scarica AEM-DOCS-6.1 da Distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-1.zip) |
| [!DNL Experience Manager] 6,0 | [Scarica AEM-DOCS-6.0 da Distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-0.zip) |
| [!DNL Experience Manager] 5.6.1 | [Scarica AEM-DOCS-5.6.1 da Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6-1.zip) |
| [!DNL Experience Manager] 5,6 | [Scarica AEM-DOCS-5.6 da Distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6.zip) |
| CQ 5.5 | [Scarica CQ-DOCS-5.5 da Distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Faem-docs%2Faem-docs-5-5.zip) |
| CQ 5.4 | [Scarica CQ-DOCS-5.4 da Distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-4.zip) |
| CQ 5.3 | [Scarica CQ-DOCS-5.3 da Distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-3.zip) |
| CRX 2.3 | [Scarica CQ-DOCS-2.3 da Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-3.zip) |
| CRX 2.2 | [Scarica CQ-DOCS-2.2 da Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-2.zip) |
| CRX 2.1 | [Scarica CQ-DOCS-2.1 da Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-1.zip) |
| CRX 2.0 | [Scarica CQ-DOCS-2.0 da Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-0.zip) |

## Come installare un pacchetto di documentazione {#how-to-install-documentation-package}

Per installare un pacchetto di documentazione legacy, è necessario che [!DNL Experience Manager] sia installato ed in esecuzione sull&#39;unità locale o di rete.

### Scaricare il pacchetto di documentazione {#download-documentation-package}

1. Dalla tabella precedente, selezionate il collegamento per la versione della documentazione [!DNL Experience Manager] da scaricare. Ad esempio, AEM 5.6.1.

1. Effettuate il login utilizzando il vostro Adobe ID . Se non disponi di un ID, creane uno.

1. Selezionare il pulsante **[!UICONTROL Download]**.

1. Esempio di ciò che verrà visualizzato:

![Esempio di distribuzione del software](assets/screen_shot_2020-07-10at161922.jpg)

### Installare il pacchetto nell&#39;istanza locale {#install-package-local-instance}

1. Aprite l&#39;interfaccia utente [!DNL Experience Manager]. In un browser Web immettete: `http://localhost:4502/`. Effettua l’accesso come Amministratore.

1. Seleziona **[!UICONTROL Strumenti]** > **[!UICONTROL Distribuzione]** > **[!UICONTROL Pacchetti]**.

1. Dall’interfaccia utente per la gestione dei pacchetti, seleziona **[!UICONTROL Carica pacchetto]**.

1. Individua il percorso in cui hai scaricato il pacchetto AEM 5.6.1 (AEM-docs-5-6-1.zip).

1. Seleziona il pacchetto e fai clic su **[!UICONTROL OK]**.

1. Una volta che il pacchetto è stato caricato, sarà necessario installarlo.

1. Nell’interfaccia utente per la gestione dei pacchetti, individua il pacchetto e seleziona **[!UICONTROL Installa]**.

1. Nella finestra di dialogo di conferma, selezionare di nuovo **[!UICONTROL Installa]**. Nota: l’installazione richiederà alcuni minuti.

1. In un browser Web, avviate la pagina della documentazione. Utilizzando l’esempio AEM 5.6.1, l’URL sarebbe: http://localhost:4502/libs/aem-docs/content/en/cq/5-6-1.html.

## Richiedi aiuto dalla community [!DNL Experience Manager] {#get-help-from-aem-community}

In caso di domande sull&#39;utilizzo  Experience Manager, ti consigliamo di [contattare i nostri esperti della community nei  [!DNL Experience Manager] forum](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community).
