---
title: Installazione di pacchetti di correzioni cumulative su  AEM Forms JEE
description: Riepilogo dei passaggi per installare e configurare Cumulative Fix Pack (CFP) in  AEM Forms JEE
contentOwner: AK
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 1%

---


# Installazione di pacchetti di correzioni cumulative su AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## Installare CFP in AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Effettuare le seguenti operazioni, nella sequenza specificata, per installare il fix pack cumulativo su AEM 6.3 [!DNL Forms JEE].

1. Per ottenere il programma di installazione AEM 6.3 [!DNL Forms JEE] per il CFP, contattare [ Adobe Support](https://www.adobe.com/account/sign-in.supportportal.html).
1. Eseguire il programma di installazione CFP e configurare AEM [!DNL Forms JEE] come descritto in [Installare e configurare AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Installare la versione più recente AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. Installare il pacchetto [!DNL Forms] Add-on per AEM CFP [6.3.3.x](aem-forms-releases.md)

### Installare AEM pacchetto [!DNL Forms JEE] pacchetti {#install-aem-forms-jee-bundles-package}

[[!DNL  Forms JEE] AEMpackage](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-bundles-package-6.3CFP1; versione 1.0.2) fornisce  [!DNL Forms] agli utenti AEM gli stessi diritti e  [!DNL Forms JEE] le stesse funzionalità di AEM  [!DNL Forms OSGi]. Controllate i pacchetti installati in Gestione pacchetti e installate il pacchetto se non è già installato.

### Istruzioni aggiuntive per CQ-4208044 {#additional-instructions-for-cq}

Se si utilizza AEM server 6.3 [!DNL Forms JEE] con  database Oracle, configurare le seguenti impostazioni dopo la distribuzione del CFP1, ovvero dopo l&#39;esecuzione di Configuration Manager. Questa impostazione è necessaria per sincronizzare utenti, gruppi e membri del gruppo quando viene eseguita la sincronizzazione del dominio Enterprise. Consultate il problema CQ-4208044 nelle note sulla versione di [AEM 6.3](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205).

1. Accedete all&#39;interfaccia **Admin**.
1. Passare a **[!UICONTROL Impostazioni]** > **[!UICONTROL Gestione utente]** > **[!UICONTROL Configurazione]** > **[!UICONTROL Importa ed esporta file di configurazione]**
1. Esportate il file config.xml.
1. Modificare la voce per &quot; `groupMemberDBQueryBatchSize`&quot; nelle configurazioni del dominio in *config.xml*. Voce di esempio:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. Importare di nuovo il file modificato ed eseguire nuovamente la sincronizzazione.

## Installare CFP in AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Effettuare le seguenti operazioni, nella sequenza specificata, per installare il fix pack cumulativo su AEM 6.2 [!DNL Forms JEE].

>[!NOTE]
>
>Se si utilizza AEM 6.2 [!DNL Forms OSGi], seguire le istruzioni di installazione in [AEM 6.2 Note sulla versione CFP.](release-notes-aem-6-2-cumulative-fix-pack.md)

1. Per ottenere il programma di installazione AEM 6.2 [!DNL Forms JEE] per il CFP, contattare [ Adobe Support](https://www.adobe.com/account/sign-in.supportportal.html).
1. Eseguire il programma di installazione CFP e configurare AEM [!DNL Forms JEE] come descritto in [Installare e configurare AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Installare [AEM Hotfix 12785 versione 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785).
1. Installare [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).
1. Installate la versione più recente di [AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md).
1. Installare il pacchetto [!DNL Forms] Add-on per [AEM 6.2 Service Pack 1 CFP](aem-forms-releases.md).

### Installare AEM pacchetto [!DNL Forms JEE] pacchetti {#install-aem-forms-jee-bundles-package-1}

[ pacchetto](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24)  AEM Forms JEE(aemfd-jee-bundles-package-6.2CFP5; versione 1.0.2) fornisce  [!DNL Forms] agli utenti AEM gli stessi diritti e  [!DNL Forms JEE] le stesse funzionalità di AEM  [!DNL Forms OSGi]. Controllate i pacchetti installati in Gestione pacchetti e installate il pacchetto se non è già installato.

### Configurazione del timeout per le operazioni a livello di componente (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Dopo AEM 6.2 CFP4, è possibile utilizzare le seguenti istruzioni per configurare il timeout per le operazioni DSC nel caso in cui si verifichino problemi a causa del timeout durante il processo di aggiornamento. (Vedere NPR-16774 in [AEM note sulla versione di CFP4 6.2](release-notes-aem-6-2-cumulative-fix-pack.md)).

La distribuzione DSC richiede un tempo variabile a causa del quale potrebbe non riuscire. Per modificare il timeout delle operazioni DSC come Install, Load, Start e Stop, è necessario impostare `adobe.component.registry.timeout` utilizzando l&#39;argomento JVM con l&#39;opzione -D.

Specificate il valore per la chiave in secondi. Esempio: `-Dadobe.component.registry.timeout=300`

Potete inoltre modificare i timeout a livello di componente utilizzando le tre proprietà seguenti:

1. `adobe.all-component.timeout`: sovrascrive i timeout di tutti i Servizi del Prodotto.
1. `adobe.<serviceName>.timeout`: sovrascrive il timeout solo per il servizio (&lt;servicename>) indicato nella chiave. Se il valore a livello di servizio è impostato, l&#39;utilizzo di questo comando sovrascrive il valore di timeout per il servizio specificato solo se è impostato a livello di applicazione.
1. `adobe.<serviceName>.<operationName>.timeout`: Sovrascrive solo il timeout per l&#39;operazione del servizio specifico(&lt;servicename>.&lt;operationname>) indicata nella chiave. Se il valore è impostato a livello di operazione, utilizzando questo comando il valore di timeout per il servizio specificato viene sovrascritto solo se è impostato a livello di applicazione o di servizio.

**Esempi:**

Utilizzate i seguenti comandi per impostare il timeout a livello di componente:

1. Per impostare il timeout di tutte le operazioni del servizio su 600 sec:

   imposta &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Per impostare il timeout dei valori di operazione `DesigntimeService` su 500 sec, utilizzare:

   imposta &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Per impostare il timeout dei valori di operazione `DesigntimeService's previewLCA` su 700 sec, utilizzare:

   imposta `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Per impostare la `DSC operations` come caricamento, installazione e così via su 600 sec, utilizzare:

   imposta &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## Installare e configurare AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Esegui un backup della cartella /deploying. È richiesto se si decide di disinstallare la correzione rapida.
1. Arrestate il server applicazione.
1. Estrarre il file di archivio del programma di installazione della patch sul disco rigido.
1. Nella directory denominata in base al sistema operativo in uso:

   **Windows**

   Andate alla directory appropriata sul supporto di installazione o sulla cartella del disco rigido in cui avete copiato il programma di installazione:

   * (Windows a 32 bit): Disk1\InstData\Windows\VM
   * (Windows a 64 bit): Disk1\InstData\Windows_64bit\VM

   Quindi, fate doppio clic sul file denominato:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux, Solaris, AIX**

   Andate alla directory appropriata:

   * (Linux): Disk1/InstData/Linux/NoVM
   * (Solaris): Disk1/InstData/Solaris/ NoVM
   * (AIX): Disk1/InstData/AIX/VM

   Da un prompt dei comandi digitare:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Viene avviata una procedura guidata di installazione che illustra le procedure di installazione.

1. Nel pannello Introduzione, fate clic su **[!UICONTROL Next]**.
1. Nella schermata Scegli cartella di installazione, verifica che il percorso predefinito visualizzato sia corretto per l&#39;installazione esistente oppure fai clic su **[!UICONTROL Sfoglia]** per selezionare la cartella alternativa in cui è attualmente installato AEM [!DNL Forms], quindi fai clic su **[!UICONTROL Avanti]**.
1. Leggere le informazioni di riepilogo delle patch per la correzione rapida e fare clic su **[!UICONTROL Avanti]**.
1. Leggere il Riepilogo pre-installazione e fare clic su **[!UICONTROL Installa]**.
1. Al termine dell&#39;installazione, fare clic su **[!UICONTROL Next]** per applicare gli aggiornamenti della correzione rapida ai file installati.
1. La casella di controllo Avvia Configuration Manager è selezionata per impostazione predefinita. Fare clic su **[!UICONTROL Fine]** per eseguire Gestione configurazione.

   Per eseguire Configuration Manager in un secondo momento, deselezionare l&#39;opzione **[!UICONTROL Avvia Configuration Manager]** prima di fare clic su **[!UICONTROL Fine]**. È possibile avviare Configuration Manager in un secondo momento utilizzando lo script appropriato nella directory *`[AEM_forms_root]`/configurationManager/bin*.

1. A seconda del server dell&#39;applicazione, scegliere uno dei seguenti documenti e seguire le istruzioni riportate nella sezione *Configurazione e distribuzione AEM[!DNL Forms]*.

   Per AEM [!DNL Forms] 6.3, fare riferimento a:

   * [Installazione e distribuzione di  [!DNL Forms] AEM per JBoss](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [Installazione e distribuzione di  [!DNL Forms] AEM per WebSphere](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [Installazione e distribuzione di  [!DNL Forms] AEM per WebLogic](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   Per AEM [!DNL Forms] 6.2, fare riferimento a:

   * [Installazione e distribuzione di  [!DNL Forms] AEM per JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62)
   * [Installazione e distribuzione di  [!DNL Forms] AEM per WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62)
   * [Installazione e distribuzione di  [!DNL Forms] AEM per WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62)

   Per  AEM Forms 6.1, fare riferimento a:

   * [Installazione e distribuzione di  [!DNL Forms] AEM per JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [Installazione e distribuzione di  [!DNL Forms] AEM per WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [Installazione e distribuzione di  [!DNL Forms] AEM per WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. Riavviate AEM [!DNL Forms] server JEE.
