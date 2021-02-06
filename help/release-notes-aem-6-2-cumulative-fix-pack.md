---
title: AEM 6.2 Cumulative Fix Pack
description: ' Experience Manager 6.2 Note sulla versione del Cumulative Fix Pack. Approfondisci i problemi risolti in diversi pacchetti di correzioni cumulativi nei componenti  Experience Manager.'
translation-type: tm+mt
source-git-commit: 98d91e0367912d8962bb2f45ae972f50ccb71b5f
workflow-type: tm+mt
source-wordcount: '19975'
ht-degree: 19%

---


# AEM 6.2 Cumulative Fix Pack - Note sulla versione{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Informazioni sulla versione {#release-information}

| **Prodotto** | Adobe Experience Manager |
|---|---|
| **Versione** | 6.2 |
| **Versione** | [Fix Pack cumulativo 6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **Prerequisito** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **Disponibilità generale** | 06 giugno 2019 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe ha introdotto un unico modello di distribuzione per il rilascio delle correzioni. Invece di rilasciare hotfix per singoli problemi,  Adobe rilascia ora un Cumulative Fix Pack (CFP) ogni mese (a condizione che vengano superati i controlli di qualità). che è un pacchetto di contenuti che aggrega più correzioni. I CFP includono principalmente correzioni di bug, ma possono includere anche Feature Pack. Offrono i seguenti vantaggi rispetto ai singoli hotfix:

* Natura cumulativa (ad esempio, un CFP contiene gli aggiornamenti distribuiti con CFP precedenti)
* Maggiore garanzia di qualità
* Installazione semplificata (l’utente installa un CFP come pacchetto singolo senza alcuna dipendenza, ad eccezione dell’ultimo service pack)

Per ulteriori informazioni su CFP e altri tipi di rilasci, vedere [Maintenance Release Vehicle](https://docs.adobe.com/content/docs/en/aem/6-2/deploy/maintenance-release-vehicle-definitions.html).

## Informazioni sulla versione {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20 è l&#39;ultimo Cumulative Fix Pack per AEM 6.2 ed è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

>[!CAUTION]
>
>Se si applica il CFP senza aver prima convalidato la compatibilità tra i Feature Pack installati, potrebbe verificarsi un errore di sistema o la perdita delle configurazioni personalizzate, per la cui soluzione potrebbe essere necessario eseguire il ripristino dal backup.

>[!NOTE]
>
>* Un nuovo bundle Sling `discovery-  api` Johnzon 1.0.0 è incluso con AEM Cumulative Fix Pack 6.2 SP1-CFP10. Inoltre, l&#39;utente di servizio sling-discovery viene aggiunto con privilegi di lettura e scrittura per il nodo */var/discovery* nell&#39;archivio CRX.
   >
   >
* È stato aggiunto il bundle e-mail di apache commons **org.apache.commons/commons-email/1.5** in sostituzione di **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
   >
   >
*  Adobe consiglia di distribuire CFP tramite la cartella di installazione per i clienti che dispongono di un numero elevato di utenti nell&#39;istanza AEM.

>



## Problemi inclusi {#issues-included}

In questa sezione sono elencati tutti i problemi e gli hotfix inclusi nel CFP corrente.

Inoltre, questo CFP include hotfix forniti in [pacchetti di correzioni cumulative precedenti](#previous).

### Integrazione {#integration}

* Supporto di più miglioramenti a livello di personalizzazione del targeting delle campagne. NPR-29163: Hotfix per CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler genera un ciclo infinito e causa aggiornamenti ai nodi nelle istanze di pubblicazione. NPR-28561: Hotfix per CQ-4263096

### DAM - Generale {#dam-general}

* Impossibile visualizzare/nascondere il pulsante di replica per gli utenti non amministratori in specifiche cartelle della DAM. NPR-29026: Hotfix per CQ-4265361

### Vulnerabilità {#vulnerability}

* Il framework di protezione CSRF non funziona con i moduli di AEM Foundation. NPR-28612: Hotfix per GRANITE-22231

### Forms {#forms}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consultate [ AEM Forms Release](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package}

>[!NOTE]
>
>Per i clienti di AEM Forms, è essenziale installare il pacchetto dei componenti aggiuntivi per AEM Forms dopo l’installazione del Service Pack, del Cumulative Fix Pack o del Feature Pack di AEM.

>[!NOTE]
>
>I pacchetti di componenti aggiuntivi per AEM Forms consentono di allineare le funzionalità di Forms ai Service Pack e i Cumulative Fix Pack di AEM. Pertanto, è necessario installare AEM pacchetto del componente aggiuntivo moduli dopo aver installato AEM Service Pack, Cumulative Fix Pack o Feature Pack.

#### Moduli adattivi {#adaptive-forms}

* Problemi di usabilità con il componente scarabocchio per i dispositivi iOS 12.1. NPR-29082: Hotfix per CQ-4261765

#### Forms - Sicurezza dei documenti {#forms-document-security}

* La verifica di tutte le firme presenti in un PDF tramite le firme elettroniche avanzate PDF (PAdES) genera InvalidOperationException. NPR-27848: Hotfix per CQ-4244837

#### Forms - Corrispondenza {#forms-correspondence}

* Quando si visualizza l&#39;anteprima della lettera come PDF, il campo di testo inserito nella pagina master non rispetta il valore immesso nella scheda dati o in base al collegamento dati specificato. NPR-29239: Hotfix per CQ-4266856.

#### Forms - Comunicazione interattiva {#forms-interactive-communication}

* Quando viene aggiunto un carattere apostrofo, i campi precompilati della lettera vengono visualizzati come caratteri ASCII invece che come alfabeti normali. NPR-28863: Hotfix per CQ-4262900

### Programma di installazione di JEE per Forms {#forms-jee-installer}

* Il programma di installazione di JEE per Forms non contiene nuove correzioni per AEM Forms.

## Hotfix e Feature Pack inclusi nei Cumulative Fix Pack precedenti {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulative Fix Pack 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Supporto abilitato per il supporto di MS Translator API v3.0 a AEM 6.2
* Messaggio di registro aggiunto dopo l’installazione corretta del pacchetto per tutti gli SP, i CFP e gli HF.

### Assets {#assets}

* Impossibile rinominare la cartella DAM se manca l&#39;autorizzazione Modifica ACL. NPR-27555: Hotfix per CQ-104652
* Strumento per l’editor di predefiniti per immagini non reattivo in CFP 17 e versioni successive 6.2.1. NPR-28147: Hotfix per CQ-4261041

### Sites {#sites}

* Il controllo collegamenti non completa il processo, si blocca con collegamenti senza risposta. NPR-27373: Hotfix per CQ-4256030
* Il file del segmento non viene caricato correttamente a causa di un percorso principale aggiuntivo che interrompe il percorso del segmento. NPR-28014: Hotfix per CQ-4260332

### Integrazione {#integration-1}

* La cancellazione dell&#39;ereditarietà LiveCopy non funziona correttamente sui contenitori di destinazione. NPR-28129: Hotfix per CQ-4259813
* Le azioni cq:non vengono prese in considerazione per un componente con targeting. NPR-27616: Hotfix per CQ-4257497

* La visualizzazione dell&#39;icona per interrompere l&#39;ereditarietà non è coerente. NPR-27671: Hotfix per CQ-4257779

### Felix {#felix}

* I dettagli del componente della console Web non vanno a buon fine con 500 dopo l’installazione di CFP 18 nell’istanza AEM 6.2 SP1. NPR-28350: Hotfix per CQ-4261095

### Traduzione {#translation}

* Abilitare il supporto per il servizio MS Translator in AEM 6.3 dopo l&#39;aggiornamento di MS Translator a API v3.0. NPR-28123: Hotfix per CQ-4259096

### Interfaccia utente - Foundation {#ui-foundation}

* Il calendario dei siti OOTB mostra date non corrette. NPR-28392

### GRANITE {#granite}

* Il dizionario non è invalidato per i bundle di risorse che utilizzano sling:basename. NPR-27624

### Manutenzione {#sustenance}

* I registri attività di Gestione pacchetti devono essere estratti in un file di registro separato. NPR-27323: Hotfix per GRANITE-14866
* Una frase/formulazione/riga/e di registro standard nel file error.log da visualizzare al termine dell&#39;installazione. NPR-27835
* Il plugin del pacchetto Granite sta scegliendo la dipendenza di una versione inferiore di org.apache.sling.i18n. Hotfix per CQ-4263245
* Il bundle com.adobe.cq.com.adobe.cq.ui.commons viene eliminato al momento dell&#39;installazione del CFP più recente dopo 6.2SP1-CFP15. Hotfix per CQ-4258808

### Forms {#forms-1}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consultate [ AEM Forms Release](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-1}

#### Moduli adattivi {#adaptive-forms-1}

* Vulnerabilità di tipo XML Injection con AEM Forms. NPR-27843: Hotfix per CQ-4257315

### Programma di installazione di JEE per Forms {#forms-jee-installer-1}

* Il programma di installazione di JEE per Forms non contiene nuove correzioni per AEM Forms.

### Pacchetti OSGI e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included}

Il testo seguente documenta l’elenco dei pacchetti OSGI e dei pacchetti di contenuti inclusi nel CFP.

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP19

[Ottieni file](assets/do-not-localize/cfp19_osgi_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP19

[Ottieni file](assets/do-not-localize/cfp19_content_packages.txt)

### Cumulative Fix Pack 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* È stato aggiunto il supporto in DAM CommandLineProcess per terminare il processo a lungo termine.
* È stata corretta una perdita di sessione in ReplicationEventListener.
* È stato aggiunto il supporto per il reindirizzamento al componente della pagina di base.

### Risorse {#assets-1}

* I processi Camera Raw si bloccano durante i periodi di caricamento massiccio e alla fine bloccano tutte le elaborazioni dei flussi di lavoro. NPR-26990: Hotfix per NPR-23860
* La funzionalità di download sfrutta  AEM Assets tramite il servlet di download delle risorse, consentendo agli utenti anonimi di scaricare tutte le risorse. NPR-27054, Hotfix per CQ-4254732
* I caratteri speciali vengono visualizzati in AEM nella riga dell’oggetto dei modelli delle e-mail. NPR-26470: Hotfix per CQ-4252368

### Siti {#sites-1}

* A causa di un comportamento errato della classe ConfigPostProcessor, la sospensione dell&#39;immagine padre rimuove cq : Tipo di mixaggio LiveRelationship dalla pagina figlio. NPR-26745: Hotfix per CQ-4254163
* Aggiungete il supporto per il reindirizzamento al componente della pagina di base. NPR-26576: Hotfix per CQ-110529
* Migra context hub a jquery 3. NPR-26956: Hotfix per CQ-4255472
* I campi di input di ancoraggio vengono visualizzati fuori dalla sezione visibile dei browser nella finestra di dialogo fino a quando non vengono ingranditi. NPR-26852: Hotfix per CQ-4255019
* Copiare e incollare del testo che inserisce &lt;br> indesiderato nel frammento di contenuto. NPR-26660: Hotfix per CRTE-151
* L&#39;amministratore del sito classico non esegue il rendering dell&#39;elenco nel riquadro di destra per alcune pagine. NPR-27247: Hotfix per CQ-4251621
* (Interfaccia classica) I tentativi di spostare/rinominare le pagine generano un errore, &quot;Si è verificato un errore durante lo spostamento della pagina.&quot; NPR-27179: Hotfix per CQ-4235907

### Integrazione {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever esamina l’intera struttura per raccogliere i marchi disponibili. NPR-27060: Hotfix per CQ-4255790

### WCM - Componenti Foundation {#wcm-foundation-components}

* Problema di funzionalità di ricerca con il componente Elenco di Foundation. NPR-26817: Hotfix per CQ-4250324

### Platform {#platform}

* A causa di un trattino em del carattere speciale, la cache non viene scaricata dal server di pubblicazione. NPR-27199: Hotfix per CQ-4242790

### GRANITE {#granite-1}

* La funzione di convalida pacchetti non convalida i pacchetti inclusi nel CFP/SP. NPR-26775: Hotfix per GRANITE-22825

### Replica {#replication}

* Perdita di sessione JCR in ReplicationListener. NPR-27063: Hotfix per CQ-4232088

### Forms {#forms-2}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consultate [ AEM Forms Release](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-2}

* Il pacchetto di componenti aggiuntivi per Forms non contiene nuove correzioni per AEM Forms.

### Programma di installazione di JEE per Forms {#forms-jee-installer-2}

* Il programma di installazione di JEE per Forms non contiene nuove correzioni per AEM Forms.

#### Pacchetti OSGI e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-1}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP18

[Ottieni file](assets/do-not-localize/62cfp18updated_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP18

[Ottieni file](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Cumulative Fix Pack 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* È stato aggiunto il supporto per gli URL senza estensione del sito in at-integration.js
* È stato rimosso l’importatore di polling S7 dalla configurazione del servizio cloud S7.
* Modifiche alla vista audience per supportare la struttura di cartelle per l&#39;implementazione multi-tenant.
* Aggiornamento a jqueryui   clientlib v1.12.1.

### Risorse {#assets-2}

* L’avvio di flussi di lavoro dall’interfaccia utente delle risorse richiede che l’utente disponga di autorizzazioni di scrittura, eliminazione o modifica. NPR-25688: Hotfix per CQ-4250140
* I pulsanti Pubblica e Annulla pubblicazione restano visibili anche per gli utenti che non dispongono di autorizzazioni di tipo &quot;replica&quot;. NPR-25094
* (Flusso di lavoro) Il flusso di lavoro per la risorsa smart tag non viene elaborato tramite la configurazione AEM proxy. NPR-25915: Hotfix per CQ-4248202
* Rimuovere S7 polling importer dalla configurazione del servizio cloud S7. NPR-25239: Hotfix per CQ-95236

### Siti {#sites-2}

* I flussi di lavoro avviati dall&#39;editor -> Informazioni pagina contengono il percorso contestuale nel payload. NPR-26389: Hotfix per CQ-76804
* (Controllo collegamenti esterni) I collegamenti https non validi vengono visualizzati come collegamenti validi. NPR-25541: Hotfix per CQ-4201333
* (Interfaccia classica) Quando si crea una pagina indipendente sotto una Live Copy, la pagina viene creata come Live Copy. NPR-25610: Hotfix per CQ-4249801
* Problemi con le risorse di pubblicazione associate al componente Importazione progettazione quando una pagina viene attivata. NPR-25638: Hotfix per CQ-102532
* L’elenco delle copertine della barra degli strumenti RTF per l’editor Rich Text è selezionabile. NPR-25165: Hotfix per CQ-4248948
* Migra contexthub a jquery 3. NPR-25059: Hotfix per GRANITE-19902
* Per un componente parsys nidificato, viene sempre applicato il primo (con un percorso meno nidificato) che soddisfa i requisiti di progettazione da più componenti disponibili. Per ulteriori informazioni, vedere [Risoluzione del percorso di progettazione](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/page-templates-static.html). NPR-25250: Hotfix per CQ-4246276

### Integrazione {#integration-3}

* Utilizzando l&#39;integrazione di destinazione OOTB, il targeting di un componente esegue il rendering dell&#39;intera pagina invece di un componente di destinazione vuoto. NPR-25273: Hotfix per CQ-4248003
* Se si interrompe l&#39;ereditarietà in modalità di targeting, il componente viene comunque visualizzato come destinazione e l&#39;ereditarietà non viene interrotta in modalità di modifica. NPR-25324: Hotfix per CQ-4248162
* Quando una personalizzazione viene definita su una pagina e un&#39;audience viene risolta, l&#39;esperienza corrispondente viene visualizzata in modalità di modifica. NPR-25731: Hotfix per CQ-4249465
* URL teaser errato quando si utilizzano AEM con un percorso contestuale non predefinito. NPR-25971: Hotfix per CQ-4250953
* Rendering vuoto quando si utilizza l’opzione optout. NPR-25295: Hotfix per CQ-4246792
* Le esperienze eliminate dall’ambiente di authoring non vengono mai rimosse dal sito di pubblicazione al momento dell’attivazione della pagina. NPR-24869: Hotfix per CQ-4247832

### DAM - Client DM {#dam-dm-client}

* (Chrome, Firefox) VideoPlayer ignora i clic del mouse sui dispositivi touch. Hotfix per CQ-4247370

### Piattaforma {#platform-1}

* Consente di configurare il numero massimo di tentativi durante l&#39;acquisizione/il rilascio di un pacchetto. NPR-25328: Hotfix per GRANITE-22376
* Registrazione errata in caso di errori di replica. NPR-25308: Hotfix per CQ-4249402
* L’installazione di Forms AEM 6.2 Forms CFP8 a CFP14 causa il fallimento di Apache POI. NPR-25053: Hotfix per GRANITE-21771

### GRANITE {#granite-2}

* Il processo di sincronizzazione utente non riesce con l&#39;eccezione OakConstraint0022. NPR-25729: Hotfix per Oak-7428

### Communities {#communities}

* il bundle cq-social-as-provider non inizia con le versioni del driver mongo 3.x. NPR-26271: Hotfix per CQ-4252710

### Interfaccia utente - Foundation {#ui-foundation-1}

* Aggiornamento a jqueryui   clientlib v1.12.1. NPR-25090: Hotfix per Granite-21981, CQ-4248897

* (Omnisearch): La proprietà &#39;Title&#39; è vulnerabile agli script tra siti (XSS) in Sites. NPR-24994: Hotfix per GRANITE-19933

### Forms {#forms-3}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consultate [ AEM Forms Release](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-3}

#### Moduli adattivi {#adaptive-forms-2}

* Codifica errata durante l&#39;invio dei dati dal modulo adattivo. NPR-25539

#### Forms - Gestione {#forms-management}

* Risorse del modulo non correlate riportate come riferimenti durante la pubblicazione della pagina. NPR-26167: Hotfix per CQ-4251004

### Forms - Programma di installazione di JEE {#forms-jee-installer-3}

#### Sicurezza dei documenti {#document-security}

* La variabile viene compilata come tipo di dati Elenco, il sottotipo è una stringa, ma viene visualizzato un errore &quot;Impossibile forzare l&#39;oggetto&quot;. NPR-26194: Hotfix per CQ-4252287
* Impossibile accedere alle configurazioni delle filigrane dopo l&#39;installazione di 6.2-SP1-CFP15. NPR-26130: Hotfix per CQ-4250984

### Pacchetti OSGI e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-2}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP17

[Ottieni file](assets/do-not-localize/62cfp17updated_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP17

[Ottieni file](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Aggiunta del supporto per STARTTLS in Day CQ Mail Service (Servizio posta Day CQ).
* È stato corretto l&#39;allineamento delle icone ContextHub nel profilo.
* Correzioni apportate alla funzionalità Mostra/Nascondi del componente del menu a discesa.
* Aggiornamento alla versione più recente di Jackson 2.8.11

### Risorse {#assets-3}

* Impossibile avviare un flusso di lavoro da una vista elenco. NPR-24393: Hotfix per CQ-4245788
* (Firefox/Chrome) Impossibile scaricare le risorse nella pagina Condivisione risorse. NPR-24523: Hotfix per CQ-4224408
* Migliorata la qualità predefinita per l’anteprima video in AEM. NPR-24148: Hotfix per CQ-4244310

### Integrazione {#integration-4}

* Quando un componente è destinato all’istanza di pubblicazione, lo sfarfallio visualizza l’esperienza predefinita prima di quella di destinazione. NPR-23992: Hotfix per CQ-4242038
* Le esperienze eliminate dall’ambiente di authoring non vengono mai rimosse dal sito di pubblicazione al momento dell’attivazione della pagina. NPR-24869: Hotfix per CQ-4247832

### Piattaforma {#platform-2}

* Applicazione della patch a jQuery 1.12.4 da clientlib per includere la correzione di sicurezza. NPR-24129: Hotfix per GRANITE-20058
* Aggiunta del supporto per STARTTLS in Day CQ Mail Service (Servizio posta Day CQ). NPR-23941: Hotfix per CQ-4240397
* Rimuovete il valore predefinito MERGE_PRESERVE aclHandling. NPR-24593: Hotfix per GRANITE-21889
* LineChecker non riesce a esternalizzare i collegamenti quando la richiesta contiene parametri di query non validi. NPR-24127: Hotfix per CQ-4241893

### MSM {#msm}

* Hotfix proattivi per attacchi di script tra siti (XSS). NPR-21893: Hotfix per CQ-4223385
* MSM LiveRelationship: effective RolloutConfig errato se BlueprintConfig è in root. NPR-23999: Hotfix per CQ-4243000

### Siti {#sites-3}

* La creazione di una nuova esperienza in un&#39;area Live Copy richiede che l&#39;ereditarietà venga interrotta per essere configurata. NPR-24995, Hotfix per CQ-4248209
* (Interfaccia touch) Diverse icone nella barra degli strumenti superiore scompaiono durante il blocco o lo sblocco di una pagina. NPR-23954: Hotfix per CQ-4243345
* I campi non sono allineati correttamente nel contexthub. NPR-23958
* Azione di pubblicazione sull’authoring delle interruzioni di pagina bloccate. NPR-23970: Hotfix per CQ-4243203
* I report OOTB in /etc/Reports/ non funzionano correttamente e non mostrano alcun grafico di dati storici. NPR-20035: Hotfix per CQ-4220180
* Creazione dell&#39;avvio non riuscita durante l&#39;avvio del flusso di lavoro &#39;Richiedi avvio&#39; in un progetto. NPR-24255: Hotfix per CQ-4245030
* Tag e attributi HTML ignorati dalle e-mail dopo l&#39;installazione di CFP10. NPR-24287: Hotfix per CQ-4240028
* TagPicker: Il suggerimento tag nel campo tag dello schema di metadati tag consente di interrogare i nodi con tag, pertanto il caricamento richiede molto tempo. NPR-24347: Hotfix per CQ-4244291
* L&#39;integrazione Salesforce non riesce con le configurazioni proxy. NPR-24418: Hotfix per CQ-4245300
* (WCM) PageManager esce da Pagina archiviata su Eccezione durante la creazione della revisione. NPR-24565: Hotfix per CQ-4246203
* Il pulsante Emulatore dispositivo scompare dalla modalità di modifica e anteprima dopo l&#39;applicazione di CFP14. NPR-24566: Hotfix per CQ-4247060
* (Interfaccia classica) Gli interi tag vengono visualizzati come vuoti una volta creati nella finestra di dialogo. NPR-24688, Hotfix per CQ-4246407
* Impossibile creare la versione al primo tentativo. NPR-24774: Hotfix per CQ-4232176
* I report OOTB in /etc/Reports/ non funzionano correttamente e non mostrano alcun grafico di dati storici. NPR-24138: Hotfix per CQ-4220180

### Vulnerabilità {#vulnerability-1}

* L’integrazione con Salesforce è vulnerabile ad attacchi di tipo SSRF (Server Side Request Forgery). NPR-24289: Hotfix per CQ-4245277
* Vulnerabilità SSRF (Server Side Request Forgery) in ReportingServicesProxyServlet. NPR-24657: Hotfix per CQ-4246880

### GRANITE {#granite-3}

* Le operazioni di lettura dei metadati non vengono terminate. NPR-24240: Hotfix per GRANITE-19866
* Aggiorna Jetty a 9.4.11.v20180605 per correggere le vulnerabilità. NPR-25033: Hotfix per GRANITE-22120

### WCM - Componenti Foundation {#wcm-foundation-components-1}

* PageComparator genera ClassCastException durante l&#39;ordinamento delle pagine. NPR-24123: Hotfix per CQ-4244048
* La funzionalità Mostra/Nascondi del componente del menu a discesa del modulo non viene eseguita come previsto. NPR-24562: Hotfix per CQ-4222853

### Interfaccia utente {#user-interface}

* È stato notato un utilizzo intensivo della CPU dovuto a un numero elevato di richieste nella funzionalità di ricerca amministrazione. NPR-23588: Hotfix per GRANITE-21286
* (Interfaccia classica) Il componente visualizza i valori predefiniti anche se il servizio del modello dati del modulo associato è impostato su un campo vuoto. NPR-21903: Hotfix per GRANITE-19744
* NPE per la generazione di più campi se non sono presenti dati modulo per la richiesta. NPR-24513: Hotfix per GRANITE-21055

## Forms {#forms-4}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consultate [ AEM Forms Release](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-4}

#### Core {#core}

* (OSGI)  AEM Forms OSGI è influenzato dall&#39;avviso di protezione del binding dei dati di Jackson. NPR-24274: Hotfix per CQ-4230245

#### Rights Management {#rights-management}

* Apache POI non riesce dopo l’installazione AEM 6.2 SP1-CFP14. NPR-25054, NPR-25052: Hotfix per CQ-4245898, CQ-4244778

#### Moduli HTML5 {#html-forms}

* I dati non vengono compilati con la precompilazione di campi con più righe nell&#39;anteprima HTML. NPR-23357: Hotfix per CQ-4244212
* Quando si visualizza l&#39;anteprima di una lettera tramite l&#39;anteprima predefinita, la mappatura del frammento di layout non viene visualizzata e lo stesso viene visualizzato correttamente quando si fa clic sul pulsante Anteprima. NPR-22993: Hotfix per CQ-4237745
* Problema con l&#39;anteprima HTML di un campo di testo quando a un modello viene applicato un pattern di numero di previdenza sociale. NPR-23205

#### Moduli adattivi {#adaptive-forms-3}

* Errore &quot;Guida non definita&quot; durante l&#39;aggiunta AEM modulo al componente parsys. NPR-24269: Hotfix per CQ-4244546

### Programma di installazione di JEE per Forms {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Le terminazioni delle righe di finestra nei file di script Shell non consentono l&#39;esecuzione di LCM in UNIX. NPR-22958

### Pacchetti OSGI e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-3}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP16

[Ottieni file](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP16

[Ottieni file](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Correzione proattiva della protezione nella tabella Foundation per mantenere la coerenza della progettazione.
* È stato aggiunto il supporto per typeHint per salvare i valori come stringa.
* Protezione avanzata per il servizio di precompilazione Forms
* Aggiornate al file adobe-reader-extensions-dsc.jar più recente per verificare la presenza di correzioni nell&#39;estensione di Reader.
* È stato modificato l&#39;amo di convalida per considerare gli elementi &quot;:non validi&quot; per l&#39;input del numero di incremento.

### Risorse {#assets-4}

* I dati di EmbedXMP sono sempre impostati su “active” per il processo di generazione Ptiff. NPR-22776: Hotfix per CQ-4234498
* Impossibile impostare più valori predefiniti nei campi con più valori. NPR-22900: Hotfix per CQ-4239000
* (Dynamic Media) Quando si seleziona la casella di controllo Rendering dinamici, il file ZIP scaricato restituisce l&#39;immagine TIFF originale con un file a byte zero. NPR-22410: Hotfix per CQ-4198471
* (Interfaccia touch) Posizione di caricamento predefinita per le risorse nella vista a colonne. NPR-23475: Hotfix per CQ-4237057

### Integrazione {#integration-5}

* In modalità Target, gli autori possono modificare un componente ereditato dal blueprint senza annullare l’ereditarietà. NPR-22751: Hotfix per CQ-4237907
* La variabile del percorso non è codificata correttamente e porta allo scripting non permanente tra siti (XSS). NPR-22851

### MSM {#msm-1}

* Durante il rollout di una LiveCopy con più configurazioni di rollout, se si verifica un conflitto ResourceName sotto la radice, il flusso di rollout termina senza includere tutti i rami. NPR-22842: Hotfix per CQ-4236188

### Piattaforma {#platform-3}

* Implementare un limite di polling in una richiesta di applicazione inversa. NPR-23351: Hotfix per GRANITE-21135****
* La modifica del pattern del messaggio non si riflette sui logger personalizzati. NPR-23486: Hotfix per CQ-4241974

### Siti {#sites-4}

* La creazione di un collegamento all&#39;interno di un testo di un editor Rich Text a un documento con spazi o altri caratteri speciali non funziona. NPR-22289: Hotfix per CQ-4224321
* Se si salva il segmento con un valore enorme (1000000000), l’incremento viene impostato su 0 e viene visualizzato un messaggio di errore. NPR-22524: Hotfix per CQ-4237006
* Impossibile fare clic su Aggiungi elemento nel componente Multicampo. NPR-22552: Hotfix per CQ-4237404
* La barra di scorrimento orizzontale non è visibile quando il segmento ha un titolo lungo. NPR-22615: Hotfix per CQ-4237001
* Il caricamento di un&#39;audience vuota genera un codice JavaScript errato. NPR-22974: Hotfix per CQ-4238734
* Quando pianificate un&#39;attivazione o disattivazione, il titolo del flusso di lavoro è obbligatorio, pertanto il titolo del flusso di lavoro personalizzato non viene tradotto nella timeline. NPR-23121: Hotfix per CQ-4237552
* Richiesta di correzioni ai problemi relativi ai segmenti di Target in Sites. NPR-23128
* (Firefox) La casella di controllo per la persona selezionata non è quella corretta. NPR-23345
* Vengono visualizzate etichette per le diverse modalità con icone. NPR-23275
* Errore &#39;Valore selettore ricorsione non valido&#39; durante la migrazione di un componente da AEM 6.0 a AEM 6.2. NPR-23503: Hotfix per CQ-4241258

### Community {#communities-1}

* Le notifiche Web ed e-mail non vengono attivate a causa di un errore del messaggio per i gruppi. NPR-23447: Hotfix per CQ-4242880

### Traduzione {#translation-1}

* Le copie della lingua delle risorse vengono create quando la risorsa &quot;Non tradurre&quot; è impostata nella configurazione di traduzione. NPR-22540: Hotfix per CQ-4237962

### Interfaccia utente {#user-interface-1}

* L&#39;utilizzo di Omnisearch con una query con trattino restituisce un errore del server. NPR-22999: Hotfix per GRANITE-19674
* DatePicker non supporta l’impostazione manuale di suggerimenti di tipo esterni impostati da un campo nascosto. Se si modifica il valore di hint “type”, viene generato un errore di conversione. NPR-23333: Hotfix per GRANITE-21194

### WCM - Componenti Foundation {#wcm-foundation-components-2}

* Il componente CAPTCHA è stato dichiarato obsoleto per una migliore sicurezza. Se utilizzate il componente CAPTCHA, viene visualizzato il messaggio &quot;Il componente Captcha è obsoleto e non deve più essere utilizzato.&quot; verranno visualizzati dopo l&#39;installazione della versione 6.2 SP2-CFP15 o successiva. AEM componente può essere personalizzato per includere reCAPTCHA per una migliore sicurezza NPR-22151: Hotfix per CQ-4220052
* Il componente WCM Foundation &#39;Table&#39; è vulnerabile agli script tra siti memorizzati. NPR-23206: Hotfix per CQ-4240760

### Vulnerabilità {#vulnerability-2}

* Vulnerabilità cross-site scripting (XSS) nei collegamenti di progetto di Interfaccia utente amministratore. NPR-23272: Hotfix per CQ-4241795

## Forms {#forms-5}

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-5}

#### Gestione della corrispondenza {#correspondence-management}

* Quando si visualizza l&#39;anteprima di una lettera tramite l&#39;anteprima predefinita, la mappatura del frammento di layout non viene visualizzata e lo stesso viene visualizzato correttamente quando si fa clic sul pulsante Anteprima. NPR-23335: Hotfix per CQ-4237745
* I dati nella lettera corrispondente ai binding definiti in XDP non vengono compilati utilizzando l&#39;URL della lettera diretta. NPR-24145: Hotfix per CQ-4244290

#### Forms mobile {#mobile-forms}

* (Gestione corrispondenza) Disallineamento dei dati durante il caricamento di lettere con XML di destinazione. NPR-22993: Hotfix per CQ-4237663

#### Servizio estensioni Reader {#reader-extensions-service}

* Impossibile applicare l&#39;estensione del lettore su  Adobe PDF. NPR-23067

#### Forms Manager {#forms-manager}

* Forms incorporato nel sito non viene pubblicato quando si ripubblica la pagina del sito. NPR-23014: Hotfix per CQ-4236566

#### Vulnerabilità {#vulnerability-3}

* Hotfix proattivi per lo scripting tra siti. NPR-20624: Hotfix per CQ-4206055
* Vulnerabilità cross-site scripting (XSS) memorizzata nella scheda delle note di Forms Manager. NPR-27157: Hotfix per CQ-4255556

#### Servizio di crittografia {#encryption-service}

* (OSGI) [JEE] Stato firma errato per PDF con allegato durante la verifica tramite &quot;Convalida processo PDF&quot;. NPR-23269, NPR-23737

### Programma di installazione di JEE per Forms {#forms-jee-installer-5}

#### Core {#core-1}

* È necessario risolvere i problemi segnalati nell’analisi del codice statico di Core-ext. NPR-13947

#### Servizio PDFG {#pdfg-service}

* Il convertitore da HTML a PDF non funziona. NPR-21545

### Pacchetti OSGI e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-4}

Il testo seguente documenta l’elenco dei pacchetti OSGI e dei pacchetti di contenuti inclusi nel CFP.

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP15

[Ottieni file](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP15

[Ottieni file](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Cumulative Fix Pack 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* È stata migliorata la possibilità di modificare le proprietà dei metadati delle risorse.
* Il processo di notifica della scadenza della password è stato riconfigurato per le risorse già in stato di scadenza.
* Console dell’interfaccia utente touch personalizzata per estendere le impostazioni internazionali aggiuntive.
* Aggiornato cq-msm-core per una sincronizzazione Livecopyindex efficiente.
* Funzionalità di replica semplificata per vari Rollout.

### Risorse {#assets-5}

* Gli utenti non possono scaricare risorse con liberatoria e nomi file lunghi. NPR-22163: Hotfix per CQ-4235274
* Il carattere di virgolette singole impedisce l’aggiornamento dei metadati in visualizzazione bulkview e l’interfaccia utente risulta completamente interrotta quando si aprono le proprietà di una risorsa mediante le azioni rapide della barra degli strumenti. NPR-22317, NPR-22353: Hotfix per CQ-4236990, CQ-4236469
* Il processo di notifica della scadenza delle risorse non disattiva le risorse scadute. NPR-22346: Hotfix per CQ-4237188
* Il download delle risorse non riesce quando si utilizza Digital Rights Management in Assets con Safari. NPR-22378: Hotfix per CQ-4236460
* La rappresentazione Web per le immagini piccole ha dimensioni pixel non precise. NPR-22435: Hotfix per CQ-4236742

### Siti {#sites-5}

* (Interfaccia touch) Il tag spostato viene visualizzato nella posizione precedente e nuova nelle proprietà della pagina. NPR-21921, Hotfix per CQ-4238598
* (Interfaccia touch) L&#39;Editor Rich Text rimuove tutti gli attributi diversi dall&#39;ID dal tag &lt;a>. NPR-22045: Hotfix per CQ-4234133
* Se si incolla il contenuto direttamente nell&#39;editor Rich Text utilizzando CTRL+V, le interruzioni di riga vengono ignorate. NPR-22117: Hotfix per CUI-5881
* (Interfaccia touch) Impossibile visualizzare più di 40 tag nello spazio dei nomi. NPR-22290: Hotfix per CQ-99114
* Problemi relativi ai feed RSS, porta da -1 a AEM 6.2 NPR-22158: Hotfix per CQ-4233339
* (IE) Quando si crea per la prima volta un carattere nel campo RTF, al carattere viene aggiunto uno spazio finale. NPR-22443: Hotfix per CQ-4235343
* Quando si tenta di trovare una corrispondenza con il nome del pacchetto, l&#39;oggetto Java Use blocca il servizio SightlyJavaCompilerService a causa di uno spazio alla fine nella dichiarazione del pacchetto. NPR-22557: Hotfix per GRANITE-20836
* La console dell’interfaccia utente touch non include nuove lingue per l’assegnazione di tag. NPR-22250: Hotfix per CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Prima di caricare i folio in DPS, era necessario impostare sia la data di pubblicazione che la data di copertina. NPR-22484

### Commerce {#commerce}

* Più vulnerabilità XSS (cross-site scripting) in commercio creano la procedura guidata catalogo. NPR-22344: Hotfix per CQ-4237017

### MSM {#msm-2}

* La sincronizzazione LiveCopyIndex comporta la congestione dei thread durante gli aggiornamenti dell&#39;indice lunghi. NPR-22214: Hotfix per CQ-90667
* la proprietà cq:cugEnabled viene disabilitata quando viene modificato un altro campo di una Live Copy, rendendo la pagina non protetta. NPR-22246: Hotfix per CQ-4236050
* L’azione Rollout pagina non riesce ad aggiornare gli elementi secondari quando una pagina viene sospesa. NPR-22483: Hotfix per CQ-4236956
* Se si esegue il rollout di una struttura spostata in una pagina mastro, cq:moveTarget non viene eseguito correttamente. NPR-22373: Hotfix per CQ-4232536

### Integrazione {#integration-6}

* Se si tenta di ordinare le offerte nella libreria del selettore delle offerte, si verifica un comportamento anomalo. NPR-22208: Hotfix per CQ-4235439
* TargetContentImpl rallenta l’esecuzione di AEM durante le query con tempi di esecuzione lunghi. NPR-22361: Hotfix per CQ-4236907
* Il motore target (mbox.js, at.js) non utilizza URL gestiti e utilizza URL contenenti due punti, che potrebbero non riuscire con determinate implementazioni. NPR-22366: Hotfix per CQ-4237854
* La personalizzazione delle pagine richiede la pubblicazione direttamente sul nodo del marchio. NPR-22370: Hotfix per CQ-4236895

### Foundation {#foundation}

* I modelli Sightly di script Apache Sling utilizzano il bundle di provider **org.apache.sling.scripting.sight.models.provider/1.0.18**. NPR-22614: Hotfix per Sling-5944, Sling-6866

### Progetti {#projects}

* Workflow Starter non è in grado di accettare il valore TypeHint di String. NPR-22436: Hotfix per CQ-4237855

### Traduzione {#translation-2}

* Esame dei problemi relativi alla funzionalità Anteprima. NPR-22201: Hotfix per CQ-4223753

### Interfaccia utente {#user-interface-2}

* (Interfaccia classica) Il componente visualizza i valori predefiniti anche se il servizio del modello dati del modulo associato è impostato su un campo vuoto. NPR-21903: Hotfix per GRANITE-19744

### WCM - Componenti Foundation  {#wcm-foundation-components-3}

* Errore durante la pubblicazione di una pagina Live Copy che punta a una pagina di importazione in Adobe Campaigns. NPR-22470: Hotfix per CQ-4237164
* Errori JavaScript durante l&#39;apertura dell&#39;Editor frammenti esperienza. NPR-22598: Hotfix per CQ-4238415

### Flusso di lavoro {#workflow}

* Il servizio di notifica e-mail del flusso di lavoro del giorno CQ attiva un messaggio e-mail per il nodo Mongo per le notifiche WorkflowCompleted e WorkflowAborted. NPR-22486: Hotfix per CQ-4238172

## Forms {#forms-6}

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-6}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

#### Moduli adattivi {#adaptive-forms-4}

* Incoerenza nel valore del segnaposto a discesa in Modulo adattivo in IE11 e Chrome. NPR-22405: Hotfix per CQ-4227096

### Programma di installazione di JEE per Forms {#forms-jee-installer-6}

#### Installazione di LCM {#install-lcm}

* Aggiornamento dei JAR di Jsafe a Cryptoj 6.1.3.1 nel programma di installazione e in LCM. NPR-22744

### Feature Pack inclusi {#feature-packs-included}

#### Gestione processi {#process-management}

* (Area di lavoro HTML) Quando un utente richiede un’attività, il numero di code viene aggiornato per quel particolare utente, ma non per altri utenti a meno che la pagina non venga aggiornata. NPR-19778: Hotfix per CQ-4233665

### Pacchetti OSGI e pacchetti di contenuti inclusi in CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP14

[Ottieni file](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP14

[Ottieni ](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
file AEM Cumulative Fix Pack 6.2 SP1-CFP13 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* È stata attivata la configurazione del campo Parametro statico nelle impostazioni dei componenti di Target quando si utilizza AT.js come libreria client.
* Correzioni apportate alla funzionalità Mostra/Nascondi del componente del menu a discesa.
* Correzioni per l&#39;utilizzo dei tipi di pubblico di sincronizzazione di destinazione.
* Maggiore versatilità per la gestione della corrispondenza per contenere caratteri speciali.

### Risorse {#assets-6}

* Version Purge non rimuove le versioni precedenti delle risorse. NPR-21682: Hotfix per CQ-4212996
* Il riordinamento delle cartelle in una cartella riordinabile non viene mantenuto. NPR-21964: Hotfix per CQ-4231761

### Siti {#sites-6}

* (TouchUI)(ClassicUI) Più vulnerabilità di scripting tra siti (XSS) in HTL e nei componenti core. NPR-21532: Hotfix per CQ-4232305 e CQ-4232511
* La creazione e la formattazione di contenuto (ad esempio, l&#39;assegnazione o la rimozione di nuovi stili di elenco) in un testo selezionato non funziona correttamente in Internet Explorer 11. NPR-21533: Hotfix per CQ-4230689
* (Safari) Gli utenti non possono visualizzare tutte le risorse nel pannello di ricerca risorse. NPR-21981: Hotfix per CQ-4213720
* L&#39;ora di alterazione restituisce l&#39;errore &quot;RecursionToDeepException&quot; con una pagina non corretta e non viene creata alcuna nuova versione anche quando la data viene modificata. NPR-21707: Hotfix per CQ-4199536
* Quando si carica una pagina nell’editor, WorkflowStatusprovider (pageinfo.json) viene caricato tre volte, causando AEM&#39;esecuzione lenta dell&#39;istanza. NPR-21778: Hotfix per CQ-59232

### Integrazione {#integration-7}

* La creazione di audience di Mobile Type &amp; Browser in modalità di authoring di Target non funziona in AEM. NPR-21676, NPR-21681: Hotfix per CQ-4232100
* Con un’elevata latenza durante l’aggiornamento di un componente di destinazione, è possibile aggiungere un’altra offerta prima che il componente venga aggiornato completamente. NPR-21744: Hotfix per CQ-4233158/CQ-4234293
* Gli utenti non sono in grado di visualizzare i valori di test Static Param nella chiamata alla mbox, che possono essere visti durante il test con AT.js come libreria client nella configurazione cloud. NPR-21930: Hotfix per CQ-4234520

### Piattaforma {#platform-4}

* Problemi di prestazioni con la sincronizzazione degli utenti quando il numero di utenti o gruppi è elevato. NPR-20431: Hotfix per CQ-4223282
* Utenti non sincronizzati con la sincronizzazione utente tramite Sling Distribution. NPR-21911: Hotfix per GRANITE-20404
* Impedire che le parole di interruzione vengano evidenziate negli estratti di ricerca (in una pagina di Geometrixx). NPR-21835: Hotfix per GRANITE-21067\
   Nota: Questa correzione richiede il CFP Oak 1.4.20 o successivo.

### Traduzione {#translation-3}

* la proprietà jcr non è presente per l&#39;ID utente iniziatore durante la creazione del progetto di traduzione. NPR-21715: Hotfix per CQ-4230713

### WCM - Componenti Foundation {#wcm-foundation-components-4}

* La funzionalità Mostra/Nascondi del componente del menu a discesa del modulo non viene eseguita come previsto. NPR-22164: Hotfix per CQ-4235288

## Forms {#forms-7}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-7}

#### Moduli adattivi {#adaptive-forms-5}

* Iniezione di entità esterna XML (XXE) in Forms adattivo. NPR-21982: Hotfix per CQ-109878
* (iOS11) Quando si fa clic su un componente allegato, l&#39;allegato del file apre la fotocamera invece del browser del file del dispositivo. NPR-21926: Hotfix per CQ-4214348
* Il titolo mancante nell’interfaccia utente per la creazione del tema causa un’eccezione e non riesce a eseguire il rendering della finestra di dialogo. Hotfix per CQ-4236143

#### Gestione della corrispondenza {#correspondence-management-1}

* Problemi di rendering con i dati xml contenenti caratteri speciali. NPR-21712: Hotfix per CQ-4229137

### Programma di installazione di JEE per Forms {#forms-jee-installer-7}

#### Servizio assemblatore {#assembler-service}

* Il file PDF generato con ASM-1017-003 6.2.0 è danneggiato. NPR-21427: Hotfix per CQ-4228046

#### Servizio PDFG {#pdfg-service-1}

* Errore OCR a causa di dimensioni pagina impreviste (PDF) dai file PNG, JPEG e TIFF. NPR-19489: Hotfix per CQ-4209079

## Pacchetti OSGI e pacchetti di contenuti inclusi in CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP13

[Ottieni file](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP13

[Ottieni file](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* È stata migliorata la gestione dei metadati per i campi multivalore.
* Supporto di codici paese con più caratteri (più di due) nei flussi di lavoro di traduzione.
* Rendering migliorato delle pagine con più componenti nidificati.
* Migliorata la sincronizzazione delle date di pubblicazione per le risorse tra AEM e  Adobe Digital Publishing Suite.

### Risorse {#assets-7}

* Un numero eccessivo di caratteri in OmniSearch causa l’arresto anomalo del server AEM. NPR-21083: Hotfix per CQ-4223602
* I valori specificati nella seconda opzione in un campo multivalore nello schema metadati non vengono aggiunti ai valori precedentemente specificati in CRX-de. NPR-21220: Hotfix per CQ-4224526
* Il download delle risorse non riesce quando si utilizza Digital Rights Management in Assets con Safari. NPR-21387: Hotfix per CQ-4230287

### Siti {#sites-7}

* (DAM) (ClassicUI) Più vulnerabilità di scripting tra siti (XSS) in alcuni file SWF in AEM CQ Author/Publish QuickStart. NPR-21073, NPR-21074: Hotfix per NPR-20612
* Il selettore di tag non traduce i tag disponibili in più lingue.NPR-21221: Hotfix per CQ-78855
* I problemi di rendering con AEM console articolo quando si utilizzano più componenti nidificati lo rendono lento. NPR-21271: Hotfix per CQ-4224158

### Integrazione {#integration-8}

* Quando si aggiunge un framework Target, la modalità Targeting non è disponibile nell&#39;elenco della modalità Select (Seleziona) dell&#39;editor. NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* (Digital Publishing Suite) Le date di pubblicazione dei folio in AEM non corrispondono alle date visualizzate in Folio Producer. NPR-21145

### MSM {#msm-3}

* Il processo di ripristino Live Copy viene interrotto dopo l&#39;eliminazione della prima pagina locale nella LC. NPR-21276: Hotfix per CQ-4229743

### Piattaforma {#platform-5}

* La libreria di tag personalizzata che fa riferimento ai tag implementati come script non viene trovata dopo l&#39;aggiornamento a AEM 6.3. NPR-20149: Hotfix per Granite-18433

### Traduzione {#translation-4}

* I flussi di lavoro di traduzione non riescono con i codici lang_country più lunghi di 2 caratteri. NPR-21088: Hotfix per CQ-4197439
* La pagina della risorsa non deve essere nuovamente inviata a un progetto di traduzione finché il progetto non viene completato. NPR-21219: Hotfix per CQ-4209908

### Interfaccia utente {#user-interface-3}

* Seleziona componente non elimina la proprietà target durante l&#39;invio del modulo. NPR-21163: Hotfix per GRANITE-14125
* HTTP.encodePathOfURI espandere la codifica doppia del segno più &quot;+&quot;. NPR-21417: Hotfix per GRANITE-16340

### Vulnerabilità {#vulnerability-4}

* Script (XSS) tra siti nell&#39;editor di metadati DAM. NPR-21434: Hotfix per CQ-83472
* Più file SWF vulnerabili agli script tra siti diversi (XSS). NPR-20612: Hotfix per CQ-4213297

## Forms {#forms-8}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms  {#forms-add-on-package-8}

#### Gestione della corrispondenza {#correspondence-management-2}

* (IE11) Il rendering iniziale del contenuto HTML viene eseguito solo a sinistra, mentre il lato destro viene caricato in modo intermittente dopo il caricamento dell&#39;interfaccia utente completa. NPR-21554
* Il pulsante Invia per anteprima lettera viene disattivato dopo l&#39;installazione di AEM 6.2 SP1-CFP9. NPR-21547
* Quando si seleziona il tipo di collegamento risorsa, la finestra Selettore risorsa non si apre nella procedura guidata Modifica binding dati lettera. NPR-21164: Hotfix per CQ-4194567
* Per modificare un modulo di testo in linea o modificabile, toccate l&#39;icona Modifica corrispondente o fate doppio clic sul modulo di testo corrispondente nell&#39;anteprima della lettera. NPR-21402

#### Moduli adattivi {#adaptive-forms-6}

* Il  componente Pulsante Invia di AEM Forms mostra type=&quot;button&quot; invece di type=&quot;submit&quot;. NPR-21007
* I dati restano persistenti quando si aggiungono o si eliminano nuovi pannelli per pannelli ripetibili. NPR-21408

### Programma di installazione di JEE per Forms {#forms-jee-installer-8}

#### Core {#core-2}

* L&#39;aggiornamento all&#39;ultimo aggiornamento di Java 8 Update 131 genera un&#39;eccezione: &quot;Provider JsafeJCE disattivato. Controllo di integrità personale richiesto FIPS 140 non riuscito&quot;. NPR-21355

   **Nota:** questo NPR richiede impostazioni aggiuntive; per ulteriori informazioni, consultate l&#39; [ultimo aggiornamento](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr) di Java 8.

* Aggiorna jars jsafe alla crittografia 6.1.3.1 in Core, Encryption, Signature &amp; Document Security. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Installazione di LCM {#install-lcm-1}

* Aggiornare Jars Jsafe a Cryptoj 6.1.3.1 nel programma di installazione e LCM. NPR-21362

#### Servizio PDFG {#pdfg-service-2}

* Aggiornare Jsafe Jars a Cryptoj 6.1.3.1 in PDFG. NPR-21359

#### Gestione processi {#process-management-1}

* (Area di lavoro HTML) Abilitazione del ridimensionamento delle colonne in modo che la categoria del nome non appaia troncata. NPR-19770: Hotfix per CQ-4233668

#### Servizio estensioni Reader {#reader-extensions-service-1}

* Aggiornare i jars jsafe alla crittografia 6.1.3.1 in RE. NPR-21357

## Pacchetti OSGI e pacchetti di contenuti inclusi in CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP12.1

[Ottieni file](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP12.1

[Ottieni file](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Aggiornato cq-msm-core per una sincronizzazione Livecopyindex efficiente.
* Maggiore efficienza di modifica per i frammenti di contenuto.
* Fornisce l&#39;opzione di convalida in Gestione pacchetti per rilevare le autorizzazioni ACL.
* È stata introdotta la capacità di Campaign di includere l&#39;ID e-mail per la corrispondenza dei clienti.
* Funzionalità di codifica video migliorate per i file Dynamic Media.
* Correzioni nei componenti Sightly e LiveCopy.

### Risorse {#assets-8}

* La codifica video Dynamic Media non riesce per i file che contengono spazi nei loro nomi. NPR-20818: Hotfix per CQ-102469
* Varie vulnerabilità XSS (cross-site scripting) in alcuni file SWF all&#39;interno AEM quickstart di CQ Author/Publish. NPR-21071, NPR-21072
* Gli utenti non possono scaricare risorse con liberatoria e nomi file lunghi. NPR-20255: Hotfix per CQ-4222139

### Siti {#sites-8}

* Integrazione AEM e Campaign: I collegamenti speciali vengono riscritti in  Adobe Campaign, impedendo ai clienti di inviare la posta elettronica: collegamenti ipertestuali nelle loro e-mail. NPR-20787: Hotfix per CQ-4225760
* (Interfaccia utente touch) AEM problemi di usabilità e prestazioni quando la lingua è impostata sul francese. NPR-20854: Hotfix per CQ-4227628
* Il collegamento di un file di risorse codificate tramite il plug-in di collegamenti nell’editor Rich Text restituisce un collegamento vuoto. NPR-20626, NPR-21059: Hotfix per CQ-4223011
* L’editor di metadati dei frammenti di contenuto impedisce agli autori di contenuti di salvare le modifiche apportate ai frammenti di contenuto. NPR-20641: Hotfix per CQ-4224755
* Alias proprietà pagina porta a Richiedi pubblicazione/Richiedi annullamento pubblicazione. NPR-20731: Hotfix per CQ-4226227
* Problemi relativi ai componenti di testo con la codifica del collegamento nell’elemento RTE. NPR-20755: Hotfix per CQ-4224321

### Piattaforma {#platform-6}

* ResourceResolverImpl.map() non richiama ResourceDecorator. NPR-20788: Hotfix per GRANITE-19718
* org.apache.sling.i18n.DefaultLocaleResolver non è in grado di elaborare le richieste tramite org.apache.sling.Engine.SlingRequestProcessor. NPR-20706: Hotfix per CQ-94880
* Richiesta di aggiungere un&#39;opzione di convalida in Gestione pacchetti per rilevare se le autorizzazioni o i privilegi ACL vengono modificati in un particolare pacchetto. Hotfix per CQ-4229196

### Integrazione {#integration-9}

* (Search&amp;Promote) La definizione ambigua del filtro per il pacchetto di contenuti porta a percorsi sovrascritti durante l&#39;installazione. NPR-20808: Hotfix per CQ-4227615

### Flusso di lavoro {#workflow-1}

* Problemi di stabilità relativi alla distribuzione del server di produzione AEM. NPR-20979: Hotfix per GRANITE-19104

### Progetti {#projects-1}

* (Interfaccia touch) Impossibile aggiungere membri del team a un progetto. NPR-20990: Hotfix per CQ-4205375

### WCM - Componenti Foundation {#wcm-foundation-components-5}

* Il componente Immagine Sightly &#39;link to&#39; genera un errore 403 a causa dell&#39;estensione .html mancante. NPR-20823: Hotfix per CQ-4195909
* In un sito di blueprint che utilizza LiveCopy, se si tenta di eliminare un componente Modulo, viene generata un&#39;eccezione NullPointerException e viene aggiunto nuovamente il componente Modulo anziché eliminarlo. NPR-20855: Hotfix per CQ-4204628
* La sincronizzazione LiveCopyIndex comporta la congestione dei thread durante gli aggiornamenti dell&#39;indice lunghi. NPR-20634: Hotfix per CQ-90667

### Sicurezza {#security}

* Aggiornamento proattivo della libreria XSS. NPR-21174
* Aggiornamento ad Apache Commons Email 1.5 che presenta un API semplificato per l&#39;invio di e-mail. NPR-20509: Hotfix per GRANITE-18240
* Patch di sicurezza applicata all&#39;API di protezione XSS Apache Sling per eliminare la possibilità di bypass XSS. NPR-21290: Hotfix per GRANITE-19924
* Bypass XSS nella funzione XSSAPI#getInvalidHref. NPR-21174: Hotfix per GRANITE-19924

### App mobili {#mobile-apps}

* Risoluzione dei problemi relativi alle richieste di intestazione curl per le risorse OOTB in AEM. NPR-20511: Hotfix per CQ-4221520 e CQ-103024

## Forms {#forms-9}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

Gli elementi di rilievo di AEM Forms sono:

* Abilitazione dell’autenticazione dei certificati per gli utenti di Workbench.
* Correzioni di usabilità per l&#39;area di lavoro di Gestione corrispondenza, moduli HTML5 e  AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-9}

#### Moduli HTML5 {#html-forms-1}

* Problemi di usabilità con il componente scarabocchio sui dispositivi iOS 10 e 11. NPR-21092

#### Gestione della corrispondenza {#correspondence-management-3}

* (Interfaccia utente di corrispondenza) Dopo un clic, disattivare il pulsante Invia. NPR-21078

### Programma di installazione di JEE per Forms {#forms-jee-installer-9}

#### Servizio assemblatore {#assembler-service-1}

* docConvertor non genera PDF/A con l&#39;errore &quot;Il prefisso &quot;stEvt&quot; per l&#39;elemento &quot;stEvt:action&quot; non è associato&quot;. NPR-21032: Hotfix per CQ-4222540
* Viene generata un&#39;eccezione con il nome java.lang.IllegalArgumentException message:No enum costante com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailedReason.SIGNED_IN_FUTURE durante la chiamata del servizio OMPFSubmission/PDFA/PDFtoPDFA. Ciò impedisce il completamento del processo di verifica della firma di breve durata fino al riavvio del server. NPR-20792

#### Workbench {#workbench}

* Abilitare l&#39;autenticazione tramite certificato per gli utenti di Workbench. NPR-17548: Hotfix per CQ-4214486

#### Gestione processi {#process-management-2}

* Il processo di preparazione dei dati richiama più volte quando viene eseguito il rendering del modulo mobile con parametri data. NPR-19801: Hotfix per CQ-4230427, CQ-4230400

## Pacchetti OSGI e pacchetti di contenuti inclusi in CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP11

[Ottieni file](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP11

[Ottieni file](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Aggiunta una nuova funzione di utilità onDialogLoaded per i test.
* Sono stati aggiunti test di unità frontend e configurazioni a ClientLibraryProxyServlet.
* Correzioni delle prestazioni nel componente Editor locale con più immagini.
* Aggiornamenti della configurazione in Apache Sling JCR ResourceBundleProvider.

### Risorse {#assets-9}

* L&#39;anteprima delle risorse non funziona se i flussi di lavoro di aggiornamento delle risorse sono disattivati. NPR-20543: Hotfix per CQ-4204986
* Problemi di rendering con la classe aggiunta nel granito: class, proprietà (cq-damadmin-admin-assets-upload). NPR-20514: Hotfix per CQ-4219238
* Le risorse miniature con caratteri speciali nel titolo mostrano l’oggetto Java nell’attributo alt di NPR-20347: Hotfix per CQ-4223620
* Sostituzione del codice di confronto delle versioni con il codice proprietario Adobe a causa di problemi di licenza. NPR-20273: Hotfix per CQ-4223758
* Problemi di elaborazione durante il caricamento di file PSB CMYK con più livelli alfa. NPR-20251: Hotfix per CQ-4220869
* I dizionari di internazionalizzazione non funzionano a meno che il server non venga riavviato in org.apache.sling.i18n 2.5.6. NPR-20525: Hotfix per Granite - 19490
* Nessun thread dumps generato in base al periodo dell&#39;utilità di pianificazione con configurazione dell&#39;agente di raccolta Thread Dump predefinita (avvio AEM predefinito). NPR-20288: Hotfix per GRANITE-19488/GRANITE-12741/CQ-90647.

### Siti {#sites-9}

* Se il filtro data modificato viene modificato dopo l’apertura della ricerca salvata, i risultati non subiscono alcun effetto e i risultati visualizzati sono gli stessi del precedente valore salvato del filtro data modificato. NPR-19739: Hotfix per CQ-4219425
* Impossibile caricare le pagine con componenti nidificati. NPR-20312
* La richiesta di eliminazione del flusso di lavoro viene attivata all&#39;eliminazione dei pacchetti del flusso di lavoro. NPR-20266: Hotfix per CQ-4221686
* (Interfaccia touch) Problema con Copia/Incolla con Appunti del sistema operativo e AEM Appunti interni. NPR-20228: Hotfix per CQ-4220383
* AEM&#39;istanza diventa lenta con la vista a elenco quando vengono caricate più risorse (oltre 100). NPR-20034: Hotfix per CQ-4222695
* [Interfaccia touch] Quando si eliminano lanci tramite la console dell’interfaccia classica, tutte le pagine non sono più modificabili. NPR-20520: Hotfix per CQ-4225074
* Il menu a discesa Target non funziona con più componenti RTE in una finestra di dialogo. NPR-20345: Hotfix per CQ-4220981

### Piattaforma {#platform-7}

* Quando si accede utilizzando una sessione anonima, ClientLibraryProxyServlet non esegue il proxy delle richieste alle librerie client nell&#39;istanza di pubblicazione e restituisce HTTP 404 non trovato errore. NPR-20195: Hotfix per GRANITE-14409

### Integrazione {#integration-10}

* Se si seleziona il motore di destinazione come  Adobe Target, il componente non viene caricato e si verifica un errore nel registro del server. NPR-20058: Hotfix per CQ-88071, CQ-109698, CQ-4201600

### Commerce {#commerce-1}

* Non viene visualizzato alcun messaggio di conferma o di reindirizzamento alla creazione di prodotti della stessa pagina. NPR-20257: Hotfix per CQ-4223414

### Interfaccia utente {#user-interface-4}

* Se il nome di un campo è multicampo, i valori salvati nei campi data non vengono memorizzati durante la modifica del componente. NPR-20077: Hotfix per GRANITE-19147
* Le query precedenti non vengono interrotte in caso di attivazione di query consecutive e vengono generati risultati non corretti. NPR-20397: Hotfix per GRANITE-19306

### WCM - Componenti Foundation {#wcm-foundation-components-6}

* La proprietà ImageMap esiste ancora anche dopo la rimozione delle immagini dal componente Editor locale per più immagini. NPR-20142: Hotfix per CQ-4222982

## Forms {#forms-10}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms  {#forms-add-on-package-10}

#### Moduli adattivi {#adaptive-forms-7}

* valueCommit Script viene eseguito due volte per DropDownList quando viene modificato nell&#39;interfaccia utente. NPR-19989: Hotfix per CQ-110212

### Programma di installazione di JEE per Forms {#forms-jee-installer-10}

**Gestione processi**

* Il pacchetto CFP contiene  AEM Forms HTML Workspace versione 2.2.26. NPR-20099
* Il modulo precompilato non funziona se il modulo per dispositivi mobili è configurato per essere visualizzato come PDF. NPR-20566

**Rights Management**

* La finestra di dialogo di selezione dei certificati di autenticazione reciproca/CAC dovrebbe visualizzare i certificati con uso chiave avanzato (EKU, Enhanced Key Usage) come accesso client-auth o smart card. NPR-20708
* JEE per Forms supporta l’autenticazione reciproca PKCS#11. NPR-15001

## Pacchetti OSGI e pacchetti di contenuti inclusi in CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

Elenco dei bundle OSGi inclusi in AEM CFP 6.2 SP1-CFP10

[Ottieni file](assets/do-not-localize/bundle-list-cfp10.txt)

Elenco dei pacchetti di contenuti inclusi in AEM CFP 6.2 SP1-CFP10

[Ottieni file](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Configurazione dell’interfaccia utente classica per Analytics adattata per l’input segreto.
* Correzioni per la cache di persistenza indipendente per Contexthub.
* Calcolo accurato delle dimensioni delle risorse.
* Prestazioni AEM ottimizzate per la pubblicazione delle risorse su Brand Portal.
* Correzioni nel valore Resourcetype nel nodo canvas.
* Funzionalità di ricerca di caratteri speciali e con distinzione tra maiuscole e minuscole abilitata per il contenuto dei frammenti di documento.
* Forms adattivo migliorato per allegare PDF come allegati in Safari.\
   Fornisce un nuovo Dynamic Media che si collega alla nuova Dynamic Media Publishing Infrastructure per una replica più rapida e scalabile.

### Risorse {#assets-10}

*  AEM Assets non è in grado di estrarre riferimenti di risorse secondarie per  risorse InDesign include collegamenti duplicati alla risorsa. NPR-19006: Hotfix per CQ-4204186
* L&#39;opzione Ordina non funziona per le risorse all&#39;interno della raccolta in Commerce. NPR-19508: Hotfix per CQ-4213622
* Quando una risorsa con lo stesso nome di una risorsa esistente viene spostata nella stessa posizione, il valore di cq: lastReplicationAction per le risorse viene scambiato tra loro, causando la creazione di metadati errati. NPR-19531
* Viene visualizzato un messaggio di errore durante la pubblicazione di un numero elevato di risorse nonostante la corretta pubblicazione di tutte le risorse. NPR-19629: Hotfix per CQ-4219611
* Le rappresentazioni statiche sono elencate con dimensioni fisse e non riflettono la dimensione della rappresentazione effettiva. NPR-20004
* Si riscontrano rallentamenti nell’istanza di AEM quando si pubblicano più di quattro risorse su Brand Portal. NPR-20009

### Siti {#sites-10}

* AEM un comportamento imprevisto quando un utente tenta di pubblicare/annullare la pubblicazione/creare la versione di una pagina bloccata da un altro utente. NPR-19249; Hotfix per CQ-4215298 e CQ-4203856
* Durante la promozione manuale del lancio nidificato, la pagina figlia viene eliminata. NPR-19704
* Problemi di persistenza quando ContextHub memorizza il livello di persistenza predefinito della sovrascrittura durante l’inizializzazione. NPR-19979: Hotfix per CQ-4218399
* I frammenti di contenuto si sovrappongono ad altri pulsanti. NPR-19980: Hotfix per CQ-4221519
* La pagina del sito non viene visualizzata quando viene visualizzato utilizzando l&#39;alias in SiteAdmin. NPR-20053: Hotfix per CQ-4221478
* Errore durante la pubblicazione di una pagina Live Copy che punta a una pagina di importazione in Adobe Campaigns. NPR-20066: Hotfix per CQ-4220846

### Piattaforma {#platform-8}

* Apache POI è stato aggiornato alla versione 3.16 per supportare l’inclusione dell’immagine di sfondo delle diapositive PPT nelle rappresentazioni. NPR-18286
* Problemi di rendering con Internet Browser 11 ed Edge durante il caricamento di più risorse nella stessa cartella. NPR-20062

### Integrazione {#integration-11}

* Il file at.js personalizzato non viene pubblicato se vi si accede con l’utente anonimo. NPR-19542: Hotfix per CQ-4219592
* Migrazione delle credenziali esistenti di Analytics all&#39;autenticazione WSSE. NPR-19962

### Brand Portal {#brand-portal}

* Abilitazione della pubblicazione di tag da AEM a Brand Portal dalla console tagadmin/tagging. NPR-20271

## Forms {#forms-11}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms  {#forms-add-on-package-11}

#### Gestione della corrispondenza {#correspondence-management-4}

* Funzionalità abilitata per la ricerca del testo effettivo nei frammenti di documento durante l&#39;anteprima di una lettera. NPR-19712

#### Moduli adattivi {#adaptive-forms-8}

* Forms adattivo migliorato per allegare PDF come allegati in Safari. Per supportare la stessa funzionalità nei moduli esistenti, è necessario apportare modifiche alla configurazione nel widget allegati e in &quot;Tipi di file supportati&quot; aggiornare il valore application/pdf invece di .pdf. NPR-19623

#### Forms Manager {#forms-manager-1}

* Se validationState non è definito in un campo di un modulo adattivo e si verifica l&#39;evento elementFocusChanged, viene restituito un evento di errore (errorState)  server Adobe Analytics. NPR-19513

### Programma di installazione di JEE per Forms {#forms-jee-installer-11}

#### Core {#core-3}

* Gestione connessione non è disponibile durante l&#39;arresto. Jboss interrompe la dipendenza JDBC prima che l&#39;autore EAR non venga distribuito causando problemi di corruzione. NPR-19703

## Feature Pack inclusi {#feature-packs-included-1}

* Miglioramenti per la correzione delle miniature e la trasparenza in Dynamic Media. NPR-15207

## Pacchetti OSGI e pacchetti di contenuti inclusi in CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP9

[Ottieni file](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Elenco dei bundle OSGi aggiornati in AEM 6.2SP1-CFP9

[Ottieni file](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Introduzione di tag a modelli utente personalizzati nel servizio modello e-mail  Adobe.
* Miglioramenti dei pulsanti TouchUI nell&#39;app Desktop.
* Pulsante Invia disattivato quando si fa clic per impedire l&#39;invio di più moduli in una pagina di traduzione.
* Configurati più componenti RTE in una finestra di dialogo.
* Riferimenti rinforzati: aggiornamenti in Live Copy.
* Funzionalità di ricerca con distinzione tra maiuscole e minuscole abilitata per il contenuto dei frammenti di documento.
* È stato aggiunto l&#39;elenco delle librerie Linux alla documentazione di installazione  AEM Forms.

### Risorse {#assets-11}

* Problemi con l&#39;applicazione del filtro Omnisearch sulle raccolte smart nel browser Safari. NPR-19511
* I metadati delle parole chiave PDF non vengono estratti correttamente e vengono modificati in modo errato se a una risorsa PDF sono associate più parole chiave. Per risolvere il problema, la proprietà dei metadati del campo Oggetto è stata rimossa per le risorse PDF. Si può, tuttavia, modificare lo schema metadati per aggiungere un campo di testo con più valori al campo Oggetto. NPR-19126
* Il servizio di notifica del flusso di lavoro non codifica i collegamenti nel messaggio e-mail, impedendo loro di caricarli dopo che gli utenti li hanno selezionati. NPR-19490: Hotfix per CQ-4218055
* Impossibile caricare l’elenco completo delle pagine/risorse nella vista a colonne utilizzando Chrome. NPR-19458: Hotfix per CQ-4214248
* L&#39;icona Ora di disattivazione non è corretta viene visualizzata AEM casella in entrata quando si attiva il flusso di lavoro &quot;Richiedi attivazione&quot;. NPR-19365: CQ-4216174
* Problemi di ordinamento nella vista a elenco. NPR-19217: CQ-95602
* Quando si modifica il titolo o l’immagine in miniatura nelle impostazioni di Cartella risorse, il gruppo e le autorizzazioni originali della cartella vengono ignorati. NPR-19283: Hotfix per CQ-4216080
* Le workstation Windows 10 passano automaticamente alla modalità Touch e disattivano alcuni pulsanti dal funzionamento. NPR-19183

### Siti {#sites-11}

* Problemi relativi all’utilizzo di più componenti RTE in una finestra di dialogo. NPR-19311, NPR-19587
* Lo svuotamento automatico della versione in vaniglia AEM 6.2 funziona solo una volta dopo l&#39;inizializzazione di VersionManagerImpl. NPR-19315: Hotfix per CQ-4217175
* L’istanza del flusso di lavoro si blocca nel passaggio del flusso di lavoro &quot;Salesforce.com Export&quot;. NPR-19222: Hotfix per CQ-4212976
* Le pagine di copia della lingua create dalle Live Copy non sono modificabili. NPR-18967
* ReferencesUpdateAction non riesce ad aggiornare i collegamenti in una LiveCopy nidificata con la modifica della gerarchia. NPR-18715: Hotfix per CQ-4214105

### Piattaforma {#platform-9}

* Il servizio Modello e-mail Adobe aggiunge tag ai modelli utente personalizzati. NPR-19190: Hotfix per CQ-4217113

### Progetti {#projects-2}

* Gli editor di progetti non possono copiare/incollare risorse nella cartella delle risorse del progetto. NPR-19619
* Impossibile generare l&#39;anteprima per i progetti di traduzione dopo l&#39;installazione di 6.2 SP1-CFP1. NPR-16481: CQ-4204655

### Integrazione {#integration-12}

* L’accesso alle proprietà per gli articoli viene impostato in modo errato nell’interfaccia classica di Adobe Digital Publishing Solution. NPR-19366
* Rendering lento delle miniature dovuto agli articoli a dimensione intera nella console AEM articolo. NPR-19086: CQ-4217148
* Comportamento non corretto della piegatura automatica quando si personalizzano le offerte tramite Campaign se gli utenti hanno accesso a più aree. NPR-19290: Hotfix per CQ-4218029
* La finestra di dialogo Impostazione destinazione non viene visualizzata in modalità di targeting quando un modulo di destinazione viene modificato e salvato più volte. NPR-19144: Hotfix per CQ-4216708

### Flusso di lavoro {#workflow-2}

* Gli utenti non possono filtrare le notifiche in Posta in arrivo per utente/gruppo nell’interfaccia classica della inbox. NPR-19122: Hotfix per CQ-4215374
* La mappa immagine non mantiene le coordinate selezionate nel componente immagine HTL. NPR-18911: CQ-4211584

## Forms {#forms-12}

* Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consultate [ AEM Forms Release](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-12}

* Quando il contenuto viene copiato da Microsoft Word o da un browser Web all&#39;editor di testo di gestione della corrispondenza, lo stile viene perso. NPR-19530
* Il contenuto senza interruzione di riga nell&#39;Editor di testo non va a capo. NPR-19481
* Funzionalità abilitata per la ricerca del testo effettivo nei frammenti di documento durante l&#39;anteprima di una lettera. NPR-17792: Hotfix per CQ-4214501

#### Gestione della corrispondenza {#correspondence-management-5}

>[!NOTE]
>
>Questa funzionalità di ricerca per i frammenti di testo presenta alcuni vincoli:-
>
>* I contenuti dei frammenti di documento sono sensibili alle maiuscole/minuscole e i titoli non fanno distinzione tra maiuscole e minuscole.
>* I risultati della ricerca non vengono evidenziati quando parte della parola ricercata è in uno stile diverso o contiene caratteri speciali come &quot; o &quot; o &quot; o &quot;.
>* La ricerca non funziona per il contenuto dinamico (come i valori degli elementi del dizionario dati o i valori delle variabili) all&#39;interno del frammento di documento.


#### Forms Manager {#forms-manager-2}

* Le proprietà dello schema XML di Forms adattivo non possono essere modificate dopo l&#39;applicazione di CFP6 in AEM 6.2. Hotfix per CQ-4219684
* Tutti i servizi del bundle di base  AEM Forms Manager non vengono avviati al riavvio del server. Hotfix per CQ-4217014

### Programma di installazione di JEE per Forms {#forms-jee-installer-12}

#### Installazione di LCM {#install-lcm-2}

* La schermata Amministratore di Microsoft Windows visualizza la versione 6.0 dopo l&#39;installazione di CFP6. Hotfix per CQ-4217573

## Feature Pack inclusi {#feature-packs-included-2}

* Miglioramenti dei pulsanti TouchUI nell&#39;app Desktop. NPR-18676

## Pacchetti OSGi inclusi in CFP8 {#osgi-bundles-included-in-cfp}

Elenco dei bundle OSGi aggiornati in AEM 6.2SP1-CFP8

[Ottieni file](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP8

[Ottieni file](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Modifica del comportamento nella visualizzazione dei titoli sulla scheda Immagine per Immagine con dc: proprietà title impostata su String [] (multifield).
* Problemi di prestazioni risolti con Cloud Services Dynamic Media, interfacce touch UI e interfaccia utente di sicurezza.
* Problemi risolti in Apache Felix Http Bridge 3.0.8
* È stata risolta la replica senza binario (BLR) tra ambiente di creazione e pubblicazione.
* Supporto per il file libreria di destinazione, AT.JS, una libreria di implementazione per l&#39;integrazione lato client con  Adobe Target progettata sia per le tipiche implementazioni Web che per le applicazioni a pagina singola.
* Prestazioni AEM migliorate grazie all&#39;introduzione del periodo di timeout della connessione configurabile dall&#39;utente per le soluzioni di Marketing Cloud (Analytics, DTM, Target e S&amp;P).

### Risorse {#assets-12}

* Durante il test dell’assimilazione video con AEM 6.3 configurato con Cloud Services Dynamic Media, si verifica l’eccezione &quot;Troppi file aperti&quot;. NPR-18734; Hotfix per CQ-4211407
* L’impostazione dell’URL personalizzato per le risorse su una pagina non funziona dopo il riavvio dell’istanza AEM. NPR-18634; Hotfix per Granite-18085
* Nell’interfaccia utente touch, il pulsante Pubblica viene visualizzato per gli utenti che non dispongono dell’autorizzazione per pubblicare le risorse. NPR-18620; Hotfix per CQ-4214042
* L&#39;opzione di rappresentazione dinamica non è presente nella finestra di dialogo di download di una risorsa una volta che il contratto di licenza è impostato per essa. NPR-18607; Hotfix per CQ-4212342
* Non è possibile scaricare il rendering dinamico per le risorse il cui nome contiene spazi. NPR-18571; Hotfix per CQ-4211738
* Impossibile salvare più utenti quando si condivide la cartella di risorse con Creative Cloud. NPR-18489; Hotfix per CQ-103297
* dc: title &amp; dc: la descrizione non viene modificata in un valore multi-campo in crx/de. NPR-18474; Hotfix per CQ-4209086
* Il funzionamento delle risorse di spostamento causa il deterioramento delle prestazioni. NPR-18346
* Quando viene aperto con l&#39;opzione predefinita Mostra tutto, nella timeline non vengono visualizzati elementi. NPR-18302; Hotfix per CQ-4211957
* Si verifica un errore quando un file di testo con codifica ASCII/UTF-8 viene caricato in AEM Assets e la generazione delle miniature non riesce. NPR-18006: CFP per CQ-4209345
* I pulsanti di azione Pubblica sono visibili anche quando l&#39;utente non dispone dell&#39;accesso replicato. NPR-17353; Hotfix per CQ-4209269
* Sia Siteadmin che Miscadmin non funzionano quando la minificazione è abilitata utilizzando min:gcc;obfuscate=true. NPR-18593; Hotfix per CQ-4209220
* Le voci di menu personalizzate non vengono visualizzate fino a quando lo schermo non viene aggiornato ogni volta. NPR-18500; Hotfix per CQ-4213581
* Aggiorna il file TIME.js alla versione 2.10.6. NPR-18596; Hotfix per Granite-11881
* Applicazione delle autorizzazioni per la visualizzazione delle interruzioni delle macro DM per l&#39;utente amministratore. NPR-18544; Hotfix per CQ-4211729
* Pubblica più tardi per le risorse sta generando ArgumentException non valido. CQ-4214532

### Siti {#sites-12}

* In un cluster di autori attivi con MongoDB, entrambi gli autori tentano di attivare la replica per lo stesso contenuto, quando il tempo raggiunge il tempo impostato per il contenuto. NPR-18708; Hotfix per CQ-4210982
* NPE quando si sposta una risorsa con un riferimento privo di jcr: content node. NPR-18664
* I segnaposto non sono visibili in una pagina che contiene più componenti parsys. NPR-18645; Hotfix per CQ-110253
* Problemi di concorrenza in AbstractCopyMoveCommand. NPR-18591
* Quando si copia il testo in un componente parsys da un&#39;altra istanza AEM, parsys viene creato senza alcun set resourceType. NPR-18511; Hotfix per CQ-4212306

### Piattaforma {#platform-10}

* Il programma di installazione JCR non aggiorna la versione del bundle dopo l&#39;installazione del pacchetto. NPR-18728; Hotfix per NPR-15135
* Replica senza binario (BLR) non riuscita con ambiente di creazione e pubblicazione binario. NPR-18704
* Richiesta di risoluzione Http Bridge Apache Felix nell’ambiente AEM. NPR-18297
* La replica non riesce quando più pagine con una struttura simile vengono replicate contemporaneamente con Sling Content Distribution. NPR-18665; Hotfix per Granite-13712
* Sling distribuzione pacchetti costruire e non auto-pulito. NPR-18601; Hotfix per Granite-16183

### Integrazione {#integration-13}

* La visualizzazione delle offerte pubblicate dalle cartelle libreria genera un NPE. NPR-18732; Hotfix per CQ-4214593
* La data di inizio/fine di un&#39;attività non viene aggiornata in JCR e Target se viene modificata da una data specifica a &quot;Quando attivata/disattivata&quot;. NPR-18612; Hotfix per CQ-104831
* L&#39;integrazione di Analytics con AEM non dispone di timeout di connessione o socket impostati per le connessioni httpclient. NPR-18497
* L&#39;integrazione DTM con AEM non dispone di timeout di connessione o socket impostati per le connessioni httpclient. NPR-18495
* L&#39;integrazione di Target con AEM non dispone di timeout di connessione o socket impostati per le connessioni httpclient. NPR-18494
* L&#39;integrazione Search &amp; Promote con AEM non dispone di timeout di connessione o socket impostati per le connessioni httpclient. NPR-18493
* L&#39;attività di destinazione viene disattivata dopo l&#39;aggiunta di un&#39;esperienza aggiuntiva. NPR-18227; Hotfix per CQ-4201895

### WCM - Componenti Foundation {#wcm-foundation-components-7}

* Le mappe immagine non mantengono le coordinate selezionate nel componente immagine HTL. NPR-18530; Hotfix per CQ-4211584

### Traduzione {#translation-5}

* I risultati della ricerca della traduzione non includono i nomi dei progetti di traduzione. NPR-18224; Hotfix per CQ-4210658

### Portale marchio {#brand-portal-1}

* Abilitazione della pubblicazione di tag da AEM a Brand Portal dalla console tagadmin/tagging. CQ-4212165

## Forms {#forms-13}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consultate [ AEM Forms Release](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-13}

#### Gestione della corrispondenza {#correspondence-management-6}

* I dati corretti non vengono visualizzati nel pannello di modifica finché il frammento non viene salvato. NPR-19092
* L&#39;aggiunta di frammento di documento a una lettera richiede molto tempo. NPR-18958
* Se esiste una dichiarazione XML in un file XML di dati e il rendering della lettera viene avviato tramite una richiesta di POST, la lettera corrispondente non visualizza i dati. NPR-18870
* Non vengono generati registri di controllo per le azioni eseguite sulle risorse di CM. NPR-16618

>[!NOTE]
>
>Non installate questo pacchetto del componente aggiuntivo CFP se vi sono problemi riscontrati con i due problemi seguenti:
>
>* L&#39;opzione Copia Incolla da Word/Web in CM Text Editor mostra il contenuto per l&#39;interruzione di riga. NPR-19530
>* Il contenuto senza interruzione di riga in CM Text Editor non va a capo. NPR-19449

>
>
Tali obiettivi saranno affrontati nel quadro della futura PCP.

#### Moduli adattivi {#adaptive-forms-9}

* Quando si aggiunge un nuovo pannello per pannelli ripetibili, il valore del campo a discesa nel pannello precedente viene eliminato. NPR-18772
* I campi modulo adattivi contrassegnati per accettare solo numeri interi accettano anche alcuni caratteri speciali dal tastierino numerico. NPR-18680
* Lo script per modificare il titolo del pulsante in corrispondenza dell&#39;evento initialize del pannello delle guide non funziona. NPR-18476
* La barra di scorrimento non viene visualizzata nel pannello a destra per le regole create nell&#39;editor di regole. NPR-18716

#### App AEM Forms {#aem-forms-app}

* Forms non esegue correttamente il rendering in  app AEM Forms quando è in modalità offline o non è connesso alla rete. CQ-4218368

### Programma di installazione di JEE per Forms  {#forms-jee-installer-13}

#### Servizio PDFG {#pdfg-service-3}

* PDF Generator non riesce a produrre documenti PDF con livelli di segnalibri specifici. Hotfix per CQ-4211102

## Pacchetti OSGi inclusi in CFP7 {#osgi-bundles-included-in-cfp-1}

Elenco dei bundle OSGi aggiornati in AEM 6.2SP1-CFP7

[Ottieni file](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP7

[Ottieni file](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Gestione efficiente dei componenti nascosti in modalità di layout su tablet.
* Introduzione alle azioni rapide sui dispositivi ibridi.
* Risoluzione dei problemi di sincronizzazione a livello di componente con le copie in tempo reale.

### Risorse {#assets-13}

* Il cliente viene bloccato quando l’utente che non dispone dell’autorizzazione richiesta tenta di spostare l’operazione su una risorsa. NPR-18330; Hotfix per CQ-4212560
* L&#39;unione di più configurazioni di servizi di contenuto avanzato causa un problema di usabilità. NPR-18273; Hotfix per CQ-4201557
* Le azioni di estrazione/flussi di lavoro non sono disponibili dalla console Timeline una volta circa 80 frammenti vengono aggiunti nella cartella Risorse. NPR-18257; Hotfix per CQ-4211214 e NPR-18251; Hotfix per CQ-4211216.
* Il sistema si arresta in modo anomalo in memoria insufficiente e manca di impaginazione durante i rapporti Risorse. NPR-17865; Hotfix per CQ-4209759
* Il video pubblicato non viene riprodotto correttamente sulla risorsa video codificata. NPR-17849; Hotfix per CQ-4210739
* La miniatura per PDF non viene generata. NPR-17831, NPR-17750; Hotfix per CQ-4210547
* Le risorse scadute non vengono disattivate  processo di notifica della scadenza di Adobe CQ DAM. NPR-17666; Hotfix per CQ-107766
* Le attività di scadenza delle risorse si fermano se a una risorsa non è assegnato un proprietario. NPR-17665; Hotfix per CQ-4197946
* Quando si sposta una cartella di risorse con più di 150 riferimenti in entrata, viene generata un’eccezione Null Pointer. CQ-4200981

### Siti {#sites-13}

* La personalizzazione funziona solo per il primo IP quando la regola di segmentazione è impostata per un intervallo IP. NPR-18121; Hotfix per CQ-83767
* L&#39;accesso non riesce a causa di NumberFormatException quando la proprietà historyShow è abilitata. NPR-18073; Hotfix per CQ-101965
* Le pagine eliminate contrassegnate sono visibili nell’interfaccia utente touch. NPR-18025; Hotfix per CQ-86694
* Problemi di prestazioni durante il caricamento di una pagina destinata a un numero elevato di utenti (oltre 2000). NPR-17884; Hotfix per CQ-4209567
* Impossibile selezionare un&#39;immagine dopo la rimozione di un&#39;altra immagine sulla pagina. NPR-17711; Hotfix per CQ-4201323

### Piattaforma {#platform-11}

* I controlli dell&#39;interfaccia touch non sono nascosti per gli utenti che non dispongono delle autorizzazioni necessarie. NPR-17945; Hotfix per CQ-4211231
* Tag giapponesi mancanti nel campo del selettore tag. NPR-17768; Hotfix per CQ-4210456
* La query getsize() restituisce risultati non corretti quando FastQuerySize è abilitato. NPR-18018
* La console Web nell&#39;istanza standby non è accessibile. NPR-17861; Hotfix per Granite-14582

### Commerce {#commerce-2}

* L&#39;attraversamento delle query viene eseguito quando il blueprint del catalogo non presenta alcuna condizione definita per una sezione. NPR-18229; Hotfix per CQ-4211924

### Community {#communities-2}

* PollingImporterImpl. ritardi AEM arresto. NPR-18298; Hotfix per CQ-96133

### Integrations (Integrazioni){#integrations}

* Risoluzione di errori del componente AEM - Ricerca che possono verificarsi quando l’OSGi AEM Day HTTP Client 3.1 è configurato con un proxy che richiede l’autenticazione digest. NPR 18128
* Casella di controllo mancante per ripristinare l&#39;ereditarietà. NPR-17753; Richiesta hotfix per CQ-4210139
* Gli utenti non sono in grado di impostare la priorità quando eseguono il targeting di un componente con più attività. NPR-18658; Hotfix per CQ-4210727
* Gli utenti non sono in grado di sfogliare la cartella /etc/segmentation per selezionare un&#39;audience creata sotto la cartella /etc/segmentation/group1. NPR-18522

### Sicurezza {#security-1}

* La procedura guidata Sposta risorsa si blocca se l’utente non dispone dell’autorizzazione di scrittura per la cartella di destinazione. NPR-18300
* Richiesta di utilizzare una versione aggiornata del servelet org.apache.sling.servlets.post (2.3.22) nell&#39;API Sling Apache per prevenire una vulnerabilità XSS. NPR-18963

### Traduzione {#translation-6}

* La pagina della risorsa non deve essere nuovamente inviata a un progetto di traduzione finché il progetto non viene completato. NPR-18249; Hotfix per CQ-4209908

### WCM - Componenti Foundation {#wcm-foundation-components-8}

* Impossibile utilizzare il componente iparsys di WCM foundation nei modelli modificabili. NPR-18223; Hotfix per CQ-4210384
* La mappa immagine non mantiene le coordinate selezionate nel componente immagine HTL. NPR-18032; Hotfix per CQ-4211584
* Quando viene eseguito il rendering di un componente immagine HTL, il nome del file nell’URL viene rinominato causando l’interruzione dell’URL. NPR-17908; Hotfix per CQ-4211587
* Impossibile uscire da Proprietà pagina dopo aver apportato le modifiche. NPR-17832; Hotfix per CQ-96110

## Forms {#forms-14}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consultate [ AEM Forms Release](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-14}

**Gestione della corrispondenza**

* Il dizionario dati viene letto più volte durante il rendering delle lettere. NPR-18482, Hotfix per CQ-4210805
* Aggiunta di JavaDocs per la classe com.adobe.livecycle.content. NPR-18467
* Quando si crea una lettera, la descrizione della lettera non viene salvata. NPR-18039
* Quando un modulo di testo viene salvato e un’espressione nel modulo di testo non contiene tag di espressione di apertura o chiusura, non viene visualizzato alcun messaggio di errore. Il modulo di testo visualizza un messaggio di errore e non riesce a eseguire il rendering nella lettera. NPR-17798
* Errori imprevisti visualizzati nei log sull&#39;installazione del pacchetto del componente aggiuntivo. NPR-18295

**Forms Manager**

* Nell’interfaccia utente di AEM Forms sono elencate tutte le risorse a partire da quelle meno recenti. Gli utenti non possono riordinare le risorse in modo da visualizzare per prime quelle più recenti. NPR-18451

### Programma di installazione di JEE per Forms  {#forms-jee-installer-14}

**Servizio di output**

* È stato migliorato il problema di prestazioni del servizio Output per AEM moduli 6.2. NPR-18033

**Servizio Firme**

* Impossibile firmare un documento PDF con il modulo di protezione hardware remoto. NPR-18017

## Pacchetti OSGi inclusi in CFP6 {#osgi-bundles-included-in-cfp-2}

Elenco dei bundle OSGi aggiornati in AEM 6.2SP1-CFP6

[Ottieni file](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP6

[Ottieni file](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Sono stati risolti diversi problemi di interfaccia utente relativi alla condivisione, allo spostamento, alla pubblicazione e al download delle risorse.
* Maggiore capacità della finestra di dialogo Sposta nella visualizzazione delle risorse di riferimento.
* Sono stati risolti diversi problemi relativi ai componenti e ai flussi di lavoro WCM, ad esempio Annulla pubblicazione e Rimuovi versione.
* È stata migliorata la reattività della barra delle azioni rispetto alla visualizzazione delle azioni della barra degli strumenti e dei componenti Corallo.

### Risorse {#assets-14}

* Miglioramenti delle prestazioni nella funzionalità di pubblicazione su Brand Portal. NPR-17189; Hotfix per CQ-4204150
* La condivisione di una risorsa tramite l’opzione Condividi collegamento non crea un file ZIP con una struttura di cartelle semplice da scaricare. NPR-17513; Hotfix per CQ-4209381
* Quando si seleziona una risorsa in DAM e si fa clic su Pubblica, l’opzione Pubblica su Brand Portal non viene visualizzata nella pagina dei dettagli della risorsa. NPR-17351; Hotfix per CQ-94905
* Nei passaggi del flusso di lavoro DAM, i flussi binari acquisiti da Session o ResourceResolver devono essere chiusi in un blocco finale per garantire che non si verifichino perdite di risorse. NPR-17385; Hotfix per CQ-4209452
* Il caricamento di un documento Word in DAM genera un&#39;eccezione di puntatore null e l&#39;istanza del flusso di lavoro rimane bloccata nello stato In esecuzione. NPR-17160; Hotfix per CQ-4207358
* I pulsanti Condividi, Sposta, Pubblica e Scarica sono visibili per le risorse scadute nella pagina Editor metadati per gli utenti non amministratori. NPR-16903; Hotfix per CQ-101440/CQ-104535
* Le azioni come Condividi, Sposta, Pubblica e Copia devono essere visibili per gli utenti amministrativi nella console Risorse. NPR-16902; Hotfix per CQ-4207111

### Siti {#sites-14}

* Quando si sposta una pagina utilizzando l’interfaccia classica e l’interfaccia touch, la finestra di dialogo Sposta non mostra riferimenti oltre 150, impedendo agli utenti di aggiornare tali riferimenti e ripubblicare la pagina. Questo problema è stato risolto introducendo una proprietà per l’interfaccia classica: &#39;maxRefNo&#39; che può essere configurato sul nodo siteadmin: &#39;/libs/wcm/core/content/siteadmin&#39;. Questa proprietà specifica il numero massimo di riferimenti (valore predefinito 150) visualizzati prima di un&#39;operazione di spostamento intensivo e, se una pagina contiene più riferimenti, non vengono visualizzati nella finestra di dialogo movePage. Questa configurazione funziona anche per damadmin e miscadmin applicando la configurazione sui nodi: `'/libs/wcm/core/content/damadmin'` e `'/libs/wcm/core/content/miscadmin'` rispettivamente. NPR-17222; Hotfix per CQ-85878

* Quando lavorate con i componenti WCM, i collegamenti ipertestuali con gli spazi vengono rimossi nell’editor Rich Text dell’interfaccia touch. NPR-17698, NPR-17570; Hotfix per CQ-4206768
* Quando si attiva il flusso di lavoro Richiedi pubblicazione dalle proprietà della pagina, gli utenti senza diritti di replica vengono visualizzati errori JavaScript. NPR-17294; Hotfix per CQ-102064
* Il rendering o l’esportazione di un componente immagine HTL modifica l’URL in un numero, rinominando il nome del file e causando l’interruzione dei collegamenti. NPR-17245; Hotfix per CQ-59616
* Se si elimina un lancio in un lancio nidificato, i lanci secondari diventano orfani. NPR-17228; Hotfix per CQ-4202639
* Se si esegue Version Purge in AEM 6.2 con Oak 1.4.13 applicato, nei registri viene visualizzato un avviso costantemente ripetuto. NPR-17391; Hotfix per CQ-4206870
* Dopo aver installato un hotfix o un aggiornamento per il componente ContextHub, il pacchetto di contenuto sovrascrive tutti i segmenti in /etc/segmentation/contexthub, con conseguente perdita di tutti i segmenti ContextHub personalizzati. NPR-17250; Hotfix per CQ-79958
* Durante l’esecuzione di un flusso di lavoro con gruppi nidificati come utenti del flusso di lavoro, WorkflowStatusProvider (pageinfo.json) blocca l’istanza del flusso di lavoro. NPR-17555; Hotfix per CQ-4202056
* Quando si utilizzano i componenti dell&#39;editor WCM-Page, alla fine della pagina esiste un&#39;enorme quantità di spazio vuoto nella modalità di modifica dell&#39;interfaccia touch dell&#39;istanza di creazione. NPR-17510; Hotfix per CQ-4205441
* Il rendering o l’esportazione di un componente immagine HTL imposta l’URL su un numero, causando l’interruzione dei collegamenti. NPR-17245; Hotfix per CQ-59616

### Interfaccia {#ui}

* Quando si seleziona una risorsa e si fa clic su Strumenti sviluppatore, le azioni della barra degli strumenti non vengono sempre visualizzate nella barra delle azioni con connessioni lente e la pagina deve essere ricaricata. NPR-17568; Hotfix per CQ-108365
* La barra delle azioni deve essere aggiornata in modo da usare due contenitori: coral-actionbar-primario e coral-actionbar-secondario, invece del coral-actionbar-contenitore. NPR-17591; Hotfix per GRANITE-15225

### Mobile-on-demand {#mobile-on-demand-2}

* Gli utenti con autorizzazioni di sola lettura per l&#39;app AEM Mobile  non possono visualizzare l&#39;anteprima dei contenuti  pagina AEM Mobile Content Management. NPR-17390; Hotfix per CQ-4209690

### Sicurezza {#security-2}

* vulnerabilità XSS nell&#39;output generato da HTMLRendererServlet. NPR-17136
* Richiesta per impedire la divulgazione AEM versione nella pagina AEM feed sindacazione Web. NPR-16219

### Forms {#forms-15}

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-15}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

**Moduli adattivi**

* Per un modulo adattivo con allegato, le voci duplicate per i tag afSubmissionInfo vengono create nel codice XML inviato quando il modulo viene inviato per la seconda volta. NPR-17364
* Quando si utilizza il browser Google Chrome, dopo aver rimosso un allegato da un modulo, il tentativo di ricollegare lo stesso allegato genera un errore. NPR-17297
* Se in Forms adattivo basato su XSD o su modello senza modulo sono presenti pannelli pigri nidificati e ripetibili, i valori compilati nel modulo non vengono conservati nel DOR (Document of Record). NPR-17176
* Gli errori visualizzati nel registro errori per l&#39;Editor regola devono essere aggiunti nel blocco catch di un codice JavaScript di blocco try/catch. NPR-16757
* Facendo clic su un file allegato in un modulo si verifica un errore della console del browser e non viene visualizzata l&#39;anteprima dell&#39;allegato. NPR-17174

**Gestione della corrispondenza**

* La funzione Crea interfaccia utente corrispondenza si blocca se nell’interfaccia utente viene aggiunto del testo in linea o una riga vuota. NPR-17748
* Il browser scorre quando una lettera viene aperta per la modifica. NPR-17576
* Durante l&#39;aggiunta di funzioni remote negli elementi del dizionario dati calcolati, se il numero di funzioni è superiore alla lunghezza della scheda che mostra le funzioni remote, la barra di scorrimento non viene visualizzata nella scheda. NPR-17359
* Il metodo API import com.adobe.icc.services.api.LetterInstanceService non funziona. NPR-17922, NPR-16008
* Una variabile aggiunta in un modulo di testo non è visibile nel pannello Binding dei dati durante la modifica di una lettera. NPR-17940
* L&#39;interfaccia utente di gestione della corrispondenza non viene avviata quando l&#39;azione di invio HTML utilizza il metodo POST. NPR-17595

**Forms Manager**

* Con un modulo adattivo configurato per il test AB, facendo clic su Avvia test AB non si avvia il test e si verifica un errore nella console del browser. NPR-17838

**Servizio Forms**

* È opportuno risolvere i problemi segnalati nell’analisi del codice statico dei moduli OSGI. NPR-13951

#### Programma di installazione di JEE per Forms {#forms-jee-installer-15}

**Servizio di output**

* L&#39;utilizzo di AEM form 6.2 Output Service per unire un modulo specifico a un XML di dati richiede 20 volte più tempo rispetto al tempo impiegato dal server di LiveCycle ES4 SP1 per la stessa operazione. È fisso negli ambienti Windows e Linux. NPR-17501

**Installazione di LCM**

* Dopo aver installato  build AEM Forms 6.2 GM e aver applicato il CFP AEM 6.2, LiveCycle Gestione configurazione  visualizza un punto e virgola indesiderato nelle Informazioni sulla versione e la data di installazione della patch non viene aggiornata. NPR-14322

**Gestione processi**

* La variabile TaskContext non viene compilata per i processi AEM Forms. CQ-4211857

####  pacchetto di pacchetti AEM Forms JEE {#aem-forms-jee-bundles-package}

* Le funzionalità degli utenti dei moduli, sia che si utilizzi la console dell’interfaccia utente amministratore JEE che OSGi, devono essere le stesse. NPR-17670

### Pacchetti di funzioni inclusi in CFP5 {#feature-packs-included-in-cfp}

**Pacchetto Forms JEE**

Gestione dei processi - Area di lavoro HTML

* Durante l&#39;assegnazione di un passaggio dell&#39;area di lavoro, nella scheda degli allegati dell&#39;area di lavoro deve essere visualizzato un contatore per gli allegati o le note, qualora siano presenti più allegati o note. NPR-17771
* Richiesta di supporto per Office 365 in AEM JEE Forms per le funzionalità e-mail nel flusso di lavoro del modulo. NPR-13866

**Forms Add-on Package**

Gestione della corrispondenza

* Durante la modifica dei frammenti nell&#39;editor di testo durante l&#39;anteprima di una lettera, il testo elaborato deve essere visualizzato per la modifica anziché nelle condizioni in linea utilizzate nei frammenti. NPR-15748, NPR-17504

### Pacchetti OSGi inclusi in CFP5 {#osgi-bundles-included-in-cfp-3}

Elenco dei bundle OSGi aggiornati tra AEM6.2 SP1-CFP5

[Ottieni file](assets/do-not-localize/cfp5_osgi_bundles.txt)

Elenco dei pacchetti di contenuti aggiornati tra AEM6.2 SP1-CFP5

[Ottieni file](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

I principali elementi di rilievo di questo Cumulative Fix Pack sono:

* Correzioni nelle risorse per la rappresentazione dei file, la visualizzazione timeline e l’orientamento dell’immagine Camera Raw
* Miglioramento

   * Avvii WCM per i siti
   * Flusso di lavoro Progetti
   * Componenti ContextHub

* Correzioni per Campaign, Mobile on-demand e Translation
* Miglioramenti a livello di usabilità nell&#39;Editor di regole per moduli adattivi
* Editor di condizioni in linea migliorato per la gestione della corrispondenza nei moduli
* Correzioni per la gestione dei processi e il servizio di output per i moduli AEM su JEE
* Correzione correlata a Forms Designer per l&#39;Editor di script

### Piattaforma {#platform-12}

* Il modulo di ricerca Search&amp;Promote ignora l&#39;impostazione `environment` quando il servizio cloud è configurato, rendendola inutilizzabile nell&#39;istanza di creazione. NPR-16594: Hotfix per CQ-4206076
* L&#39;aggiunta o la personalizzazione di colonne ai risultati di **Risorse OmniSearch** tramite la sovrapposizione in /apps non funziona. NPR-16737: Hotfix per CQ-4206785
* Lo strumento **Diagnosi **page non funziona dopo un aggiornamento sul posto da AEM 6.1 SP2 a AEM 6.2 SP1. NPR-17121; Hotfix per CQ-4196786
* HTL: Quando selezionate un forum, create un argomento e un post, la proprietà `Sightly SightlyCompiledScript` aggiunge `addSelectors` errata a `RequestDispatcherOption`. NPR-17008: Hotfix per GRANITE-16384

* È stato aggiunto il supporto per `CRON expressions` in `ManagedPollConfigs` utilizzato da `ReportImporter`. NPR-16608: Richiesta hotfix per CQ-4206066

* Il caricamento di un’immagine avatar per un utente LDAP non riesce. NPR-16561; Hotfix per Granite-17013
* Il numero di risultati visualizzati nella schermata Gestione utente è diverso nelle viste a schede e a elenco. NPR-16241; Hotfix per GRANITE-16914
* Le notifiche del flusso di lavoro non possono essere caricate pigre durante la visualizzazione nel browser Google Chrome in modalità Schermo intero. NPR-17013: Hotfix per CQ-4207567

### Risorse {#assets-15}

* L&#39;orientamento dell&#39;immagine non viene applicato correttamente durante l&#39;importazione di un&#39;immagine con un orientamento definito. NPR-16750: Hotfix per CQ-4204356
* La visualizzazione Timeline delle risorse non visualizza alcuna risorsa anche se &#39;Mostra tutto&#39; è impostata per impostazione predefinita. NPR-16957: Hotfix per CQ-98780
* I file non elaborati della fotocamera (inclusi ARW, CR2, NEF, DNG ed EPS) aggiunti come rappresentazione nelle risorse, non possono essere selezionati o eliminati. Tali file vengono scaricati automaticamente quando l&#39;utente li seleziona. NPR-16949: Hotfix per CQ-4206846
* La creazione di un pdf in un altro pdf nell’interfaccia utente di Risorse non visualizza i file PDF creati nell’interfaccia utente di DAM, anche se questi sono visibili nell’archivio crx. NPR-16833: Hotfix per CQ-4206501
* Il caricamento di una risorsa come nodo figlio diretto di se stesso tramite l’interfaccia touch causa un problema. La risorsa viene caricata come elemento secondario diretto della risorsa precedentemente selezionata. NPR-16534: Hotfix per CQ-4204287
* Nell’interfaccia utente di DAM, i commenti su una risorsa e i tag a un utente nel commento non generano una notifica e-mail. NPR-16589: Hotfix per CQ-102318

### Progetti {#projects-3}

La console del flusso di lavoro Progetti mostra un&#39;eccezione NullPointerException sulla pagina quando i flussi di lavoro vengono eliminati. NPR-17017: Hotfix per CQ-4194269

### Siti {#sites-15}

* I file in `ContextHub` non vengono ridotti a icona nell&#39;istanza di creazione. NPR-17022: Hotfix per CQ-79456
* La promozione di lancio WCM-Lanci richiede molto tempo per promuovere un lancio che consiste in una struttura ad albero grande di una pagina. NPR-16480: Hotfix per CQ-82731
* `ClientContext` Il renderer delle condizioni di segmento si blocca quando un segmento (o un&#39;audience) viene creato con una regola non funzionante o non completata. NPR-16759: Hotfix per CQ-4205104
* In Avvii WCM, le pagine associate a un lancio non vengono annullate quando l&#39;azione viene avviata dall&#39;interno delle proprietà della pagina nell&#39;interfaccia touch. NPR-16560: Hotfix per CQ-4204681
* Link Rewriter riscrive erroneamente i valori href contenenti due punti, presumendo che i due punti &quot;:&quot;definiscano uno spazio dei nomi JCR. NPR-16753: Hotfix per CQ-4203762
* In WCM-Design Importer, se si apre una pagina di Importazione test e si tenta di caricare un file ZIP si verificano dei problemi se è stato caricato ed eliminato in precedenza. NPR-16486: Hotfix per CQ-90962
* La navigazione al riquadro **[!UICONTROL Navigazione globale]** utilizzando i browser Firefox Safari e Google Chrome offre un&#39;esperienza utente diversa. Il browser Firefox visualizza il menu **[!UICONTROL Strumenti]**, mentre il browser Google Chrome mostra il menu **[!UICONTROL Navigazione]**. NPR-16770; Hotfix per CQ-4200456

### Campaign {#campaign}

* Durante il test AEM modelli di campagna e la modifica degli indirizzi iniziali per includere &quot;Dati aggiuntivi&quot;, l&#39;elenco a discesa  Adobe Campaign scompare nell&#39;hub contestuale dell&#39;interfaccia utente touch. NPR-16771: Hotfix per CQ-105748

### Mobile on-demand {#mobile-on-demand-3}

* Quando si verifica l&#39;anteprima di una pubblicazione dall&#39;ambiente di authoring AEM, un&#39;azione di verifica preliminare che dura più di 5 secondi causa un picco insolito nel dashboard suddiviso AEMM - AEM Integrazione PECS con un numero elevato di richieste di stato al secondo. NPR-16908: Hotfix per CQ-4207055
* La  gestione della configurazione AEM Mobile non riesce dopo l&#39;installazione dell&#39;aggiornamento AEM-6.2-SP1-CFP1-1.0. NPR-16909: Hotfix per CQ-4204892

### Traduzione {#translation-7}

* L&#39;anteprima dei processi di traduzione non funziona dopo l&#39;installazione di 6.2 SP1 - CFP1. NPR-16481; Hotfix per CQ-4204655
* La copia della lingua creata utilizzando i punti di traduzione nella cartella principale anziché nella Live Copy locale del paese. NPR-17257; Hotfix per CQ-4208287

### Sicurezza {#security-3}

* Non viene eseguita alcuna convalida del tipo MIME quando i file binari vengono caricati in AEM. NPR-16617
* Problemi relativi al caricamento di immagini avatar per gli utenti LDAP. NPR-16561

### Forms {#forms-16}

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-16}

**Moduli adattivi**

* Nell&#39;editor Forms adattivo, il commento Impostazione destinazione in head.jsp deve essere sostituito con la nuova istruzione Context Hub. NPR-17173
* Nell&#39;Editor regola Forms adattiva, l&#39;evento **[!UICONTROL Choose an Item]** viene visualizzato come &quot;null&quot;. NPR-17139
* Il modulo inviato viene nuovamente inviato quando si procede con la freccia (>). NPR-17080
* Durante l&#39;invio di un modulo adattivo tramite AJAX, la funzione di callback &#39;error&#39; non viene mai richiamata in caso di errore. NPR-17034
* Se si fa clic sul pulsante **[!UICONTROL Salva modulo]** in Editor regole in fase di esecuzione, il modulo non viene salvato. NPR-16905
* Il testo statico deve essere escluso dall&#39;ordine di tabulazione nel modulo adattivo. NPR-16749
* Il valore calcolato di un campo decimale non viene visualizzato correttamente. NPR-16596
* Nei moduli adattivi l&#39;icona per la visualizzazione del contenuto della Guida deve essere inclusa nell&#39;ordine di tabulazione. NPR-16484
* Supporto per l&#39;uso di espressioni regolari di tipo `dataRef=C:/Users/`in &#39; **[!UICONTROL Prefill Service Configuration]**&#39; per la precompilazione dei dati per Forms adattivo. NPR-16425

* Le convalide non vengono attivate correttamente per tutti i pannelli in presenza di uno scenario di caricamento pigro nidificato. NPR-15821

**Gestione della corrispondenza**

* La rappresentazione della lettera non riesce se una lettera contiene un modulo di testo vuoto (uno senza testo). NPR-17054
* Le interruzioni di riga e gli spazi di tabulazione vengono rimossi dal contenuto dopo essere stati incollati nell&#39;Editor di testo. NPR-17039
* La visualizzazione dei riferimenti di un modulo di testo richiede molto tempo se al modulo di testo viene fatto riferimento in più lettere. NPR-17035
* La modifica, il salvataggio, l&#39;eliminazione e l&#39;impostazione dei riferimenti per i frammenti di documento richiedono molto tempo. NPR-17033
* Il testo giustificato viene rappresentato in un font diverso durante l&#39;anteprima della lettera. NPR-16976
* La funzionalità di ricerca non funziona correttamente se il testo ricercato contiene più occorrenze. NPR-16920
* La barra degli strumenti Editor di testo viene visualizzata in modo intermittente nel browser. NPR-16919
* Il costrutto **[!UICONTROL Salva modulo]** dall&#39;Editor regole non funziona. NPR-16905
* L&#39;elenco a discesa Font non compila la famiglia Font durante la creazione di un modulo di testo basato sul dizionario dati tramite Internet Explorer. NPR-16944
* Dopo la creazione di un frammento di testo, il font della lettera cambia durante la visualizzazione dell&#39;anteprima della lettera. NPR-16830
* Non è possibile eseguire il rendering o l&#39;anteprima delle lettere contenenti spazi tabulazione all&#39;inizio o tra le espressioni incluse nel frammento di documento. NPR-16769

**Mobile Forms**

* Nell&#39;anteprima dei moduli per dispositivi mobili viene visualizzato il contenuto sovrapposto, anche se il modulo viene visualizzato correttamente per il rendering PDF. NPR-17105

**Forms Portal**

* Facendo clic sul collegamento **[!UICONTROL Scarica]** per un modulo inviato si apre una pagina HTML invece di un modulo PDF. NPR-17082

* `Upload Comments` i file allegati non vengono visualizzati nell&#39;interfaccia utente per le istanze inviate, anche se sono presenti nel file XML memorizzato nell&#39;archivio crx. NPR-17075

**Servizio estensioni Reader**

* Un file specifico non è un Reader esteso AEM&#39;installazione OSGI dei moduli. NPR-16625

#### Programma di installazione di JEE per Forms  {#forms-jee-installer-16}

**Core**

* Durante il processo di aggiornamento, Configuration Manager non riesce con timeout. NPR-16774 (vedere [Configurazione del timeout per le operazioni a livello di componente](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Gestione dei processi - Area di lavoro HTML**

* Il punto di inizio di un&#39;attività di avvio non inizia con i dati inviati al momento dell&#39;invio del punto di inizio. NPR-16917
* Facendo clic sul pulsante **[!UICONTROL Return]** per un modulo nell&#39;area di lavoro HTML, il modulo non viene chiuso ma viene riportato nella coda di gruppo.\
   NPR-16352

**Gestione processi**

* Consentire agli utenti di impostare il nome visualizzato delle attività precedenti su una qualsiasi delle attività successive in un&#39;istanza di processo. NPR-15382

**Servizio di output**

* Il servizio di output non è in grado di elaborare un PDF modificato per includere un campo &#39;milli-sec&#39; aggiuntivo nei metadati `date-time format`. NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer Script Editor non rispetta le impostazioni predefinite di Proprietà modulo per `Calculate Event`e `Validate Event`. NPR-15921

### Pacchetti di funzioni inclusi in CFP4 {#feature-packs-included-in-cfp-1}

**Forms Add-on Package**

* Miglioramento nell&#39;Editor delle condizioni in linea per la gestione della corrispondenza. NPR-10981

### Pacchetti OSGi inclusi in CFP4 {#osgi-bundles-included-in-cfp-4}

Elenco dei bundle OSGi aggiornati tra AEM 6.2 SP1 e CFP4

I punti salienti di CFP3 sono:

* Funzionalità di ricerca più efficienti per l’interfaccia classica e per il componente di ricerca AEM tramite proxy con autenticazione digest
* Correzioni dei problemi durante il caricamento delle risorse e la visualizzazione dei metadati delle risorse
* Corregge i problemi durante la creazione di cartelle e lo spostamento di pagine nel caso in cui il titolo contenga caratteri speciali.
* Correzioni per l&#39;utilizzo del targeting - sincronizzazione dei tipi di pubblico, pubblicazione di campagne e selezione di Metrica obiettivo nell&#39;interfaccia utente touch
* Risolti i problemi di sincronizzazione per i processi di traduzione
* Protezione avanzata per il servizio di precompilazione Forms
* Miglioramenti nel componente Bozza e Invii del portale moduli e nel servizio Forms con codice a barre
* Miglioramenti a livello di usabilità per i moduli adattivi contenenti widget di allegati di file o frammenti caricati in modo pigro.
* Sono stati apportati miglioramenti in termini di usabilità nella gestione della corrispondenza, tra cui funzionalità di ricerca avanzate, registrazione di risorse eliminate e importazione di dizionari di dati.

### Piattaforma {#platform-13}

* Una condizione race in **ModelAdapterFactory**, che è possibile quando due thread tentano di inserire lo stesso campo, non riesce a costruire il modello. NPR-16443: Hotfix per SLING-6584
* Opzione di convalida in Gestione pacchetti per rilevare eventuali conflitti tra il file sovrapposto (file JSP o JavaScript) in /apps e quello contenuto in un Hotfix in /libs. La sovrapposizione interessata può quindi essere ridotta in modo da includere le modifiche dal file in /libs. NPR-16216: Hotfix per CQ-81729
* L&#39;accesso nel file error.log a volte si arresta alcuni secondi dopo l&#39;avvio dell&#39;editore e deve essere cancellato per essere eseguito di nuovo. Richiesta di aggiornare il framework di registrazione e fornire la registrazione Sling. NPR-15913: Hotfix per GRANITE-15452
* Richiesta di aggiornamento dell&#39;API JavaScript &quot; `use"` per evitare errori nell&#39;implementazione dell&#39;API Use JavaScript HTL. NPR-16461: Hotfix per SLING-6780

### Siti {#sites-16}

* Dopo l’aggiornamento da AEM 6.0 a AEM 6.2, l’interfaccia classica mostra prestazioni rallentate durante la ricerca dei tag a causa di numerose query. Per risolvere il problema, è possibile seguire la procedura descritta in [Disattivazione dello stato di replica nella console di assegnazione tag (interfaccia classica)](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr). NPR-15842: Hotfix per CQ-4201748.

* Durante la creazione di una pagina nell’interfaccia utente touch, il campo Input check for &#39;name&#39; non verifica il carattere speciale &#39;Apostrofo&#39; (come nell’interfaccia classica). Pertanto, non è possibile spostare la pagina. NPR-16404: Hotfix per CQ-4205321.
* Se si applicano stili diversi su due righe nell’editor Rich Text e si uniscono questi stili, viene rimosso lo stile applicato alla seconda riga. NPR-16389: Hotfix per CQ-4203835.
* Nella schermata Siti dell&#39;interfaccia touch, il tentativo di incollare una pagina all&#39;interno di una pagina senza pagine secondarie non funziona in quanto il pulsante Incolla non viene visualizzato. NPR-15894: Hotfix per CQ-4201696.
* Durante lo scorrimento della scheda Pagine nel pannello Content Finder, alcuni set di pagine vengono visualizzati all’infinito nell’interfaccia classica, mentre l’interfaccia touch mostra un set limitato di poche pagine non ripetute. NPR-16271: Hotfix per CQ-4202371
* Se si aprono le proprietà pagina di una LiveCopy nell&#39;interfaccia utente touch e si fa clic su Salva senza apportare alcuna modifica, qualsiasi scheda LiveCopy viene annotata e viene creato un nodo di configurazione LiveSync. NPR-16327: Hotfix per CQ-108562
* Il vincolo del modulo non è in grado di leggere la proprietà `ConstraintMessage`. NPR-16388: Hotfix per CQ-101330
* Il componente `wcm/foundation/components/parsys` non visualizza il segnaposto **[!UICONTROL &#39;Trascina qui i componenti]**&#39;. NPR: 16748: Hotfix per CQ-4205187

### Risorse {#assets-16}

* Il rasterizzatore pdf smette di funzionare e causa problemi di memoria insufficiente dopo l&#39;installazione di 6.2 SP1 o Hotfix 12430. NPR-15991
* I metadati di una proprietà stringa `documentNumber` vengono visualizzati come data, mentre devono essere numeri. NPR-16134: Hotfix per GRANITE-16916
* Troncamenti di testo nel fumetto evento della cronologia. NPR-16226: Hotfix per CQ-85226
* Quando create una cartella sotto la gerarchia del contenuto con un titolo con caratteri speciali, viene visualizzato il modulo codificato del carattere speciale. NPR-15935: Hotfix per CQ-4202987
* L’utente non può caricare risorse o creare cartelle mentre naviga tra le risorse a causa di comportamenti non coerenti visualizzati quando utilizza il pulsante &quot;Crea&quot;. NPR-16410: Hotfix per CQ-4204793
* Errori imprevisti durante il caricamento di risorse HTML condivise dalla visualizzazione degli articoli in AEM Authoring. NPR-16133: Hotfix per AEMM-4155970

### Integrazione {#integration-14}

* Quando si abilita l&#39;autenticazione proxy con l&#39;autenticazione Digest, il componente AEM Search genera un&#39;eccezione ConcurrentModificationException. NPR-15309: Hotfix per CQ-4199191
* Quando si crea un&#39;attività Test A/B Target in AEM, l&#39;audience non si sincronizza con Target e non mostra &#39;nessun pubblico&#39;. NPR-16229: Hotfix per CQ-4204210
* Dopo aver installato SP1+NPR-11577 v1.2, quando si sceglie &quot;Usa una metrica Analytics&quot; per la metrica Obiettivo durante il targeting nell&#39;interfaccia touch, l&#39;elenco a discesa delle metriche non si carica mai. NPR-16129: Hotfix per CQ-4204316
* Quando si utilizza il targeting, la pubblicazione della campagna non pubblica automaticamente l&#39;intero albero, incluso il marchio e il master. NPR-15855: Hotfix per CQ-94630

### Traduzione {#translation-8}

* Il processo di conversione della sincronizzazione non viene attivato automaticamente e AEM polling non si verifica senza il blocco dei progetti di traduzione. NPR-15163: Hotfix per CQ-90856

### Forms {#forms-17}

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-17}

**Moduli adattivi**

* Durante il salvataggio di un modulo adattivo con un allegato, il percorso completo dell&#39;allegato viene aggiunto nel tag `fileAttachment` dell&#39;XML generato, anziché nel nome dell&#39;allegato. NPR-16529
* Nei moduli adattivi basati su XDP, il wrapper `afData/afBoundData` è presente nel file XML inviato, anche se anche il file XML di precompilazione non contiene wrapper `afData/afBoundData`. NPR-16118

* Notazione esponenziale nel campo Numero: Quando si utilizzano i moduli adattivi, se viene immesso un numero con una frazione decimale superiore a dieci caratteri in totale, il numero diventa una notazione esponenziale nell&#39;XML inviato. NPR-16106
* Per i moduli che contengono sia un componente allegato che un frammento caricato pigro, l&#39;XML dei dati inviato non contiene le informazioni relative al componente allegato. NPR-16022
* Per un pannello ripetibile caricato pigro che non ha un predecessore ripetibile, gli elementi secondari ripetibili all’interno di una seconda istanza del pannello non vengono ripetuti. NPR-15944
* Durante il tentativo di salvare un frammento all&#39;interno di un frammento nell&#39;editor del modulo, l&#39;elemento principale del modello di frammento non compila il valore del frammento secondario. NPR-15943
* Durante la creazione di una casella di controllo con un solo elemento e il tentativo di mostrare il titolo della casella di controllo mantenendo nascosto il titolo dell&#39;elemento, l&#39;azione Crea dizionario genera un `ArrayIndexOutOfBoundException` se il testo dell&#39;elemento è vuoto. Il dizionario non viene creato e sullo schermo non viene generata alcuna risposta di errore. NPR-15816
* Per i moduli adattivi con widget di allegati, alcune parti del modulo vengono disattivate dopo l&#39;anteprima del file allegato.\
   NPR: 16611

* Per i widget di allegati contenenti più allegati, se una nuova istanza di modulo con un allegato viene inviata a un widget con un allegato precedente, all’apertura dell’allegato aggiunto viene visualizzato un codice di errore anziché il contenuto effettivo. NPR-16258
* Proteggere il servizio di precompilazione dei moduli dall&#39;accesso non autorizzato tramite protocolli quali `file://`, `http://` e `ftp://`. Fare riferimento a &quot; [Configurazione del servizio di precompilazione tramite Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754).&quot; NPR-15414

* Richiesta di eseguire il rendering del modulo adattivo in formato PDF anziché HTML nel passaggio Verifica e aggiunta di tutti gli allegati al PDF, in modo che la stampa visualizzi il modulo completo. NPR-9011

**Gestione della corrispondenza**

* Quando si lavora con un frammento di testo in una lettera in modalità Anteprima/Modifica, se il testo viene convertito in elenco, viene generata un&#39;interruzione dell&#39;intera funzionalità delle lettere e un errore JavaScript. NPR-16460
* L&#39;importazione di un file XSD per creare un dizionario dati nel nodo Gestione corrispondenza non riesce poiché il browser non risponde ogni volta che viene caricato XSD e selezionato il nodo principale. Questo problema è indipendente dal browser e non viene visualizzato nei registri del server. NPR-16452
* Quando si visualizza l&#39;anteprima di una lettera utilizzando il browser Internet Explorer e si tenta di modificare la dimensione del font del contenuto, i valori duplicati vengono visualizzati da 8 a 72 nel menu a discesa delle dimensioni del font. NPR-16387
* Se un campo mobile viene visualizzato come campo di input da un frammento XDP, il campo non si espande nell&#39;anteprima della lettera durante l&#39;utilizzo del browser Internet Explorer. NPR-16367
* Quando si tenta di inviare una lettera direttamente dall&#39;anteprima, la finestra a comparsa per il nome della lettera non viene visualizzata correttamente a causa del fatto che è nascosta. NPR-16353
* Gli spazi di riga aggiunti durante la modifica di una lettera non vengono visualizzati nella finestra Anteprima. Per gli elenchi in frammenti di testo, l&#39;output PDF non mostra la spaziatura corretta. NPR-16267
* Durante l&#39;utilizzo di un frammento di documento di testo in Internet Explorer, il tentativo di applicare un rientro al testo non riesce in quanto il cursore non consente il rientro del testo. NPR-16128
* L&#39;aggiunta o la modifica di un dizionario dati a un frammento di documento di testo esistente richiede molto tempo e l&#39;utente non riceve sempre notifiche. NPR-16102
* Durante l&#39;anteprima di una lettera con contenuto scorrevole mediante il browser Internet Explorer, la barra di scorrimento del browser si sovrappone alla barra di scorrimento della lettera e l&#39;intero contenuto non può essere visualizzato per i frammenti sul lato destro. NPR-16068
* Durante la creazione o la modifica di frammenti di documento di testo mediante il browser Google Chrome, il menu a discesa di selezione del colore viene visualizzato automaticamente e non può essere rimosso. Per poter modificare il frammento, l&#39;utente deve selezionare l&#39;elenco come tipo di immissione dati. NPR-16067
* Quando si utilizza l&#39;API Letterinstance, il metodo `import com.adobe.icc.services.api.LetterInstanceService` non funziona. NPR-16008
* La modifica dei formati di visualizzazione della data in `locale=en_US; dateFormat=MMM dd,yyyy;` nella configurazione di Asset Composer non funziona come previsto e il formato della data viene visualizzato come caratteri indesiderati. NPR-16007
* Il tipo di collegamento dati in lettere durante la re-authoring viene visualizzato come &quot;Utente&quot; anche se impostato diversamente in precedenza. NPR-16619

**Forms Portal**

* Gli scenari di aggiornamento per i componenti bozza e invio non funzionano con l&#39;implementazione di esempio di database. NPR: 16752

**Servizio Forms con codice a barre (BCF)**

* L&#39;analisi del codice statico dei report di Forms Service (BCF) con codice a barre ha dei problemi. NPR-13855

#### Programma di installazione di JEE per Forms  {#forms-jee-installer-17}

**Gestione dei processi - Area di lavoro HTML**

* Proteggere il servizio di precompilazione dei moduli dall&#39;accesso non autorizzato tramite protocolli quali &quot;file://&quot;, &quot;http://&quot; e ftp://. Per informazioni dettagliate, consultate [Configurazione del servizio di precompilazione tramite Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754). NPR-15434

**User Management **

* Nella schermata di accesso SAML viene mostrata la versione non corretta (6.1.0) sul server AEM 6.2. NPR-13825
* Con  AEM Forms configurato per l&#39;autenticazione Single Sign On (Kerberos), se l&#39;autenticazione dell&#39;utente non riesce durante il tentativo di accesso, viene restituito un codice di errore &#39;404&#39;. L’utente viene reindirizzato al sito di accesso solo dopo l’aggiornamento della pagina. NPR-15015

#### Forms Designer {#forms-designer-1}

* La modifica delle impostazioni internazionali del modulo in francese (Canada) nel controllo ortografia dizionario non funziona in  AEM Forms Designer.\
   NPR-15896

### Pacchetti di funzioni inclusi in CFP3 {#feature-packs-included-in-cfp-2}

**Forms Add-on Package**

* Quando si elimina una risorsa nella gestione della corrispondenza, nel file error.log deve essere registrato un messaggio di avviso. NPR-13225
* Migliorate la funzionalità di ricerca durante l&#39;anteprima di una lettera nella gestione della corrispondenza, per consentire la ricerca del testo nel contenuto del frammento di testo, invece di cercare solo il titolo o l&#39;etichetta della lettera. NPR-16103

### Pacchetti OSGi inclusi in CFP3 {#osgi-bundles-included-in-cfp-5}

Elenco dei bundle OSGi aggiornati tra AEM 6.2 SP1 e CFP3

[Get ](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
FileLe principali caratteristiche di Cumulative Fix Pack 2 sono:

* Correzioni di stabilità e miglioramenti delle prestazioni AEM piattaforma, inclusi Sling framework e operazioni
* Gestione delle risorse migliorata con diverse correzioni per accedere, spostare, cercare, caricare e pubblicare le risorse
* Miglioramento della creazione e della gestione di siti con correzioni nei frammenti di contenuto, plug-in di ancoraggio, presentazione e componenti Context Hub
* Diverse correzioni nell’interfaccia utente touch, tra cui editor di testo, ricerca Omnisearch e processo di creazione delle varianti
* Flussi di lavoro di traduzione migliorati; è stato migliorato il connettore Microsoft per l&#39;utilizzo delle nuove API di traduzione per il portale di Azure
* Problemi risolti in progetti e campagne
* Gestione e authoring migliorati con correzioni nei moduli adattivi, gestione della corrispondenza e funzioni del portale dei moduli
* Correzioni nei componenti core, XTG e dell’area di lavoro HTML di Forms JEE

### Piattaforma {#platform-14}

* La `SlingPostProcessor` viene attivata se viene modificata la pagina che fa direttamente riferimento al framework Sling. NPR-15754: Hotfix per CQ-104153

* Il valore per i tag con proprietà `tagBasePath` non viene recuperato nella finestra di dialogo dell&#39;interfaccia classica mentre si passa a un componente di pagina. NPR-15543: Hotfix per CQ-4199950

* Durante le operazioni Sling, quando si dispone di un blocco denominato &#39;chunk_n_n-1&#39; `SlingFileUpload handler.getLastChunk` viene eseguito in un ciclo infinito con blocchi vuoti. NPR-15455: Hotfix per SLING-5701

* Quando un&#39;interfaccia estende un&#39;altra interfaccia, i metodi iniettabili nell&#39;interfaccia super non vengono iniettati correttamente. NPR-15202: Hotfix per SLING-5710
* Una potenziale eccezione di puntatore nullo non viene impedita quando si utilizza la chiamata alla funzione `com.adobe.granite.infocollector.impl.FilesTraversal`. Hotfix NPR-15169 per CQ-4197640
* Lo stato del flusso di lavoro non è coerente per alcuni nodi secondari e viene visualizzato un errore durante l&#39;invio di eventi di osservazione per tale nodo. NPR-15701: Hotfix per GRANITE-13786
* Quando l&#39;utente seleziona un nodo in CRXDE (ad esempio, /content/dam/) e quindi la scheda &quot;Controllo di accesso&quot;, accertandosi che esista un elenco di controllo di accesso, trascinando e rilasciando alcuni elementi si spostano gli elementi diversi da quello selezionato. Hotfix NPR-15696 per GRANITE-16300
* Se selezionate un utente dall’elenco a discesa quando tentate di spacciarsi, viene visualizzata l’intera finestra a comparsa dell’utente. NPR-15774: Hotfix per CQ-4201738/GRANITE-11895
* In Omnisearch, la ricerca per tag con suggerimenti popolati automaticamente non funziona. NPR-15088: Hotfix per GRANITE-14426.\
   Nota: Questa correzione richiede il CFP Oak 1.4.11 o versione successiva.

### Mobile AEM Author {#mobile-aem-author}

* Quando utilizzate pacchetti  AEM Mobile e ContentSync con un&#39;applicazione ibrida, AEM risponde a una richiesta di recupero (con marche temporali) effettuata dall&#39;applicazione con il pacchetto più vecchio, invece di quella richiesta dall&#39;applicazione. NPR-15749: Hotfix per CQ-104153

### Siti {#sites-17}

* Lo stato di modifica per Workflow Inbox nel core WCM non cambia se l&#39;utente modifica una pagina dopo l&#39;attivazione di un flusso di lavoro. NPR-15684: Correzione per CQ-4196974
* Il plug-in Ancoraggio in Editor Rich Text per l’interfaccia utente Touch genera HTML5 non conforme quando l’utente fa clic sull’icona di ancoraggio e aggiunge un nome. Dovrebbe aggiungere un attributo &#39;id&#39; invece dell&#39;attributo &#39;name&#39; nel tag HTML5 per l&#39;elemento di ancoraggio. NPR-15650: Hotfix per CQ-89782
* Quando si crea uno schema di metadati con numerosi campi e lo si applica ai metadati dei frammenti di contenuto, nella schermata dei metadati dei frammenti di contenuto non viene creata alcuna barra di scorrimento che rende i campi non modificabili. NPR-15478: Hotfix per CQ-4202622
* La modifica del componente Campo `TagInput` non mostra i valori configurati in precedenza rispetto ai campi della finestra di dialogo. NPR-15464: Correzione per CQ-4200360

* Nell’interfaccia utente dell’editor dei frammenti di contenuto, se vengono create molte varianti di un frammento di contenuto, il pannello laterale non mostra la barra di scorrimento per navigare tra tutte le varianti. NPR-15445: Correzione per CQ-4199444
* Quando gli utenti vengono rimossi dai gruppi diretti, vengono aggiunti ai gruppi ereditati. NPR-15400: Hotfix per CQ-98758
* Authoring WCM: L&#39;autore dell&#39;interfaccia touch non consente la modifica di pagine con virgole nel nome. NPR-15396: Hotfix per CQ-4199723
* Quando si utilizza l&#39;interfaccia utente touch per la creazione, la funzione `Granite.author.editableHelper.doSelectParent` trasmette gli argomenti in ordine errato generando un errore JavaScript. NPR-15349: Hotfix per CQ-4198594
* Il segmento ContextHub visualizza l&#39;esperienza anche se è presente il cookie di rinuncia. NPR-15293: Hotfix per CQ-4198024
* Il componente Presentazione nell’interfaccia classica non può creare diapositive né trascinare e rilasciare immagini per creare nuove diapositive. NPR-15281: Hotfix per CQ-4194164
* Agli utenti, a prescindere dall&#39;autorizzazione, vengono visualizzate le opzioni &quot;Crea&quot; quali Crea pagina, Crea sito, Crea Live Copy, Crea lancio e Crea catalogo, come voci di menu nella console Site Admin (Amministrazione sito). NPR-15278: Hotfix per CQ-94436
* Dopo aver installato AEM 6.2 Service Pack 1, il cursore &#39;Includi sottopagine&#39; smette di funzionare per gli avvii di pagina. NPR-15230: Hotfix per CQ-4198449
* Richiesta per migliorare Version Purge per recuperare ed elaborare le versioni in blocchi ed anche per poter utilizzare un percorso specificato in una query XPath. NPR-15186: Hotfix per CQ-109205
* Il pulsante Cancella non è presente nella scheda della miniatura Proprietà pagina nel componente Siti. Hotfix NPR-15143 per CQ-4196997
* Per un sito che utilizza Live Copy, quando si seleziona la casella di controllo Live Copy nel riquadro Colonne nella console di amministrazione del sito lo stato Live Copy non viene visualizzato correttamente e viene visualizzata solo la marcatura HTML. NPR-15108: Hotfix per CQ-97086
* Durante la modifica di frammenti di contenuto, se l&#39;utente fa clic su Fine (&#39; ño&#39;) per la modifica prima di ottenere la risposta del post, il contenuto modificato non viene salvato correttamente. NPR-15014: Hotfix per CQ-4194095
* Se si chiude la pagina Modifica in modalità Timewarp e si tenta di riaprirla da Siteadmin, si verifica un errore con lo stato &#39;500&#39; invece di riaprire la pagina. NPR-14965: Hotfix per CQ-109647:
* Nell’interfaccia utente di Digital Asset Manager (DAM), la ricerca nel selettore utente Trova autorizzabili causa un’eccezione &quot;Memoria insufficiente&quot;. NPR: 15307: Correzione per CQ-98542

### Risorse {#assets-17}

* Dopo aver cercato una risorsa in Omnisearch, selezionando una risorsa e provando a modificarne le proprietà facendo clic su &#39;Visualizza proprietà&#39;, quindi il pulsante &#39;Salva&#39; reindirizzerà gli utenti a una pagina vuota. NPR-15900: Hotfix per CQ-4202372
* Risorse L&#39;interfaccia utente non risponde agli eventi. Se selezionate una risorsa e fate clic su &#39;Pubblica&#39; o &#39;Rappresentazioni&#39;, non viene generata alcuna attività. NPR-15828: Hotfix per CQ-4202247
* Quando pubblicate una risorsa dalla vista Scheda, la scheda non viene aggiornata per riflettere lo stato di pubblicazione a meno che la pagina non venga aggiornata. NPR-15826: Correzione per CQ-102732
* Hotfix cumulativo contenente hotfix di risorse. NPR-15225
* Se il carattere e commerciale (&#39;&amp;&#39;) è incluso nel nome di una cartella di risorse, il nome della cartella non viene visualizzato correttamente quando si passa alla risorsa. NPR-15775: Hotfix per CQ-4201735
* L&#39;utilizzo del carattere e commerciale (&#39;&amp;&#39;) nel nome di un file di risorse causa problemi durante l&#39;accesso alle relative proprietà. NPR-15770: Hotfix per CQ-4201737
* Durante la navigazione nelle risorse e la modalità di visualizzazione &quot;Vista a colonne&quot;, se l’utente aggiorna la pagina dopo aver selezionato e fatto clic su una risorsa, i dettagli della risorsa vengono visualizzati al posto del contenuto aggiornato. NPR-15768: Hotfix per CQ-4201727
* L&#39;assimilazione PDS richiede un utilizzo della CPU al 100% con un mucchio di librerie per i servizi pdf. Correzione NPR-15606 per GRANITE-12929
* L&#39;accesso all&#39;interfaccia utente &quot;Condivisione collegamento personale&quot; mediante il browser Firefox non visualizza gli elementi condivisi o gli utenti e lo schermo non è utilizzabile. NPR-15539: Correzione per CQ-4200992
* Quando si utilizza Digital Asset Manager, se una pagina è associata a un set di immagini, lo spostamento delle immagini in una nuova cartella interrompe l’associazione di pagina e nella pagina associata mancano alcune immagini. NPR-15538: Hotfix per CQ-111479
* Nel componente Visualizzatore Dam, l’utilizzo della modalità di esecuzione &quot;nosamplecontent&quot; genera errori con i contenuti multimediali dinamici. NPR-15449: Hotfix per CQ-4195425
* Durante la creazione di profili video, se sono stati scelti sia un predefinito di qualità elevata che un predefinito di codifica video di qualità media, le modifiche apportate non vengono salvate. NPR-15447: Hotfix per CQ-4195482
* Anche se il caricamento di una risorsa in Brand Portal non riesce a causa di una risposta di errore del server, lo stato viene aggiornato a &quot;Pubblicato&quot; nell’interfaccia utente del portale dei marchi, rendendo difficile il tracciamento del file perduto. NPR-15442: Hotfix per CQ-4197968
* Quando si pubblica una cartella di risorse nel Brand Portal, dove la pubblicazione richiede più di un&#39;ora, alcuni file non vengono pubblicati. NPR-15441: Hotfix per CQ-4199493
* Se si utilizza la console di Asset Finder nella vista a colonne, il tentativo di creare una cartella non riesce una volta ma riesce a riprovare. NPR-15370: Hotfix per CQ-4199448
* Se una risorsa o una cartella selezionata nell’interfaccia utente di DAM ha una virgola nel nome, la scheda Riferimenti non è disponibile e compare il messaggio &quot;Elenco di riferimenti non è disponibile per selezioni multiple&quot;. NPR-15362: Hotfix per CQ-4199721
* La pubblicazione di una cartella in Brand Portal non modifica lo stato di pubblicazione della cartella, anche se le risorse in essa contenute sono state pubblicate correttamente. NPR-15292: Hotfix per CQ-4197667
* Mentre andate alla console Risorse nell’interfaccia touch, compare un’eccezione durante l’attivazione di determinate risorse. NPR-15217: Correzione per CQ-108779
* Pubblicazione di un video su Youtube quando la connessione viene stabilita tramite un server proxy. NPR-15109: Correzione per CQ-110332
* Utilizzo di una risorsa con un nome contenente un punto o un punto (.) in data-side-resource non risolve la stessa risorsa e il percorso di output viene terminato in corrispondenza del punto. NPR-15069: Hotfix per CQ-4195914
* Dopo aver aggiornato AEM 6.2 a Service Pack1, la sincronizzazione delle risorse in Scene7 non riesce. La proprietà dam:Scene7FileStatus visualizza lo stato &#39; `UploadFailed`&#39; anche per le risorse pubblicate. NPR-15269: Hotfix per CQ-4197708

### Interfaccia utente {#user-interface-5}

* In **[!UICONTROL Touch UI]**, la data salvata non viene visualizzata per i campi data che non hanno tipo=&#39;datetime&#39; quando si utilizza il browser Internet Chrome versione 56.0.2924.87. NPR-15383: Hotfix per GRANITE-16481
* In **[!UICONTROL Interfaccia touch]**, l&#39;Editor Rich Text rimuove il thread e gli elementi della didascalia dalle tabelle HTML durante il rendering. NPR-15267: Hotfix per CRTE-41
* `FileUpload Validator` non gestisce i casi in cui l&#39;avvio automatico è vero o quando  `uploadFile()` viene chiamato manualmente e genera in questi casi un rapporto di convalida non valido. NPR-15295: Hotfix per GRANITE-13499

* Omnisearch non consente ai clienti che utilizzano /apps di aggiungere un&#39;origine dati di colonna in quanto presuppone che la configurazione della posizione sia elencata in */libs/granite/omnisearch/content/metadata/*. Hotfix NPR-13188 per GRANITE-16479
* Quando si utilizza l&#39; **[!UICONTROL Touch UI]**, le varianti di prodotto non vengono create allo stesso livello del prodotto. L&#39;utente non è informato sullo stato del processo di creazione della variante. NPR-15345: Correzione per CQ-4198948

**Scene7**

* L&#39;esecuzione del flusso di lavoro Scene7 genera file aperti che non vengono chiusi. Richiesta di migliorare il servizio AEM-S7 in modo da mantenere e riutilizzare una singola istanza HttpClient con configurazione di pooling condivisa. NPR-15357: Correzione per CQ-109958

### Traduzione {#translation-9}

* Quando si utilizzano progetti di traduzione, aggiornando le copie della lingua dal master inglese, vengono generati 11 avvii separati con lo stesso nome e radice di origine, ma con radici di avvio leggermente diverse, nel caso in cui il nome della pagina segua un pattern impostato. NPR-15605: Hotfix per CQ-4200699
* I progetti di traduzione non vengono creati per le pagine quando le radici della lingua contengono trattini e trattini nel nome. NPR-15171: Correzione per CQ-96286
* Richiesta di aggiornamento del connettore Microsoft per poter utilizzare le API Microsoft Translator, che Microsoft rende disponibili nel portale di Azure. NPR-15320: Hotfix per CQ-101010

### Progetti {#projects-4}

* Nella schermata Progetti sono visibili solo 20 progetti inattivi anche se nella directory archivio sono presenti più di 20 progetti inattivi. NPR-15656: Hotfix per CQ-4200903

### Campaign {#campaign-1}

* Se utilizzate i componenti Campaign - Targeting e MAC - Integrazione di Test e Target, la disattivazione della pubblicazione delle attività non aggiorna lo stato dell&#39;attività nell&#39;interfaccia utente principale. NPR-15401: Correzione per CQ-4199839
* Durante lo spostamento di un prodotto in AEM Commerce, la Creazione guidata spostamento prodotto non presenta i valori precompilati per il nome del prodotto, il titolo, le pagine a cui viene fatto riferimento, la creazione dell&#39;autore e la data di creazione. NPR-15228: Hotfix per CQ-98617

### Sicurezza {#security-4}

* Parametro token CSRF aggiunto ai moduli con un metodo GET. NPR-15229

### Forms {#forms-18}

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-18}

`**Adaptive Forms**`

* I valori predefiniti vengono sostituiti da valori vuoti in xml durante la precompilazione del modulo adattivo con l&#39;XML di input. NPR-15721
* Il wrapper `afData/afBoundData` è presente nel file XML inviato, anche se anche il file XML di precompilazione non contiene il wrapper `afData/afBoundData` nei moduli adattivi basati su schema XML. NPR-15541

* I titoli nella barra degli Accordion devono essere titoli HTML &#39;h2&#39; modificabili invece del tag &#39;a&#39;. NPR-15475
* Il layout a soffietto di un pannello del modulo non è accessibile agli utenti dell&#39;assistente vocale. Gli utenti non possono passare alla scheda Accordion utilizzando la sola tastiera utilizzando un software di lettura dello schermo come JAWS o NVDA. NPR-15474

`**Correspondence Management**`

* Il salvataggio, l&#39;eliminazione e l&#39;impostazione del riferimento per un frammento di documento richiedono molto tempo. NPR-15939
* Allineamento tabulazione impostato in Gestione risorse su testo contenente più interruzioni di intestazione nell’interfaccia utente CCR. NPR-15818
* Le miniature dei moduli di testo non mostrano contenuto allineato, anche se il testo contiene contenuto allineato creato utilizzando Tabulazioni in Google Chrome. NPR-15819

`**Forms Portal**`

* Il servizio di precompilazione non funziona per XDP Forms. NPR-15466
* Quando si memorizzano le bozze dei moduli adattivi e si inviano al database, lo stato del modulo adattivo viene danneggiato quando la connettività del database non riesce per qualsiasi motivo (ad esempio, dopo un lungo periodo di inattività). NPR-15297

#### Programma di installazione di JEE per Forms  {#forms-jee-installer-18}

`**Core**`

* Dopo l&#39;aggiornamento alla versione più recente di Java 1.8.0_121-b13, l&#39;interfaccia utente amministratore non è accessibile in  AEM Forms. NPR-15330

`**XTG**`

* Durante l&#39;utilizzo del servizio Output per unire un modulo specifico a un dataxml, il tempo di risposta è 20 volte superiore al tempo impiegato dal server ES4 SP1 per la stessa operazione. NPR-15283

#### App AEM Forms {#aem-forms-app-1}

* Durante il ripristino delle attività non salvate, è necessario rendere più chiaro il messaggio visualizzato al ripristino delle attività non salvate per ridurre gli errori dell&#39;utente. NPR-15377
* &#39;app AEM Forms non esegue il rendering dei moduli creati da modelli personalizzati. NPR-15892
* Gli utenti non sono in grado di accedere all&#39;app  AEM Forms. NPR-15891

I punti salienti di AEM 6.2 SP2-CFP1 sono:

* Semplifica la funzionalità di replica in Sites:

   * Correzioni a vari problemi di rollout, LiveCopy e scrittura non corretta

* Ottimizza la reattività dell&#39;interfaccia utente touch durante:

   * Ricerche di risorse
   * ordinamento basato sulle dimensioni

* Migliora la gestione dei tag nelle raccolte intelligenti
* Controlli di accesso più rigidi durante le operazioni CRUD sulle cartelle

### Piattaforma {#previous}

* Richiesta di rimozione delle chiamate API `ReplicationQueue#forceRetry` durante l&#39;avvio degli agenti di replica, in quanto tali chiamate rallentano notevolmente l&#39;istanza, soprattutto quando ha molti agenti di replica. NPR-14032: Hotfix per GRANITE-13095
* Richiedi la configurazione `DurboImportConfigurationProviderService` OSGi per supportare i campi in grado di memorizzare un array di valori. NPR-14570: Hotfix per CQ-108684
* Se si utilizza il componente Sightly in una pagina dopo la migrazione alla AEM 6.2, la finestra di dialogo Proprietà della pagina non funziona più. NPR-14328: Hotfix per CQ-108355
* La disprogrammazione di un processo pianificato in precedenza non rimuove il nodo corrispondente sotto */var/eventing/Scheduled-jobs*. NPR-14253: Hotfix per SLING-5666
* Quando un amministratore tenta di spacciarsi per un utente eliminato, l&#39;interfaccia utente non viene aggiornata. NPR-14247: Hotfix per CQ-107446
* Controllo protezione XSS che causa una codifica non corretta nel componente Sightly. NPR-14004: Hotfix per CQ-93821
* Richiesta di aggiornare Jackrabbit Filevault alla versione 3.1.30 per risolvere più problemi. NPR-13454
* L&#39;errore della cache si verifica quando la distribuzione Sling sincronizza i pacchetti di distribuzione dall&#39;autore alla pubblicazione. NPR-13034: Hotfix per GRANITE-13970

### Siti {#sites-18}

* Problemi con VersionManagerImpl che eliminano versioni non corrette dalla cronologia delle versioni. NPR-14372
* Il componente Parsys di WCM Sightly Foundation ignora i nomi dei tag della dichiarazione del componente, `cq:htmlTag / cq:tagName`. NPR-14225
* Quando Sightly Parsys viene utilizzato per eseguire il rendering dei componenti inseriti tramite JavaScript nell&#39;interfaccia utente touch, la decorazione personalizzata viene ignorata dopo l&#39;aggiornamento della pagina. NPR-14122
* Gli elenchi a discesa Target non funzionano nella finestra di dialogo dell&#39;interfaccia utente touch quando vengono creati più campi Richtext, ad esempio i collegamenti. NPR-13911
* Quando si modifica un campo di testo con più proprietà Editor Rich Text (RTE) in una finestra di dialogo (interfaccia utente touch), lo stato attivo si sposta in modo casuale su una specifica proprietà RTE. NPR-13703
* Il componente video predefinito non esegue il rendering della miniatura video. NPR-14976
* Informazioni caricate lentamente nella scheda Live Usages (Uso live) nell&#39;Editor modelli. NPR-14880: Hotfix per CQ-83417
* L&#39;installazione di Hotfix-10936 su un&#39;istanza AEM 6.2 disattiva il componente iparsys. NPR-14330: Hotfix per CQ-106982
* Più problemi relativi ai componenti Rollout e un problema di Live Copy dopo la migrazione a AEM 6.1 SP1. NPR-15256
* L’azione Rollout pagina non riesce a creare elementi figlio oltre il primo livello anche per più configurazioni di rollout. NPR-15055
* Quando si invia la finestra di dialogo Proprietà pagina dall&#39;Editor, i dati non modificati nelle schede LiveCopy vengono riscritti. NPR-14693
* Quando la finestra di dialogo Proprietà pagina viene inviata dall&#39;editor, MSM Post Processor scrive alcuni parametri dalla richiesta invece del parametro `msm:writeLiveCopyConfig`. NPR-14434
* Numerosi problemi relativi al componente Rollout, Live Copy e altri aspetti di MSM. NPR-12235

### Risorse {#assets-18}

* Flusso di lavoro di annullamento del pacchetto: impossibile gestire le immagini con caratteri speciali nel nome del file immagine. NPR-15227: Hotfix per CQ-103887
* Le risorse con espressione Ripeti con condizione non vengono visualizzate correttamente. Quando l&#39;utente visualizza l&#39;anteprima del modello di lettera `*CDN3835RLCEN*`, non vengono visualizzate risorse che si trovano nell&#39;area di destinazione del corpo. Quando la risorsa `*VIPReassement*`, che è una risorsa opzionale, è deselezionata, le altre risorse preselezionate vengono visualizzate nella lettera. NPR-14844

* Durante la creazione di una raccolta smart, il tag di stile non viene mantenuto al momento del salvataggio della raccolta smart. NPR-15081: Hotfix per CQ-4195494
* Query di ricerca delle risorse eseguite lentamente nell’interfaccia utente touch durante ricerche simultanee da parte di più utenti. NPR-15019: Hotifx per CQ-4195405
* I metadati estratti per una proprietà di tipo `Long[]` vengono convertiti in tipo `String[]` quando la risorsa originale viene ricaricata in un percorso diverso. NPR-15016: Hotfix di CQ-4195005

* Gli utenti non possono eliminare una ricerca salvata o una raccolta avanzata. NPR-14924: Hotfix per CQ-108494
* La modifica dei metadati per le risorse in blocco (modalità di accodamento) mentre si utilizza un valore booleano per TypeHint in un campo a discesa nello schema di metadati sottostante genera un errore. NPR-14529: Hotfix per CQ-106876
* Gli utenti senza diritti di replica non possono eliminare le cartelle delle risorse. NPR-14321: Hotfix per CQ-88271
* Quando si tenta di modificare i profili video di un video in Editor canale, la finestra di dialogo di progettazione non si apre e nel registro degli errori genera un&#39;eccezione di puntatore Null. NPR-14144: Hotfix per CQ-81101
* La proprietà di marca temporale &quot;Creato&quot; generata dal sistema visualizzata nella pagina delle proprietà per una risorsa non è corretta. NPR-13992: Hotfix per CQ-95029
* Richiesta di abilitare il rilevamento di risorse duplicate per gli utenti senza accesso in lettura  AEM Assets NPR-13851: Hotfix per CQ-102281
* Gli utenti non possono modificare i metadati delle risorse in blocco dalla pagina delle proprietà. NPR-13721: Hotfix per CQ-100703
* Messaggio di errore non corretto nell’interfaccia classica quando viene caricata una risorsa duplicata. Il messaggio di errore non indica il motivo per cui il caricamento non è riuscito. NPR-13691: Hotfix per CQ-99272
*  AEM Assets non è in grado di ordinare più di 50 risorse per dimensione alla volta nella visualizzazione Elenco se la cartella contiene numerose risorse. CQ-100588
* Se selezionate più risorse, viene generato un errore con Codice risposta - 414 (URI richiesta troppo lungo) se l’URI di risorsa/cartella è troppo lungo. NPR-13516: Hotfix per CQ-76076
* La pagina Report risorse non risponde quando l’utente seleziona tutte le opzioni nella finestra di dialogo Configura colonne. NPR-13187: Hotfix per CQ-95589
* Comportamento imprevisto del Selettore tag in Safari e Internet Explorer. NPR-13134
* La modifica della ricerca salvata dalla barra delle risorse Ricerca per l’amministratore consente di salvarle come selezioni intelligenti nidificate, che causano problemi di stabilità dell’ambiente. NPR-13119: Hotfix per CQ-99460
* Dopo aver spostato un file (o una cartella) e averlo rinominato, i metadati &#39;cq:name&#39; non riflettono il nuovo nome file (nome cartella). NPR-13036: Hotfix per CQ-99141
* La risorsa con nomi che contengono caratteri speciali non può essere scaricata dal collegamento di download condiviso tramite e-mail. NPR-12872: Hotfix per CQ-95795
* I rapporti sulle risorse pronte all’uso generati in presenza di un numero consistente di risorse causano spostamenti pesanti dove la ricerca non ha raggiunto picchi di utilizzo di indice e CPU. NPR-12811: Hotfix per CQ-84409
* Gli utenti di AMS  AEM Assets accedono all’istanza di creazione da reti diverse che non possono caricare le risorse tramite il caricamento di blocchi senza eliminare i privilegi sulle cartelle. NPR-12768: Hotfix per CQ-82715
* Nelle ricerche basate su tag per le risorse mediante la barra Ricerca risorse, la funzione Tipo avanti non si limita al percorso principale e visualizza i tag di tutti gli spazi dei nomi. NPR-12666
* Il componente StaticRenditions genera un&#39;eccezione di puntatore null. NPR-12665
* Richiesta di disabilitare MissingMetadataNotificationJob perché causa l&#39;interruzione della pagina da parte dell&#39;interfaccia utente delle notifiche di Badge con un&#39;eccezione di runtime &quot;Unable to scan input&quot;. NPR-12500: Hotfix per CQ-93573
* L&#39;opzione &quot;Disattiva modifica&quot; per un campo tag non funziona nelle pagine delle proprietà delle risorse nell&#39;interfaccia utente touch. NPR-12429: Hotfix per CQ-88835
* Correzioni dell&#39;API in  AEM Assets 6.2 per l&#39;implementazione di Companion App SMB. NPR-11099
* Dall&#39;aggiornamento di Jquery, gli utenti non possono selezionare una raccolta di risorse e confermare la selezione nel pannello Contenuto associato di un frammento di contenuto. NPR-14847: Backport per CQ-4194209
* Nonostante venga richiamato l&#39;ordinamento infinito sul lato client, solo gli articoli/banner/raccolte attualmente visualizzati nell&#39;interfaccia utente sono ordinati. NPR-14493: Hotfix per CQ-109926
* Richiesta di implementazione della funzionalità di ricerca per AEM servizio mobile su richiesta. La ricerca di parole chiave per qualsiasi articolo, raccolta o banner non restituisce alcuna corrispondenza. NPR-14093: Hotfix per CQ-101394
* Quando si utilizza il componente Coral-select (*granite/ui/components/coral/foundation/form/select*) in una finestra di dialogo, l&#39;inizializzazione dei valori non funziona correttamente in Internet Explorer (IE11 o browser Edge) quando il valore selezionato contiene un singolo elemento. NPR-13395: Hotfix per CQ-101013

### Progetti {#projects-5}

* Quando si esporta un progetto di traduzione creato con Metodo di traduzione come &#39;umano&#39; e Provider di traduzione come &#39;none&#39;, non viene generato alcun file Translation_export_summary.xml perché il file di mappatura GUID è mancante. NPR-13137: Hotfix per CQ-91976
* Nei progetti AEM, quando si crea un progetto con la proprietà scadenza impostata, la conversione della data imposta l&#39;ora in modo errato a causa della differenza di fuso orario tra server e client. NPR-13003: Hotfix per CQ-98288
* L&#39;opzione &quot;Rivela nei siti&quot; viene persa dal processo di traduzione quando un progetto di traduzione viene aggiornato. NPR-12966: Hotfix per CQ-93740
* Quando viene creato un progetto di traduzione per una pagina del sito esportata, il rendering non viene eseguito correttamente nell&#39;anteprima. NPR-12964: Hotfix per CQ-84627

### Flusso di lavoro {#workflow-3}

* Il collegamento payload nella scheda Archivio della console Flusso di lavoro restituisce un errore con il codice di risposta &#39;404&#39; quando si fa clic su di esso. NPR-14993: Hotfix per CQ-4194977
* Quando si utilizzano AEM flussi di lavoro predefiniti, CQ Mailer non invia una notifica e-mail al gruppo per il quale manca l&#39;indirizzo e-mail di un singolo membro. NPR-14804: Richiesta hotfix per CQ-91499
* Miglioramenti delle prestazioni per la inbox e il contrassegno di notifica nell&#39;interfaccia utente touch. NPR-14145: Hotfix per CQ-101125
* Gli utenti non possono visualizzare l&#39;anteprima del payload dalla console Inbox del flusso di lavoro durante l&#39;avvio dei flussi di lavoro. NPR-13226: Hotfix per CQ-100275
* Il cookie &#39;saml_request_path&#39; configurato utilizzando il gestore autenticazione SAML visualizza il cookie impostato con un &#39;?&#39; aggiuntivo carattere. Inoltre, quando una risposta SAML viene postata in AEM, il cookie AEM &#39;saml_request_path&#39; restituisce un valore non valido a causa di caratteri già codificati. NPR-13517: Hotfix proattivo per GRANITE-11722 e GRANITE-14414

### Integrazione della soluzione {#solution-integration}

* Dopo aver integrato AEM 6.2 con l&#39;Search&amp;Promote, se un utente cerca un termine che restituisce un banner, la funzionalità di ricerca non risponde. NPR-14549: CFP per CQ-109631

### Dynamic Media {#dynamic-media}

* Numerosi processi di sling AEM-Scene7 creati e annullati durante AEM&#39;attivazione vengono registrati come processi di archiviazione durante la replica. NPR-12835: Hotfix per CQ-86115

### Sicurezza {#security-5}

* Richiesta di risoluzione del problema di convalida dell&#39;input nel filtro WCMDebug. NPR-12444: Richiesta hotfix per CQ-94890
* Richiesta proattiva per correggere il comportamento XSS durante l&#39;utilizzo della Creazione guidata lancio.\
   NPR-13062: Richiesta hotfix per CQ-99577

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-19}

`Adaptive Forms`

* Quando si crea un pannello ripetibile utilizzando moduli adattivi, non è possibile aggiornare il titolo del pannello in fase di esecuzione. NPR-15325
* Quando il valore predefinito di un pulsante di scelta è impostato e durante il salvataggio o l&#39;invio viene selezionato un valore diverso da quello predefinito, il valore non viene visualizzato nella precompilazione. NPR-15304
* Google Chrome mostra un comportamento non corretto quando si utilizza l&#39;evento options per compilare in modo dinamico l&#39;elenco a discesa e inviare il valore dell&#39;elemento selezionato. NPR-15198
* Quando si crea un pannello ripetibile utilizzando moduli adattivi, non è possibile aggiornare il titolo del pannello in fase di esecuzione. NPR-15181
* Quando si utilizza la modalità di modifica per i moduli adattivi, si verificano errori JavaScript quali - &#39;Handler of component is invalid&#39; (Gestore del componente non valido) e &#39;guidelib is undefined&#39; (Guida non definita). NPR-15112
* Il caricamento invisibile del frammento in un pannello ripetuto non funziona come previsto. NPR-13916, NPR-14785

`Correspondence Management`

* Le risorse di gestione della corrispondenza con `'Repeat with condition'`set di espressioni non vengono visualizzate correttamente. NPR-14844
* Quando si cerca una risorsa Gestione corrispondenza (ad esempio una lettera, un frammento di documento o un altro tipo), l&#39;icona Coda per il download non compare nella barra degli strumenti. NPR-14745
* Quando si crea un modulo Elenco, l’attivazione o disattivazione delle proprietà specifiche della risorsa (come modificabili, obbligatorie) non funziona. NPR-14689
* Il pannello Elementi dati nell&#39;utility Generatore di espressioni continua a caricarsi nel caso in cui venga creato un modulo di condizione senza selezionare un dizionario dati. NPR-14688
* Quando si visualizza l&#39;anteprima di una lettera, gli utenti non possono utilizzare spazi di tabulazione per allineare il contenuto in formato tabulare. NPR-14481
* Quando si esportano in massa risorse di Gestione corrispondenza dall&#39;interfaccia utente,  server AEM Forms genera registri non necessari. NPR-15226
* Quando si visualizza l&#39;anteprima di una lettera, il testo giustificato viene visualizzato in un font diverso. NPR-15468

`**Forms Portal**`

* Gli allegati dei moduli inviati nel portale Forms non sono visibili quando viene inviata una nuova bozza dall&#39;invio del portale. NPR-13515

`**Forms Manager**`

* Durante la navigazione nella directory *FormatiDocumenti*, il pulsante Incolla non viene visualizzato quando l&#39;utente copia una risorsa e quindi passa a un&#39;altra cartella. CQ-111327

#### Programma di installazione di JEE per Forms {#forms-jee-installer-19}

`Rights Management`

* L&#39;evento di controllo relativo al login utente viene registrato con un&#39;ora non valida. L&#39;ora corretta per l&#39;evento di controllo non è tracciabile. NPR-13107
*  Reader Adobe Acrobat e Microsoft Office non riescono ad aprire documenti protetti con l&#39;autenticazione estesa. NPR-14482

`Process Management`

* Quando un&#39;attività bozza inoltrata nell&#39;area di lavoro HTML viene restituita all&#39;utente iniziale, l&#39;attività non viene visualizzata nella coda dell&#39;utente iniziale. NPR-15178

`Assembler Service`

*  AEM Forms non è in grado di convalidare un PDF/A-2b con più di due firme. NPR-14101

`XTG`

* Durante la stampa di un documento utilizzando un vassoio di bypass della stampante, la funzione `GeneratePrintedOutput` non consente il recupero della carta dal vassoio di bypass destro. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer si blocca se l&#39;utente esegue l&#39;utilità Controllo ortografia con le impostazioni internazionali del modulo selezionate come francese (Canada). NPR-13740
* Forms Designer si chiude inaspettatamente quando l&#39;utente seleziona l&#39;evento calculate o validate per un campo del modulo e modifica il linguaggio in JavaScript e immette `this.` nella finestra **[!UICONTROL Editor di script]**. NPR-12974

### Pacchetti di funzioni inclusi in CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms Add-on Package):

* Quando un modulo adattivo viene creato da un file XDP, la tabulazione per l&#39;accessibilità non segue il pattern impostato. NPR-12562

`Adaptive forms` (Forms Add-on Package):

* Il Generatore di regole per i moduli adattivi non fornisce l&#39;accesso basato sui ruoli. Le modifiche apportate da un autore non sono tracciabili. NPR-12840

`Core` (Programma di installazione di JEE per Forms):

* La funzionalità CORS (CoreCross Origin Resource Sharing) come filtro servlet non è abilitata per Jboss+. NPR-13050

## Istruzioni per il download di CFP tramite distribuzione software {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Per  clienti AEM Forms, è essenziale installare AEM pacchetto del componente aggiuntivo moduli dopo l&#39;installazione AEM Service Pack, Cumulative Service Pack o Feature Pack.

È possibile scaricare il pacchetto CFP direttamente da Software Distribution oppure eseguire i seguenti passaggi:

1. Aprire [Distribuzione software](https://experience.adobe.com/downloads). È necessario un Adobe ID  per accedere a Distribuzione software.
1. Toccate **[!UICONTROL Adobe Experience Manager]** disponibile nel menu di intestazione.
1. Toccate il nome del pacchetto, selezionate **[!UICONTROL Accetta termini EULA]**, quindi toccate **[!UICONTROL Scarica]**.

## Istruzioni di installazione per CFP {#installation-instructions-for-cfp}

Questa sezione descrive i requisiti e i passaggi necessari per installare il CFP.

### Prima dell’installazione  {#before-you-install}

>[!NOTE]
>
>I Feature Pack opzionali forniti da Adobe dipendono dalla versione e dal Cumulative Fix Pack disponibili. Se hai installato un Feature Pack, contatta il [team di Assistenza clienti di AEM](https://helpx.adobe.com/it/marketing-cloud/contact-support.html) per verificare la compatibilità con questo Cumulative Fix Pack per AEM 6.2.

>[!NOTE]
>
>Prima di installare il pacchetto, è consigliabile eseguire la convalida su ogni nuovo pacchetto di installazione. La pre-convalida analizza e segnala eventuali errori rilevati prima dell’installazione e segnala agli utenti tali errori, sovrapposizioni e autorizzazioni in modo proattivo.
>
>È possibile accedere alla documentazione per l&#39;opzione Convalida all&#39;indirizzo [https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator)

* AEM 6.2 Service Pack 1 è un prerequisito per il CFP. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).

* Il download Cumulative Fix Pack è disponibile su [Distribuzione software](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20), a cui puoi accedere direttamente dall&#39;istanza AEM.
* Per una distribuzione cluster tramite (RDBMK o MongoDB), il pacchetto CFP può essere installato in qualsiasi istanza Author che utilizza Package Manager.

* Prima di installare il Cumulative Fix Pack, assicurati di creare uno snapshot o eseguire un backup dell’istanza AEM.
* La disinstallazione del CFP non è supportata.

### Installare il CFP tramite distribuzione software {#install-the-cfp-via-package-share}

Per installare Cumulative Fix Pack in un&#39;istanza AEM 6.2 SP1 esistente, effettuate le seguenti operazioni:

1. Fate clic sul collegamento [Distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) per scaricare il pacchetto.

1. Aprite [Gestione pacchetti](http://localhost:4502/crx/packmgr/index.jsp) e fate clic su **[!UICONTROL Carica pacchetto]** per caricare il pacchetto.

1. Selezionate il nome del pacchetto e fate clic su **[!UICONTROL Installa]**.

### Installazione automatica {#automatic-installation}

Il CFP può essere installato automaticamente in un’istanza in esecuzione nei seguenti modi:

* Inserite il pacchetto in ../crx-quickstart/install mentre il server è in esecuzione. Il pacchetto viene installato automaticamente.
* Utilizzate l&#39; [API HTTP da Package Manager](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html) - accertatevi di utilizzare `cmd=install&recursive=true` - per installare il pacchetto nidificato.

### Convalidare l’installazione {#validate-installation}

1. La pagina Informazioni prodotto (/system/console/ productinfo ) deve ora mostrare la stringa di versione aggiornata &quot;Adobe Experience Manager, versione 6.2.0.SP1-CFP20&quot; in Prodotti installati.
1. Tutti i bundle OSGi risultano come ATTIVI o FRAMMENTI nella console OSGi (usa la console Web: /system/console/bundles).

>[!NOTE]
>
>Dopo l&#39;installazione corretta del pacchetto, viene visualizzato un messaggio informativo che indica che il pacchetto di contenuti è stato installato correttamente, ad esempio &quot;Content Package AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 installato correttamente&quot;.

>[!NOTE]
>
>A partire da AEM 6.2 SP1-CFP1, il livello di registro in Jackrabbit FileVault è cambiato da INFO a DEBUG per la maggior parte dei messaggi. Per ottenere i registri di installazione per un pacchetto di contenuti installato AEM 6.2 SP1-CFP1 o versione successiva, abilitare il livello di registro DEBUG per `org.apache.jackrabbit.vault.packaging.impl`.

### Installare AEM Forms {#install-forms}

>[!NOTE]
>
>Ignora questa sezione se non usi AEM Forms.

#### Installare il componente aggiuntivo per AEM Forms  {#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms su JEE solo**) La procedura per installare un CFP su  AEM Forms su JEE è descritta in [Installazione di CFP su  AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Assicurarsi di aver installato il pacchetto CFP AEM 6.2 SP1.
1. Scaricate il pacchetto del componente aggiuntivo Forms corrispondente elencato in [ versioni di AEM Forms](aem-forms-releases.md) per il sistema operativo in uso.
1. Installare il pacchetto del componente aggiuntivo Forms come descritto in [Installazione di pacchetti del componente aggiuntivo AEM moduli](https://helpx.adobe.com/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html).

#### Installare il pacchetto dei bundle di JEE per AEM Forms {#install-aem-forms-jee-bundles-package}

Le correzioni apportate a JEE per AEM Forms vengono distribuite tramite un programma di installazione separato. Per informazioni sull’installazione di un CFP in JEE per AEM Forms, consulta [Installing Cumulative Fix Packs on AEM Forms JEE](install-cfp-aem-forms-jee.md) (Installazione di Cumulative Fix Pack in JEE per AEM Forms).

#### Programma di installazione di Forms Designer  {#designer-installer}

1. Per installare l&#39;aggiornamento, eseguire il file Designer6.2.0_&lt;Lingua>_Cumulative_QF.msp.
1. Nella schermata di benvenuto, fai clic su **Aggiorna**. L’installazione viene avviata.
1. Al termine dell’installazione, fai clic su **Fine**.

## Parametri di timeout configurabili dall&#39;utente per le connessioni DTM, Analytics, Target, Search &amp; Promote {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Con AEM Cumulative Fix Pack 6.2 SP1-CFP7 e versioni successive, i periodi di timeout della connessione sono stati configurati su tutte le connessioni di cui sopra come indicato di seguito:

| **Connessioni** | **Timeout della connessione*** | **Timeout socket**** |
|---|---|---|
| DTM | 30000 ms | 30000 ms |
| Analisi | 30000 ms | 30000 ms |
| Destinazione | 60000 ms | 30000 ms |
| Search&amp;Promote | 30000 ms | 30000 ms |

* **Timeout connessione***- Timeout in millisecondi fino a quando non viene stabilita una connessione. Un valore di timeout pari a zero viene interpretato come un timeout infinito.
* **Timeout socket****- Timeout in millisecondi per l&#39;attesa di dati o per un periodo massimo di inattività tra due pacchetti di dati consecutivi.

>[!NOTE]
>
>Con AEM Fix Pack cumulativo 6.2 SP1-CFP6 e versioni successive, la configurazione OSGi utilizzata per l&#39;integrazione Search &amp; Promote è la configurazione proxy dei componenti Apache HTTP. La configurazione proxy di Day Commons HTTP Client 3.1 non viene più utilizzata.

## Disattivazione dello stato di replica nella console di assegnazione tag (interfaccia classica) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Se si utilizza CFP3 o versione successiva, attenersi alle istruzioni riportate di seguito per disabilitare Stato replica nella console Assegnazione tag nell&#39;interfaccia classica:

* Sovrapposizione *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;* in */apps*

* Aggiungi `replicationStateRequired`: &quot;false&quot; dopo la riga 416.

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## L&#39;ultimo aggiornamento 131 di Java 8 genera un&#39;eccezione (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Queste impostazioni di configurazione sono specifiche per  clienti AEM Forms che utilizzano Document Security.

L&#39;NPR-21355 è incluso nel CFP12.1. Se si sta installando CFP12.1 o versione successiva, eseguire la procedura seguente per configurare NPR-21355 sul server applicazioni JBoss. Se si sta installando CFP12.1 su  server AEM Forms in esecuzione  server applicazioni Oracle WebLogic o IBM WebSpehere, non è richiesta alcuna configurazione aggiuntiva:

1. Eseguire il backup, eliminare e creare un nuovo file module.xml. Il percorso predefinito del file è [AEM_Forms_Installation_directory]/jboss/module/system/layer/base/com/adobe/livecycle/main/

1. Aprite il file module.xml appena creato per la modifica. Aggiungi al file il codice seguente:

   ```xml
   <module xmlns="urn:jboss:module:1.1"
   name="com.adobe.livecycle">
   <resources>
   <resource-root path="cryptojcommon.jar"/>
   <resource-root path="cryptojce.jar"/>
   <resource-root path="jcmFIPS.jar"/>
   <resource-root path="certj.jar"/>
   <resource-root path="cglib.jar"/>
   </resources>
   <dependencies>
   <module name="javax.api"/>
   <module name="asm.asm"/>
   </dependencies>
   </module>
   ```

1. Create un backup dei file jsafeFIPS.jar, jsafeJCEFIPS.jar e certjFIPS.jar che si trovano in [AEM_Forms_Installation_directory]/jboss/module/system/layer/base/com/adobe/livecycle/main/ ed eliminate i file dalla directory sopra indicata.

   Per ottenere nuovi file JAR, contattare [ supporto Adobe](https://helpx.adobe.com/marketing-cloud/contact-support.html). Inserire i file JAR ottenuti da [ supporto Adobe](https://helpx.adobe.com/marketing-cloud/contact-support.html) in [AEM_Forms_Installation_directory]/jboss/module/system/layer/base/com/adobe/livecycle/main/

1. (Solo per Windows) Modificate i file di configurazione `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` o `domain.conf.bat`:

   * Per il server JBoss in configurazione standalone, aprite il file standalone.conf.bat per la modifica.
   * Per il server JBoss nella configurazione del cluster, aprite domain.conf.bat per la modifica.

   Aggiungete le seguenti righe alla fine e salvate il file:

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   impostate &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140Initialmode=NON_FIPS140_MODE&quot;

1. (Solo sistema operativo basato su Linux) Modificate i file di configurazione [AEM_Forms_Installation_directory]/jboss/standalone.conf o domain.conf:

   * Per il server JBoss in configurazione standalone, aprite il file standalone.conf per la modifica.
   * Per il server JBoss nella configurazione del cluster, aprite domain.conf per la modifica.

   Aggiungete le seguenti righe alla fine e salvate il file:

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140Initialmode=NON_FIPS140_MODE&quot;

## Impostazioni di configurazione richieste per NPR-19778 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>L&#39;NPR-19778 fa parte della CFP14.

Per impostazione predefinita, il conteggio per la coda condivisa non viene aggiornato per gli altri utenti quando un utente richiede un&#39;attività. Per questo abbiamo introdotto una nuova proprietà. Per configurare questa proprietà nell’istanza AEM, effettuate le operazioni seguenti:

1. Vai all&#39;interfaccia utente Amministratore -> Servizi -> Area di lavoro -> Amministrazione globale.
1. Esporta impostazioni globali.
1. Nel file XML scaricato, aggiungete il tag `<client_tasksPollingInterval>10</client_tasksPollingInterval>` Qui, 10 è il valore di esempio in secondi. Potete modificarlo di conseguenza.
1. Salvate il file.
1. Torna all&#39;interfaccia utente Amministratore -> Servizi -> Area di lavoro -> Amministrazione globale.
1. Importate il file xml nella sezione Importa impostazioni globali.
1. Ora potete disconnettervi dal sistema ed effettuare di nuovo l&#39;accesso.
1. Il conteggio della coda condivisa inizia ad aggiornarsi per gli altri utenti nell&#39;area di lavoro.
1. Per disattivare il polling, modificare il valore su 0 e importare di nuovo il file XML.

## Modifiche interfaccia utente {#ui-changes}

* Modifica del comportamento nella visualizzazione dei titoli sulla scheda Immagine per Immagine con dc: proprietà title impostata su Stringa [] ( multifield ): sulla scheda Immagine nell’interfaccia utente verrà visualizzato solo il titolo modificato più recente, anche se tutti i titoli verranno salvati in CRX. Hotfix per CQ-4217165

## Problemi noti {#known-issues}

* Se si aggiornano AEM 6.2SP1-CFP19 e AEM 6.2SP1-CFP20 da CFP18, il reindirizzamento principale alla pagina di benvenuto dell&#39;interfaccia classica viene modificato invece di /sites.html/content. Potrebbe essere necessario correggere la fionda: proprietà target da /welcome.html a /index.html con CRX Explorer. Questo problema non viene rilevato durante l&#39;aggiornamento da CFP17 o versione precedente.

I seguenti errori temporanei possono verificarsi quando si installa AEM 6.2 SP1-CFPx. Tuttavia, per questi errori non è necessaria alcuna risoluzione perché non influiscono sull&#39;istanza AEM e se ne vanno dopo l&#39;installazione di CFP:

* Quando si esegue l&#39;aggiornamento dell&#39;istanza AEM 6.2SP1-CFP20 a AEM 6.5, alcuni URL personalizzati potrebbero non funzionare come:

   * */projects.html*
   * */sites.html*

Tuttavia, la soluzione alternativa consiste nel riavviare l&#39;istanza AEM dopo un aggiornamento.

* HTTP 500 Internal Server Error viene ricevuto quando si apre la pagina dei dettagli del componente della console Web.
* Si verificano degli errori in quanto **crea l&#39;istanza del componente** e **Service factory ha restituito null** a causa del riavvio del repository:

   * com.day.cq.cq-personalization [com.day.cq.pesonalization.impl.DefaultProfileProvider(938)] Impossibile creare l&#39;istanza del componente a causa di un errore nel binding di profileManager di riferimento
   * org.apache.sling.commons.scheduler FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory ha restituito null. (Componente: com.day.cq.tagging.impl.TagGarbageCollector (1687))

* Errore rilevato nell&#39;installazione CFP in Mongo e DB2: **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Eccezione: java.lang.NullPointerException**. Questo errore non si verificherà dopo l&#39;installazione di un CFP su CFP8.
* ( Adobe Attività aggiornamento utilità di pianificazione manutenzione granita) com.adobe.granite.Maintenance.impl.TaskScheduler: Nessuna attività di manutenzione trovata con nome WorkflowPurgeTask per il granito della finestra:settimanale
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* Quando installate CFPx su AEM 6.2 SP1 che include il feature pack Smart Tags, il passaggio del flusso di lavoro precedentemente aggiunto per le risorse Smart Tag viene eliminato dal flusso di lavoro DAM Update Asset (Aggiorna risorsa).

Consultate l&#39;elenco dei [Problemi noti in AEM 6.2 SP1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known noti).

## JAR Uber {#uber-jar}

La Jar Uber per 6.2 SP1-CFP20 è disponibile all&#39;indirizzo [ repository Public Maven del Adobe](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/).

Per utilizzare Uber Jar in un progetto Maven, includi la seguente dipendenza nel tuo progetto POM:

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## Pacchetti OSGI e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-5}

Il testo seguente documenta l’elenco dei pacchetti OSGI e dei pacchetti di contenuti inclusi nel CFP.

* [Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP20](assets/do-not-localize/updated.txt)
* [Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP20](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [Pagina degli hotfix di AEM 6.2](https://helpx.adobe.com/it/experience-manager/kb/aem62-available-hotfixes.html)
>* [Note sulla versione di AEM 6.2 SP1](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [Note sulla versione di AEM 6.2](https://docs.adobe.com/docs/it/aem/6-2/release-notes.html)
>* [Pagina del prodotto AEM](http://www.adobe.com/it/solutions/web-experience-management.html)
>* [Documentazione di AEM 6.2](https://docs.adobe.com/content/docs/en/aem/6-2.html)
>* [](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) Iscrizione agli aggiornamenti di prodotto con priorità di  [Adobe](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)

