---
title: Installazione di Cumulative Fix Pack in AEM Forms JEE
description: Riepilogo dei passaggi d’installazione e configurazione di Cumulative Fix Pack (CFP) in AEM Forms JEE.
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 437dad5fffe71592b6f9f9b4099a253e3a55b0c8
workflow-type: ht
source-wordcount: '909'
ht-degree: 100%

---

# Installazione di Cumulative Fix Pack in AEM [!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## Installare CFP in AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Per installare il Cumulative Fix Pack su AEM 6.3 [!DNL Forms JEE], esegui la sequenza di passaggi seguente.

1. Per ottenere il programma di installazione di AEM 6.3 [!DNL Forms JEE] per il CFP, contatta il [Supporto Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=homehome?lang=it#support).
1. Esegui il programma di installazione del Cumulative Fix Pack e configura AEM [!DNL Forms JEE] come descritto in [Installare e configurare AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Installare la versione più recente di AEM CFP 6.3.3.x
1. Installare il pacchetto del componente aggiuntivo [!DNL Forms] per AEM CFP [6.3.3.x](aem-forms-releases.md)

### Installare il pacchetto di bundle AEM [!DNL Forms JEE] {#install-aem-forms-jee-bundles-package}

Il pacchetto [!DNL  Forms JEE] per AEM (aemfd-jee-bundles-package-6.3CFP1; versione 1.0.2) fornisce all’[!DNL Forms] utente su AEM [!DNL Forms JEE] gli stessi diritti e le stesse funzionalità disponibili in AEM [!DNL Forms OSGi]. Verifica i pacchetti installati in Gestione pacchetti e installa il pacchetto se non è già installato.

### Istruzioni aggiuntive per CQ-4208044 {#additional-instructions-for-cq}

Se si utilizza un server per AEM 6.3 [!DNL Forms JEE] con database Oracle, configura le seguenti impostazioni successivamente alla distribuzione di CFP1, ovvero dopo l’esecuzione di Configuration Manager. Questa impostazione è necessaria per sincronizzare utenti, gruppi e membri di gruppi quando viene eseguita la sincronizzazione di un dominio aziendale.

1. Accedi all’interfaccia utente **Amministratore**.
1. Passa a **[!UICONTROL Impostazioni]** > **[!UICONTROL Gestione utente]** > **[!UICONTROL Configurazione]** > **[!UICONTROL Import and Export Configuration File]** (Importa ed esporta file di configurazione).
1. Esporta il file config.xml.
1. Modifica la voce “`groupMemberDBQueryBatchSize`” nelle configurazioni del dominio in *config.xml*. Voce di esempio:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. Importa di nuovo il file modificato ed esegui nuovamente la sincronizzazione.

## Installare CFP in AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Per installare il Cumulative Fix Pack su AEM 6.2 [!DNL Forms JEE], esegui la sequenza di passaggi seguente.

1. Per ottenere il programma di installazione di AEM 6.2 [!DNL Forms JEE] per il CFP, contatta il [Supporto Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=homehome?lang=it#support).
1. Esegui il programma di installazione del Cumulative Fix Pack e configura AEM [!DNL Forms JEE] come descritto in [Installare e configurare AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Installa AEM Hotfix 12785 versione 7.0.
1. Installa AEM 6.2 Service Pack 1.
1. Installa l’ultimo pacchetto release-notes-aem-6-2-cumulative-fix-pack.md.
1. Installa il pacchetto del componente aggiuntivo [!DNL Forms] per AEM 6.2 Service Pack 1 CFP.

### Installare il pacchetto di bundle AEM [!DNL Forms JEE] {#install-aem-forms-jee-bundles-package-1}

Il pacchetto JEE per AEM Forms (aemfd-jee-bundles-package-6.2CFP5; versione 1.0.2) fornisce all’[!DNL Forms] utente su AEM [!DNL Forms JEE] gli stessi diritti e le stesse funzionalità disponibili in AEM [!DNL Forms OSGi]. Verifica i pacchetti installati in Gestione pacchetti e installa il pacchetto se non è già installato.

### Configurazione del timeout per le operazioni a livello di componente (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Dopo AEM 6.2 CFP4, puoi utilizzare le seguenti istruzioni per configurare il timeout per operazioni DSC, qualora si verifichino problemi dovuti a errori di timeout durante il processo di aggiornamento.

L’implementazione di DSC richiede un intervallo tempo variabile e, per questo motivo, potrebbe non riuscire. Per modificare il valore di timeout per le operazioni DSC come l’installazione, il caricamento, l’avvio e l’arresto, è necessario impostare `adobe.component.registry.timeout` utilizzando l’argomento JVM con l’opzione -D.

Specifica il valore relativo alla chiave in secondi. Esempio: `-Dadobe.component.registry.timeout=300`

È inoltre possibile modificare i valori di timeout a livello di componente utilizzando le tre proprietà seguenti:

1. `adobe.all-component.timeout`: sovrascrive i valori di timeout di tutti i servizi del prodotto.
1. `adobe.<serviceName>.timeout`: sovrascrive il valore di timeout solo per il servizio (&lt;serviceName>) indicato nella chiave. Se il valore è impostato a livello di servizio, questo comando sovrascrive solo il valore di timeout relativo al servizio specificato, se impostato a livello di applicazione.
1. `adobe.<serviceName>.<operationName>.timeout`: sovrascrive solo il valore di timeout relativo all’operazione del servizio (&lt;serviceName>.&lt;operationName>) indicato nella chiave. Se il valore è impostato a livello di operazione, questo comando sovrascrive solo il valore di timeout relativo al servizio specificato, se impostato a livello di applicazione o di servizio.

**Esempi:**

Utilizza i seguenti comandi per impostare il valore di timeout a livello di componente:

1. Per impostare su 600 sec il valore di timeout per tutte le operazioni del servizio:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Per impostare su 500 sec i valori di timeout dell’operazione `DesigntimeService`:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Per impostare su 700 sec i valori di timeout dell’operazione `DesigntimeService's previewLCA`:

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Per impostare su 600 secondi il `DSC operations`, come il caricamento e l’installazione, utilizza:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## Installare e configurare AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Esegui una copia di backup della cartella /deploy. Sarà necessaria se decidi di disinstallare la correzione rapida.
1. Arresta il server applicazioni.
1. Estrai sul disco rigido il file archivio del programma di installazione della patch.
1. Nella directory denominata in base al sistema operativo in uso:

   **Windows**

   Passa alla directory appropriata sul supporto di installazione o sulla cartella del disco rigido in cui è stato copiato il programma di installazione:

   * (`Windows 32-bit`): `Disk1\InstData\Windows\VM`
   * (`Windows 64-bit`): `Disk1\InstData\Windows_64bit\VM`

   Quindi, fai doppio clic sul file denominato:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux®, Solaris™, AIX®**

   Passa alla directory appropriata:

   * (Linux®): Disk1/InstData/Linux/ NoVM
   * (Solaris™): Disk1/InstData/Solaris/ NoVM
   * (AIX®): Disk1/InstData/AIX/VM

   Da un prompt dei comandi digita:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Viene avviata la procedura guidata di installazione per fornirti una guida.

1. Nel pannello introduttivo, fai clic su **[!UICONTROL Avanti]**.
1. Nella schermata Scegli cartella di installazione, verifica che la posizione predefinita visualizzata sia corretta per l’installazione esistente. Oppure fai clic su **[!UICONTROL Sfoglia]** per selezionare la cartella alternativa in cui è installato AEM [!DNL Forms] , quindi fai clic su **[!UICONTROL Successivo]**.
1. Leggi le informazioni di riepilogo della patch di correzione rapida e fai clic su **[!UICONTROL Avanti]**.
1. Leggi le informazioni di riepilogo di pre-installazione e fai clic su **[!UICONTROL Installa]**.
1. Al termine dell’installazione, fai clic su **[!UICONTROL Avanti]** per applicare gli aggiornamenti della correzione rapida ai file installati.
1. La casella di controllo Avvia Configuration Manager è selezionata per impostazione predefinita. Fai clic su **[!UICONTROL Fine]** per eseguire Configuration Manager.

   Per eseguire Configuration Manager in un secondo momento, deseleziona l’opzione **[!UICONTROL Avvia Configuration Manager]** prima di fare clic su **[!UICONTROL Fine]**. È possibile avviare Configuration Manager in un secondo momento utilizzando lo script appropriato nella directory *`[AEM_forms_root]`/configurationManager/bin*.

1. In base al server applicazioni in uso, scegli uno dei seguenti documenti e segui le istruzioni riportate nella sezione *Configurazione e distribuzione di AEM [!DNL Forms]*.

   Per AEM [!DNL Forms] 6.3, consulta:

   * Installazione e distribuzione di AEM [!DNL Forms] per JBoss®
   * Installazione e distribuzione di AEM [!DNL Forms] per WebSphere®
   * Installazione e distribuzione di AEM [!DNL Forms] per WebLogic

1. Riavvia il server AEM [!DNL Forms] JEE.
