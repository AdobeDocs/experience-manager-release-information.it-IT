---
title: AEM 6.2 Cumulative Fix Pack
description: Note sulla versione AEM 6.2 Cumulative Fix Pack.
exl-id: f1c2d4ff-590b-46b5-b2b1-e2b5141f7cc0
source-git-commit: ce1026216ccb79a3c268b3f6b24698fa3a3388dc
workflow-type: tm+mt
source-wordcount: '19928'
ht-degree: 100%

---

# Note sulla versione AEM 6.2 Cumulative Fix Pack{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Informazioni sulla versione {#release-information}

| **Prodotto** | Adobe Experience Manager |
|---|---|
| **Versione** | 6.2 |
| **Versione** | Cumulative Fix Pack 6.2 SP1-CFP20 |
| **Prerequisito** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **Disponibilità generale** | 6 giugno 2019 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe ha introdotto un unico modello di distribuzione per il rilascio delle correzioni. Invece di rilasciare hotfix per singoli problemi, Adobe rilascia ogni mese un Cumulative Fix Pack (CFP) (soggetto a controlli di qualità), che è un pacchetto di contenuti che aggrega più correzioni. I CFP includono principalmente correzioni di bug, ma possono includere anche Feature Pack. Offrono i seguenti vantaggi rispetto ai singoli hotfix:

* Natura cumulativa (ad esempio, un CFP contiene gli aggiornamenti distribuiti con CFP precedenti)
* Maggiore garanzia di qualità
* Installazione semplificata (l’utente installa un CFP come pacchetto singolo senza alcuna dipendenza, ad eccezione dell’ultimo service pack)

Per ulteriori informazioni sul CFP e su altri tipi di versioni, consulta [Maintenance Release Vehicle](https://docs.adobe.com/content/docs/en/aem/6-2/deploy/maintenance-release-vehicle-definitions.html) (Gestione delle versioni di aggiornamento).

## Informazioni sulla versione {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20 è l’ultimo Cumulative Fix Pack per AEM 6.2 e costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/it/experience-manager/6-2/release-notes/sp1.html).

>[!CAUTION]
>
>Se si applica il CFP senza aver prima convalidato la compatibilità tra i Feature Pack installati, potrebbe verificarsi un errore di sistema o la perdita delle configurazioni personalizzate, per la cui soluzione potrebbe essere necessario eseguire il ripristino dal backup.

>[!NOTE]
>
>* Con AEM Cumulative Fix Pack 6.2 SP1-CFP10 viene fornito un nuovo bundle Sling `discovery-  api` Johnzon 1.0.0. È inoltre disponibile una funzione di rilevamento sling per l’utente del servizio con privilegi di lettura e scrittura relativi al nodo */var/discovery* dell’archivio CRX.
>
>* È stato anche aggiunto il bundle per l’e-mail di Apache Commons **org.apache.commons/commons-email/1.5** in sostituzione di **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
>
>* Per i clienti con un numero elevato di utenti nell’istanza di AEM, Adobe consiglia di implementare il CFP tramite la cartella di installazione.
>

## Problemi corretti {#issues-included}

In questa sezione sono elencati tutti i problemi e gli hotfix inclusi nel CFP corrente.

Questo CFP include inoltre gli hotfix distribuiti in [Cumulative Fix Pack precedenti](#previous).

### Integrazione {#integration}

* Backporting di vari miglioramenti a livello di personalizzazione del targeting delle campagne. NPR-29163: Hotfix per CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler genera un ciclo infinito e causa aggiornamenti ai nodi nelle istanze di pubblicazione. NPR-28561: Hotfix per CQ-4263096

### DAM - Generale {#dam-general}

* Impossibile visualizzare/nascondere il pulsante di replica per gli utenti non amministratori in specifiche cartelle DAM. NPR-29026: Hotfix per CQ-4265361

### Vulnerabilità {#vulnerability}

* Il framework di protezione CSRF non funziona con i moduli di AEM Foundation. NPR-28612: Hotfix per GRANITE-22231

### Forms {#forms}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package}

>[!NOTE]
>
>Per i clienti di AEM Forms, è essenziale installare il pacchetto dei componenti aggiuntivi per AEM Forms dopo l’installazione del Service Pack, del Cumulative Fix Pack o del Feature Pack di AEM.

>[!NOTE]
>
>I pacchetti di componenti aggiuntivi per AEM Forms consentono di allineare le funzionalità di Forms ai Service Pack e i Cumulative Fix Pack di AEM. È quindi obbligatorio installare il pacchetto di componenti aggiuntivi per AEM Forms dopo aver installato eventuali Service Pack, Cumulative Fix Pack o Feature Pack di AEM.

#### Moduli adattivi {#adaptive-forms}

* Problemi di usabilità con il componente Scribble per dispositivi iOS 12.1. NPR-29082: Hotfix per CQ-4261765

#### Forms - Sicurezza dei documenti {#forms-document-security}

* Durante la verifica delle firme in un PDF tramite l’uso di firme elettroniche avanzate PDF (PAdES) viene generata l’eccezione InvalidOperationException. NPR-27848: Hotfix per CQ-4244837

#### Forms - Corrispondenza {#forms-correspondence}

* Quando si visualizza l’anteprima della lettera come PDF, il campo di testo inserito nella pagina mastro non rispetta il valore immesso nella scheda dati o in base ai collegamenti dati specificati. NPR-29239: Hotfix per CQ-4266856.

#### Forms - Comunicazione interattiva {#forms-interactive-communication}

* Quando viene aggiunto un apostrofo, i campi precompilati nella lettera vengono visualizzati come caratteri ASCII anziché normali caratteri alfabetici. NPR-28863: Hotfix per CQ-4262900

### Programma di installazione Forms JEE {#forms-jee-installer}

* Il programma di installazione Forms JEE non contiene nuove correzioni per AEM Forms.

## Hotfix e Feature Pack inclusi nei Cumulative Fix Pack precedenti {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulative Fix Pack 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/it/experience-manager/6-2/release-notes/sp1.html).

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* Abilitazione del supporto dell’API v3.0 di MS Translator per AEM 6.2
* Aggiunta del messaggio di registro dopo la corretta installazione del pacchetto per tutti gli SP, CFP e HF.

### Assets {#assets}

* Impossibile rinominare la cartella DAM se manca l’autorizzazione d modifica dell’ACL. NPR-27555: Hotfix per CQ-104652
* Mancata risposta dell’editor dei predefiniti immagine in CFP 17 6.2.1 e versioni successive. NPR-28147: Hotfix per CQ-4261041

### Sites {#sites}

* Link Checker non completa il processo e si blocca in presenza di collegamenti senza risposta. NPR-27373: Hotfix per CQ-4256030
* Il file del segmento non viene caricato correttamente a causa di un percorso principale aggiuntivo che interrompe il percorso del segmento. NPR-28014: Hotfix per CQ-4260332

### Integrazione {#integration-1}

* L’annullamento dell’ereditarietà Live Copy non funziona correttamente sui contenitori di destinazione. NPR-28129: Hotfix per CQ-4259813
* Le azioni  cq  :actions non vengono considerate per un componente di destinazione. NPR-27616: Hotfix per CQ-4257497

* La visualizzazione dell’icona per interrompere l’ereditarietà non è coerente. NPR-27671: Hotfix per CQ-4257779

### Felix {#felix}

* Per i dettagli del componente della console web viene visualizzato il messaggio di errore 500 dopo l’installazione di CFP 18 nell’istanza AEM 6.2 SP1. NPR-28350: Hotfix per CQ-4261095

### Traduzione {#translation}

* Abilitazione del supporto per il servizio MS Translator in AEM 6.3 dopo l’aggiornamento di MS Translator all’API v3.0. NPR-28123: Hotfix per CQ-4259096

### Interfaccia utente - Foundation {#ui-foundation}

* Nel calendario incluso in Sites sono presenti date non corrette. NPR-28392

### Granite {#granite}

* Il dizionario non è invalidato per i bundle di risorse che utilizzano lo sling :basename. NPR-27624

### Manutenzione {#sustenance}

* I registri attività di Gestione pacchetti devono essere estratti in un file di registro separato. NPR-27323: Hotfix per GRANITE-14866
* Frase/testo/riga registro standard nel file error.log da visualizzare al termine dell’installazione. NPR-27835
* Il plugin del pacchetto Granite rileva la dipendenza di una versione inferiore di org.apache.sling.i18n. Hotfix per CQ-4263245
* Il bundle com.adobe.cq.com.adobe.cq.ui.commons viene eliminato al momento dell’installazione del CFP più recente dopo 6.2SP1-CFP15. Hotfix per CQ-4258808

### Forms {#forms-1}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-1}

#### Moduli adattivi {#adaptive-forms-1}

* Vulnerabilità di tipo XML Injection con AEM Forms. NPR-27843: Hotfix per CQ-4257315

### Programma di installazione Forms JEE {#forms-jee-installer-1}

* Il programma di installazione Forms JEE non contiene nuove correzioni per AEM Forms.

### Bundle OSGi e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included}

Nei documenti di testo seguenti sono elencati i bundle OSGi e i pacchetti di contenuti inclusi nel CFP.

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP19

[Ottieni file](assets/do-not-localize/cfp19_osgi_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP19

[Ottieni file](assets/do-not-localize/cfp19_content_packages.txt)

### Cumulative Fix Pack 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/it/experience-manager/6-2/release-notes/sp1.html).

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* In DAM CommandLineProcess è stato aggiunto il supporto per terminare un processo che impiega troppo tempo.
* È stata corretta una perdita di sessione in ReplicationEventListener.
* Al componente core Pagina è stato aggiunto il supporto per il reindirizzamento.

### Assets {#assets-1}

* I processi Camera Raw si bloccano durante i periodi di caricamenti massicci, bloccando di conseguenza l’elaborazione di tutti i flussi di lavoro. NPR-26990: Hotfix per NPR-23860
* La funzionalità di download usufruisce di AEM Assets tramite il servlet assetdownload, consentendo agli utenti anonimi di scaricare tutte le risorse. NPR-27054: Hotfix per CQ-4254732
* I caratteri speciali vengono visualizzati danneggiati nella riga oggetto dei modelli di e-mail in AEM. NPR-26470: Hotfix per CQ-4252368

### Sites {#sites-1}

* A causa di un comportamento errato della classe ConfigPostProcessor, la sospensione dell’immagine padre rimuove il tipo mixing cq : LiveRelationship dalla pagina figlio. NPR-26745: Hotfix per CQ-4254163
* Al componente core Pagina è stato aggiunto il supporto per il reindirizzamento. NPR-26576: Hotfix per CQ-110529
* È stata eseguita la migrazione di contexthub a jquery 3. NPR-26956: Hotfix per CQ-4255472
* I campi di input con ancoraggio vengono visualizzati fuori dalla sezione visibile del browser se la finestra di dialogo non viene ingrandita. NPR-26852: Hotfix per CQ-4255019
* Quando si copia e incolla del testo, nel frammento di contenuto viene inserito un tag &lt;br> indesiderato. NPR-26660: Hotfix per CRTE-151
* Per alcune pagine, la funzione classica di amministrazione del sito non riproduce l’elenco nel riquadro di destra. NPR-27247: Hotfix per CQ-4251621
* (Interfaccia utente classica) I tentativi di spostare/rinominare le pagine generano un errore di tipo “Si è verificato un errore durante lo spostamento della pagina.” NPR-27179: Hotfix per CQ-4235907

### Integrazione {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever esamina l’intera struttura per raccogliere i marchi disponibili. NPR-27060: Hotfix per CQ-4255790

### WCM - Componenti Foundation {#wcm-foundation-components}

* Problema della funzionalità di ricerca per il componente Elenco di Foundation. NPR-26817: Hotfix per CQ-4250324

### Platform {#platform}

* A causa della presenza di un carattere speciale trattino lungo, la cache non viene scaricata dall’istanza di pubblicazione. NPR-27199: Hotfix per CQ-4242790

### Granite {#granite-1}

* La funzione di convalida pacchetti non convalida i pacchetti inclusi in CFP/SP. NPR-26775: Hotfix per GRANITE-22825

### Replica {#replication}

* Perdita della sessione JCR in ReplicationListener. NPR-27063: Hotfix per CQ-4232088

### Forms {#forms-2}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-2}

* Il pacchetto di componenti aggiuntivi per Forms non contiene nuove correzioni per AEM Forms.

### Programma di installazione Forms JEE {#forms-jee-installer-2}

* Il programma di installazione Forms JEE non contiene nuove correzioni per AEM Forms.

#### Bundle OSGi e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-1}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP18

[Ottieni file](assets/do-not-localize/62cfp18updated_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP18

[Ottieni file](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Cumulative Fix Pack 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/it/experience-manager/6-2/release-notes/sp1.html).

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* È stato aggiunto il supporto per gli URL senza estensione del sito in at-integration.js
* È stato rimosso il modulo di importazione polling S7 dalla configurazione del servizio cloud S7.
* Sono state apportate modifiche alla vista dei tipi di pubblico per supportare la struttura di cartelle per l’implementazione multi-tenant.
* Sono stati introdotti aggiornamenti in jqueryui clientlib v1.12.1.

### Assets {#assets-2}

* L’avvio di flussi di lavoro dall’interfaccia utente di Assets richiede che l’utente disponga di autorizzazioni di scrittura, eliminazione e modifica. NPR-25688: Hotfix per CQ-4250140
* I pulsanti Pubblica e Annulla pubblicazione restano visibili anche per gli utenti che non dispongono di autorizzazioni di replica. NPR-25094
* (Flusso di lavoro) Il flusso di lavoro per tag avanzati di Assets non viene elaborato tramite la configurazione del proxy AEM. NPR-25915: Hotfix per CQ-4248202
* È stato rimosso il modulo di importazione polling S7 dalla configurazione del servizio cloud S7. NPR-25239: Hotfix per CQ-95236

### Sites {#sites-2}

* I flussi di lavoro avviati da Editor -> Informazioni pagina contengono il percorso di contesto nel payload. NPR-26389: Hotfix per CQ-76804
* (Link Checker esterno) I collegamenti https non validi vengono visualizzati come collegamenti validi. NPR-25541: Hotfix per CQ-4201333
* (Interfaccia classica) Quando si crea una pagina indipendente sotto una Live Copy, la pagina viene creata come Live Copy. NPR-25610: Hotfix per CQ-4249801
* Problemi con la pubblicazione di risorse associate al componente Design Importer quando viene attivata una pagina. NPR-25638: Hotfix per CQ-102532
* La barra degli strumenti dell’Editor Rich Text copre l’elenco di selezione. NPR-25165: Hotfix per CQ-4248948
* È stata eseguita la migrazione di contexthub a jquery 3. NPR-25059: Hotfix per GRANITE-19902
* Per i componente parsys nidificati, viene sempre applicato il primo design adeguato (quello con il percorso con meno nidificazioni) tra i vari componenti disponibili. Per ulteriori informazioni, consulta [Design Path Resolution](https://helpx.adobe.com/it/experience-manager/6-3/sites/developing/using/page-templates-static.html) (Risoluzione del percorso di progettazione). NPR-25250: Hotfix per CQ-4246276

### Integrazione {#integration-3}

* Utilizzando l’integrazione di targeting inclusa, il targeting di un componente riproduce l’intera pagina e non un componente di destinazione vuoto. NPR-25273: Hotfix per CQ-4248003
* Se si interrompe l’ereditarietà in modalità di targeting, il componente viene comunque visualizzato come destinazione e l’ereditarietà non viene interrotta in modalità di modifica. NPR-25324: Hotfix per CQ-4248162
* Quando in una pagina viene definita una personalizzazione e viene risolto un pubblico, l’esperienza corrispondente viene visualizzata in modalità di modifica. NPR-25731: Hotfix per CQ-4249465
* Viene visualizzato un URL teaser errato quando si utilizza AEM con un percorso di contesto non predefinito. NPR-25971: Hotfix per CQ-4250953
* Viene eseguito un rendering vuoto quando si utilizza l’opzione opt-out. NPR-25295: Hotfix per CQ-4246792
* Le esperienze eliminate dall’ambiente di authoring non vengono mai rimosse dal sito pubblicato al momento dell’attivazione della pagina. NPR-24869: Hotfix per CQ-4247832

### DAM - Client DM {#dam-dm-client}

* (Chrome, Firefox) VideoPlayer ignora i clic del mouse sui dispositivi touch. Hotfix per CQ-4247370

### Platform {#platform-1}

* Consente di configurare il numero massimo di tentativi durante l’acquisizione o il rilascio di un pacchetto. NPR-25328: Hotfix per GRANITE-22376
* Registrazione errata in caso di errori di replica. NPR-25308: Hotfix per CQ-4249402
* L’installazione di Forms AEM 6.2 da CFP8 a CFP14 causa un errore in Apache POI. NPR-25053: Hotfix per GRANITE-21771

### Granite {#granite-2}

* Il processo di sincronizzazione utente ha esito negativo con l’eccezione OakConstraint0022. NPR-25729: Hotfix per Oak-7428

### Communities {#communities}

* Il bundle cq -social-as-provider non si avvia con le versioni 3.x del driver Mongo. NPR-26271: Hotfix per CQ-4252710

### Interfaccia utente - Foundation {#ui-foundation-1}

* Aggiornamento a jqueryui clientlib v1.12.1. NPR-25090: Hotfix per GRANITE-21981, CQ-4248897

* (Omnisearch): La proprietà “Title” è vulnerabile ad attacchi cross-site scripting (XSS) in Sites. NPR-24994: Hotfix per GRANITE-19933

### Forms {#forms-3}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-3}

#### Moduli adattivi {#adaptive-forms-2}

* Codifica errata durante l’invio di dati da un modulo adattivo. NPR-25539

#### Forms - Gestione {#forms-management}

* Risorse di moduli non correlate vengono riportate come riferimenti durante la pubblicazione della pagina. NPR-26167: Hotfix per CQ-4251004

### Forms - Programma di installazione JEE {#forms-jee-installer-3}

#### Document Security {#document-security}

* La variabile viene compilata come tipo di dati Elenco e il sottotipo è una stringa, ma viene visualizzato un errore di tipo “Impossibile assegnare l’oggetto”. NPR-26194: Hotfix per CQ-4252287
* Impossibile accedere alle configurazioni delle filigrane dopo l’installazione di 6.2-SP1-CFP15. NPR-26130: Hotfix per CQ-4250984

### Bundle OSGi e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-2}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP17

[Ottieni file](assets/do-not-localize/62cfp17updated_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP17

[Ottieni file](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/it/experience-manager/6-2/release-notes/sp1.html).

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* È stato aggiunto il supporto per STARTTLS in Day CQ Mail Service.
* È stato corretto l’allineamento delle icone ContextHub nel popover del profilo.
* Sono state apportate correzioni alla funzionalità Mostra/Nascondi del componente del menu a discesa.
* Aggiornamento alla versione più recente di Jackson 2.8.11

### Assets {#assets-3}

* Impossibile avviare un flusso di lavoro da una vista elenco. NPR-24393: Hotfix per CQ-4245788
* (Firefox/Chrome) Impossibile scaricare risorse nella pagina Condivisione risorse. NPR-24523: Hotfix per CQ-4224408
* È stata migliorata la qualità predefinita per l’anteprima video in AEM. NPR-24148: Hotfix per CQ-4244310

### Integrazione {#integration-4}

* Quando un componente è destinato a un’istanza di pubblicazione, un effetto sfarfallio rende brevemente visibile l’esperienza predefinita prima di quella di destinazione. NPR-23992: Hotfix per CQ-4242038
* Le esperienze eliminate dall’ambiente di authoring non vengono mai rimosse dal sito pubblicato al momento dell’attivazione della pagina. NPR-24869: Hotfix per CQ-4247832

### Platform {#platform-2}

* Applicazione della patch a jQuery 1.12.4 da clientlib per includere la correzione di sicurezza. NPR-24129: Hotfix per GRANITE-20058
* È stato aggiunto il supporto per STARTTLS in Day CQ Mail Service. NPR-23941: Hotfix per CQ-4240397
* È stato rimosso il valore predefinito MERGE_PRESERVE aclHandling. NPR-24593: Hotfix per GRANITE-21889
* La funzionalità LineChecker non riesce a esternalizzare i collegamenti se una richiesta contiene parametri di query non validi. NPR-24127: Hotfix per CQ-4241893

### MSM {#msm}

* Hotfix proattivi per attacchi che sfruttano le vulnerabilità cross-site scripting (XSS). NPR-21893: Hotfix per CQ-4223385
* MSM LiveRelationship: RolloutConfig effettivo errato se BlueprintConfig è nella radice. NPR-23999: Hotfix per CQ-4243000

### Sites {#sites-3}

* Se si crea una nuova esperienza in un’area Live Copy, è necessario interrompere l’ereditarietà per consentirne la configurazione. NPR-24995: Hotfix per CQ-4248209
* (Interfaccia touch) Varie icone sulla barra degli strumenti superiore scompaiono quando si blocca o si sblocca una pagina. NPR-23954: Hotfix per CQ-4243345
* I campi non sono correttamente allineati nel contexthub. NPR-23958
* Se si esegui un’azione di pubblicazione su una pagina bloccata, viene interrotto il processo di authoring. NPR-23970: Hotfix per CQ-4243203
* I rapporti inclusi in /etc/reports/ non funzionano correttamente e non presentano alcun grafico di dati storici. NPR-20035: Hotfix per CQ-4220180
* La creazione di un lancio non riesce quando si avvia il flusso di lavoro “Richiedi lancio” in un progetto. NPR-24255: Hotfix per CQ-4245030
* I tag e gli attributi HTML vengono ignorati dalle e-mail dopo l’installazione di CFP10. NPR-24287: Hotfix per CQ-4240028
* TagPicker: il suggerimento di tag nel campo tag dello schema di metadati tag interroga i nodi che supportano i tag e richiede quindi un tempo di caricamento molto lungo. NPR-24347: Hotfix per CQ-4244291
* L’integrazione di Salesforce ha esito negativo con le configurazioni proxy. NPR-24418: Hotfix per CQ-4245300
* (WCM) Quando si crea una revisione, PageManager lascia la pagina consegnata in stato di Eccezione. NPR-24565: Hotfix per CQ-4246203
* Il pulsante Emulatore dispositivo scompare dalla modalità di modifica e anteprima in seguito all’applicazione di CFP14. NPR-24566: Hotfix per CQ-4247060
* (Interfaccia classica) Tutti i tag vengono visualizzati come vuoti dopo essere stati creati nella finestra di dialogo. NPR-24688: Hotfix per CQ-4246407
* Impossibile creare la versione al primo tentativo. NPR-24774: Hotfix per CQ-4232176
* I rapporti inclusi in /etc/reports/ non funzionano correttamente e non presentano alcun grafico di dati storici. NPR-24138: Hotfix per CQ-4220180

### Vulnerabilità {#vulnerability-1}

* L’integrazione con Salesforce è vulnerabile ad attacchi di tipo SSRF (Server Side Request Forgery). NPR-24289: Hotfix per CQ-4245277
* Vulnerabilità SSRF (Server Side Request Forgery) in ReportingServicesProxyServlet. NPR-24657: Hotfix per CQ-4246880

### Granite {#granite-3}

* Le operazioni di lettura dei metadati non vengono terminate. NPR-24240: Hotfix per GRANITE-19866
* Jetty è stato aggiornato a 9.4.11.v20180605 per correggere alcune vulnerabilità. NPR-25033: Hotfix per GRANITE-22120

### WCM - Componenti Foundation {#wcm-foundation-components-1}

* PageComparator genera un’eccezione ClassCastException durante l’ordinamento delle pagine. NPR-24123: Hotfix per CQ-4244048
* La funzionalità Mostra/Nascondi del componente del menu a discesa del modulo non viene eseguita come previsto. NPR-24562: Hotfix per CQ-4222853

### Interfaccia utente {#user-interface}

* È stato notato un utilizzo intensivo della CPU dovuto a un numero elevato di richieste nella funzionalità di amministrazione Ricerca. NPR-23588: Hotfix per GRANITE-21286
* (Interfaccia classica) Il componente visualizza i valori predefiniti anche se il servizio del modello dati del modulo associato è impostato su un campo vuoto. NPR-21903: Hotfix per GRANITE-19744
* Multifield genera un’eccezione NPE se per la richiesta non sono disponibili FormData. NPR-24513: Hotfix per GRANITE-21055

## Forms {#forms-4}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-4}

#### Core {#core}

* (OSGI) AEM Forms OSGi è interessato da un avviso di sicurezza sul data binding di Jackson. NPR-24274: Hotfix per CQ-4230245

#### Rights Management {#rights-management}

* Errore di Apache POI dopo l’installazione di AEM 6.2 SP1-CFP14. NPR-25054, NPR-25052: Hotfix per CQ-4245898, CQ-4244778

#### Moduli HTML5 {#html-forms}

* nell’anteprima HTML, i dati non vengono inseriti con la precompilazione di campi con più righe di testo. NPR-23357: Hotfix per CQ-4244212
* Quando si esegue l’anteprima predefinita di una lettera, la mappatura dei frammenti di layout non viene visualizzata; appare invece correttamente se si fa clic sul pulsante Anteprima. NPR-22993: Hotfix per CQ-4237745
* Si verifica un problema con l’anteprima HTML di un campo di testo quando a un modello viene applicato un pattern di numero di previdenza sociale. NPR-23205

#### Moduli adattivi {#adaptive-forms-3}

* Si verifica un errore “Guidelib non definita” quando si aggiunge un modulo AEM a un componente parsys. NPR-24269: Hotfix per CQ-4244546

### Programma di installazione Forms JEE {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Le terminazioni delle righe di finestra nei file di script Shell impediscono l’esecuzione di LCM in UNIX. NPR-22958

### Bundle OSGi e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-3}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP16

[Ottieni file](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP16

[Ottieni file](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di [AEM 6.2 SP1](https://helpx.adobe.com/it/experience-manager/6-2/release-notes/sp1.html).

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* Correzione proattiva della sicurezza nella tabella di Foundation per mantenere un design coerente.
* È stato aggiunto il supporto di typeHint per salvare i valori come stringa.
* È stata potenziata la sicurezza del servizio di precompilazione di Forms.
* È stato eseguito l’aggiornamento alla versione più recente del file adobe-reader-extensions-dsc.jar per introdurre alcune correzioni in Reader Extension.
* È stato modificato l’hook di convalida in modo da considerare gli elementi “:invalid” per l’input del numero di incremento.

### Assets {#assets-4}

* I dati EmbedXMP sono sempre impostati su “active” per il processo di generazione Ptiff. NPR-22776: Hotfix per CQ-4234498
* Impossibile impostare più valori predefiniti nei campi con più valori. NPR-22900: Hotfix per CQ-4239000
* (Dynamic Media) Quando si seleziona la casella di controllo Rappresentazioni dinamiche, il file ZIP scaricato restituisce l’immagine TIFF originale con un file da zero byte. NPR-22410: Hotfix per CQ-4198471
* (Interfaccia touch) Percorso di caricamento predefinito per le risorse nella vista a colonne. NPR-23475: Hotfix per CQ-4237057

### Integrazione {#integration-5}

* In modalità Target gli autori possono modificare un componente ereditato dalla blueprint senza annullare l’ereditarietà. NPR-22751: Hotfix per CQ-4237907
* La variabile del percorso non è codificata correttamente e determina una vulnerabilità cross-site scripting (XSS) non permanente. NPR-22851

### MSM {#msm-1}

* Durante il rollout di una Live Copy con più configurazioni di rollout, se si verifica un conflitto ResourceNameConflict sotto la radice, il flusso di rollout termina senza includere tutti i rami. NPR-22842: Hotfix per CQ-4236188

### Platform {#platform-3}

* È stato implementato un limite di polling in una richiesta di applicazione inversa. NPR-23351: Hotfix per GRANITE-21135****
* La modifica al pattern dei messaggi non si riflette sui logger personalizzati. NPR-23486: Hotfix per CQ-4241974

### Sites {#sites-4}

* In un testo in un Editor Text, non è possibile creare un collegamento con spazi o altri caratteri speciali a un documento. NPR-22289: Hotfix per CQ-4224321
* Se si salva un segmento con un valore molto grande (10000000000), l’incremento viene impostato su 0 e viene generato un messaggio di errore. NPR-22524: Hotfix per CQ-4237006
* Impossibile fare clic su Aggiungi elemento nel componente Multifield. NPR-22552: Hotfix per CQ-4237404
* La barra di scorrimento orizzontale non è visibile per i segmenti con un titolo lungo. NPR-22615: Hotfix per CQ-4237001
* Il caricamento di un pubblico vuoto genera un codice JavaScript errato. NPR-22974: Hotfix per CQ-4238734
* Quando si pianifica un’attivazione o una disattivazione, il titolo del flusso di lavoro è obbligatorio e il titolo del flusso di lavoro personalizzato non viene quindi tradotto nella timeline. NPR-23121: Hotfix per CQ-4237552
* Correzioni richieste per problemi relativi ai segmenti Target in Sites. NPR-23128
* (Firefox) La casella di controllo per la persona selezionata non è quella corretta. NPR-23345
* Oltre alle icone, per le diverse modalità vengono visualizzate anche delle etichette. NPR-23275
* Errore di tipo “Valore del selettore di ricorsione non valido” durante la migrazione di un componente da AEM 6.0 a AEM 6.2. NPR-23503: Hotfix per CQ-4241258

### Communities {#communities-1}

* Le notifiche web ed e-mail non vengono attivate a causa di un errore del messaggio per i gruppi. NPR-23447: Hotfix per CQ-4242880

### Traduzione {#translation-1}

* Se nella configurazione di traduzione viene impostata l’opzione “Non tradurre” per una risorsa, vengono comunque create delle copie in lingua della risorsa. NPR-22540: Hotfix per CQ-4237962

### Interfaccia utente {#user-interface-1}

* L’utilizzo di Omnisearch con una query contenente un trattino restituisce un errore del server. NPR-22999: Hotfix per GRANITE-19674
* DatePicker non supporta l’impostazione manuale di suggerimenti di tipo esterni impostati da un campo nascosto. Se si modifica il valore di hint “type”, viene generato un errore di conversione. NPR-23333: Hotfix per GRANITE-21194

### WCM - Componenti Foundation {#wcm-foundation-components-2}

* Il componente CAPTCHA è stato dichiarato obsoleto per una maggiore sicurezza. Se si utilizza il componente CAPTCHA, viene visualizzato il messaggio “Il componente Captcha è obsoleto e non deve più essere utilizzato” dopo l’installazione della versione 6.2 SP2-CFP15 o di una versione successiva. Per maggiore sicurezza, si può personalizzare il componente AEM in modo da includere reCAPTCHA. NPR-22151: Hotfix per CQ-4220052
* L’oggetto “Table” del componente WCM Foundation presenta una vulnerabilità cross-site scripting archiviati. NPR-23206: Hotfix per CQ-4240760

### Vulnerabilità {#vulnerability-2}

* Vulnerabilità cross-site scripting (XSS) nei collegamenti di progetto di Interfaccia utente amministratore. NPR-23272: Hotfix per CQ-4241795

## Forms {#forms-5}

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-5}

#### Gestione della corrispondenza {#correspondence-management}

* Quando si esegue l’anteprima predefinita di una lettera, la mappatura dei frammenti di layout non viene visualizzata; appare invece correttamente se si fa clic sul pulsante Anteprima. NPR-23335: Hotfix per CQ-4237745
* Nella lettera corrispondente ai binding definiti in XDP, i dati non vengono aggiunti tramite l’URL diretto della lettera. NPR-24145: Hotfix per CQ-4244290

#### Forms Mobile {#mobile-forms}

* (Gestione corrispondenza) Si verifica un disallineamento dei dati quando si carica una lettera con XML di destinazione. NPR-22993: Hotfix per CQ-4237663

#### Servizio estensioni Reader {#reader-extensions-service}

* Impossibile applicare l’estensione Reader a un file Adobe PDF. NPR-23067

#### Forms Manager {#forms-manager}

* I moduli incorporati in Sites non vengono pubblicati quando si ripubblica un pagina di Sites. NPR-23014: Hotfix per CQ-4236566

#### Vulnerabilità {#vulnerability-3}

* Hotfix proattivi per vulnerabilità cross-site scripting. NPR-20624: Hotfix per CQ-4206055
* Vulnerabilità cross-site scripting (XSS) memorizzata nella scheda delle note di Forms Manager. NPR-27157: Hotfix per CQ-4255556

#### Servizio Encryption {#encryption-service}

* (OSGI) [JEE] Stato firma non corretto per PDF con allegato durante la verifica tramite il processo di convalida PDF. NPR-23269, NPR-23737

### Programma di installazione Forms JEE {#forms-jee-installer-5}

#### Core {#core-1}

* Sono stati risolti i problemi segnalati nell’analisi del codice statico di Core-ext. NPR-13947

#### Servizio PDFG {#pdfg-service}

* Il convertitore da HTML a PDF non funziona. NPR-21545

### Bundle OSGi e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-4}

Nei documenti di testo seguenti sono elencati i bundle OSGi e i pacchetti di contenuti inclusi nel CFP.

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP15

[Ottieni file](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP15

[Ottieni file](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Cumulative Fix Pack 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* È stata migliorata la possibilità di modifica delle proprietà dei metadati delle risorse.
* Il processo di notifica della scadenza delle password è stato riconfigurato per le risorse già in stato di scadenza.
* La console dell’interfaccia touch è stata personalizzata ed estesa con lingue aggiuntive.
* È stato aggiornato cq-msm-core per una sincronizzazione più efficiente di Livecopyindex.
* È stata semplificata la funzionalità di replica per vari Rollout.

### Assets {#assets-5}

* Gli utenti non possono scaricare risorse con liberatoria e nomi file lunghi. NPR-22163: Hotfix per CQ-4235274
* La presenza di virgolette singole impedisce l’aggiornamento dei metadati nella vista per la modifica in massa e l’interfaccia utente risulta completamente danneggiata quando si aprono le proprietà di una risorsa mediante le azioni rapide della barra degli strumenti. NPR-22317, NPR-22353: Hotfix per CQ-4236990, CQ-4236469
* Il processo di notifica di scadenza delle risorse non disattiva le risorse scadute. NPR-22346: Hotfix per CQ-4237188
* Il download delle risorse non riesce quando si utilizza Digital Rights Management in Assets con Safari. NPR-22378: Hotfix per CQ-4236460
* Le rappresentazioni web di piccole immagini presentano dimensioni pixel non accurate. NPR-22435: Hotfix per CQ-4236742

### Sites {#sites-5}

* (Interfaccia touch) I tag spostati vengono visualizzati sia nella posizione precedente che in quella nuova nelle proprietà delle pagine. NPR-21921: Hotfix per CQ-4238598
* (Interfaccia touch) L’Editor Rich Text rimuove tutti gli attributi dal tag &lt;a>, ad eccezione degli id. NPR-22045: Hotfix per CQ-4234133
* Quando si incollano contenuti direttamente nell’Editor Rich Text tramite CTRL+V, le interruzioni di riga vengono ignorate. NPR-22117: Hotfix per CUI-5881
* (Interfaccia touch) Impossibile visualizzare più di 40 tag per namespace. NPR-22290: Hotfix per CQ-99114
* Problemi relativi ai feed RSS, porta -1 a AEM 6.2. NPR-22158: Hotfix per CQ-4233339
* (IE) Quando si crea per la prima volta un carattere in un campo Rich Text, al carattere viene aggiunto uno spazio finale. NPR-22443: Hotfix per CQ-4235343
* Quando si tenta di trovare una corrispondenza con il nome del pacchetto, l’oggetto Java “Use” blocca il servizio SightlyJavaCompilerService a causa di uno spazio finale nella dichiarazione del pacchetto. NPR-22557: Hotfix per GRANITE-20836
* La console dell’interfaccia utente touch non rileva nuove lingue per l’assegnazione di tag. NPR-22250: Hotfix per CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Prima di caricare i folio in DPS, era necessario impostare sia la data di pubblicazione che la data di copertina. NPR-22484

### Commerce {#commerce}

* Più vulnerabilità cross-site scripting (XSS) nella creazione guidata di cataloghi in Commerce. NPR-22344: Hotfix per CQ-4237017

### MSM {#msm-2}

* La sincronizzazione LiveCopyIndex provoca una congestione di thread durante gli aggiornamenti di indici particolarmente lunghi. NPR-22214: Hotfix per CQ-90667
* La proprietà cq:cugEnabled viene disabilitata quando viene modificato un altro campo in una Live Copy, rendendo la pagina non protetta. NPR-22246: Hotfix per CQ-4236050
* L’azione Rollout pagina non aggiorna gli elementi secondari quando una pagina viene sospesa. NPR-22483: Hotfix per CQ-4236956
* Se si esegue il rollout di una struttura spostata in una pagina mastro, cq:moveTarget non viene eseguito correttamente. NPR-22373: Hotfix per CQ-4232536

### Integrazione {#integration-6}

* Se si tenta di ordinare le offerte nella libreria di selezione delle offerte, si verifica un comportamento anomalo. NPR-22208: Hotfix per CQ-4235439
* TargetContentImpl rallenta l’esecuzione di AEM durante le query con tempi di esecuzione lunghi. NPR-22361: Hotfix per CQ-4236907
* Il motore target (mbox.js, at.js) non utilizza URL gestiti e utilizza URL contenenti due punti, che potrebbero non riuscire con determinate implementazioni. NPR-22366: Hotfix per CQ-4237854
* La personalizzazione di una pagina richiede la pubblicazione direttamente sul nodo del marchio. NPR-22370: Hotfix per CQ-4236895

### Foundation {#foundation}

* I modelli Apache Sling Scripting Sightly utilizzano il bundle di provider **org.apache.sling.scripting.sight.models.provider/1.0.18**. NPR-22614: Hotfix per Sling-5944, Sling-6866

### Progetti {#projects}

* Il flusso di lavoro Starter non è in grado di accettare il valore TypeHint di String. NPR-22436: Hotfix per CQ-4237855

### Traduzione {#translation-2}

* Esame dei problemi relativi alla funzionalità Anteprima. NPR-22201: Hotfix per CQ-4223753

### Interfaccia utente {#user-interface-2}

* (Interfaccia classica) Il componente visualizza i valori predefiniti anche se il servizio del modello dati del modulo associato è impostato su un campo vuoto. NPR-21903: Hotfix per GRANITE-19744

### WCM - Componenti Foundation  {#wcm-foundation-components-3}

* Errore durante la pubblicazione di una pagina Live Copy che punta a una pagina di importazione in Adobe Campaigns. NPR-22470: Hotfix per CQ-4237164
* Errori JavaScript durante l’apertura dell’editor di frammenti di esperienza. NPR-22598: Hotfix per CQ-4238415

### Flusso di lavoro {#workflow}

* Il servizio di notifica e-mail del flusso di lavoro Day CQ attiva un messaggio e-mail per ciascun nodo Mongo per le notifiche WorkflowCompleted e WorkflowAborted. NPR-22486: Hotfix per CQ-4238172

## Forms {#forms-6}

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-6}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

#### Moduli adattivi {#adaptive-forms-4}

* Incoerenza nel valore del segnaposto a discesa nel modulo adattivo in IE11 e Chrome. NPR-22405: Hotfix per CQ-4227096

### Programma di installazione Forms JEE {#forms-jee-installer-6}

#### Installazione di LCM {#install-lcm}

* Aggiornamento dei file JAR di Jsafe a Cryptoj 6.1.3.1 nel programma di installazione e in LCM. NPR-22744

### Feature Pack inclusi {#feature-packs-included}

#### Gestione processi {#process-management}

* (Area di lavoro HTML) Quando un utente richiede un’attività, il numero nella coda viene aggiornato per quel particolare utente, ma non per altri utenti, a meno che la pagina non venga aggiornata. NPR-19778: Hotfix per CQ-4233665

### Bundle OSGi e pacchetti di contenuti inclusi in CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP14

[Ottieni file](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP14

[Ottieni file](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
AEM Cumulative Fix Pack 6.2 SP1-CFP13 costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* È stata abilitata la configurazione del campo Parametro statico nelle impostazioni del componente Target quando si utilizza AT.js come libreria client.
* Sono state apportate correzioni alla funzionalità Mostra/Nascondi del componente del menu a discesa.
* Sono state apportate correzioni inerenti all’utilizzo di tipi di pubblico per la sincronizzazione delle destinazioni.
* È stata migliorata la versatilità di Gestione della corrispondenza, che ora supporta i caratteri speciali.

### Assets {#assets-6}

* La funzionalità Pulizia delle versioni non rimuove le versioni precedenti delle risorse. NPR-21682: Hotfix per CQ-4212996
* Il nuovo ordine delle cartelle in una cartella riordinabile non viene mantenuto. NPR-21964: Hotfix per CQ-4231761

### Sites {#sites-6}

* (Interfaccia touch)(Interfaccia classica) Più vulnerabilità cross-site scripting (XSS) in HTL e nei componenti core. NPR-21532: Hotfix per CQ-4232305 e CQ-4232511
* La creazione e la formattazione di contenuto (ad esempio, l’assegnazione o la rimozione di nuovi stili di elenco) in un testo selezionato non funziona correttamente in Internet Explorer 11. NPR-21533: Hotfix per CQ-4230689
* (Safari) Gli utenti non riescono a visualizzare tutte le risorse nel pannello per la ricerca delle risorse. NPR-21981: Hotfix per CQ-4213720
* La modifica temporale restituisce l’errore “RecursionTooDeepException” con una pagina illeggibile e non viene creata una nuova versione, anche se la data viene modificata. NPR-21707: Hotfix per CQ-4199536
* Quando si carica una pagina nell’editor, WorkflowStatusprovider (pageinfo.json) viene caricato tre volte, rallentando le prestazioni dell’istanza di AEM. NPR-21778: Hotfix per CQ-59232

### Integrazione {#integration-7}

* La creazione di tipi di pubblico per Tipo mobile e Browser nella modalità di authoring di Target non funziona in AEM. NPR-21676, NPR-21681: Hotfix per CQ-4232100
* Con un’elevata latenza durante l’aggiornamento di un componente di destinazione, è possibile aggiungere un’altra offerta prima che il componente venga aggiornato completamente. NPR-21744: Hotfix per CQ-4233158/CQ-4234293
* Gli utenti non possono visualizzare i valori di test di Parametro statico nella chiamata mBox, visibili quando si esegue il test utilizzando AT.js come libreria client nella configurazione cloud. NPR-21930: Hotfix per CQ-4234520

### Platform {#platform-4}

* Si verificano problemi di prestazioni con la sincronizzazione degli utenti quando il numero di utenti o gruppi è elevato. NPR-20431: Hotfix per CQ-4223282
* Gli utenti non vengono sincronizzati con la funzionalità Sincronizzazione utenti nella distribuzione Sling. NPR-21911: Hotfix per GRANITE-20404
* Impedire che le parole non significative (stop word) vengano evidenziate negli estratti di ricerca (in una pagina di Geometrixx). NPR-21835: Hotfix per GRANITE-21067\
  Nota: questa correzione richiede Oak CFP 1.4.20 o versione successiva.

### Traduzione {#translation-3}

* Manca la proprietà jcr per l’ID utente iniziatore durante la creazione di un progetto di traduzione. NPR-21715: Hotfix per CQ-4230713

### WCM - Componenti Foundation {#wcm-foundation-components-4}

* La funzionalità Mostra/Nascondi del componente del menu a discesa del modulo non viene eseguita come previsto. NPR-22164: Hotfix per CQ-4235288

## Forms {#forms-7}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-7}

#### Moduli adattivi {#adaptive-forms-5}

* Iniezione di XXE (XML External Entity) nei moduli adattivi. NPR-21982: Hotfix per CQ-109878
* (iOS11) Quando si fa clic su un componente allegato, il file allegato apre la fotocamera invece del visualizzatore file del dispositivo. NPR-21926: Hotfix per CQ-4214348
* La mancanza del titolo nell’interfaccia di creazione del tema genera un’eccezione e impedisce il rendering della finestra di dialogo. Hotfix per CQ-4236143

#### Gestione della corrispondenza {#correspondence-management-1}

* Problemi di rendering con i dati XML contenenti caratteri speciali. NPR-21712: Hotfix per CQ-4229137

### Programma di installazione Forms JEE {#forms-jee-installer-7}

#### Servizio assemblatore {#assembler-service}

* Il file PDF generato con 6.2.0-ASM-1017-003 è danneggiato. NPR-21427: Hotfix per CQ-4228046

#### Servizio PDFG {#pdfg-service-1}

* Errore OCR a causa di dimensioni di pagina impreviste (PDF) da file PNG, JPEG e TIFF. NPR-19489: Hotfix per CQ-4209079

## Bundle OSGi e pacchetti di contenuti inclusi in CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP13

[Ottieni file](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP13

[Ottieni file](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 costituisce un aggiornamento di rilievo contenente importanti correzioni per i clienti introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* È stata migliorata la gestione dei metadati per i campi multivalore.
* È stato aggiunto il supporto per i codici dei paesi con più di due caratteri nei flussi di lavoro di traduzione.
* È stato migliorato il rendering delle pagine con più componenti nidificati.
* È stata migliorata la sincronizzazione delle date di pubblicazione delle risorse tra AEM e Adobe Digital Publishing Suite.

### Assets {#assets-7}

* Un numero eccessivo di caratteri in OmniSearch causa l’arresto anomalo del server AEM. NPR-21083: Hotfix per CQ-4223602
* I valori specificati nella seconda opzione di un campo multivalore nello schema metadati non vengono aggiunti ai valori precedentemente specificati in CRX-de. NPR-21220: Hotfix per CQ-4224526
* Il download delle risorse non riesce quando si utilizza Digital Rights Management in Assets con Safari. NPR-21387: Hotfix per CQ-4230287

### Sites {#sites-7}

* (DAM) (Interfaccia classica) Più vulnerabilità cross-site scripting (XSS) in alcuni file SWF nel modulo quickstart di AEM CQ Author/Publish. NPR-21073, NPR-21074: Hotfix per NPR-20612
* Il selettore di tag non traduce i tag disponibili in più lingue. NPR-21221: Hotfix per CQ-78855
* Si verificano problemi di rendering con la console di articoli AEM, poiché l’utilizzo di più componenti nidificati rallentano le prestazioni. NPR-21271: Hotfix per CQ-4224158

### Integrazione {#integration-8}

* Quando si aggiunge un framework Target, la modalità Targeting non è disponibile nell’elenco per la selezione della modalità nell’editor. NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* (Digital Publishing Suite) Le date di pubblicazione dei folio in AEM non corrispondono alle date visualizzate in Folio Producer. NPR-21145

### MSM {#msm-3}

* Il processo di ripristino di una Live Copy viene interrotto dopo l’eliminazione della prima pagina locale nella Live Copy. NPR-21276: Hotfix per CQ-4229743

### Platform {#platform-5}

* La libreria taglib personalizzata che fa riferimento a tag implementati come script non viene trovata dopo l’aggiornamento ad AEM 6.3. NPR-20149: Hotfix per GRANITE-18433

### Traduzione {#translation-4}

* I flussi di lavoro di traduzione hanno esito negativo in presenza di codici lang_country con più di 2 caratteri. NPR-21088: Hotfix per CQ-4197439
* Non è possibile inviare una pagina di risorsa a un progetto di traduzione finché il progetto non viene completato. NPR-21219: Hotfix per CQ-4209908

### Interfaccia utente {#user-interface-3}

* La selezione di un componente non elimina la proprietà di destinazione durante l’invio di un modulo. NPR-21163: Hotfix per GRANITE-14125
* L’espansione HTTP.encodePathOfURI codifica due volte il segno più (+). NPR-21417: Hotfix per GRANITE-16340

### Vulnerabilità {#vulnerability-4}

* Vulnerabilità cross-site scripting (XSS) nell’editor di metadati DAM. NPR-21434: Hotfix per CQ-83472
* Più file SWF vulnerabili ad attacchi cross-site scripting (XSS). NPR-20612: Hotfix per CQ-4213297

## Forms {#forms-8}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-8}

#### Gestione della corrispondenza {#correspondence-management-2}

* (IE11) Il rendering iniziale del contenuto HTML viene eseguito solo nella parte sinistra, mentre il lato destro viene caricato in modo intermittente, anche dopo il caricamento dell’interfaccia utente completa. NPR-21554
* Il pulsante di invio dell’anteprima di una lettera risulta disattivato dopo l’installazione di AEM 6.2 SP1-CFP9. NPR-21547
* Quando si seleziona il tipo di collegamento Risorsa, la finestra Selezione risorsa non si apre nella procedura guidata di associazione dati per Modifica lettera. NPR-21164: Hotfix per CQ-4194567
* Per modificare un modulo di testo in linea o modificabile, tocca l’icona Modifica corrispondente o fai doppio clic sul modulo di testo corrispondente nell’anteprima della lettera. NPR-21402

#### Moduli adattivi {#adaptive-forms-6}

* Il componente per il pulsante Invio di AEM Forms mostra type=&quot;button&quot; invece di type=&quot;submit&quot;. NPR-21007
* I dati rimangono invariati quando si aggiungono o si eliminano nuovi pannelli nell’ambito dei pannelli ripetibili. NPR-21408

### Programma di installazione Forms JEE {#forms-jee-installer-8}

#### Core {#core-2}

* L’aggiornamento al più recente Java 8 Update 131 genera un’eccezione: “JsafeJCE provider is disabled, a FIPS 140 required self-integrity check failed”. NPR-21355

  **Nota:** questo NPR richiede impostazioni aggiuntive; per ulteriori informazioni, consulta l’[ultimo aggiornamento Java 8](#latest-java-update-throws-an-exception-npr).

* Aggiornamento dei file JAR di Jsafe a Cryptoj 6.1.3.1 nei servizi Core, Encryption, Signature e Document Security. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Installazione di LCM {#install-lcm-1}

* Aggiornamento dei file JAR di Jsafe a Cryptoj 6.1.3.1 nel programma di installazione e in LCM. NPR-21362

#### Servizio PDFG {#pdfg-service-2}

* Aggiornamento dei file JAR di Jsafe a Cryptoj 6.1.3.1 in PDFG. NPR-21359

#### Gestione processi {#process-management-1}

* (Area di lavoro HTML) È stato abilitato il ridimensionamento colonne per evitare che la categoria del nome non venga interamente visualizzata. NPR-19770: Hotfix per CQ-4233668

#### Servizio estensioni Reader {#reader-extensions-service-1}

* Aggiornamento dei file JAR di Jsafe a Cryptoj 6.1.3.1 in RE. NPR-21357

## Bundle OSGi e pacchetti di contenuti inclusi in CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP12.1

[Ottieni file](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP12.1

[Ottieni file](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* È stato aggiornato cq-msm-core per una sincronizzazione più efficiente di Livecopyindex.
* È stata migliorata l’efficienza nella modifica dei frammenti di contenuto.
* In Gestione pacchetti è disponibile un’opzione di convalida per l’identificazione delle autorizzazioni ACL.
* In Campaign è stata introdotta la possibilità di includere l’ID e-mail per la corrispondenza con i clienti.
* Sono state migliorate le funzionalità di codifica video per i file Dynamic Media.
* Sono state introdotte correzioni nel componente Sightly e nelle Live Copy.

### Assets {#assets-8}

* La codifica video in Dynamic Media ha esito negativo per i file il cui nome contiene degli spazi. NPR-20818: Hotfix per CQ-102469
* Più vulnerabilità cross-site scripting (XSS) in alcuni file SWF nel modulo quickstart di AEM CQ Author/Publish. NPR-21071, NPR-21072
* Gli utenti non possono scaricare risorse con liberatoria e nomi file lunghi. NPR-20255: Hotfix per CQ-4222139

### Sites {#sites-8}

* Integrazione AEM e Campaign: i collegamenti speciali vengono riscritti in Adobe Campaign, impedendo ai clienti di inviare collegamenti “mailto:” nelle e-mail. NPR-20787: Hotfix per CQ-4225760
* (Interfaccia utente touch) Problemi di prestazioni e di usabilità con AEM quando la lingua è impostata sul francese. NPR-20854: Hotfix per CQ-4227628
* Il collegamento di un file di risorse codificato con l’apposito plugin nell’Editor Rich Text restituisce un collegamento vuoto. NPR-20626, NPR-21059: Hotfix per CQ-4223011
* L’editor di metadati per frammenti di contenuto impedisce agli autori di salvare le modifiche apportate ai frammenti di contenuto. NPR-20641: Hotfix per CQ-4224755
* L’alias di proprietà pagina conduce all’opzione Richiedi pubblicazione/Richiedi annullamento pubblicazione. NPR-20731: Hotfix per CQ-4226227
* Problemi nei componenti di testo relativi alla codifica dei collegamenti nell’elemento Editor Rich Text. NPR-20755: Hotfix per CQ-4224321

### Platform {#platform-6}

* ResourceResolverImpl.map() non richiama ResourceDecorator. NPR-20788: Hotfix per GRANITE-19718
* org.apache.sling.i18n.DefaultLocaleResolver non è in grado di elaborare le richieste tramite org.apache.sling.Engine.SlingRequestProcessor. NPR-20706: Hotfix per CQ-94880
* Richiesta per l’aggiunta di un’opzione di convalida in Gestione pacchetti per rilevare se, per un determinato pacchetto, sono cambiate le autorizzazioni o i privilegi ACL. Hotfix per CQ-4229196

### Integrazione {#integration-9}

* (Search&amp;Promote) Una definizione ambigua del filtro per il pacchetto di contenuti determina la sovrascrittura di alcuni percorsi durante l’installazione. NPR-20808: Hotfix per CQ-4227615

### Flusso di lavoro {#workflow-1}

* Problemi di stabilità relativi all’implementazione del server di produzione AEM. NPR-20979: Hotfix per GRANITE-19104

### Progetti {#projects-1}

* (Interfaccia touch) Impossibile aggiungere membri del team a un progetto. NPR-20990: Hotfix per CQ-4205375

### WCM - Componenti Foundation {#wcm-foundation-components-5}

* Il componente immagine Sightly “link to” genera un errore 403 a causa della mancanza dell’estensione .html. NPR-20823: Hotfix per CQ-4195909
* In un sito blueprint che utilizza Live Copy, se si tenta di eliminare un componente Modulo viene generata un’eccezione NullPointerException e il componente viene nuovamente aggiunto, anziché essere eliminato. NPR-20855: Hotfix per CQ-4204628
* La sincronizzazione LiveCopyIndex provoca una congestione di thread durante gli aggiornamenti di indici particolarmente lunghi. NPR-20634: Hotfix per CQ-90667

### Sicurezza {#security}

* Aggiornamento proattivo della libreria XSS. NPR-21174
* Aggiornamento ad Apache Commons Email 1.5, che presenta un’API semplificata per l’invio di e-mail. NPR-20509: Hotfix per GRANITE-18240
* È stata applicata la patch di sicurezza applicata all’API Apache Sling XSS Protection per impedire che le vulnerabilità cross-site scripting vengano ignorate. NPR-21290: Hotfix per GRANITE-19924
* Possibilità di bypassare XSS nella funzione XSSAPI#getValidHref. NPR-21174: Hotfix per GRANITE-19924

### App mobili {#mobile-apps}

* Risoluzione dei problemi relativi alle richieste di intestazione curl per le risorse incluse con AEM. NPR-20511: Hotfix per CQ-4221520 e CQ-103024

## Forms {#forms-9}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

Gli elementi di rilievo di AEM Forms sono:

* Abilitazione dell’autenticazione dei certificati per gli utenti di Workbench.
* Correzioni relative all’usabilità per Gestione della corrispondenza, moduli HTML5 e l’area di lavoro AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-9}

#### Moduli HTML5 {#html-forms-1}

* Problemi di usabilità con il componente Scribble su dispositivi iOS 10 e 11. NPR-21092

#### Gestione della corrispondenza {#correspondence-management-3}

* (Interfaccia utente per la corrispondenza) Dopo un clic, il pulsante Invia viene disattivato. NPR-21078

### Programma di installazione Forms JEE {#forms-jee-installer-9}

#### Servizio assemblatore {#assembler-service-1}

* docConvertor non è in grado di produrre il file PDF/A e genera un errore di tipo “Il prefisso “stEvt” per l&#39;elemento “stEvt:action” non è associato”. NPR-21032: Hotfix per CQ-4222540
* Durante la chiamata del servizio OMPFSubmission/PDFA/PDFtoPDFA, viene generata l’eccezione “java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE”. Questa eccezione impedisce che il processo di verifica della firma di breve durata possa essere completato, fino al riavvio del server. NPR-20792

#### Workbench {#workbench}

* Abilitazione dell’autenticazione dei certificati per gli utenti di Workbench. NPR-17548: Hotfix per CQ-4214486

#### Gestione processi {#process-management-2}

* Il processo di preparazione dei dati viene richiamato più volte quando si esegue il rendering del modulo mobile con parametri dataref. NPR-19801: Hotfix per CQ-4230427, CQ-4230400

## Bundle OSGi e pacchetti di contenuti inclusi in CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP11

[Ottieni file](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.2 SP1-CFP11

[Ottieni file](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* È stata aggiunta la nuova funzione di utilità onDialogLoaded per i test.
* Sono stati aggiunti configurazioni e test di unità front-end a ClientLibraryProxyServlet.
* Sono state apportate correzioni delle prestazioni nel componente per la modifica locale di più immagini.
* Sono stati apportati aggiornamenti alla configurazione in Apache Sling JCR ResourceBundleProvider.

### Assets {#assets-9}

* L’anteprima delle risorse non funziona se i flussi di lavoro di aggiornamento delle risorse sono disattivati. NPR-20543: Hotfix per CQ-4204986
* Problemi di rendering con la classe aggiunta nella proprietà della classe granite: (cq-damadmin-admin-assets-upload). NPR-20514: Hotfix per CQ-4219238
* Le risorse miniature il cui titolo contiene dei caratteri speciali mostrano l’oggetto Java nell’attributo alt. NPR-20347: Hotfix per CQ-4223620
* Il codice di confronto delle versioni è stato sostituito con il codice proprietario Adobe a causa di problemi di licenza. NPR-20273: Hotfix per CQ-4223758
* Problemi di elaborazione durante il caricamento di file PSB CMYK con più livelli alfa. NPR-20251: Hotfix per CQ-4220869
* I dizionari di internazionalizzazione non funzionano a meno che il server non venga riavviato in org.apache.sling.i18n 2.5.6. NPR-20525: Hotfix per Granite - 19490
* Con la configurazione Thread Dump Collector predefinita (avvio predefinito di AEM), non viene generato alcun dump di thread in base al periodo di pianificazione. NPR-20288: Hotfix per GRANITE-19488 / GRANITE-12741 / CQ-90647.

### Sites {#sites-9}

* Se il filtro data modificato è stato modificato dopo l’apertura della ricerca salvata, i risultati restano invariati rispetto al precedente valore salvato del filtro data modificato. NPR-19739: Hotfix per CQ-4219425
* Impossibile caricare le pagine con componenti nidificati. NPR-20312
* Il flusso di lavoro Richiesta eliminazione viene attivato al momento dell’eliminazione dei pacchetti del flusso di lavoro. NPR-20266: Hotfix per CQ-4221686
* (Interfaccia touch) Problema con Copia/Incolla sia con lo strumento Appunti del sistema operativo sia con lo strumento Appunti interno di AEM. NPR-20228: Hotfix per CQ-4220383
* L’istanza AEM diventa lenta in modalità Vista a elenco quando vengono caricate molte risorse (oltre 100). NPR-20034: Hotfix per CQ-4222695
* (Interfaccia touch) Quando si eliminano dei lanci tramite la console dell’interfaccia classica, tutte le pagine diventano non modificabili. NPR-20520: Hotfix per CQ-4225074
* Il menu a discesa Target non funziona con più componenti Editor Rich Text in una finestra di dialogo. NPR-20345: Hotfix per CQ-4220981

### Platform {#platform-7}

* Se si accede utilizzando una sessione anonima, ClientLibraryProxyServlet non esegue il proxy delle richieste alle librerie client nell’istanza di pubblicazione e restituisce l’errore “HTTP 404 - Pagina non trovata”. NPR-20195: Hotfix per GRANITE-14409

### Integrazione {#integration-10}

* Se si seleziona il motore di destinazione come Adobe Target, il componente non viene caricato e viene generato un errore nel registro del server. NPR-20058: Hotfix per CQ-88071, CQ-109698, CQ-4201600

### Commerce {#commerce-1}

* Non viene visualizzato alcun messaggio di conferma o di reindirizzamento quando si creano prodotti della stessa pagina. NPR-20257: Hotfix per CQ-4223414

### Interfaccia utente {#user-interface-4}

* Se DatePicker è un campo all’interno di un campo multiplo, i valori salvati nei campi data non vengono mantenuti durante la modifica del componente. NPR-20077: Hotfix per GRANITE-19147
* Le query precedenti non vengono interrotte in caso di attivazione di query consecutive e vengono generati risultati non corretti. NPR-20397: Hotfix per GRANITE-19306

### WCM - Componenti Foundation {#wcm-foundation-components-6}

* La proprietà ImageMap è ancora presente anche dopo aver eliminato le immagini dal componente di modifica locale di più immagini. NPR-20142: Hotfix per CQ-4222982

## Forms {#forms-10}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-10}

#### Moduli adattivi {#adaptive-forms-7}

* Lo script valueCommit viene eseguito due volte per DropDownList quando viene modificato tramite l’interfaccia utente. NPR-19989: Hotfix per CQ-110212

### Programma di installazione Forms JEE {#forms-jee-installer-10}

**Gestione processi**

* Il pacchetto CFP include AEM Forms HTML Workspace versione 2.2.26. NPR-20099
* Il modulo precompilato non funziona se il modulo mobile è configurato per essere visualizzato come PDF. NPR-20566

**Rights Management**

* La finestra di dialogo di selezione dei certificati di autenticazione reciproca/CAC dovrebbe visualizzare i certificati con Utilizzo chiavi avanzato (EKU) per l’accesso con autenticazione client o smart card. NPR-20708
* JEE per Forms supporta l’autenticazione reciproca PKCS#11. NPR-15001

## Bundle OSGi e pacchetti di contenuti inclusi in CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

Elenco dei bundle OSGi inclusi in AEM CFP 6.2 SP1-CFP10

[Ottieni file](assets/do-not-localize/bundle-list-cfp10.txt)

Elenco dei pacchetti di contenuti inclusi in AEM CFP 6.2 SP1-CFP10

[Ottieni file](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* La configurazione dell’interfaccia utente classica di Analytics è stata adattata per l’input segreto.
* Sono state apportate correzioni alla cache di persistenza indipendente per Contexthub.
* È possibile calcolare con esattezza le dimensioni delle risorse.
* Sono state ottimizzate le prestazioni di AEM durante la pubblicazione di risorse in Brand Portal.
* Sono state apportate correzioni al valore Resourcetype nel nodo canvas.
* È stata abilitata la funzionalità di ricerca di caratteri speciali e con distinzione tra maiuscole e minuscole per i contenuti di frammenti di documento.
* I moduli adattivi sono stati migliorati in modo da poter inviare file PDF come allegati in Safari.\
  Viene fornita una nuova versione di Dynamic Media che si collega alla nuova infrastruttura di pubblicazione di Dynamic Media per una replica più rapida e scalabile.

### Assets {#assets-10}

* AEM Assets non è in grado di estrarre riferimenti di risorse secondarie per le risorse InDesign e include collegamenti duplicati alla risorsa. NPR-19006: Hotfix per CQ-4204186
* L’opzione di ordinamento non funziona per le risorse all’interno della raccolta in Commerce. NPR-19508: Hotfix per CQ-4213622
* Se una risorsa con lo stesso nome di una risorsa pre-esistente viene spostata nella stessa posizione, il valore di cq: lastReplicationAction relativo alle risorse viene scambiato, determinando la creazione di metadati errati. NPR-19531
* Viene visualizzato un messaggio di errore quando si pubblica un numero elevato di risorse, anche se le risorse sono state pubblicate correttamente. NPR-19629: Hotfix per CQ-4219611
* Le rappresentazioni statiche sono elencate con dimensioni fisse e non riflettono le dimensioni della rappresentazione effettiva. NPR-20004
* Si riscontrano rallentamenti nell’istanza di AEM quando si pubblicano più di quattro risorse su Brand Portal. NPR-20009

### Sites {#sites-10}

* AEM visualizza un comportamento imprevisto quando un utente tenta di pubblicare/annullare la pubblicazione/creare la versione di una pagina bloccata da un altro utente. NPR-19249: Hotfix per CQ-4215298 e CQ-4203856
* Durante la promozione manuale del lancio nidificato, la pagina figlia viene eliminata. NPR-19704
* Problemi di persistenza quando ContextHub memorizza il livello di persistenza predefinito della sovrascrittura durante l’inizializzazione. NPR-19979: Hotfix per CQ-4218399
* I pulsanti di Content Fragment si sovrappongono ad altri pulsanti. NPR-19980: Hotfix per CQ-4221519
* La pagina del sito non viene visualizzata quando viene aperta utilizzando il relativo alias in SiteAdmin. NPR-20053: Hotfix per CQ-4221478
* Errore durante la pubblicazione di una pagina Live Copy che punta a una pagina di importazione in Adobe Campaigns. NPR-20066: Hotfix per CQ-4220846

### Platform {#platform-8}

* Apache POI è stato aggiornato alla versione 3.16 per supportare l’inclusione dell’immagine di sfondo delle diapositive PPT nelle rappresentazioni. NPR-18286
* Si verificano problemi di rendering con Internet Browser 11 ed Edge quando si caricano più risorse nella stessa cartella. NPR-20062

### Integrazione {#integration-11}

* Il file at.js personalizzato non viene pubblicato se vi si accede con l’utente anonimo. NPR-19542: Hotfix per CQ-4219592
* Migrazione delle credenziali esistenti di Analytics all’autenticazione WSSE. NPR-19962

### Brand Portal {#brand-portal}

* Abilitazione della pubblicazione di tag da AEM a Brand Portal dalla console tagadmin/tagging. NPR-20271

## Forms {#forms-11}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-11}

#### Gestione della corrispondenza {#correspondence-management-4}

* È stata abilitata la funzionalità di ricerca del testo effettivo nei frammenti di documento durante l’anteprima di una lettera. NPR-19712

#### Moduli adattivi {#adaptive-forms-8}

* I moduli adattivi sono stati migliorati in modo da poter inviare file PDF come allegati in Safari. Per aggiungere il supporto di questa funzionalità nei moduli esistenti, è necessario apportare la modifica di configurazione nel widget degli allegati e in “Tipi di file supportati” aggiornare il valore application/pdf anziché .pdf. NPR-19623

#### Forms Manager {#forms-manager-1}

* Se validationState non è stato definito nel campo di un modulo adattivo e si verifica l’evento elementFocusChanged, nel server di Adobe Analytics viene restituito un evento di errore (errorState). NPR-19513

### Programma di installazione Forms JEE {#forms-jee-installer-11}

#### Core {#core-3}

* Gestione connessioni non è disponibile durante l’arresto. Jboss interrompe la dipendenza JDBC prima che venga annullata l’implementazione del file EAR dell’istanza di authoring, causando problemi di file danneggiato. NPR-19703

## Feature Pack inclusi {#feature-packs-included-1}

* Sono stati apportati miglioramenti in termini di trasparenza e correzione delle miniature in Dynamic Media. NPR-15207

## Bundle OSGi e pacchetti di contenuti inclusi in CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP9

[Ottieni file](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Elenco dei bundle OSGi inclusi in AEM 6.2SP1-CFP9

[Ottieni file](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* Sono stati introdotti tag ai modelli utente personalizzati del servizio Modello e-mail Adobe.
* Sono stati apportati miglioramenti ai pulsanti dell’interfaccia utente dell’app desktop.
* Il pulsante Invia viene disattivato dopo un clic per impedire l’invio di più moduli in una pagina di traduzione.
* Sono stati configurati più componenti Editor Rich Text in una finestra di dialogo.
* Sono stati potenziati i ReferenceUpdates in Live Copy.
* È stata abilitata la funzionalità con distinzione tra maiuscole e minuscole per i contenuti di frammenti di documento.
* Nella documentazione per l’installazione di AEM Forms è stato aggiunto l’elenco delle librerie Linux.

### Assets {#assets-11}

* Problemi con l’applicazione del filtro Omnisearch alle raccolte avanzate nel browser Safari. NPR-19511
* I metadati delle parole chiave PDF non vengono estratti correttamente e vengono modificati in modo errato se a una risorsa PDF sono associate più parole chiave. Per risolvere il problema, la proprietà dei metadati del campo Oggetto è stata rimossa per le risorse PDF. Si può, tuttavia, modificare lo schema metadati per aggiungere un campo di testo con più valori al campo Oggetto. NPR-19126
* Il servizio di notifica dei flussi di lavoro non codifica i collegamenti nei messaggio e-mail, impedendone il caricamento dopo essere stati selezionati dagli utenti. NPR-19490: Hotfix per CQ-4218055
* Impossibile caricare l’elenco completo delle pagine/risorse nella vista a colonne utilizzando Chrome. NPR-19458: Hotfix per CQ-4214248
* Viene visualizzata un’icona di disattivazione errata nella casella in entrata di AEM quando si attiva il flusso di lavoro Richiedi attivazione. NPR-19365: CQ-4216174
* Problemi di ordinamento nella vista a elenco. NPR-19217: CQ-95602
* Quando si modifica il titolo o l’immagine in miniatura nelle impostazioni di Cartella risorse, il gruppo e le autorizzazioni originali della cartella vengono ignorati. NPR-19283: Hotfix per CQ-4216080
* Le workstation Windows 10 passano automaticamente alla modalità touch, disattivando alcuni pulsanti. NPR-19183

### Sites {#sites-11}

* Si verificano problemi in presenza di più componenti Editor Rich Text in una finestra di dialogo. NPR-19311: NPR-19587
* La funzionalità automatica Pulizia delle versioni funziona in Vanilla AEM 6.2 solo dopo aver inizializzato VersionManagerImpl. NPR-19315: Hotfix per CQ-4217175
* L’istanza del flusso di lavoro si blocca durante il passaggio del flusso di lavoro “Esportazione Salesforce.com”. NPR-19222: Hotfix per CQ-4212976
* Le pagine delle copie in altre lingue create da Live Copy non sono modificabili. NPR-18967
* ReferencesUpdateAction non riesce ad aggiornare i collegamenti in una Live Copy nidificata con la modifica della gerarchia. NPR-18715: Hotfix per CQ-4214105

### Platform {#platform-9}

* Il servizio Modello e-mail Adobe aggiunge tag ai modelli utente personalizzati. NPR-19190: Hotfix per CQ-4217113

### Progetti {#projects-2}

* Gli editor di progetti non possono copiare/incollare risorse nella cartella delle risorse del progetto. NPR-19619
* Impossibile generare l’anteprima per i progetti di traduzione dopo l’installazione della versione 6.2 SP1-CFP1. NPR-16481: CQ-4204655

### Integrazione {#integration-12}

* L’accesso alle proprietà per gli articoli viene impostato in modo errato nell’interfaccia classica di Adobe Digital Publishing Solution. NPR-19366
* Rendering lento delle miniature a causa di articoli a dimensione intera nella console degli articoli di AEM. NPR-19086: CQ-4217148
* Comportamento non corretto della piegatura automatica quando si personalizzano le offerte tramite Campaign se gli utenti hanno accesso a più aree. NPR-19290: Hotfix per CQ-4218029
* La finestra di dialogo Impostazione destinazione non viene visualizzata in modalità di targeting quando un modulo di destinazione viene modificato e salvato più volte. NPR-19144: Hotfix per CQ-4216708

### Flusso di lavoro {#workflow-2}

* Nell’interfaccia utente classica, gli utenti non possono filtrare le notifiche in Posta in arrivo per utente/gruppo. NPR-19122: Hotfix per CQ-4215374
* La mappa delle immagini non mantiene alcune coordinate nel componente immagine HTL. NPR-18911: CQ-4211584

## Forms {#forms-12}

* Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-12}

* Quando il contenuto viene copiato da Microsoft Word o da un browser web all’editor di testo di Gestione della corrispondenza, lo stile non viene mantenuto. NPR-19530
* I contenuti senza interruzione di riga non vanno a capo nell’editor di testo. NPR-19481
* È stata abilitata la funzionalità di ricerca del testo effettivo nei frammenti di documento durante l’anteprima di una lettera. NPR-17792: Hotfix per CQ-4214501

#### Gestione della corrispondenza {#correspondence-management-5}

>[!NOTE]
>
>Questa funzionalità di ricerca per i frammenti di testo presenta alcuni vincoli:
>
>* I contenuti di frammenti di documento fanno distinzione tra maiuscole e minuscole, ma non i titoli.
>* I risultati della ricerca non vengono evidenziati se una parte della parola ricercata è in uno stile diverso o contiene caratteri speciali come &quot; oppure &#39; oppure \.
>* La ricerca non funziona con eventuali contenuti dinamici (ad es. valori di elementi del dizionario dati o valori di variabili) all’interno del frammento di documento.

#### Forms Manager {#forms-manager-2}

* Le proprietà dello standard XML Schema nei moduli adattivi non possono essere modificate dopo aver applicato CFP6 in AEM 6.2. Hotfix per CQ-4219684
* Tutti i servizi del bundle di base di AEM Forms Manager non vengono avviati al riavvio del server. Hotfix per CQ-4217014

### Programma di installazione Forms JEE {#forms-jee-installer-12}

#### Installazione di LCM {#install-lcm-2}

* Nella schermata Amministratore di Microsoft Windows viene visualizzato il numero di versione 6.0 dopo l’installazione di CFP6. Hotfix per CQ-4217573

## Feature Pack inclusi {#feature-packs-included-2}

* Sono stati apportati miglioramenti ai pulsanti dell’interfaccia utente dell’app desktop. NPR-18676

## Pacchetti OSGi inclusi in CFP8 {#osgi-bundles-included-in-cfp}

Elenco dei bundle OSGi inclusi in AEM 6.2SP1-CFP8

[Ottieni file](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP8

[Ottieni file](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* Modifica del comportamento nella visualizzazione dei titoli nella scheda Immagine per un’immagine con la proprietà dc: title impostata su String [] (Multifield).
* Sono stati risolti alcuni problemi relativi alle prestazioni con Dynamic Media Cloud Services, all’interfaccia utente touch e all’interfaccia utente del servizio Security.
* Sono stati risolti problemi in Apache Felix Http Bridge 3.0.8
* È stata risolta la replica senza binario tra gli ambienti di creazione e di pubblicazione.
* È stato aggiunto il supporto per il file della libreria di destinazione AT.JS, una libreria di implementazione per l’integrazione lato client con Adobe Target progettata sia per le tipiche implementazioni web sia per le applicazioni a pagina singola.
* Sono state migliorate le prestazioni di AEM con l’introduzione di un periodo di timeout della connessione configurabile dall’utente per le soluzioni Experience Cloud (Analytics, DTM, Target e S&amp;P).

### Assets {#assets-12}

* Durante il test di immissione video con AEM 6.3 configurato con Cloud Services Dynamic Media, viene generata l’eccezione “Troppi file aperti”. NPR-18734: Hotfix per CQ-4211407
* L’impostazione dell’URL personalizzato per le risorse di una pagina non funziona dopo il riavvio dell’istanza AEM. NPR-18634: Hotfix per GRANITE-18085
* Nell’interfaccia utente touch, il pulsante Pubblica viene visualizzato anche per gli utenti non autorizzati a pubblicare risorse. NPR-18620: Hotfix per CQ-4214042
* L’opzione di rappresentazione dinamica non è più disponibile nella finestra di dialogo di download di una risorsa dopo l’impostazione del contratto di licenza. NPR-18607: Hotfix per CQ-4212342
* Non è possibile scaricare il rendering dinamico per le risorse il cui nome contiene spazi. NPR-18571: Hotfix per CQ-4211738
* Impossibile salvare più di un utente se si condivide la cartella di risorse con Creative Cloud. NPR-18489: Hotfix per CQ-103297
* dc: title e dc: description non vengono modificati in un valore a più campi in crx/de. NPR-18474: Hotfix per CQ-4209086
* Lo spostamento della posizione di funzionamento delle risorse provoca un deterioramento delle prestazioni. NPR-18346
* Non viene visualizzato alcun elemento nella timeline se viene aperta con set di opzioni Mostra tutto. NPR-18302: Hotfix per CQ-4211957
* Si verifica un errore quando un file di testo con codifica ASCII/UTF-8 viene caricato in AEM Assets e la generazione delle miniature non riesce. NPR-18006: CFP per CQ-4209345
* I pulsanti dell’azione Pubblica sono visibili anche se l’utente non è autorizzato alla replica. NPR-17353: Hotfix per CQ-4209269
* Sia Siteadmin che Miscadmin non funzionano se la minimizzazione è stata abilitata tramite min:gcc;obfuscate=true. NPR-18593: Hotfix per CQ-4209220
* Le voci di menu personalizzate non vengono visualizzate fino a quando non viene aggiornato lo schermo. NPR-18500: Hotfix per CQ-4213581
* Il file moment.js è stato aggiornato alla versione 2.10.6. NPR-18596: Hotfix per GRANITE-11881
* L’applicazione delle autorizzazioni per le macro DM provoca errori nella vista per l’utente amministratore. NPR-18544: Hotfix per CQ-4211729
* L’opzione Pubblica in seguito per le risorse genera l’eccezione Illegal ArgumentException. CQ-4214532

### Sites {#sites-12}

* In un cluster di authoring attivo-attivo con MongoDB, entrambe le istanze di authoring tentano di attivare la replica per lo stesso contenuto quando viene raggiunto il momento di attivazione impostato. NPR-18708: Hotfix per CQ-4210982
* Viene generata l’eccezione NPE quando si sposta una risorsa con un riferimento privo di jcr:content node. NPR-18664
* I segnaposto non sono visibili in una pagina che contiene più componenti parsys. NPR-18645: Hotfix per CQ-110253
* Problemi di concorrenza in AbstractCopyMoveCommand. NPR-18591
* Quando si copia il testo in un componente parsys da un’altra istanza AEM, il componente parsys viene creato senza l’opzione resourceType impostata. NPR-18511: Hotfix per CQ-4212306

### Platform {#platform-10}

* Il programma di installazione di JCR non aggiorna la versione del bundle dopo l’installazione del pacchetto. NPR-18728: Hotfix per NPR-15135
* La replica senza dati binari (BLR) ha esito negativo con dati binari tra gli ambienti di authoring e pubblicazione. NPR-18704
* Richiesta di risoluzione di Apache Felix Http Bridge nell’ambiente AEM. NPR-18297
* La replica ha esito negativo quando più pagine con una struttura simile vengono replicate contemporaneamente tramite Sling Content Distribution. NPR-18665: Hotfix per GRANITE-13712
* I pacchetti Sling Distribution creati non dispongono della funzione di pulizia automatica. NPR-18601: Hotfix per GRANITE-16183

### Integrazione {#integration-13}

* La visualizzazione delle offerte pubblicate dalle cartelle della libreria genera un’eccezione NPE. NPR-18732: Hotfix per CQ-4214593
* La data di inizio/fine di un’attività non viene aggiornata in JCR e Target se viene modificata da una data specifica a Quando viene attivato/disattivato. NPR-18612: Hotfix per CQ-104831
* Nell’integrazione di Analytics con AEM non è impostato alcun timeout del socket o di connessione per le connessioni httpclient. NPR-18497
* Nell’integrazione di DTM con AEM non è impostato alcun timeout del socket o di connessione per le connessioni httpclient. NPR-18495
* L’integrazione di Target con AEM non fa riferimento ad alcun timeout del socket o di connessione impostato per le connessioni httpclient. NPR-18494
* Nell’integrazione di Search &amp; Promote con AEM non è impostato alcun timeout del socket o di connessione per le connessioni httpclient. NPR-18493
* L’attività di Target viene disattivata dopo l’aggiunta di un’esperienza aggiuntiva. NPR-18227: Hotfix per CQ-4201895

### WCM - Componenti Foundation {#wcm-foundation-components-7}

* Le mappe delle immagini non mantengono alcune coordinate nel componente immagine HTL. NPR-18530: Hotfix per CQ-4211584

### Traduzione {#translation-5}

* I risultati della ricerca della traduzione non includono i nomi dei progetti di traduzione. NPR-18224: Hotfix per CQ-4210658

### Brand Portal {#brand-portal-1}

* Abilitazione della pubblicazione di tag da AEM a Brand Portal dalla console tagadmin/tagging. CQ-4212165

## Forms {#forms-13}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-13}

#### Gestione della corrispondenza {#correspondence-management-6}

* I dati corretti non vengono visualizzati nel pannello di modifica finché il frammento non viene salvato. NPR-19092
* L’aggiunta di un frammento di documento a una lettera richiede molto tempo. NPR-18958
* Se esiste una dichiarazione XML in un file XML dati e il rendering della lettera viene avviato tramite una richiesta POST, nella lettera corrispondente i dati non vengono visualizzati. NPR-18870
* Non vengono generati registri di controllo per le azioni eseguite su risorse CM. NPR-16618

>[!NOTE]
>
>È opportuno non installare questo pacchetto CFP aggiuntivo se sono stati riscontrati i due problemi seguenti:
>
>* L’opzione Copia/Incolla da Word o dal web nell’editor di testo CM mostra i contenuti con interruzioni di riga. NPR-19530
>* I contenuti senza interruzioni di riga non vanno a capo nell’editor di testo CM. NPR-19449
>
>Questi problemi saranno affrontati nei pacchetti CFP futuri.

#### Moduli adattivi {#adaptive-forms-9}

* Quando si aggiunge un nuovo pannello nell’ambito dei pannelli ripetibili, il valore del campo a discesa del pannello precedente viene eliminato. NPR-18772
* I campi dei moduli adattivi contrassegnati per accettare solo numeri interi accettano anche alcuni caratteri speciali immessi dal tastierino numerico. NPR-18680
* Lo script per modificare il titolo del pulsante nel momento in cui viene inizializzato l’evento del pannello Guideroot non funziona. NPR-18476
* La barra di scorrimento non viene visualizzata nel pannello a destra per le regole create nell’editor di regole. NPR-18716

#### App AEM Forms {#aem-forms-app}

* Forms non esegue correttamente il rendering nell’app AEM Forms quando è in modalità offline o non è connesso alla rete. CQ-4218368

### Programma di installazione Forms JEE  {#forms-jee-installer-13}

#### Servizio PDFG {#pdfg-service-3}

* PDF Generator non riesce a produrre documenti PDF con livelli di segnalibri specifici. Hotfix per CQ-4211102

## Pacchetti OSGi inclusi in CFP7 {#osgi-bundles-included-in-cfp-1}

Elenco dei bundle OSGi inclusi in AEM 6.2SP1-CFP7

[Ottieni file](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP7

[Ottieni file](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* Gestione efficiente dei componenti nascosti in modalità layout nei dispositivi tablet.
* Introduzione delle azioni rapide nei dispositivi ibridi.
* Risoluzione dei problemi di sincronizzazione a livello di componente con le Live Copy.

### Assets {#assets-13}

* Il cliente viene bloccato quando l’utente che non dispone dell’autorizzazione richiesta tenta di eseguire l’operazione Sposta su una risorsa. NPR-18330: Hotfix per CQ-4212560
* L’unione di più configurazioni Smart Content Service causa problemi di usabilità. NPR-18273: Hotfix per CQ-4201557
* I flussi di lavoro e le azioni di checkout non sono più disponibili dalla console Timeline quando alla cartella Assets sono stati aggiunti circa 80 frammenti. NPR-18257: Hotfix per CQ-4211214 e NPR-18251; Hotfix per CQ-4211216.
* Il sistema si arresta per memoria insufficiente o mancata paginazione durante la generazione dei rapporti sulle risorse. NPR-17865: Hotfix per CQ-4209759
* Il video pubblicato non viene riprodotto correttamente sulla risorsa video codificata. NPR-17849: Hotfix per CQ-4210739
* Non viene generata la miniatura per PDF. NPR-17831, NPR-17750: Hotfix per CQ-4210547
* Le risorse scadute non vengono disattivate dal processo di notifica delle scadenze di Adobe CQ DAM. NPR-17666: Hotfix per CQ-107766
* Le attività di scadenza delle risorse si fermano se a una risorsa non è assegnato un proprietario. NPR-17665: Hotfix per CQ-4197946
* Quando si sposta una cartella di risorse con più di 150 riferimenti in entrata, viene generata un’eccezione Null Pointer. CQ-4200981

### Sites {#sites-13}

* Se la regola di segmentazione è impostata per un intervallo di indirizzi IP, la personalizzazione funziona solo per il primo IP. NPR-18121: Hotfix per CQ-83767
* L’accesso non riesce perché viene generata l’eccezione NumberFormatException quando la proprietà historyShow è abilitata. NPR-18073: Hotfix per CQ-101965
* Le pagine eliminate contrassegnate sono visibili nell’interfaccia utente touch. NPR-18025: Hotfix per CQ-86694
* Problemi di prestazioni durante il caricamento di una pagina destinata a un numero elevato di utenti (oltre 2000). NPR-17884: Hotfix per CQ-4209567
* Non è possibile selezionare un’immagine dopo aver rimosso un’altra immagine nella pagina. NPR-17711: Hotfix per CQ-4201323

### Platform {#platform-11}

* I controlli dell’interfaccia touch non risultano nascosti per gli utenti che non dispongono delle autorizzazioni necessarie. NPR-17945: Hotfix per CQ-4211231
* Mancano i tag giapponesi nel campo TagPicker. NPR-17768: Hotfix per CQ-4210456
* La query getsize() restituisce risultati non corretti se è abilitato FastQuerySize. NPR-18018
* La console web nell’istanza in standby non è accessibile. NPR-17861: Hotfix per GRANITE-14582

### Commerce {#commerce-2}

* Si verifica un attraversamento delle query se nel blueprint del catalogo non è stata definita alcuna condizione per una sezione. NPR-18229: Hotfix per CQ-4211924

### Communities {#communities-2}

* PollingImporterImpl. ritarda l’arresto di AEM. NPR-18298: Hotfix per CQ-96133

### Integrazioni {#integrations}

* Risoluzione di errori del componente AEM - Ricerca che possono verificarsi quando OSGi AEM Day HTTP Client 3.1 è configurato con un proxy che richiede l’autenticazione digest. NPR 18128
* Manca la casella di controllo per ripristinare l’ereditarietà. NPR-17753; Richiesta hotfix per CQ-4210139
* Gli utenti non riescono a impostare la priorità quando eseguono il targeting di un componente con più attività. NPR-18658: Hotfix per CQ-4210727
* Gli utenti non riescono a esplorare la cartella /etc/segmentation per selezionare un pubblico creato nella cartella /etc/segmentation/group1. NPR-18522

### Sicurezza {#security-1}

* La procedura guidata Sposta risorsa si blocca se l’utente non dispone dell’autorizzazione di scrittura per la cartella di destinazione. NPR-18300
* Richiesta di utilizzare una versione aggiornata di org.apache.sling.servlets.post servlet (2.3.22) nell’API Sling Apache per evitare una vulnerabilità ad attacchi XSS (Cross-Site Scripting). NPR-18963

### Traduzione {#translation-6}

* Non è possibile inviare una pagina di risorsa a un progetto di traduzione finché il progetto non viene completato. NPR-18249: Hotfix per CQ-4209908

### WCM - Componenti Foundation {#wcm-foundation-components-8}

* Non è possibile utilizzare il componente parsys di WCM Foundation nei modelli modificabili. NPR-18223: Hotfix per CQ-4210384
* La mappa delle immagini non mantiene alcune coordinate nel componente immagine HTL. NPR-18032: Hotfix per CQ-4211584
* Quando viene eseguito il rendering di un componente immagine HTL, il nome file nell’URL viene modificato e l’URL non funziona più. NPR-17908: Hotfix per CQ-4211587
* Non è possibile uscire da Proprietà pagina dopo aver apportato modifiche. NPR-17832: Hotfix per CQ-96110

## Forms {#forms-14}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-14}

**Gestione della corrispondenza**

* Il dizionario dati viene letto ripetutamente durante il rendering delle lettere. NPR-18482: Hotfix per CQ-4210805
* Aggiunta di JavaDocs per la classe com.adobe.livecycle.content. NPR-18467
* Quando si crea una lettera, la descrizione della lettera non viene salvata. NPR-18039
* Quando un modulo di testo viene salvato e un’espressione nel modulo di testo non contiene tag di apertura o chiusura, non viene visualizzato alcun messaggio di errore. Il modulo di testo visualizza un messaggio di errore e non riesce a eseguire il rendering nella lettera. NPR-17798
* Nei registri vengono visualizzati errori imprevisti durante l’installazione del pacchetto aggiuntivo. NPR-18295

**Forms Manager**

* Nell’interfaccia utente di AEM Forms tutte le risorse sono elencate a partire da quelle meno recenti. Gli utenti non possono riordinare le risorse in modo da visualizzare per prime quelle più recenti. NPR-18451

### Programma di installazione Forms JEE  {#forms-jee-installer-14}

**Servizio di output**

* Sono state migliorate le prestazioni del servizio di output per AEM Forms 6.2. NPR-18033

**Servizio Signatures**

* Non è possibile firmare un documento PDF con il modulo di protezione hardware remoto. NPR-18017

## Pacchetti OSGi inclusi in CFP6 {#osgi-bundles-included-in-cfp-2}

Elenco dei bundle OSGi inclusi in AEM 6.2SP1-CFP6

[Ottieni file](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP6

[Ottieni file](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* Sono stati risolti diversi problemi di interfaccia utente relativi alla condivisione, allo spostamento, alla pubblicazione e al download delle risorse.
* È stata aumentata la capacità della finestra di dialogo Sposta in termini di visualizzazione delle risorse di riferimento.
* Sono stati risolti vari problemi relativi ai componenti e ai flussi di lavoro di WCM, ad esempio le opzioni Annulla pubblicazione e Pulizia delle versioni.
* È stata migliorata la reattività della barra delle azioni rispetto alla visualizzazione delle azioni presenti nella barra degli strumenti e dei componenti di Coral.

### Assets {#assets-14}

* Sono state migliorate le prestazioni della funzionalità di pubblicazione su Brand Portal. NPR-17189: Hotfix per CQ-4204150
* La condivisione di una risorsa tramite Condividi collegamento non crea un file ZIP con una struttura di cartelle piatta per il download. NPR-17513: Hotfix per CQ-4209381
* Se si seleziona una risorsa in DAM e si fa clic su Pubblica, nella pagina dei dettagli della risorsa non viene visualizzata l’opzione Pubblica su Brand Portal. NPR-17351: Hotfix per CQ-94905
* Nei passaggi del flusso di lavoro DAM, i flussi binari acquisiti da Session o ResourceResolver devono essere chiusi in un blocco finale per garantire che non si verifichino perdite di risorse. NPR-17385: Hotfix per CQ-4209452
* Il caricamento di un documento Word in DAM genera un’eccezione NPE e l’istanza del flusso di lavoro rimane bloccata nello stato In esecuzione. NPR-17160: Hotfix per CQ-4207358
* Nella pagina dell’editor dei metadati, i pulsanti Condividi, Sposta, Pubblica e Scarica rimangono visibili per le risorse scadute anche per gli utenti non amministratori. NPR-16903: Hotfix per CQ-101440/CQ-104535
* Azioni quali Condividi, Sposta, Pubblica e Copia devono essere visibili per gli utenti amministrativi nella console di Assets. NPR-16902: Hotfix per CQ-4207111

### Sites {#sites-14}

* Quando si sposta una pagina dall’interfaccia utente classica o touch, nella finestra di dialogo Sposta vengono visualizzati solo i primi 150 riferimenti; pertanto non è possibile aggiornare gli altri riferimenti e ripubblicare la pagina. Questo problema è stato risolto introducendo una proprietà per l’interfaccia classica: maxRefNo, che può essere configurata nel nodo siteadmin: /libs/wcm/core/content/siteadmin. Questa proprietà specifica il numero massimo di riferimenti (valore predefinito: 150) visualizzati prima di un’operazione di spostamento massiccia. Se una pagina contiene un maggior numero di riferimenti, questi non vengono visualizzati nella finestra di dialogo movePage. Questa configurazione può essere utilizzata anche per damadmin e miscadmin applicando la configurazione, rispettivamente, sui nodi: `'/libs/wcm/core/content/damadmin'` e `'/libs/wcm/core/content/miscadmin'`. NPR-17222: Hotfix per CQ-85878

* Quando si eseguono operazioni sui componenti WCM, dall’Editor Rich Text dell’interfaccia touch vengono rimossi i collegamenti ipertestuali contenenti spazi. NPR-17698, NPR-17570: Hotfix per CQ-4206768
* Quando si attiva il flusso di lavoro Request for Unpublication dalle proprietà della pagina, per gli utenti senza diritti di replica vengono visualizzati errori JavaScript. NPR-17294: Hotfix per CQ-102064
* Il rendering o l’esportazione di un componente immagine HTL modifica l’URL in un numero, cambiando il nome del file, e i collegamenti non funzionano più. NPR-17245: Hotfix per CQ-59616
* Se si elimina un lancio in un lancio nidificato, i lanci secondari diventano orfani. NPR-17228: Hotfix per CQ-4202639
* Quando si esegue Pulizia delle versioni in AEM 6.2 con Oak 1.4.13 applicato, viene aggiunto un avviso ripetuto nei registri. NPR-17391: Hotfix per CQ-4206870
* Dopo aver installato un hotfix o un aggiornamento per il componente ContextHub, il pacchetto di contenuto sovrascrive tutti i segmenti in /etc/segmentation/contexthub, determinando la perdita di tutti i segmenti ContextHub personalizzati. NPR-17250: Hotfix per CQ-79958
* Quando si esegue un flusso di lavoro e gli utenti del flusso di lavoro sono gruppi nidificati, WorkflowStatusProvider (pageinfo.json) blocca l’istanza del flusso di lavoro. NPR-17555: Hotfix per CQ-4202056
* Quando si utilizzano i componenti dell’editor WCM-Page, rimane un’enorme quantità di spazio vuoto alla fine della pagina nella modalità di modifica dell’interfaccia touch dell’istanza di authoring. NPR-17510: Hotfix per CQ-4205441
* Il rendering o l’esportazione di un componente immagine HTL modifica l’URL in un numero e i collegamenti non funzionano più. NPR-17245: Hotfix per CQ-59616

### Interfaccia {#ui}

* Se si seleziona una risorsa e si fa clic su Strumenti sviluppatore, in presenza di connessioni lente le azioni della barra degli strumenti non vengono sempre visualizzate e la pagina deve essere ricaricata. NPR-17568: Hotfix per CQ-108365
* La barra delle azioni deve essere aggiornata in modo da usare due contenitori: coral-actionbar-primary e coral-actionbar-secondary, anziché coral-actionbar-container. NPR-17591: Hotfix per GRANITE-15225

### Mobile-on-demand {#mobile-on-demand-2}

* Gli utenti con autorizzazioni di sola lettura per l’app AEM Mobile non possono visualizzare l’anteprima dei contenuti dalla pagina di gestione dei contenuti di AEM Mobile. NPR-17390: Hotfix per CQ-4209690

### Sicurezza {#security-2}

* Vulnerabilità ad attacchi XSS (Cross-Site Scripting) nell’output generato da HTMLRendererServlet. NPR-17136
* Richiesta di impedire la divulgazione della versione di AEM nella pagina dei feed RSS di AEM Web. NPR-16219

### Forms {#forms-15}

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-15}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

**Moduli adattivi**

* Per un modulo adattivo con allegato, le voci duplicate per i tag afSubmissionInfo vengono create nel codice XML inviato nel momento in cui il modulo viene inviato per la seconda volta. NPR-17364
* Se si utilizza il browser Google Chrome, dopo aver rimosso un allegato da un modulo, il tentativo di ricollegare lo stesso allegato genera un errore. NPR-17297
* Se in moduli adattivi basati su XSD o su modelli senza modulo sono presenti pannelli con caricamento lazy nidificati e ripetibili, i valori inseriti nel modulo non vengono mantenuti nel documento del record (DOR, Document of Record). NPR-17176
* Gli errori visualizzati nel registro errori per l’editor di regole devono essere aggiunti nel blocco Catch nel codice JavaScript per un blocco Try/Catch. NPR-16757
* Se si fa clic su un file allegato in un modulo, si verifica un errore nella console del browser e l’anteprima dell’allegato non viene visualizzata. NPR-17174

**Gestione della corrispondenza**

* L’opzione Crea corrispondenza dell’interfaccia utente non funziona più se nell’interfaccia viene aggiunto testo in linea o una riga vuota. NPR-17748
* Nel browser si produce un effetto sfarfallio quando si apre una lettera per la modifica. NPR-17576
* Durante l’aggiunta di funzioni remote in elementi calcolati del dizionario dati, se il numero di funzioni è superiore alla lunghezza della scheda con le funzioni remote, la barra di scorrimento non viene visualizzata nella scheda. NPR-17359
* Il metodo API “import com.adobe.icc.services.api.LetterInstanceService” non funziona. NPR-17922, NPR-16008
* Una variabile aggiunta in un modulo di testo non è visibile nel pannello Associazione dati durante la modifica di una lettera. NPR-17940
* L’interfaccia utente di gestione della corrispondenza non viene avviata se l’azione di invio HTML utilizza il metodo POST. NPR-17595

**Forms Manager**

* Con un modulo adattivo configurato per il test A/B, facendo clic su Avvia test A/B, il test non viene avviato e viene generato un errore nella console del browser. NPR-17838

**Servizio Forms**

* Sono stati risolti i problemi segnalati nell’analisi del codice statico dei moduli OSGI. NPR-13951

#### Programma di installazione Forms JEE {#forms-jee-installer-15}

**Servizio di output**

* L’utilizzo del servizio di output di AEM Forms 6.2 per combinare un modulo specifico con un XML dati richiede un tempo fino a 20 volte maggiore rispetto al tempo impiegato dal server LiveCycle ES4 SP1 per eseguire la stessa operazione. È fisso negli ambienti Windows e Linux. NPR-17501

**Installazione di LCM**

* Dopo aver installato la build AEM Forms 6.2 GM e aver applicato AEM 6.2 CFP, in LiveCycle Configuration Manager viene visualizzato un punto e virgola indesiderato nelle Informazioni sulla versione e la data di installazione della patch non viene aggiornata. NPR-14322

**Gestione processi**

* La variabile TaskContext non viene compilata per i processi AEM Forms. CQ-4211857

#### Pacchetto dei bundle di JEE per AEM Forms {#aem-forms-jee-bundles-package}

* Che si utilizzi la console dell’interfaccia utente di amministrazione di JEE o la console OSGi, le funzionalità degli utenti di Forms devono essere le stesse. NPR-17670

### Pacchetti di funzioni inclusi in CFP5 {#feature-packs-included-in-cfp}

**Pacchetto Forms JEE**

Gestione dei processi - Area di lavoro HTML

* Durante l’assegnazione di un passaggio dell’area di lavoro, nella scheda degli allegati dell’area di lavoro deve essere visualizzato un contatore per gli allegati o le note, qualora siano presenti più allegati o note. NPR-17771
* Richiesta di supporto per Office 365 in AEM JEE Forms per le funzionalità e-mail nel flusso di lavoro di Forms. NPR-13866

**Pacchetto di componenti aggiuntivi per Forms**

Gestione della corrispondenza

* Durante la modifica di frammenti nell’editor di testo con l’anteprima di una lettera, deve essere visualizzato il testo elaborato per la modifica anziché le condizioni in linea utilizzate nei frammenti. NPR-15748, NPR-17504

### Pacchetti OSGi inclusi in CFP5 {#osgi-bundles-included-in-cfp-3}

Elenco dei bundle OSGi inclusi in AEM 6.2SP1-CFP5

[Ottieni file](assets/do-not-localize/cfp5_osgi_bundles.txt)

Elenco dei pacchetti di contenuti aggiornati in AEM 6.2SP1-CFP5

[Ottieni file](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 è un aggiornamento importante che include correzioni di problemi fondamentali per il cliente, introdotte successivamente alla data di disponibilità generale di AEM 6.2 SP1.

Gli elementi di rilievo di questo Cumulative Fix Pack sono:

* Correzioni alle risorse per la rappresentazione, la visualizzazione della timeline e l’orientamento delle immagini per file Camera Raw
* Miglioramenti in:

   * WCM Launches per Sites
   * Flusso di lavoro Projects
   * Componenti di ContextHub

* Correzioni per Campaign, Mobile on-demand e Translation
* Miglioramenti a livello di semplicità di utilizzo dell’editor di regole per moduli adattivi
* Editor delle condizioni in linea ottimizzato per la gestione della corrispondenza in Forms
* Correzioni ai servizi di output e di gestione dei processi per AEM Forms su JEE
* Correzione relativa a Forms Designer per l’editor di script

### Platform {#platform-12}

* Il modulo di ricerca Search&amp;Promote ignora l’impostazione `environment` quando è configurato il servizio cloud, impedendone l’utilizzo nell’istanza di authoring. NPR-16594: Hotfix per CQ-4206076
* L’aggiunta o la personalizzazione di colonne ai risultati di **Assets OmniSearch** tramite la sovrapposizione in /apps non funziona. NPR-16737: Hotfix per CQ-4206785
* La pagina dello **strumento di diagnosi** non funziona dopo un aggiornamento sul posto da AEM 6.1 SP2 a AEM 6.2 SP1. NPR-17121: Hotfix per CQ-4196786
* HTL: Quando si seleziona un forum e si crea un argomento e un post, `Sightly SightlyCompiledScript` aggiunge la proprietà `addSelectors` errata a `RequestDispatcherOption`. NPR-17008: Hotfix per GRANITE-16384

* È stato aggiunto il supporto per `CRON expressions` in `ManagedPollConfigs` utilizzato da `ReportImporter`. NPR-16608; Richiesta hotfix per CQ-4206066

* Il caricamento di un’immagine avatar per un utente LDAP ha esito negativo. NPR-16561: Hotfix per GRANITE-17013
* Il numero di risultati visualizzati nella schermata User Management è diverso tra la vista a schede e quella a elenco. NPR-16241: Hotfix per GRANITE-16914
* Il caricamento lazy delle notifiche del flusso di lavoro ha esito negativo durante la visualizzazione nel browser Google Chrome in modalità Schermo intero. NPR-17013: Hotfix per CQ-4207567

### Assets {#assets-15}

* L’orientamento dell’immagine non viene applicato correttamente durante l’importazione di un’immagine con un orientamento definito. NPR-16750: Hotfix per CQ-4204356
* Nella vista Timeline risorse non è presente nessuna risorsa anche se l’opzione Mostra tutto è attiva per impostazione predefinita. NPR-16957: Hotfix per CQ-98780
* I file Camera Raw (inclusi ARW, CR2, NEF, DNG ed EPS) non possono essere selezionati o eliminati quando vengono aggiunti come rappresentazioni nelle risorse. Vengono scaricati automaticamente quando l’utente li seleziona. NPR-16949: Hotfix per CQ-4206846
* Se si crea un file PDF in un altro PDF nell’interfaccia utente di Assets, i file PDF creati nell’interfaccia utente di DAM non vengono visualizzati, anche se sono visibili nell’archivio crx. NPR-16833: Hotfix per CQ-4206501
* Nell’interfaccia touch, il caricamento di una risorsa come nodo figlio diretto di se stesso causa un problema. La risorsa viene caricata come elemento figlio diretto della risorsa selezionata in precedenza. NPR-16534: Hotfix per CQ-4204287
* Nell’interfaccia utente di DAM, l’inserimento di un commento in una risorsa e l’applicazione di un tag a un utente nel commento non generano una notifica e-mail. NPR-16589: Hotfix per CQ-102318

### Progetti {#projects-3}

La console del flusso di lavoro Progetti mostra un’eccezione NullPointerException nella pagina quando viene eliminato un flusso di lavoro. NPR-17017: Hotfix per CQ-4194269

### Sites {#sites-15}

* I file in `ContextHub` non vengono ridotti a icona nell’istanza di authoring. NPR-17022: Hotfix per CQ-79456
* La promozione di lancio WCM-Launches richiede molto tempo poiché prevede la promozione di un lancio costituito da una grande struttura ad albero di una pagina. NPR-16480: Hotfix per CQ-82731
* Il modulo di rendering della condizione di segmento `ClientContext` si blocca quando si crea un segmento (o un pubblico) con una regola non funzionante o non completata. NPR-16759: Hotfix per CQ-4205104
* In WCM Launches, non viene annullata la pubblicazione delle pagine associate a un lancio se l’azione viene avviata dalle proprietà della pagina nell’interfaccia utente touch. NPR-16560: Hotfix per CQ-4204681
* La funzione Riscrittura collegamenti riscrive erroneamente i valori href contenenti due punti, presumendo che i due punti (:) definiscano un namespace JCR. NPR-16753: Hotfix per CQ-4203762
* In WCM-Design Importer, se si apre una pagina di importazione di test e si tenta di caricare un file ZIP, si verificano dei problemi se il file è già stato caricato ed eliminato in precedenza. NPR-16486: Hotfix per CQ-90962
* L’esperienza di accesso al pannello **[!UICONTROL Navigazione globale]** cambia a seconda che si utilizzi il browser Firefox, Safari o Google Chrome. Il browser Firefox visualizza il menu **[!UICONTROL Strumenti]**, mentre Google Chrome mostra il menu **[!UICONTROL Navigazione]**. NPR-16770: Hotfix per CQ-4200456

### Campaign {#campaign}

* Mentre si esegue il test dei modelli di AEM Campaign e si modificano gli indirizzi iniziali per includere dati aggiuntivi, l’elenco a discesa di Adobe Campaign scompare nel componente ContextHub dell’interfaccia utente touch. NPR-16771: Hotfix per CQ-105748

### Mobile On-Demand {#mobile-on-demand-3}

* Quando si esegue la verifica preliminare di una pubblicazione dall’ambiente di authoring AEM, se un’azione di verifica preliminare dura più di 5 secondi, si genera un picco insolito nel dashboard dell’integrazione AEMM - AEM PECS Splunk, con un numero elevato di richieste di stato al secondo. NPR-16908: Hotfix per CQ-4207055
* L’attività di gestione della configurazione di AEM Mobile ha esito negativo dopo l’installazione dell’aggiornamento AEM-6.2-SP1-CFP1-1.0. NPR-16909: Hotfix per CQ-4204892

### Traduzione {#translation-7}

* L’anteprima dei processi di traduzione non funziona dopo l’installazione di 6.2 SP1 - CFP1. NPR-16481: Hotfix per CQ-4204655
* La copia in lingua creata con lo strumento di traduzione punta alla cartella principale anziché alla Live Copy locale. NPR-17257: Hotfix per CQ-4208287

### Sicurezza {#security-3}

* Non viene eseguita alcuna convalida del tipo MIME quando in AEM vengono caricati file binari. NPR-16617
* Problemi relativi al caricamento di immagini avatar per gli utenti LDAP. NPR-16561

### Forms {#forms-16}

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-16}

**Moduli adattivi**

* Nell’editor dei moduli adattivi, il commento di impostazione della destinazione in head.jsp deve essere sostituito con la nuova istruzione ContextHub. NPR-17173
* Nell’editor di regole per moduli adattivi, in **[!UICONTROL Scegli un elemento]** l’evento viene visualizzato come “null”. NPR-17139
* Il modulo inviato viene nuovamente inviato quando si procede al passaggio successivo con la freccia in avanti (>). NPR-17080
* Durante l’invio di un modulo adattivo tramite AJAX, la funzione di callback “error” non viene mai richiamata in caso di errore. NPR-17034
* Se si fa clic sul pulsante **[!UICONTROL Salva modulo]** nell’editor di regole in fase di esecuzione, il modulo non viene salvato. NPR-16905
* Il testo statico deve essere escluso dall’ordine di tabulazione nel modulo adattivo. NPR-16749
* Il valore calcolato di un campo decimale non viene visualizzato correttamente. NPR-16596
* Nei moduli adattivi, l’icona per la visualizzazione del contenuto della Guida deve essere inclusa nell’ordine di tabulazione. NPR-16484
* Supporto per l’uso di espressioni regolari di tipo `dataRef=C:/Users/` nella **[!UICONTROL Configurazione predefinita servizio di compilazione]** per la precompilazione dei dati nei moduli adattivi. NPR-16425

* Le convalide non vengono attivate correttamente per tutti i pannelli in presenza di uno scenario di caricamento lazy nidificato. NPR-15821

**Gestione della corrispondenza**

* La rappresentazione di una lettera ha esito negativo se la lettera contiene un modulo di testo vuoto (senza testo). NPR-17054
* Le interruzioni di riga e gli spazi di tabulazione vengono rimossi dal contenuto dopo essere stati incollati nell’editor di testo. NPR-17039
* La visualizzazione dei riferimenti di un modulo di testo richiede molto tempo se al modulo di testo si fa riferimento in più lettere. NPR-17035
* Per modificare, salvare, eliminare e impostare riferimenti nei frammenti di documento è necessario molto tempo. NPR-17033
* Il testo giustificato viene visualizzato in un font diverso nell’anteprima della lettera. NPR-16976
* La funzionalità di ricerca non funziona correttamente se al testo cercato corrispondono più occorrenze. NPR-16920
* La barra degli strumenti dell’editor di testo viene visualizzata nel browser in modo intermittente. NPR-16919
* Il costrutto **[!UICONTROL Salva modulo]** dall’editor di regole non funziona. NPR-16905
* Nell’elenco a discesa Font non è disponibile la famiglia dei font quando si crea un modulo di testo basato sul dizionario dati tramite Internet Explorer. NPR-16944
* Dopo la creazione di un frammento di testo, il font della lettera cambia quando si visualizza l’anteprima della lettera. NPR-16830
* Non è possibile eseguire il rendering o l’anteprima di lettere contenenti spazi di tabulazione all’inizio o tra le espressioni del frammento di documento. NPR-16769

**Forms Mobile**

* Nell’anteprima di Forms Mobile è visibile contenuto sovrapposto, anche se il modulo viene visualizzato correttamente per il rendering PDF. NPR-17105

**Portale Forms**

* Se si fa clic sul collegamento **[!UICONTROL Scarica]** per un modulo inviato, si apre una pagina HTML anziché un modulo PDF. NPR-17082

* `Upload Comments` per i file allegati non viene visualizzato nell’interfaccia utente per le istanze inviate, anche se è presente nel file XML memorizzato nell’archivio crx. NPR-17075

**Servizio estensioni Reader**

* Un file specifico non è un PDF esteso di Reader nell’installazione OSGI di AEM Forms. NPR-16625

#### Programma di installazione Forms JEE  {#forms-jee-installer-16}

**Core**

* Durante il processo di aggiornamento, Configuration Manager ha esito negativo con errore di timeout. NPR-16774 (vedere [Configurazione del timeout per le operazioni a livello di componente](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Gestione dei processi - Area di lavoro HTML**

* Il punto di inizio di un’attività di avvio non inizia con i dati inviati al momento dell’invio del punto di inizio. NPR-16917
* Quando si fa clic sul pulsante **[!UICONTROL Torna indietro]** per un modulo nell’area di lavoro HTML, il modulo non viene chiuso ma viene reinoltrato nella rispettiva coda di gruppo.\
  NPR-16352

**Gestione processi**

* Consentire agli utenti di impostare il nome visualizzato delle attività precedenti su una qualsiasi delle attività successive di un’istanza di processo. NPR-15382

**Servizio di output**

* Il servizio di output non è in grado di elaborare un PDF modificato in modo da includere un campo “milli-sec” aggiuntivo nei metadati `date-time format`. NPR-16838

#### Forms Designer {#forms-designer}

* L’editor di script di AEM Designer non rispetta le impostazioni predefinite di Proprietà modulo per `Calculate Event` e `Validate Event`. NPR-15921

### Pacchetti di funzioni inclusi in CFP4 {#feature-packs-included-in-cfp-1}

**Pacchetto di componenti aggiuntivi per Forms**

* Ottimizzazione dell’editor delle condizioni in linea per la gestione della corrispondenza. NPR-10981

### Pacchetti OSGi inclusi in CFP4 {#osgi-bundles-included-in-cfp-4}

Elenco dei bundle OSGi aggiornati tra AEM 6.2 SP1 e CFP4

Gli elementi di rilievo di CFP3 sono:

* È stata migliorata l’efficienza della ricerca nell’interfaccia classica e nel componente AEM Search tramite proxy con autenticazione digest.
* Sono stati corretti alcuni problemi che si verificavano durante il caricamento delle risorse e la visualizzazione dei metadati delle risorse.
* Sono stati corretti alcuni problemi che si verificavano durante la creazione di cartelle e lo spostamento di pagine il cui titolo conteneva dei caratteri speciali.
* Sono state apportate correzioni inerenti all’utilizzo di tipi di pubblico per la sincronizzazione delle destinazioni, la pubblicazione di campagne e la selezione della metrica Obiettivo nell’interfaccia utente touch.
* Sono stati risolti alcuni problemi di sincronizzazione per i processi di traduzione.
* È stata potenziata la sicurezza del servizio di precompilazione di Forms.
* Sono stati apportati miglioramenti al componente per bozze e invi del portale Forms e nel servizio BFS ( Barcoded Forms Service)
* È stato semplificato l’utilizzo dei moduli adattivi contenenti widget di allegati o frammenti con caricamento lazy.
* È stato semplificato l’utilizzo dello strumento Gestione della corrispondenza, con funzionalità di ricerca avanzate, registro delle risorse eliminate e importazione di dizionari dati.

### Platform {#platform-13}

* Una condizione race in **ModelAdapterFactory**, che può verificarsi quando due thread tentano di inserire lo stesso campo, impedisce la costruzione del modello. NPR-16443: Hotfix per Sling-6584
* Opzione di convalida in Gestione pacchetti per rilevare eventuali conflitti tra il file sovrapposto (file JSP o JavaScript) in /apps e quello contenuto in un Hotfix nella cartella /libs. La sovrapposizione interessata può essere ridotta in modo da includere le modifiche provenienti dal file presente in /libs. NPR-16216: Hotfix per CQ-81729
* In alcuni casi, la registrazione in error.log si blocca alcuni secondi dopo aver avviato lo strumento di pubblicazione e deve essere annullata per essere nuovamente eseguita. È necessario aggiornare il framework di registrazione e fornire Sling Logging. NPR-15913: Hotfix per GRANITE-15452
* Richiesta di aggiornamento dell’API JavaScript `use"` per evitare errori nell’implementazione dell’API HTL JavaScript Use. NPR-16461: Hotfix per Sling-6780

### Sites {#sites-16}

* Dopo l’aggiornamento da AEM 6.0 a AEM 6.2, l’interfaccia utente classica presenta un rallentamento delle prestazioni durante la ricerca dei tag a causa dell’elevato numero di query. Per risolvere il problema, è possibile seguire la procedura descritta in [Disattivazione dello stato di replica nella console di assegnazione tag (interfaccia classica)](#disable-replication-status-in-tagging-console-classic-ui-npr). NPR-15842: Hotfix per CQ-4201748.

* Durante la creazione di una pagina nell’interfaccia utente touch, la verifica dell’input per il campo “name” non verifica il carattere speciale apostrofo (come nell’interfaccia classica). Non è quindi possibile spostare la pagina. NPR-16404: Hotfix per CQ-4205321.
* Se si applicano stili diversi a due righe nell’Editor Rich Text e si uniscono le due righe, viene rimosso lo stile applicato alla seconda riga. NPR-16389: Hotfix per CQ-4203835.
* Nella schermata Sites dell’interfaccia touch, non è possibile incollare una pagina in un’altra pagina priva di pagine secondarie poiché non viene visualizzato il pulsante Incolla. NPR-15894: Hotfix per CQ-4201696.
* Durante lo scorrimento della scheda Pagine nel pannello Trova contenuto, alcuni gruppi di pagine vengono visualizzati ripetutamente nell’interfaccia classica, mentre nell’interfaccia touch viene mostrato un set limitato di poche pagine non ripetute. NPR-16271: Hotfix per CQ-4202371
* Se si aprono le proprietà di pagina di una Live Copy nell’interfaccia utente touch e si fa clic su Salva senza apportare alcuna modifica, vengono scritte tutte le schede Live Copy e viene creato un nodo di configurazione LiveSync. NPR-16327: Hotfix per CQ-108562
* Il vincolo di Forms non è in grado di leggere la proprietà `ConstraintMessage`. NPR-16388: Hotfix per CQ-101330
* Nel componente `wcm/foundation/components/parsys` non viene visualizzato il segnaposto **[!UICONTROL Trascina qui i componenti]**. NPR 16748: Hotfix per CQ-4205187

### Assets {#assets-16}

* L’unità di rasterizzazione dei PDF smette di funzionare e causa problemi di memoria insufficiente dopo l’installazione di 6.2 SP1 o di Hotfix 12430. NPR-15991
* I metadati di una proprietà stringa, `documentNumber`, vengono visualizzati sotto forma di data, mentre dovrebbero essere un numero. NPR-16134: Hotfix per GRANITE-16916
* Testo troncato nel fumetto degli eventi della timeline. NPR-16226: Hotfix per CQ-85226
* Se nella gerarchia dei contenuti si crea una cartella il cui titolo contiene caratteri speciali, viene visualizzato un formato codificato del carattere speciale. NPR-15935: Hotfix per CQ-4202987
* L’utente non può caricare risorse o creare cartelle mentre naviga tra le risorse a causa di comportamenti non coerenti che si sono presentati durante l’utilizzo del pulsante Crea. NPR-16410: Hotfix per CQ-4204793
* Si verificano errori imprevisti durante il caricamento di risorse HTML condivise dalla vista degli articoli in AEM Authoring. NPR-16133: Hotfix per AEMM-4155970

### Integrazione {#integration-14}

* Se si abilita l’autenticazione proxy con l’autenticazione Digest, il componente AEM Search genera un’eccezione ConcurrentModificationException. NPR-15309: Hotfix per CQ-4199191
* Quando si crea un’attività di test A/B di Adobe Target in AEM, il pubblico non si sincronizza con Target e viene visualizzato “Nessun pubblico”. NPR-16229: Hotfix per CQ-4204210
* Dopo aver installato SP1+NPR-11577 v1.2, se si sceglie “Usa una metrica Analytics” per la metrica Obiettivo durante il targeting nell’interfaccia touch, l’elenco a discesa delle metriche non si carica mai. NPR-16129: Hotfix per CQ-4204316
* Se si utilizza il targeting e si pubblica una campagna, non viene pubblicato automaticamente l’intero albero comprensivo di marchio ed elemento principale. NPR-15855: Hotfix per CQ-94630

### Traduzione {#translation-8}

* Il processo di sincronizzazione della traduzione non viene attivato automaticamente e in AEM non viene applicato alcun limite di polling senza il blocco dei progetti di traduzione. NPR-15163: Hotfix per CQ-90856

### Forms {#forms-17}

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-17}

**Moduli adattivi**

* Durante il salvataggio di un modulo adattivo con un allegato, il percorso completo dell’allegato viene aggiunto al tag `fileAttachment` dell’XML generato, anziché al nome dell’allegato. NPR-16529
* Nei moduli adattivi basati su XDP, il wrapper `afData/afBoundData` è presente nel file XML inviato, anche se anche il file XML precompilato non contiene wrapper `afData/afBoundData`. NPR-16118

* Notazione esponenziale nel campo Numero: quando si utilizzano moduli adattivi, se viene immesso un numero con una frazione decimale superiore a dieci caratteri, nell’XML inviato il numero diventa una notazione esponenziale. NPR-16106
* Per i moduli che contengono sia un componente allegato che un frammento con caricamento lazy, l’XML dati inviato non contiene le informazioni relative al componente allegato. NPR-16022
* Per un pannello ripetibile con caricamento lazy che non ha un predecessore ripetibile, gli elementi figli ripetibili all’interno di una seconda istanza del pannello non vengono ripetuti. NPR-15944
* Durante il tentativo di salvare un frammento all’interno di un altro frammento nell’editor dei moduli, il valore del frammento figlio non viene recuperato dalla radice del modello di frammento. NPR-15943
* Durante la creazione di una casella di controllo con un solo elemento, se si tenta di mostrare il titolo della casella di controllo e mantenere nascosto il titolo dell’elemento, l’azione di creazione del dizionario genera un’eccezione `ArrayIndexOutOfBoundException` se il testo dell’elemento risulta vuoto. Il dizionario non viene creato e sullo schermo non viene visualizzata alcuna risposta di errore. NPR-15816
* Per i moduli adattivi con widget di allegati, alcune parti del modulo vengono disattivate dopo l’anteprima del file allegato.\
  NPR-16611

* Per i widget di allegati che possono contenere più allegati, se si invia una nuova istanza del modulo con un allegato a un widget contenente già un allegato, all’apertura dell’allegato aggiunto viene visualizzato un codice di errore anziché il contenuto effettivo. NPR-16258
* Proteggere il servizio di precompilazione dei moduli da accessi non autorizzati tramite protocolli quali `file://`, `http://` e `ftp://`. Consulta [Configurazione del servizio di precompilazione tramite Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754). NPR-15414

* Richiesta di eseguire il rendering del modulo adattivo in formato PDF, anziché HTML, nel passaggio di verifica e di aggiungere al PDF tutti gli allegati, in modo che venga visualizzato il modulo completo. NPR-9011

**Gestione della corrispondenza**

* Quando si utilizza un frammento di testo in una lettera in modalità Anteprima/Modifica, se il testo viene convertito in elenco, la funzionalità lettera si interrompe e viene generato un errore JavaScript. NPR-16460
* Non è possibile importare un file XSD per la creazione di un dizionario dati nel nodo Gestione corrispondenza in quanto il browser smette di rispondere ogni volta che viene caricato il file XSD e selezionato il nodo principale. Questo problema è indipendente dal browser e non viene visualizzato nei registri del server. NPR-16452
* Quando si visualizza l’anteprima di una lettera con Internet Explorer e si tenta di modificare la dimensione del font del contenuto, nel menu a discesa delle dimensioni del font vengono visualizzati valori duplicati per le dimensioni comprese tra 8 e 72. NPR-16387
* Se come campo di input viene visualizzato un campo mobile proveniente da un frammento XDP, il campo non si espande nell’anteprima della lettera con Internet Explorer. NPR-16367
* Se si tenta di inviare una lettera direttamente dall’anteprima, la finestra a comparsa relativa al nome della lettera non viene visualizzata correttamente poiché è nascosta. NPR-16353
* Gli spazi di riga aggiunti durante la modifica di una lettera non vengono visualizzati nella finestra di anteprima. In caso di frammenti di testo con elenchi, l’output PDF non mostra la spaziatura corretta. NPR-16267
* Se si lavora su un frammento di documento di testo in Internet Explorer, il tentativo di applicare un rientro al testo non riesce in quanto il cursore non consente il rientro del testo. NPR-16128
* L’aggiunta o la modifica di un dizionario dati a un frammento di documento di testo esistente richiede molto tempo e l’utente non riceve sempre l’apposita notifica. NPR-16102
* Quando in Internet Explorer si visualizza in anteprima una lettera con contenuto scorrevole, la barra di scorrimento del browser si sovrappone alla barra di scorrimento della lettera e non è possibile visualizzare tutto il contenuto dei frammenti sul lato destro. NPR-16068
* Quando in Google Chrome si creano o si modificano dei frammenti di documento di testo, il menu a discesa per la selezione del colore si apre automaticamente e non può essere rimosso. Per poter modificare il frammento, occorre quindi selezionare l’elenco come tipo di immissione dati. NPR-16067
* Quando si utilizza l’API Letterinstance, il metodo `import com.adobe.icc.services.api.LetterInstanceService` non funziona. NPR-16008
* La modifica del formato di visualizzazione della data in `locale=en_US; dateFormat=MMM dd,yyyy;` nella configurazione di Asset Composer non funziona come previsto e il formato della data viene visualizzato come caratteri indesiderati. NPR-16007
* Il tipo di Collegamento dati nelle lettere viene visualizzato come Utente durante il re-authoring, anche se in precedenza era stato impostato diversamente. NPR-16619

**Portale Forms**

* Gli scenari di aggiornamento per i componenti Bozza e Invio non funzionano con l’implementazione del database di esempio. NPR-16752

**Barcoded Forms Service (BCF)**

* L’analisi del codice statico del servizio BCF (Barcoded Forms Service) segnala alcuni problemi. NPR-13855

#### Programma di installazione Forms JEE  {#forms-jee-installer-17}

**Gestione dei processi - Area di lavoro HTML**

* Proteggere il servizio di precompilazione dei moduli da accessi non autorizzati tramite protocolli quali “file://”, “http://” e “ftp://”. Per informazioni dettagliate, consulta [Configurazione del servizio di precompilazione tramite Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754). NPR-15434

**User Management**

* Nella schermata di accesso SAML viene mostrata una versione non corretta (6.1.0) relativamente al server AEM 6.2. NPR-13825
* Con AEM Forms configurato per l’autenticazione Single Sign On (Kerberos), se l’autenticazione utente non riesce durante il tentativo di accesso, viene restituito un codice di errore 404. L’utente viene reindirizzato al sito di accesso solo dopo l’aggiornamento della pagina. NPR-15015

#### Forms Designer {#forms-designer-1}

* L’impostazione dizionario per il controllo ortografico sulla lingua francese (Canada) non funziona in AEM Forms Designer.\
  NPR-15896

### Pacchetti di funzioni inclusi in CFP3 {#feature-packs-included-in-cfp-2}

**Pacchetto di componenti aggiuntivi per Forms**

* Quando si elimina una risorsa nella gestione della corrispondenza, nel file error.log deve essere registrato un messaggio di avviso. NPR-13225
* È stata migliorata la funzionalità di ricerca quando si visualizza in anteprima una lettera in Gestione della corrispondenza e nel contenuto del frammento di testo è ora possibile cercare anche il testo (oltre al titolo o all’etichetta della lettera). NPR-16103

### Pacchetti OSGi inclusi in CFP3 {#osgi-bundles-included-in-cfp-5}

Elenco dei bundle OSGi aggiornati tra AEM 6.2 SP1 e CFP3

[Ottieni file](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
Gli elementi di rilievo di Cumulative Fix Pack 2 sono:

* Correzioni di stabilità e miglioramenti di prestazioni nella piattaforma AEM, inclusi il framework e le operazioni di Sling
* Gestione delle risorse migliorata grazie a numerose correzioni per accedere, spostare, cercare, caricare e pubblicare le risorse in modo più efficiente
* Miglioramento delle funzionalità di authoring e gestione di Sites grazie a correzioni apportate ai componenti Frammenti di contenuti, plugin Ancoraggio, Presentazione e ContextHub
* Varie correzioni all’interfaccia utente touch, ad esempio all’editor di testo, a Omnisearch e al processo di creazione delle varianti
* Miglioramento dei flussi di lavoro di traduzione; è stato migliorato il connettore Microsoft per l’utilizzo delle nuove API di traduzione per il portale Azure
* Correzioni apportate ai flussi di lavoro Projects e Campaign
* Gestione e authoring migliorati grazie a correzioni ai moduli adattivi, alla gestione della corrispondenza e ad alcune funzioni del portale di Forms
* Correzioni ai componenti delle aree di lavoro HTML e XTG e ai componenti di base di Forms JEE

### Platform {#platform-14}

* `SlingPostProcessor` viene attivato se viene modificata la pagina che fa direttamente riferimento al framework di Sling. NPR-15754: Hotfix per CQ-104153

* Il valore dei tag con proprietà `tagBasePath` non viene recuperato nella finestra di dialogo dell’interfaccia classica quando si passa a un componente pagina. NPR-15543: Hotfix per CQ-4199950

* Mentre si eseguono operazioni Sling, se si dispone di un blocco denominato “chunk_n_n-1” `SlingFileUpload handler.getLastChunk` viene eseguito in ciclo infinito con blocchi vuoti. NPR-15455: Hotfix per Sling-5701

* Quando un’interfaccia estende un’altra interfaccia, i metodi iniettabili nella super-interfaccia non vengono iniettati correttamente. NPR-15202: Hotfix per SLING- 5710
* Una potenziale eccezione Null Pointer non può essere impedita se si utilizza la chiamata alla funzione `com.adobe.granite.infocollector.impl.FilesTraversal`. NPR-15169: Hotfix per CQ-4197640
* Lo stato del flusso di lavoro non è coerente per alcuni nodi secondari e viene quindi visualizzato un errore durante l’invio di eventi di osservazione per i nodi. NPR-15701: Hotfix per GRANITE-13786
* Se un utente seleziona un nodo in CRXDE (ad esempio, /content/dam/) e quindi la scheda Controllo accessi, accertandosi che esista un elenco di controllo per l’accesso, nel momento in cui trascina e rilascia alcuni elementi, vengono spostati elementi diversi da quelli selezionati. NPR-15696: Hotfix per GRANITE-16300
* Se si seleziona un utente dall’elenco a discesa mentre si tenta di accedere come un’altra persona, la finestra a comparsa dell’utente sparisce. NPR-15774: Hotfix per CQ-4201738/GRANITE-11895
* In Omnisearch, la ricerca per tag con suggerimenti popolati automaticamente non funziona. NPR-15088: Hotfix per GRANITE-14426.\
  Nota: questa correzione richiede Oak CFP 1.4.11 o versione successiva.

### Authoring di AEM Mobile {#mobile-aem-author}

* Quando si utilizzano pacchetti AEM Mobile e ContentSync con un’applicazione ibrida, AEM risponde a una richiesta di recupero (con timestamp) dell’applicazione con il pacchetto più vecchio e non con quello effettivamente richiesto dall’applicazione. NPR-15749: Hotfix per CQ-104153

### Sites {#sites-17}

* Lo stato di modifica relativo alla casella in entrata del flusso di lavoro in WCM Core non cambia se l’utente modifica una pagina dopo l’attivazione di un flusso di lavoro. NPR-15684: Hotfix per CQ-4196974
* Il plug-in Ancoraggio nell’Editor Rich Text per l’interfaccia utente touch genera HTML5 non conforme quando l’utente fa clic sull’icona di ancoraggio e aggiunge un nome. Dovrebbe infatti aggiungere un attributo “id” invece dell’attributo “name” nel tag HTML5 relativo all’elemento di ancoraggio. NPR-15650: Hotfix per CQ-89782
* Quando si crea uno schema di metadati con numerosi campi e lo si applica ai metadati di Content Fragment, nella schermata dei metadati di Content Fragment non viene creata alcuna barra di scorrimento, rendendo i campi non modificabili. NPR-15478: Hotfix per CQ-4202622
* La modifica del componente campo `TagInput` non mostra i valori precedentemente configurati per i campi della finestra di dialogo. NPR-15464: Hotfix per CQ-4200360

* Nell’interfaccia utente dell’editor di frammenti di contenuto, se vengono create molte varianti di un frammento di contenuto, nel pannello laterale non viene visualizzata la barra di scorrimento per l’accesso a tutte le varianti. NPR-15445: Hotfix per CQ-4199444
* Gli utenti rimossi da gruppi diretti vengono aggiunti a gruppi ereditati. NPR-15400: Hotfix per CQ-98758
* WCM-Authoring: lo strumento di authoring dell’interfaccia touch non consente la modifica di pagine il cui nome contiene una virgola. NPR-15396: Hotfix per CQ-4199723
* Quando si utilizza l’interfaccia utente touch per l’authoring, la funzione `Granite.author.editableHelper.doSelectParent` trasmette gli argomenti in ordine errato, generando un errore JavaScript. NPR-15349: Hotfix per CQ-4198594
* Il segmento ContextHub visualizza l’esperienza anche se è presente il cookie di opt-out. NPR-15293: Hotfix per CQ-4198024
* Nell’interfaccia classica, il componente Presentazione non consente di creare diapositive né di trascinare e rilasciare immagini per creare nuove diapositive. NPR-15281: Hotfix per CQ-4194164
* Indipendentemente dal tipo di autorizzazione dell’utente, le opzioni di creazione (come Crea pagina, Crea sito, Crea Live Copy, Crea lancio e Crea catalogo) sono disponibili come voci di menu nella console di amministrazione sito. NPR-15278: Hotfix per CQ-94436
* Dopo aver installato AEM 6.2 Service Pack 1, il cursore “Includi pagine secondarie” non funziona più per i lanci di pagina. NPR-15230: Hotfix per CQ-4198449
* Richiesta di migliorare la funzione Pulizia delle versioni per recuperare ed elaborare le versioni in blocchi e poter utilizzare un percorso specificato in una query XPath. NPR-15186: Hotfix per CQ-109205
* Il pulsante Cancella non è presente nella scheda della miniatura di Proprietà pagina nel componente Sites. NPR-15143: Hotfix per CQ-4196997
* Per un sito che utilizza Live Copy, quando si seleziona la casella di controllo Live Copy nel riquadro Colonne della console SiteAdmin, lo stato della Live Copy non viene visualizzato correttamente e viene visualizzata solo la markup HTML. NPR-15108: Hotfix per CQ-97086
* Mentre si eseguono attività di modifica in Content Fragment, se per una modifica l’utente fa clic su Fatto (√) prima di ottenere la risposta del post, il contenuto modificato non viene salvato correttamente. NPR-15014: Hotfix per CQ-4194095
* Se si chiude la pagina Modifica in modalità Timewarp e si tenta di riaprirla da SiteAdmin, viene visualizzato l’errore di stato 500 e la pagina non viene riaperta. NPR-14965: Hotfix per CQ-109647:
* Nell’interfaccia utente di Digital Asset Manager (DAM), la ricerca di Trova autorizzabili in UserPicker causa un’eccezione con errore “Memoria insufficiente”. NPR 15307: Hotfix per CQ-98542

### Assets {#assets-17}

* Dopo aver cercato una risorsa in Omnisearch, selezionando una risorsa e provando a modificarne le proprietà facendo clic su Visualizza proprietà e quindi sul pulsante Salva, gli utenti verranno reindirizzati a una pagina vuota. NPR-15900: Hotfix per CQ-4202372
* L’interfaccia utente di Assets non risponde agli eventi. Se si seleziona una risorsa e si fa clic su Pubblica o Rappresentazioni, non viene generato alcun tipo di attività. NPR-15828: Hotfix per CQ-4202247
* Quando si pubblica una risorsa dalla vista Scheda, la scheda non viene aggiornata in modo da riflettere lo stato di pubblicazione fino a quando non si aggiorna la pagina. NPR-15826: Hotfix per CQ-102732
* Hotfix cumulativo contenente hotfix di Assets. NPR-15225
* Se il carattere “e commerciale” (&amp;) è incluso nel nome di una cartella di risorsa, il nome della cartella non viene visualizzato correttamente quando si passa alla risorsa. NPR-15775: Hotfix per CQ-4201735
* L’utilizzo del carattere “e commerciale” (&amp;) nel nome di un file di risorse genera problemi quando si accede alle proprietà del file. NPR-15770: Hotfix per CQ-4201737
* Quando in Assets è attiva la modalità Vista a colonne, se l’utente aggiorna la pagina dopo aver selezionato e fatto clic su una risorsa, vengono visualizzati i dettagli della risorsa e non il contenuto aggiornato. NPR-15768: Hotfix per CQ-4201727
* L’inserimento di un file PDS utilizza il 100% della CPU con un heap di librerie per i servizi PDF. NPR-15606: Hotfix per GRANITE-12929
* Se si accede all’interfaccia utente di “Le mie condivisioni di collegamenti” con Firefox, non vengono visualizzati gli utenti o gli elementi condivisi e la schermata non è utilizzabile. NPR-15539: Hotfix per CQ-4200992
* Quando si utilizza Digital Asset Manager, se a una pagina è associato un set di immagini e si spostano le immagini in una nuova cartella, l’associazione di pagina non funziona e nella pagina associata alcune immagini risultano mancanti. NPR-15538: Hotfix per CQ-111479
* Nel componente Visualizzatore Dam, l’utilizzo della modalità di esecuzione “nosamplecontent” genera errori con gli elementi multimediali dinamici. NPR-15449: Hotfix per CQ-4195425
* Durante la creazione di profili video, se vengono scelte impostazioni di codifica video di qualità sia media che alta, le modifiche apportate non vengono salvate. NPR-15447: Hotfix per CQ-4195482
* Anche se il caricamento di una risorsa in Brand Portal non riesce a causa di una risposta di errore del server, lo stato viene aggiornato a Pubblicato nell’interfaccia utente di Brand Portal, rendendo difficile rintracciare il file mancante. NPR-15442: Hotfix per CQ-4197968
* Quando si pubblica una cartella di risorse in Brand Portal e la pubblicazione richiede più di un’ora, alcuni file non vengono pubblicati. NPR-15441: Hotfix per CQ-4199493
* Se si utilizza la console di Asset Finder nella vista a colonne, il tentativo di creare una cartella ha esito positivo la prima volta, ma funziona se si riprova. NPR-15370: Hotfix per CQ-4199448
* Se una risorsa o una cartella selezionata nell’interfaccia utente di DAM ha una virgola nel nome, la scheda Riferimenti non è disponibile e viene visualizzato un messaggio di tipo “Elenco di riferimenti non disponibile per selezioni multiple”. NPR-15362: Hotfix per CQ-4199721
* La pubblicazione di una cartella in Brand Portal non ne modifica lo stato di pubblicazione, anche se le risorse presenti nella cartella sono state pubblicate correttamente. NPR-15292: Hotfix per CQ-4197667
* Nell’interfaccia touch, quando si accede alla console Assets viene generata un’eccezione durante l’attivazione di alcune risorse. NPR-15217: Hotfix per CQ-108779
* La pubblicazione di un video su YouTube quando la connessione viene stabilita tramite un server proxy. NPR-15109: Hotfix per CQ-110332
* L’utilizzo di una risorsa il cui nome contiene un punto (.) in data-sly-resource non viene risolto nella stessa risorsa e il percorso di output viene terminato in corrispondenza del punto. NPR-15069: Hotfix per CQ-4195914
* Dopo aver aggiornato AEM 6.2 a Service Pack1, la sincronizzazione delle risorse in Scene7 ha esito negativo. La proprietà dam:Scene7FileStatus visualizza lo stato “`UploadFailed`” anche per le risorse pubblicate. NPR-15269: Hotfix per CQ-4197708

### Interfaccia utente {#user-interface-5}

* Nell’**[!UICONTROL interfaccia utente touch]**, la data salvata non viene visualizzata per i campi che non presentano type=&#39;datetime&#39; se si utilizza Internet Chrome versione 56.0.2924.87. NPR-15383: Hotfix per GRANITE-16481
* Nell’**[!UICONTROL interfaccia touch]**, l’Editor Rich Text rimuove il thread e gli elementi di didascalia dalle tabelle HTML durante il rendering. NPR-15267: Hotfix per CRTE-41
* `FileUpload Validator` non gestisce i casi in cui l’avvio automatico è impostato su true o quando `uploadFile()` viene chiamato manualmente e, in questi casi, genera un rapporto di convalida non valido. NPR-15295: Hotfix per GRANITE-13499

* Omnisearch non consente ai clienti che utilizzano /apps di aggiungere un’origine dati di colonna in quanto presuppone che la configurazione della posizione sia elencata in */libs/granite/omnisearch/content/metadata/*. NPR-13188: Hotfix per GRANITE-16479
* Quando si utilizza l’**[!UICONTROL interfaccia utente touch]**, le varianti di prodotto non vengono create allo stesso livello del prodotto. L’utente non è informato sullo stato del processo di creazione delle varianti. NPR-15345: Hotfix per CQ-4198948

**Scene7**

* L’esecuzione di un flusso di lavoro Scene7 genera file aperti che non vengono chiusi. Richiesta di migliorare il servizio AEM-S7 in modo da mantenere e riutilizzare una singola istanza HttpClient con una configurazione di pooling condivisa. NPR-15357: Hotfix per CQ-109958

### Traduzione {#translation-9}

* Quando si utilizzano progetti di traduzione, aggiornando le copie in lingua create dalla copia master in inglese, vengono generati 11 diversi lanci con lo stesso nome e radice di origine, ma con radici di lancio leggermente diverse nel caso in cui il nome della pagina segua un pattern preimpostato. NPR-15605: Hotfix per CQ-4200699
* I progetti di traduzione non vengono creati per le pagine se le radici della lingua contengono trattini nel nome. NPR-15171: Hotfix per CQ-96286
* Richiesta di aggiornare il connettore Microsoft in modo da poter utilizzare le API Microsoft Translator, che Microsoft rende disponibili nel portale di Azure. NPR-15320: Hotfix per CQ-101010

### Progetti {#projects-4}

* Nella schermata Progetti sono visibili solo 20 progetti inattivi, sebbene nell’archivio siano presenti più di 20 progetti inattivi. NPR-15656: Hotfix per CQ-4200903

### Campaign {#campaign-1}

* Se si utilizzano i componenti di integrazione Campaign - Targeting e MAC - Test and Target, l’annullamento della pubblicazione delle attività non aggiorna lo stato dell’attività nell’interfaccia utente principale. NPR-15401: Hotfix per CQ-4199839
* Durante lo spostamento di un prodotto in AEM Commerce, nella procedura guidata non vengono precompilati i valori relativi a nome, titolo, pagine di riferimento, autore e data di creazione del prodotto. NPR-15228: Hotfix per CQ-98617

### Sicurezza {#security-4}

* Il parametro token CSRF è stato aggiunto ai moduli con un metodo GET. NPR-15229

### Forms {#forms-18}

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-18}

`**Adaptive Forms**`

* I valori predefiniti vengono sostituiti da valori vuoti in xml durante la precompilazione del modulo adattivo con l’XML di input. NPR-15721
* Il wrapper `afData/afBoundData` è presente nel file XML inviato, sebbene il file XML di precompilazione non contenga il wrapper `afData/afBoundData` nei moduli adattivi basati su schema XML. NPR-15541

* I titoli nella barra di un pannello a soffietto devono essere titoli HTML h2 modificabili e non un tag “a”. NPR-15475
* Il layout con pannello a soffietto di un modulo non è accessibile agli utenti di utility per la lettura dello schermo. Gli utenti non possono passare al pannello a soffietto utilizzando solo la tastiera se si avvalgono di un’utility per la lettura dello schermo come JAWS o NVDA. NPR-15474

`**Correspondence Management**`

* Per salvare, eliminare e impostare riferimenti in un frammento di documento è necessario molto tempo. NPR-15939
* L’allineamento delle tabulazioni impostato in Gestione risorse su un testo contenente più intestazioni interrompe il funzionamento dell’interfaccia utente CCR. NPR-15818
* Nelle miniature dei moduli di testo, il contenuto non viene visualizzato allineato, anche se il testo contiene contenuto allineato creato utilizzando Tabulazioni in Google Chrome. NPR-15819

`**Forms Portal**`

* Il servizio di precompilazione non funziona per XDP Forms. NPR-15466
* Quando si archiviano invii e bozze di moduli adattivi a un database, lo stato del modulo adattivo viene danneggiato se la connettività del database si interrompe per qualsiasi motivo (ad esempio, dopo un lungo periodo di inattività). NPR-15297

#### Programma di installazione Forms JEE  {#forms-jee-installer-18}

`**Core**`

* Dopo l’aggiornamento alla versione più recente di Java 1.8.0_121-b13, l’interfaccia utente per amministratori non è accessibile in AEM Forms. NPR-15330

`**XTG**`

* Se si utilizza il servizio di output per combinare un modulo specifico con un XML dati, il tempo di risposta risulta fino a 20 volte superiore rispetto al tempo impiegato dal server ES4 SP1 per eseguire la stessa operazione. NPR-15283

#### App AEM Forms {#aem-forms-app-1}

* Durante il ripristino di attività non salvate, il messaggio visualizzato al ripristino dell’attività deve essere reso più chiaro per poter ridurre gli errori degli utenti. NPR-15377
* L’app AEM Forms non esegue il rendering dei moduli creati da modelli personalizzati. NPR-15892
* Gli utenti non sono in grado di accedere all’app AEM Forms. NPR-15891

Gli elementi di rilievo di AEM 6.2 SP2-CFP1 sono:

* Maggiore semplicità della funzionalità di replica in Sites:

   * Correzioni a vari problemi di rollout, Live Copy e scrittura non corretta

* Riduzione del tempo di risposta dell’interfaccia utente touch durante:

   * Ricerche di risorse
   * Ordinamento basato sulle dimensioni

* Maggiore efficienza di gestione dei tag nelle raccolte avanzate
* Controlli di accesso più rigidi durante le operazioni CRUD sulle cartelle

### Platform {#previous}

* richiesta di rimuovere le chiamate all’API `ReplicationQueue#forceRetry` durante l’avvio degli agenti di replica, poiché rallentano notevolmente l’istanza, soprattutto se questa include molti agenti di replica. NPR-14032: Hotfix per GRANITE-13095
* Necessità che la configurazione OSGi `DurboImportConfigurationProviderService` supporti i campi in grado di memorizzare un array di valori. NPR-14570: Hotfix per CQ-108684
* Se si utilizza il componente Sightly in una pagina dopo la migrazione ad AEM 6.2, la finestra di dialogo Proprietà della pagina non si apre più. NPR-14328: Hotfix per CQ-108355
* L’annullamento della pianificazione di un processo precedentemente pianificato non rimuove il nodo corrispondente in */var/eventing/Scheduled-jobs*. NPR-14253: Hotfix per Sling-5666
* Se un amministratore tenta di accedere come un utente eliminato, l’interfaccia utente non viene aggiornata. NPR-14247: Hotfix per CQ-107446
* Il controllo della protezione da vulnerabilità ad attacchi XSS (Cross-Site Scripting) genera una codifica non corretta nel componente Sightly. NPR-14004: Hotfix per CQ-93821
* Richiesta di aggiornare Jackrabbit Filevault alla versione 3.1.30 per risolvere vari problemi. NPR-13454
* Si verifica un errore di cache quando la distribuzione Sling sincronizza i pacchetti di distribuzione dall’ambiente di authoring a quello di pubblicazione. NPR-13034: Hotfix per GRANITE-13970

### Sites {#sites-18}

* Problemi con VersionManagerImpl che elimina versioni non corrette dalla cronologia delle versioni. NPR-14372
* Il componente WCM Sightly Foundation ignora i nomi dei tag di dichiarazione del componente: `cq:htmlTag / cq:tagName`. NPR-14225
* Se si utilizza il parsys Sightly per eseguire il rendering dei componenti inseriti tramite JavaScript nell’interfaccia utente touch, la decorazione personalizzata viene ignorata dopo l’aggiornamento della pagina. NPR-14122
* Gli elenchi a discesa di Target non funzionano nelle finestre di dialogo dell’interfaccia utente touch se vengono creati più campi Rich Text, come i collegamenti. NPR-13911
* Quando si modifica un campo di testo con più proprietà Editor Rich Text (RTE) in una finestra di dialogo (interfaccia utente touch), viene attivata in modo casuale una delle proprietà RTE. NPR-13703
* Il componente video predefinito non esegue il rendering della miniatura video. NPR-14976
* Le informazioni vengono caricate lentamente nella scheda Utilizzi live dell’Editor modelli. NPR-14880: Hotfix per CQ-83417
* L’installazione di Hotfix-10936 su un’istanza AEM 6.2 disattiva il componente iparsys. NPR-14330: Hotfix per CQ-106982
* Si sono verificati vari problemi relativi ai componenti di rollout e un problema alle Live Copy dopo la migrazione ad AEM 6.1 SP1. NPR-15256
* L’azione Rollout pagina non riesce a creare elementi figlio oltre il primo livello, anche per più configurazioni di rollout. NPR-15055
* Quando si invia la finestra di dialogo PageProperties dall’editor, i dati non modificati nelle schede Live Copy vengono riscritti. NPR-14693
* Quando si invia la finestra di dialogo PageProperties dall’editor, il post-processore MSM scrive alcuni parametri dalla richiesta e non dal parametro `msm:writeLiveCopyConfig`. NPR-14434
* Numerosi problemi relativi al componente Rollout, alle Live Copy e ad altri aspetti di MSM. NPR-12235

### Assets {#assets-18}

* Il flusso di lavoro UnPack non è in grado di gestire immagini con caratteri speciali nel nome del file di immagine. NPR-15227: Hotfix per CQ-103887
* Le risorse contenenti l’espressione “Repeat with condition” non vengono visualizzate correttamente. Quando l’utente visualizza l’anteprima del modello di lettera `*CDN3835RLCEN*`, non vengono visualizzate le risorse che si trovano nell’area di destinazione del corpo. Se si deseleziona la risorsa opzionale `*VIPReassement*` preselezionata, le altre risorse preselezionate vengono visualizzate nella lettera. NPR-14844

* Durante la creazione di una raccolta avanzata, il tag di stile non viene mantenuto nel momento in cui si salva la raccolta avanzata. NPR-15081: Hotfix per CQ-4195494
* Se più utenti effettuano ricerche simultaneamente, le query per la ricerca di risorse vengono eseguite lentamente nell’interfaccia utente touch. NPR-15019; Hotifx per CQ-4195405
* I metadati estratti per una proprietà di tipo `Long[]` vengono convertiti in tipo `String[]` quando la risorsa originale viene ricaricata in un percorso diverso. NPR-15016: Hotfix per CQ-4195005

* Gli utenti non riescono a eliminare una ricerca salvata o una raccolta avanzata. NPR-14924: Hotfix per CQ-108494
* Si verifica un errore se si modificano metadati per risorse in blocco (modalità di accodamento) mentre si utilizza un valore booleano per TypeHint in un campo a discesa dello schema di metadati sottostante. NPR-14529: Hotfix per CQ-106876
* Gli utenti senza diritti di replica non possono eliminare cartelle di Assets. NPR-14321: Hotfix per CQ-88271
* Quando si tenta di modificare i profili di un video nell’editor canale, la finestra di dialogo di progettazione non si apre e nel registro degli errori viene generata un’eccezione NPE. NPR-14144: Hotfix per CQ-81101
* La proprietà di timestamp Creato generata dal sistema, visualizzata nella pagina delle proprietà di una risorsa, non è corretta. NPR-13992: Hotfix per CQ-95029
* Richiesta di abilitare il rilevamento di risorse duplicate per gli utenti senza accesso in lettura in AEM Assets. NPR-13851: Hotfix per CQ-102281
* Gli utenti non possono modificare i metadati di risorse in blocco dalla pagina delle proprietà. NPR-13721: Hotfix per CQ-100703
* Nell’interfaccia classica viene visualizzato un messaggio di errore non corretto quando viene caricata una risorsa duplicata. Il messaggio di errore non indica il motivo per cui il caricamento non è riuscito. NPR-13691: Hotfix per CQ-99272
* Nella vista a elenco, AEM Assets non è in grado di ordinare contemporaneamente più di 50 risorse per dimensione se la cartella contiene numerose risorse. CQ-100588
* Quando si selezionano più risorse, viene generato un errore con Codice risposta - 414 (URI richiesta troppo lungo), se l’URI della risorsa o cartella è troppo lungo. NPR-13516: Hotfix per CQ-76076
* La pagina Rapporti di Assets non risponde se l’utente seleziona tutte le opzioni disponibili nella finestra di dialogo Configura colonne. NPR-13187: Hotfix per CQ-95589
* Comportamento imprevisto di TagPicker in Safari e Internet Explorer. NPR-13134
* Se si modifica una ricerca salvata dalla barra di ricerca di Assets per amministratori, è possibile salvarla come selezione avanzata nidificata e questo provoca problemi di stabilità dell’ambiente. NPR-13119: Hotfix per CQ-99460
* Dopo aver spostato un file (o una cartella) e averlo rinominato, i metadati “cq:name” non riflettono il nuovo nome del file (o della cartella). NPR-13036: Hotfix per CQ-99141
* Le risorse con nomi contenenti caratteri speciali non possono essere scaricate da un collegamento di download condiviso tramite e-mail. NPR-12872: Hotfix per CQ-95795
* I rapporti predefiniti di Assets generati in presenza di un elevato numero di risorse causano numerosi attraversamenti laddove la ricerca non coinvolge alcun indice, e quindi picchi di utilizzo della CPU. NPR-12811: Hotfix per CQ-84409
* Gli utenti di AMS AEM Assets che accedono all’istanza di authoring da reti diverse non possono caricare le risorse tramite la funzione di caricamento in blocchi senza eliminare i privilegi sulle cartelle. NPR-12768: Hotfix per CQ-82715
* Nelle operazioni di ricerca di risorse basate su tag effettuate tramite la barra di ricerca di Assets, la funzione di completamento automatico non è limitata al percorso principale e visualizza i tag di tutti gli spazi dei nomi. NPR-12666
* Il componente StaticRenditions genera un’eccezione NPE. NPR-12665
* Richiesta di disabilitare MissingMetadataNotificationJob poiché determina l’interruzione della pagina da parte dell’interfaccia utente di Notifica badge con l’eccezione runtime “Impossibile analizzare l’input”. NPR-12500: Hotfix per CQ-93573
* L’opzione “Disattiva modifica” per un campo tag non funziona nelle pagine Proprietà risorse dell’interfaccia utente touch. NPR-12429: Hotfix per CQ-88835
* Correzioni dell’API in AEM Assets 6.2 per l’implementazione SMB di Companion App. NPR-11099
* Dall’aggiornamento di Jquery, gli utenti non possono selezionare una raccolta di risorse e confermare la selezione nel pannello Contenuto associato di un frammento di contenuto. NPR-14847: Backport per CQ-4194209
* Anche se viene richiamato un ordinamento infinito sul lato client, vengono ordinati solo gli articoli/banner/raccolte attualmente visualizzati nell’interfaccia utente. NPR-14493: Hotfix per CQ-109926
* Richiesta di implementare la funzionalità Omnisearch per il servizio mobile-on-demand di AEM. La ricerca di parole chiave per qualsiasi articolo, raccolta o banner non restituisce alcuna corrispondenza. NPR-14093: Hotfix per CQ-101394
* Quando si utilizza il componente Coral-select (*granite/ui/components/coral/foundation/form/select*) in una finestra di dialogo, l’inizializzazione dei valori non funziona correttamente in Internet Explorer (IE11 o Edge) se il valore selezionato contiene un singolo elemento. NPR-13395: Hotfix per CQ-101013

### Progetti {#projects-5}

* Quando si esporta un progetto di traduzione creato impostando Metodo di traduzione su Umano e Provider di traduzione su Nessuno, non viene generato alcun file Translation_export_summary.xml poiché manca il file di mappatura GUID. NPR-13137: Hotfix per CQ-91976
* Nei progetti AEM, quando si crea un progetto con la proprietà Scadenza impostata, la conversione della data imposta l’ora in modo errato a causa della differenza di fuso orario tra server e client. NPR-13003: Hotfix per CQ-98288
* L’opzione Mostra in Sites scompare dal processo di traduzione quando viene aggiornato un progetto di traduzione. NPR-12966: Hotfix per CQ-93740
* Quando viene creato un progetto di traduzione per una pagina di sito esportata, il rendering dell’anteprima non viene eseguito correttamente. NPR-12964: Hotfix per CQ-84627

### Flusso di lavoro {#workflow-3}

* Quando si fa clic sul collegamento Payload nella scheda Archivio della console Flusso di lavoro, viene restituito un errore con codice di risposta 404. NPR-14993: Hotfix per CQ-4194977
* Quando si utilizzano i flussi di lavoro predefiniti di AEM, CQ Mailer non riesce a inviare una notifica e-mail a un gruppo se manca l’indirizzo e-mail anche di un solo membro. NPR-14804; Richiesta hotfix per CQ-91499
* Miglioramenti delle prestazioni per la casella in entrata e il badge di notifica nell’interfaccia utente touch. NPR-14145: Hotfix per CQ-101125
* Durante l’avvio di un flusso di lavoro, gli utenti non possono visualizzare l’anteprima del payload dalla console Casella in entrata del flusso di lavoro. NPR-13226: Hotfix per CQ-100275
* Il cookie saml_request_path configurato utilizzando lo strumento di gestione delle autorizzazioni SAML visualizza il cookie impostato con un carattere “?” aggiuntivo. Se viene eseguito il postback di una risposta SAML in AEM, il cookie AEM saml_request_path restituisce un valore non valido a causa di caratteri già codificati. NPR-13517: Hotfix proattivo per GRANITE-11722 e GRANITE-14414

### Integrazione della soluzione {#solution-integration}

* Dopo aver integrato AEM 6.2 con Search&amp;Promote, se un utente cerca un termine che restituisce un banner, la funzionalità di ricerca non risponde. NPR-14549: CFP per CQ-109631

### Dynamic Media {#dynamic-media}

* Numerosi processi Sling AEM-Scene7 creati e annullati durante l’attivazione vengono registrati come processi di archiviazione durante la replica. NPR-12835: Hotfix per CQ-86115

### Sicurezza {#security-5}

* Necessità di risolvere il problema di convalida degli input nel filtro WCMDebug. NPR-12444; Richiesta hotfix per CQ-94890
* Richiesta proattiva per la correzione del comportamento XSS (Cross-Site Scripting) durante la creazione guidata di lanci.\
  NPR-13062; Richiesta hotfix per CQ-99577

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-19}

`Adaptive Forms`

* Quando si crea un pannello ripetibile utilizzando moduli adattivi, non è possibile aggiornare il titolo del pannello in fase di esecuzione. NPR-15325
* Quando il valore predefinito di un pulsante di scelta è impostato e durante il salvataggio o l’invio viene selezionato un valore diverso da quello predefinito, il valore non viene visualizzato nella precompilazione. NPR-15304
* Google Chrome presenta un comportamento errato quando si utilizza l’evento Opzioni per compilare in modo dinamico un elenco a discesa e si invia il valore dell’elemento selezionato. NPR-15198
* Quando si crea un pannello ripetibile utilizzando moduli adattivi, non è possibile aggiornare il titolo del pannello in fase di esecuzione. NPR-15181
* Quando si utilizza la modalità di modifica per i moduli adattivi, si verificano errori JavaScript di tipo “Handler del componente non valido” e “guidelib non definita”. NPR-15112
* Un frammento con caricamento lazy in un pannello ripetuto non funziona come previsto. NPR-13916, NPR-14785

`Correspondence Management`

* Le risorse di Gestione della corrispondenza per le quali è impostata l’espressione `'Repeat with condition'` non vengono visualizzate correttamente. NPR-14844
* Quando si cerca una risorsa di Gestione della corrispondenza (ad esempio una lettera, un frammento di documento o un altro tipo), l’icona relativa alla coda per il download non viene più visualizzata nella barra degli strumenti. NPR-14745
* Quando si crea un modulo Elenco, non funziona l’attivazione o la disattivazione delle proprietà specifiche di una risorsa (ad es. Modificabile, Obbligatoria). NPR-14689
* Il pannello Elementi dati nell’utility Generatore di espressioni continua a caricarsi nel caso in cui venga creato un modulo di condizione senza aver selezionato un dizionario dati. NPR-14688
* Quando si visualizza l’anteprima di una lettera, gli utenti non possono utilizzare spazi di tabulazione per allineare il contenuto in formato tabulare. NPR-14481
* Quando si esportano in massa risorse di Gestione della corrispondenza dall’interfaccia utente, il server AEM Forms genera registri superflui. NPR-15226
* Quando si visualizza l’anteprima di una lettera, il testo giustificato viene visualizzato in un font diverso. NPR-15468

`**Forms Portal**`

* Gli allegati dei moduli inviati nel portale Forms non sono visibili quando viene inviata una nuova bozza dal portale. NPR-13515

`**Forms Manager**`

* Quando si accede alla directory *FormsandDocuments*, il pulsante Incolla non viene visualizzato se l’utente copia una risorsa e quindi passa a un’altra cartella. CQ-111327

#### Programma di installazione Forms JEE {#forms-jee-installer-19}

`Rights Management`

* L’evento di audit per l’accesso utente viene registrato con un’ora non valida. L’ora corretta per l’evento di audit non è tracciabile. NPR-13107
* I documenti protetti con l’autenticazione estesa non possono essere aperti in Adobe Acrobat Reader e Microsoft Office. NPR-14482

`Process Management`

* Quando un’attività bozza inoltrata nell’area di lavoro HTML viene restituita all’utente iniziale, l’attività non viene più visualizzata nella coda dell’utente iniziale. NPR-15178

`Assembler Service`

* AEM Forms non riesce a convalidare un PDF/A-2b con più di due firme. NPR-14101

`XTG`

* Durante la stampa di un documento utilizzando un cassetto bypass della stampante, la funzione `GeneratePrintedOutput` non consente il recupero della carta dal cassetto bypass corretto. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer si chiude inaspettatamente se l’utente esegue il controllo ortografico con la lingua Francese (Canada) selezionata nelle impostazioni internazionali. NPR-13740
* Forms Designer si chiude inaspettatamente se l’utente seleziona un evento di calcolo o di convalida per un campo del modulo, modifica il linguaggio in JavaScript e immette `this.` nella finestra **[!UICONTROL Editor di script]**. NPR-12974

### Pacchetti di funzioni inclusi in CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Pacchetto di componenti aggiuntivi per Forms):

* Quando un modulo adattivo viene creato da un file XDP, la tabulazione per l’accessibilità non segue il pattern preimpostato. NPR-12562

`Adaptive forms` (Pacchetto di componenti aggiuntivi per Forms):

* Generatore regole per i moduli adattivi non fornisce l’accesso basato sui ruoli. Le modifiche apportate da un autore non sono tracciabili. NPR-12840

`Core` (Programma di installazione di JEE per Forms):

* La funzionalità CORS (CoreCross Origin Resource Sharing) come filtro servlet non è abilitata per Jboss+. NPR-13050

## Istruzioni per il download di CFP tramite Software Distribution {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Per i clienti di AEM Forms, è essenziale installare il pacchetto dei componenti aggiuntivi per AEM Forms dopo l’installazione del Service Pack, del Cumulative Fix Pack o del Feature Pack di AEM.

Scarica il pacchetto CFP direttamente da Software Distribution oppure esegui i seguenti passaggi:

1. Apri [Software Distribution](https://experience.adobe.com/downloads). Per accedere a Software Distribution è necessario disporre di un Adobe ID.
1. Tocca **[!UICONTROL Adobe Experience Manager]** che si trova nel menu di intestazione.
1. Tocca il nome del pacchetto, seleziona **[!UICONTROL Accetta termini EULA]**, quindi tocca **[!UICONTROL Scarica]**.

## Istruzioni di installazione per CFP {#installation-instructions-for-cfp}

Questa sezione descrive i requisiti e i passaggi necessari per installare il CFP.

### Prima dell’installazione {#before-you-install}

>[!NOTE]
>
>I Feature Pack opzionali forniti da Adobe dipendono dalla versione e dal Cumulative Fix Pack disponibili. Se hai installato un Feature Pack, contatta il [team di Assistenza clienti di AEM](https://helpx.adobe.com/it/marketing-cloud/contact-support.html) per verificare la compatibilità con questo Cumulative Fix Pack per AEM 6.2.

>[!NOTE]
>
>Prima di installare il pacchetto, è consigliabile eseguire la convalida su ogni nuovo pacchetto di installazione. La pre-convalida analizza e segnala eventuali errori riscontrati prima dell’installazione avvisando gli utenti di tali errori, sovrapposizioni e permessi in modo proattivo.
>
>Per accedere alla documentazione relativa all’opzione di Convalida, consulta [https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator)

* AEM 6.2 Service Pack 1 è un prerequisito per CFP. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).

* Il download del Cumulative Fix Pack è disponibile su [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/it/aem.html), a cui è possibile accedere direttamente dall’istanza di AEM.
* Per un’implementazione cluster tramite RDBMK o MongoDB, il pacchetto CFP può essere installato in una qualsiasi delle istanze di authoring che utilizzano Gestione pacchetti.

* Prima di installare il Cumulative Fix Pack, assicurati di creare uno snapshot o eseguire un backup dell’istanza di AEM.
* La disinstallazione del CFP non è supportata.

### Installare CFP tramite Software Distribution {#install-the-cfp-via-package-share}

Per installare il Cumulative Fix Pack in un’istanza di AEM 6.2 SP1 esistente, effettua le seguenti operazioni:

1. Fai clic sul collegamento [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) per scaricare il pacchetto.

1. Apri [Gestione pacchetti](http://localhost:4502/crx/packmgr/index.jsp) e fai clic su **[!UICONTROL Carica pacchetto]** per caricarlo.

1. Seleziona il nome del pacchetto e fai clic su **[!UICONTROL Installa]**.

### Installazione automatica {#automatic-installation}

Il CFP può essere installato automaticamente in un’istanza in esecuzione nei seguenti modi:

* Inserisci il pacchetto in ../crx-quickstart/install mentre il server è in esecuzione. Il pacchetto viene installato automaticamente.
* Utilizza l’[API HTTP da Gestione pacchetti](https://helpx.adobe.com/it/experience-manager/6-2/sites/administering/using/package-manager.html). In questo caso assicurati di utilizzare `cmd=install&recursive=true` in modo che il pacchetto nidificato venga installato.

### Convalidare l’installazione {#validate-installation}

1. Nella pagina Informazioni prodotto (/system/console/ productinfo), in Prodotti installati deve essere ora visualizzata la stringa di versione aggiornata “Adobe Experience Manager, versione 6.2.0.SP1-CFP20”.
1. Tutti i bundle OSGi risultano come ATTIVI o FRAMMENTI nella console OSGi (usa la console web: /system/console/bundles).

>[!NOTE]
>
>Dopo l’installazione corretta del pacchetto, viene visualizzato un messaggio informativo per indicare che il pacchetto di contenuti è stato installato correttamente, ad esempio “Pacchetto di contenuti AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 installato correttamente”.

>[!NOTE]
>
>A partire da AEM 6.2 SP1-CFP1, il livello registro in Jackrabbit FileVault è cambiato da INFO a DEBUG per la maggior parte dei messaggi. Per ottenere i registri di installazione per un pacchetto di contenuti installato in AEM 6.2 SP1-CFP1 o versione successiva, abilita il livello di registro DEBUG per `org.apache.jackrabbit.vault.packaging.impl`.

### Installare AEM Forms {#install-forms}

>[!NOTE]
>
>Ignora questa sezione se non usi AEM Forms.

#### Installare il componente aggiuntivo per AEM Forms {#install-aem-forms-add-on}

>[!NOTE]
>
>(**Solo AEM Forms su JEE**) La procedura per installare un CFP su AEM Forms su JEE è descritta in [Installazione di CFP su AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Assicurarsi di aver installato il pacchetto AEM 6.2 SP1 CFP.
1. Scaricare il pacchetto corrispondente dei componenti aggiuntivi per Forms elencato in [Versioni di AEM Forms](aem-forms-releases.md) per il sistema operativo in uso.
1. Installa il pacchetto dei componenti aggiuntivi per Forms come descritto in [Installazione dei pacchetti aggiuntivi per AEM Forms](https://helpx.adobe.com/it/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html).

#### Installare il pacchetto dei bundle di JEE per AEM Forms {#install-aem-forms-jee-bundles-package}

Le correzioni apportate a JEE per AEM Forms vengono distribuite tramite un programma di installazione separato. Per informazioni sull’installazione di un CFP in JEE per AEM Forms, consulta [Installing Cumulative Fix Packs on AEM Forms JEE](install-cfp-aem-forms-jee.md) (Installazione di Cumulative Fix Pack in JEE per AEM Forms).

#### Programma di installazione di Forms Designer {#designer-installer}

1. Per installare l’aggiornamento, esegui il file Designer6.2.0_&lt;Lingua>_Cumulative_QF.msp.
1. Nella schermata di benvenuto, fai clic su **Aggiorna**. L’installazione viene avviata.
1. Al termine dell’installazione, fai clic su **Fine**.

## Parametri di timeout configurabili dall’utente per le connessioni a DTM, Analytics, Target e Search &amp; Promote {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Con AEM Cumulative Fix Pack 6.2 SP1-CFP7 e versioni successive, i periodi di timeout di connessione sono stati resi configurabili su tutte le connessioni precedenti, come indicato di seguito:

| **Connessioni** | **Timeout della connessione&#42;** | **Timeout socket&#42;&#42;** |
|---|---|---|
| DTM | 30000 ms | 30000 ms |
| Analytics | 30000 ms | 30000 ms |
| Target | 60000 ms | 30000 ms |
| Search&amp;Promote | 30000 ms | 30000 ms |

* **Timeout connessione&#42;** - Timeout in millisecondi fino a quando non viene stabilita una connessione. Un valore di timeout pari a zero viene interpretato come un timeout infinito.
* **Timeout socket&#42;&#42;** - Timeout in millisecondi in attesa dei dati o per un periodo massimo di inattività tra due pacchetti di dati consecutivi.

>[!NOTE]
>
>Con AEM Cumulative Fix Pack 6.2 SP1-CFP6 e versioni successive, la configurazione OSGi utilizzata per l’integrazione di Search&amp;Promote è Apache HTTP Components Proxy Configuration. La configurazione proxy di Day Commons HTTP Client 3.1 non viene più utilizzata.

## Disattivazione dello stato di replica nella console di assegnazione tag (interfaccia classica) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Per CFP3 o versione successiva, procedi in base alle istruzioni seguenti per disabilitare lo stato di replica nella console di assegnazione tag dell’interfaccia classica:

* Sovrapponi */libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js* in */apps*

* Aggiungi `replicationStateRequired`: &quot;false&quot; dopo la riga 416.

  ```js
  415    baseParams: {
  416                    count: "false",
  417                    "replicationStateRequired": "false"
  418                },
  ```

## Il più recente Java 8 Update 131 genera un’eccezione (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Queste impostazioni di configurazione sono specifiche per i clienti di AEM Forms che utilizzano il servizio Document Security.

NPR-21355 è incluso in CFP12.1. Se si sta installando CFP 12.1 o versione successiva, attenersi alla procedura seguente per configurare NPR-21355 sul server applicazioni JBoss. Se si sta installando CFP12.1 nel server AEM Forms in esecuzione su un server applicazioni Oracle WebLogic o IBM WebSphere, non è richiesta alcuna configurazione aggiuntiva:

1. Esegui il backup, elimina e crea un nuovo file module.xml. Il percorso predefinito del file è [AEM_Forms_Installation_directory]/jboss/module/system/layer/base/com/adobe/livecycle/main/

1. Apri il file module.xml appena creato per modificarlo. Aggiungi al file il codice seguente:

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

1. Crea un backup dei file jsafeFIPS.jar, jsafeJCEFIPS.jar e certjFIPS.jar disponibili in [AEM_Forms_Installation_directory]/jboss/module/system/layer/base/com/adobe/livecycle/main/ ed elimina i file dalla directory sopra indicata.

   Per ottenere nuovi file JAR, contatta il servizio di [supporto Adobe](https://helpx.adobe.com/it/marketing-cloud/contact-support.html). Inserisci i file JAR ottenuti dal [supporto Adobe](https://helpx.adobe.com/it/marketing-cloud/contact-support.html) in [AEM_Forms_Installation_directory]/jboss/module/system/layer/base/com/adobe/livecycle/main/

1. (Solo per Windows) Modifica il file di configurazione `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` o `domain.conf.bat`:

   * In caso di server JBoss in configurazione standalone, apri il file standalone.conf.bat per la modifica.
   * In caso di server JBoss in configurazione cluster, apri il file domain.conf.bat per la modifica.

   Aggiungi le seguenti righe alla fine e salvare il file:

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. (Solo sistemi operativi basati su Linux) Modifica i file di configurazione [AEM_Forms_Installation_directory]/jboss/standalone.conf o domain.conf:

   * In caso di server JBoss in configurazione standalone, apri il file standalone.conf per la modifica.
   * In caso di server JBoss in configurazione cluster, apri il file domain.conf per la modifica.

   Aggiungi le seguenti righe alla fine e salvare il file:

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## Impostazioni di configurazione richieste per NPR-19778 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>NPR-19778 fa parte di CFP14.

Quando un utente richiede un’attività, per impostazione predefinita il conteggio della coda condivisa non viene aggiornato per gli altri utenti. Per questo è stata introdotta una nuova proprietà. Per configurare questa proprietà in un’istanza di AEM, segui la procedura seguente:

1. Accedi all’interfaccia utente Amministratore -> Servizi -> Area di lavoro -> Amministrazione globale.
1. Esporta le impostazioni globali.
1. Nel file XML scaricato, aggiungi il tag `<client_tasksPollingInterval>10</client_tasksPollingInterval>`. In questo caso, 10 è il valore di esempio in secondi. È possibile modificarlo in base alle proprie esigenze.
1. Salva il file.
1. Torna all’interfaccia utente Amministratore -> Servizi -> Area di lavoro -> Amministrazione globale.
1. Importa il file XML nella sezione Importa impostazioni globali.
1. Ora puoi uscire dal sistema e accedere di nuovo.
1. Il conteggio della coda condivisa si aggiorna anche per gli altri utenti dell’area di lavoro.
1. Per disattivare il limite di polling, impostare il valore su 0 e importare di nuovo il file XML.

## Modifiche all’interfaccia utente {#ui-changes}

* È stata modificata la modalità di visualizzazione dei titoli nella scheda Immagine per le immagini con la proprietà dc: title impostata su String [] (multicampo): nell’interfaccia utente, nella scheda Immagine verrà visualizzato solo l’ultimo titolo modificato; tutti i titoli saranno comunque salvati in CRX. Hotfix per CQ-4217165

## Problemi noti {#known-issues}

* Se si aggiornano AEM 6.2SP1-CFP19 e AEM 6.2SP1-CFP20 da CFP18, il reindirizzamento porta alla pagina iniziale dell’interfaccia classica e non più a /sites.html/content. Potrebbe essere necessario correggere la proprietà di destinazione sling: da /welcome.html a /index.html con CRX Explorer. Questo problema non viene rilevato se si esegue l’aggiornamento da CFP17 o versione precedente.

I seguenti errori temporanei possono verificarsi quando si installa AEM 6.2 SP1-CFPx. Per questi errori, tuttavia, non è prevista una soluzione poiché non influiscono sull’istanza di AEM e spariscono dopo l’installazione del CFP:

* Quando si esegue l’aggiornamento da un’istanza AEM 6.2SP1-CFP20 a AEM 6.5, è possibile che alcuni URL personalizzati non funzionino, ad esempio:

   * */projects.html*
   * */sites.html*

Questo viene risolto riavviando l’istanza di AEM dopo un aggiornamento.

* Quando si apre la pagina dei dettagli del componente WebConsole, viene visualizzato il messaggio “HTTP 500 - Errore interno del server”.
* A causa del riavvio del repository si verificano errori quali **create component instance** e **Service factory returned null**:

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Cannot create component instance due to failure to bind reference profileManager
   * org.apache.sling.commons.scheduler FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Componente: com.day.cq.tagging.impl.TagGarbageCollector (1687))

* Errore rilevato nell’installazione di CFP in Mongo e DB2: **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Eccezione: java.lang.NullPointerException**. Questo errore non si verificherà dopo l’installazione di un CFP su CFP8.
* (Adobe Granite Maintenance Scheduler Update Task) com.adobe.granite.maintenance.impl.TaskScheduler: No maintenance task found with name WorkflowPurgeTask for window granite:weekly
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
* Quando si installa CFPx su AEM 6.2 SP1 che include il feature pack Smart Tags, il passaggio del flusso di lavoro precedentemente aggiunto per le risorse con tag avanzati viene eliminato dal flusso di lavoro DAM Aggiorna risorse.

Consulta l’elenco dei [Problemi noti in AEM 6.2 SP1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known Issues).

## JAR Uber {#uber-jar}

Il file JAR Uber per 6.2 SP1-CFP20 è disponibile nell’[archivio pubblico Maven di Adobe](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/).

Per utilizzare il file JAR Uber in un progetto Maven, includi la seguente dipendenza nel POM di progetto:

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## Bundle OSGi e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-5}

Nei documenti di testo seguenti sono elencati i bundle OSGi e i pacchetti di contenuti inclusi nel CFP.

* [Elenco dei bundle OSGi inclusi in AEM 6.2 SP1-CFP20](assets/do-not-localize/updated.txt)
* [Elenco dei pacchetti di contenuti inclusi in AEM 6.2SP1-CFP20](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [Pagina degli hotfix di AEM 6.2](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates.html?lang=it)
>* [Note sulla versione di AEM 6.2 SP1](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [Note sulla versione di AEM 6.2](https://docs.adobe.com/docs/en/aem/6-2/release-notes.html)
>* [Pagina del prodotto AEM](http://www.adobe.com/it/solutions/web-experience-management.html)
>* [Documentazione di AEM 6.2](https://docs.adobe.com/content/docs/en/aem/6-2.html)
>* [Adobe Priority Product Updates](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it)
