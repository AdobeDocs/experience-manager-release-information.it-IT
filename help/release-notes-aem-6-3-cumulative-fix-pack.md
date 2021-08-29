---
title: AEM 6.3 Cumulative Fix Pack
description: Note sulla versione AEM 6.3 Cumulative Fix Pack.
source-git-commit: 3c798116db7314f4220f8a183a989c2b37678054
workflow-type: tm+mt
source-wordcount: '15916'
ht-degree: 99%

---

# Note sulla versione AEM 6.3 Cumulative Fix Pack {#release-notes-aem-cumulative-fix-pack}

## Informazioni sulla versione {#release-information}

| **Prodotto** | Adobe Experience Manager |
|---|---|
| **Versione** | 6.3 |
| **Versione** | Cumulative Fix Pack 6.3.3.8 in [PackageShare](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8), [Sofware Distribution (Beta)](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) |
| **Prerequisito** | [AEM 6.3 Service Pack 3 (6.3.3.0)](https://helpx.adobe.com/it/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **Disponibilità generale** | 5 marzo 2020 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe ha introdotto un unico modello di distribuzione per il rilascio delle correzioni. Invece di rilasciare hotfix per singoli problemi, Adobe rilascia ogni mese un Cumulative Fix Pack (CFP) (soggetto a controlli di qualità), che è un pacchetto di contenuti che aggrega più correzioni. I CFP includono principalmente correzioni di bug, ma possono includere anche Feature Pack. Offrono i seguenti vantaggi rispetto ai singoli hotfix:

* Natura cumulativa (ad esempio, un CFP contiene gli aggiornamenti distribuiti con CFP precedenti)
* Maggiore garanzia di qualità
* Installazione semplificata (l’utente installa un CFP come pacchetto singolo senza alcuna dipendenza, ad eccezione dell’ultimo service pack)

Per ulteriori informazioni sul CFP e su altri tipi di versioni, consulta [Definizioni relative alle versioni di aggiornamento](https://docs.adobe.com/content/docs/en/aem/6-3/deploy/maintenance-release-vehicle-definitions.html).

## Informazioni sulla versione {#about-the-release}

AEM Cumulative Fix Pack 6.3.3.8 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 3 (6.3.3.0) nel settembre 2018.

AEM Cumulative Fix Pack 6.3.3.8 dipende da AEM 6.3 Service Pack 3. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.3.x dopo aver installato AEM 6.3 Service Pack 3. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Gli elementi di rilievo di **AEM Cumulative Fix Pack** sono:

* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.20.

>[!CAUTION]
>
>Se si applica il CFP senza aver prima convalidato la compatibilità tra i Feature Pack installati, potrebbe verificarsi un errore di sistema o la perdita delle configurazioni personalizzate, per la cui soluzione potrebbe essere necessario eseguire il ripristino dal backup.

>[!NOTE]
>
>Per le stanze di AEM con una versione precedente alla 6.3.3.0, Adobe consiglia di distribuire SP/CFP tramite la cartella di installazione per i clienti che hanno un numero elevato di utenti dell’istanza AEM.

>[!NOTE]
>
>MongoDB Enterprise 3.6 è supportato a partire da AEM versione 6.3.3.1.

## Elenco dei problemi {#changes}

In questa sezione sono elencati tutti i problemi e gli hotfix inclusi nel CFP corrente.

Questo CFP include inoltre gli hotfix distribuiti in [Cumulative Fix Pack precedenti](#previous).

### Assets {#assets}

* La pagina Aggiungi alla raccolta non mostra tutte le raccolte disponibili in Vista schede quando si aggiungono risorse alla raccolta (NPR-32537).

### Sites {#sites}

* Quando si selezionano un parsys e un componente al suo interno e si utilizza la scelta rapida da tastiera per eliminare gli elementi selezionati, l’azione elimina sia il componente che i relativi parsys padre (NPR-32071).
* Quando si salvano le proprietà di una pagina, viene creato un nodo non corretto (NPR-31774).

### Integrations (Integrazioni) {#integrations}

* ReportSuitesServlet è vulnerabile a SSRF (NPR-32162).

### Campaign Targeting {#campaign-targeting}

* Il contenuto di un componente modificato nell’istanza Author e quindi attivato, non è visibile nell’istanza Pubblica finché il componente non viene riavviato **com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489 e NPR-32232).
* Le prestazioni di Contexthub si bloccano durante la pubblicazione (NPR-31170).

### Brand Portal {#brand-portal}

* Adobe I/O non è integrato con Adobe Experience Manager 6.3 per Brand Portal (NPR-32056).

### Forms {#forms}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

#### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package}

>[!NOTE]
>
>I pacchetti di componenti aggiuntivi per AEM Forms consentono di allineare le funzionalità di Forms ai Service Pack e i Cumulative Fix Pack di AEM. È quindi obbligatorio installare il pacchetto di componenti aggiuntivi per AEM Forms dopo aver installato eventuali Service Pack, Cumulative Fix Pack o Feature Pack di AEM.

* Designer: se l’opzione relativa ai tag è abilitata, il bordo del sottomodulo scompare nell’output del PDF generato (NPR-32324 e NPR-32545).
* Designer: se in una tabella sono presenti celle unite, il test di accessibilità non riesce per il file PDF di output convertito da un modulo XDP utilizzando l’apposito servizio (NPR-32068).
* Sicurezza dei documenti: errore nell’apertura offline di un file PDF protetto con l’opzione `DisableGlobalOfflineSynchronizationData` impostata su `True` (NPR-32080).

## Hotfix e Feature Pack inclusi nei Cumulative Fix Pack precedenti {#previous}

### Cumulative Fix Pack 6.3.3.7 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.3.3.7 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 3 (6.3.3.0) nel settembre 2018.

AEM Cumulative Fix Pack 6.3.3.7 dipende da AEM 6.3 Service Pack 3. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.3.x dopo aver installato AEM 6.3 Service Pack 3. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Risorse {#assets-1}

* Vengono spostate anche le risorse selezionate (nella vista a colonne dell’interfaccia touch) prima di selezionare l’opzione di filtro dall’elenco a discesa Solo contenuto e quindi l’opzione di spostamento (NPR-30693).
* La variabile `${extension}` non viene rappresentata nell’istanza di creazione durante l’elaborazione del flusso di lavoro (NPR-31694).
* Il valore di scadenza (durata della cache del client) configurato per la modalità ibrida di Dynamic Media non viene replicato nell’ambiente di distribuzione di Dynamic Media (NPR-31114).
* Le risorse vengono replicate nell’istanza di pubblicazione dall’istanza di creazione in esecuzione nell’implementazione di Dynamic Media - Scene7 anche dopo l’utilizzo di filtri predefiniti (NPR-30856).

### Sites {#sites-1}

* Le proprietà di una pagina mastro non vengono caricate e viene restituita un’eccezione NullPointerException. Il problema è stato risolto con l’aggiunta della proprietà cq:blueprint (NPR-30901).
* Le configurazioni di rollout non vengono recuperate correttamente da blueprintConfig sul nodo principale. Viene attivata la disattivazione sia per le blueprint che per le Live Copy. La disattivazione deve essere attivata solo per le blueprint (NPR-30866).
* Quando un utente effettua il rollout di una pagina, nella finestra di dialogo della configurazione di rollout vengono visualizzati percorsi di Live Copy duplicati (NPR-30438).
* Come impostazione predefinita, lo scaffolding Editor Rich Text applica in modo imprevisto la dimensione del font inline agli elementi (NPR-31283, NPR-30922).
* Impossibile sincronizzare in Adobe Campaign la campagna che contiene il componente predefinito Importazione progettazione (NPR-30890).
* Editor Rich Text non consente di inserire una tabella incorporata come voce di elenco (NPR-30878).
* Quando un utente usa i campi della barra a sinistra e una scelta rapida da tastiera per incollare il contenuto, viene incollato il contenuto degli Appunti dell’Editor pagina invece del contenuto copiato dai campi della barra a sinistra (NPR-31173).
* Quando un utente modifica un frammento di contenuto, viene ripristinata la variante già eliminata del frammento di contenuto (NPR-31272).
* In AEM Sites non è presente l’opzione per creare una copia per lingua (NPR-30690).
* Nelle azioni dell’Editor pagina non sono presenti i controlli per il rollout delle Live Copy (NPR-30613).

### Communities {#communities}

* I titoli di Attività e Notifiche non sono coerenti (NPR-30940).
* I rapporti di Analytics non vengono compilati nell’ambiente di authoring di AEM. Viene visualizzata una pagina vuota (NPR-30905).
* La paginazione non funziona correttamente nei blog di Communities (NPR-30827).

### Foundation {#foundation}

* Gli aggiornamenti nella configurazione della dimensione del buffer per il servizio HTTP basato su Jetty non vengono salvati (NPR-30925).

### Forms {#forms-1}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-1}

>[!NOTE]
>
>I pacchetti di componenti aggiuntivi per AEM Forms consentono di allineare le funzionalità di Forms ai Service Pack e i Cumulative Fix Pack di AEM. È quindi obbligatorio installare il pacchetto di componenti aggiuntivi per AEM Forms dopo aver installato eventuali Service Pack, Cumulative Fix Pack o Feature Pack di AEM.

#### Moduli adattivi {#adaptive-forms}

* I valori a virgola mobile calcolati utilizzando uno script non vengono visualizzati correttamente in un modulo che fa parte di un set moduli (NPR-30802).

#### Moduli HTML5 {#html-forms}

* Quando si genera l’anteprima HTML5 di un modulo XDP, viene visualizzato uno sfarfallio durante l’aggiunta di istanze di un sottomodulo (NPR-30908).

### Programma di installazione JEE per Forms {#forms-jee-installer}

#### Servizi documentali {#document-services}

* OutputService visualizza una risposta errata dopo l’applicazione di una patch per correggere i problemi di conversione da HTML a PDF (NPR-31504).

#### Servizio PDFG {#pdfg-service}

* Il conteggio massimo dei riutilizzi con la console JMX non viene visualizzato per il servizio HTML2PDF (NPR-30305).

#### JEE per Foundation {#foundation-jee}

* Il conteggio massimo dei riutilizzi con la console JMX non viene visualizzato per il servizio HTML2PDF (NPR-30136).

### Cumulative Fix Pack 6.3.3.6 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.3.3.6 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 3 (6.3.3.0) nel settembre 2018.

AEM Cumulative Fix Pack 6.3.3.6 dipende da AEM 6.3 Service Pack 3. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.3.x dopo aver installato AEM 6.3 Service Pack 3. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Risorse {#assets-2}

* Con l’aggregazione video effettuata da Dynamic Video vengono restituiti solo i primi 100 elementi del set di risultati. NPR-30441: Hotfix per CQ-4213561
* Problema di connettività di Tag avanzati di Adobe tramite DataPower. NPR-30026: Hotfix per CQ-4269457
* Non è possibile utilizzare l’interfaccia di Assets per decomprimere e aprire un archivio contenente una cartella il cui nome include un segno di percentuale (%). NPR-29989: Hotfix per CQ-4270467
* Quando si elaborano risorse secondarie di file PDF di grandi dimensioni, viene generata un’eccezione OutOfMemoryError (OOME). NPR-29851: Hotfix per CQ-4269574

### Sites {#sites-2}

* Errore di ContextHub durante l’integrazione di AEM e Campaign. NPR-30624: Hotfix per CQ-4250790
* Le proprietà dei metadati “onTime” o “offTime” salvate nelle risorse non vengono richiamate in caso di riavvio del server AEM. NPR-30412: Hotfix per CQ-4272784
* Se, durante la generazione di un’esportazione CSV, vengono aggiunte colonne personalizzate per la vista a elenco, il rapporto viene interrotto. NPR-30208: Hotfix per CQ-4273344
* I rapporti OOTB in /etc/reports/ non funzionano correttamente e il grafico dei dati della cronologia non viene visualizzato. NPR-30016: Hotfix per CQ-4220180
* Il valore del parametro di richiesta resourceType viene copiato nel valore di un attributo di tag HTML che è racchiuso tra virgolette doppie. NPR-29832: Hotfix per CQ-4255365

### Community {#communities-1}

* Problema di contenuto duplicato relativo alla console di moderazione di AEM Communities. NPR-30667: Hotfix per CQ-4276829

### Traduzione {#translation}

* Problema di traduzione - Solo alcuni componenti vengono tradotti utilizzando la traduzione automatica. NPR-30079: Hotfix per CQ-4273764
* Se si utilizza il framework di traduzione, viene generato un errore quando si aggiungono pagine a più processi di traduzione. NPR-29746: Hotfix per CQ-4270953

### Forms {#forms-2}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-2}

>[!NOTE]
>
>I pacchetti di componenti aggiuntivi per AEM Forms consentono di allineare le funzionalità di Forms ai Service Pack e i Cumulative Fix Pack di AEM. È quindi obbligatorio installare il pacchetto di componenti aggiuntivi per AEM Forms dopo aver installato eventuali Service Pack, Cumulative Fix Pack o Feature Pack di AEM.

#### Moduli HTML5 {#html-forms-1}

* Quando si utilizza l’accesso desktop non visivo in modalità Sfoglia per leggere un modulo HTML5, il browser Chrome legge l’elemento “grafico” prima di qualsiasi file SVG nella struttura del modulo. NPR-30451: Hotfix per CQ-4274732

#### Forms - Integrazione back-end {#forms-backend-integration}

* Impossibile visualizzare il servizio o l’origine dati per la connessione al database durante la creazione del modello dati del modulo. NPR-30108: Hotfix per CQ-4273359

### Programma di installazione JEE per Forms {#forms-jee-installer-1}

#### Forms - Servizi basati su documenti {#forms-document-services}

* Quando si esegue un test di caricamento su un servizio di conversione da HTML a PDF, il test non riesce, viene restituito un errore e le impostazioni del tipo di file vengono rimosse dal server AEM Forms. NPR-30111, NPR-30086: Hotfix per CQ-4271495

### Cumulative Fix Pack 6.3.3.5 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.3.3.5 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 3 (6.3.3.0) nel settembre 2018.

AEM Cumulative Fix Pack 6.3.3.5 dipende da AEM 6.3 Service Pack 3. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.3.x dopo aver installato AEM 6.3 Service Pack 3. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Gli elementi di rilievo di **AEM Cumulative Fix Pack** sono:

* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.17.

### Risorse {#assets-3}

* Aggiornamento dell’interfaccia DMGateway di DAM per il supporto multipart di S3. NPR-29740: Hotfix per Q-4226303
* Impossibile eliminare un rendering immagini su una risorsa video dalla pagina dei dettagli della risorsa. NPR-29417: Hotfix per CQ-4268675
* Il proprietario non può creare una cartella privata all’interno di una cartella privata. NPR-29397: Hotfix per CQ-4229830
* Viene generato un errore di spazio di heap Java quando si carica un file di grafica di Adobe Illustrator di dimensioni superiori a 2 GB. NPR-29265: Hotfix per CQ-4226217
* Le risorse diventano inutilizzabili dopo l’applicazione del testo per m3u8 nel servizio del tipo MIME cq di DAM. NPR-29259: Hotfix per CQ-4264052
* L’opzione Crea non funziona durante il tentativo di creazione di raccolte in Edge. NPR-29248: Hotfix per CQ-4265699 e CQ-4265438
* Nella condivisione dei collegamenti delle risorse vengono visualizzate schede grigie vuote per alcune risorse presenti nella cartella. NPR-29831: Hotfix per CQ-4270187
* I nuovi tag aggiunti alle risorse non vengono salvati né rimossi dalle proprietà. Hotfix per CQ-4271931, CQ-4270476

### Sites {#sites-3}

* Se utilizzato con Multifield, CoralUI memorizza il parametro fileReferenceParameter a livello di componente anziché a livello di multicampo. NPR-29535: Hotfix per CQ-4266129
* Si verifica un problema quando si prova a confrontare la versione corrente e quella più recente della pagina in AEM 6.3.3.3. NPR-29532: Hotfix per CQ-4269639
* Il campo del percorso viene aperto nel percorso principale indipendentemente dal percorso specificato per la ricerca. NPR-29398: Hotfix per CQ-4268897
* (Frammenti di esperienza) FacebookApplication#setUpApp utilizza un’API obsoleta, che non funziona più. NPR-29213: Hotfix per CQ-4266630
* Viene generato un avviso di errore durante l’aggiunta di componenti alla pagina WCM quando nell’istanza è abilitata la minificazione. NPR-29476: Hotfix per CQ-4266197
* Le proprietà vuote e multiple non vengono propagate dalla blueprint durante il rollout. La reimpostazione della Live Copy con la blueprint non funziona per i componenti. NPR-29252: Hotfix per CQ-4264928, CQ-4264926, CQ-4267722
* Se si riduce a icona la finestra a schermo intero di Editor Rich Text nella modalità di modifica dell’origine, si verifica una perdita di contenuto. NPR-28838: Hotfix per CQ-4260584

### Community {#communities-2}

* Visitatori e membri senza privilegi di moderatore possono visualizzare post non approvati e in sospeso incollando l’URL. NPR-29726: Hotfix per CQ-4271124
* Durante l’accesso dell’utente alla community è possibile notare un tempo di risposta elevato, fino a 40-50 secondi. NPR-29679: Hotfix per CQ-4269444
* Impossibile ripristinare la password quando si effettua l’accesso con un nome utente e un indirizzo e-mail diversi, poiché la chiave sembra essere stata generata con un nome utente e un indirizzo e-mail scambiati. NPR-29281: Hotfix per CQ-4268694

### Frammenti di esperienza {#experience-fragments}

* Impossibile esportare i frammenti di esperienza nella destinazione quando si utilizza l’immagine intelligente. Hotfix per CQ-4269606

### Replica {#replication}

* Il componente Agente di replica è soggetto a una vulnerabilità per cui informazioni sensibili vengono rivelate a utenti non autorizzati. NPR-29613: Hotfix per GRANITE-25070
* I dati forniti dall’utente non sono preceduti dall’escape nell’output nel componente `cq/replication/components/agent` e causano la memorizzazione di una vulnerabilità cross-site scripting (XSS). NPR-29452: Hotfix per CQ-4266263

### Forms {#forms-3}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-3}

* Il pacchetto di componenti aggiuntivi per Forms non contiene nuove correzioni per AEM Forms.

### Programma di installazione JEE per Forms {#forms-jee-installer-2}

* Il programma di installazione JEE per Forms non contiene nuove correzioni per AEM Forms.

### Bundle OSGi e pacchetti di contenuti inclusi nella versione 6.3.3.5 {#osgi-bundles-and-content-packages-included-in}

Elenco dei bundle OSGi inclusi in AEM 6.3.3.5

[Ottieni file](assets/do-not-localize/6_5-bundle-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.3.3.5

[Ottieni file](assets/do-not-localize/content_packages6335.txt)

### Cumulative Fix Pack 6.3.3.4 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.3.3.4 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 3 (6.3.3.0) nel settembre 2018.

AEM Cumulative Fix Pack 6.3.3.4 dipende da AEM 6.3 Service Pack 3. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.3.x dopo aver installato AEM 6.3 Service Pack 3. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Gli elementi di rilievo di **AEM Cumulative Fix Pack** sono:

* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.16.
* Aggiunta dei timeout per socket e connessione negli agenti di replica di Brand Portal.

### Risorse {#assets-4}

* Se si ricarica un archivio con lo stesso nome, non vengono generate le rappresentazioni per le nuove risorse elaborate. NPR-28643: Hotfix per CQ-4262286
* Il flusso di lavoro CommandLineProcess non riesce se il nome file contiene virgolette singole. NPR-28805: Hotfix per CQ-4262287
* I valori della pagina della raccolta sono diversi rispetto alla pagina della raccolta filtrata. NPR-28642: Hotfix per CQ-4261405
* Quando si caricano risorse di archivio ZIP di grandi dimensioni, viene attivata l’eccezione CommitFailedException. NPR-28528: Hotfix per CQ-4260903
* I metadati della cartella non vengono salvati quando si modifica una cartella che contiene caratteri speciali. NPR-28211: Hotfix per CQ-4260401
* Impossibile eliminare i rendering immagini di una risorsa video dalla pagina Dettagli risorsa. NPR-29149: Hotfix per CQ-4266073
* Per la distribuzione di video desktop DMS7 con DMComponent viene utilizzato il download progressivo invece dello streaming per la riproduzione di video in modalità di pubblicazione. NPR-28754: Hotfix per CQ-4263732
* Impossibile creare/modificare i predefiniti immagine perché la limitazione dell’accesso a /etc/dam/video/dynamicmedia comporta la disattivazione delle funzioni per i gestori di immagini. NPR-28662: Hotfix per CQ-4263022
* Se si esegue Condivisione collegamenti utilizzando file video con codifica DMS7, vengono generate cartelle vuote. NPR-28851: Hotfix per CQ-4206743
* La replica da AEM a Brand Portal si blocca per lunghi periodi. NPR-28913: Hotfix per CQ-4254932

### Community {#communities-3}

* Impossibile aprire messaggi con allegati nelle cartelle Posta inviata e Posta in arrivo di Outlook. NPR-28559: Hotfix per CQ-4217072

### Sites {#sites-4}

* Vulnerabilità cross-site scripting (XSS) in SuggestionHandler per la versione 6.3. NPR-28692: Hotfix per CQ-4253821
* Il rollout profondo termina senza includere tutti i rami nella rispettiva Live Copy. NPR-29175: Hotfix per CQ-4239472
* (MSM) Implementa LiveCopyIndex utilizzando l’indice OAK. NPR-29198: Hotfix per CQ-4222472
* Il file coral.js include una versione vulnerabile della libreria handlebars.js. NPR-26973: Hotfix per CQ-4255377
* Se si utilizza un componente Target con un contenitore di layout e un componente testo nidificati, viene generato un errore JavaScript di tipo “Impossibile leggere la proprietà currentPos pari a null” quando si modifica il testo o si fa clic sul contenitore. NPR-29077: Hotfix per CQ-4246594
* (Interfaccia touch) Impossibile aggiornare in blocco i tag in pagine a cui sono già assegnati tag diversi. NPR-28729: Hotfix per CQ-4262922
* Quando si apre la variante nella vista a schede, viene generato un errore 500. NPR-28611: Hotfix per CQ-4263571
* Se si esegue il rollout di una struttura spostata in una pagina mastro, cq:moveTarget non viene eseguito correttamente. NPR-28968: Hotfix per CQ-4265280

### Integrazione {#integration}

* (Configurazioni servizi cloud) La casella di controllo “Ereditato da” visualizzata al livello principale deve essere rimossa. NPR-28771: Hotfix per CQ-4259676
* com.day.cq.personalization.impl.TeaserResourceEventHandler genera un ciclo infinito e causa aggiornamenti ai nodi nelle istanze di pubblicazione. NPR-28561: Hotfix per CQ-4263096
* L’utilizzo delle credenziali Brightedge non riesce e viene restituito un errore di connessione. NPR-29167: Hotfix per CQ-4265872
* Problema di compilazione in OfferproxyTandtProvider.java a causa di un’istruzione di importazione mancante per la classe Resource. Istruzione import mancante: import org.apache.sling.api.resource.Resource. NPR-28772

### Commerce {#commerce}

* L’opzione di ordinamento non funziona per le risorse all’interno della raccolta Commerce. NPR-28755: Hotfix per CQ-4213622

### Jetty {#jetty}

* Eccezioni Jetty in error.log ogni 302 reindirizzamenti dopo l’installazione di CFP2 sulla versione 6.3.3. NPR-28606: Backport per CQ-4262844

### Interfaccia utente - Foundation {#ui-foundation}

* Se si fa clic su un tag, viene rimosso l’evento globale di rilascio del mouse e la finestra di dialogo rimane bloccata nella “modalità trascinabile”. NPR-28641: Hotfix per CUI-7294

### WCM - MSM {#wcm-msm}

* Il rollout PushOnModify per lo spostamento di PageManager viene confermato più volte da due sessioni causando una race condition. NPR-28880: Hotfix per CQ-4266191

### Vulnerabilità {#vulnerability}

* Il framework di protezione CSRF non funziona con i moduli di AEM Foundation. NPR-28612: Hotfix per GRANITE-22231

### Forms {#forms-4}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

Gli elementi di rilievo di AEM Forms sono:

* Abilitazione dell’opzione per la selezione di elementi per pagina nella pagina per la visualizzazione dei set di criteri.
* Aggiunta della funzionalità di condivisione coda per tutti i browser.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-4}

#### Forms - Flusso di lavoro {#forms-workflow}

* Con l’attività di risposta della coda condivisa viene aperto un elemento Flash nell’area di lavoro HTML5. NPR-29161: Hotfix per CQ-4266498
* Impossibile inviare da Workspace se il pulsante contiene il carattere umlaut. NPR-29014: Hotfix per CQ-4263172

#### Forms - Sicurezza dei documenti {#forms-document-security}

* Abilitazione dell’opzione per la selezione di elementi per pagina nella pagina di visualizzazione dei set di criteri. NPR-29243: Hotfix per CQ-4268567 e CQ-4265132

#### Forms - Servizi basati su documenti {#forms-document-services-1}

* L’assemblatore di OSGi Forms non funziona con file Acrobat. NPR-29049: Hotfix per CQ-4254426

#### Moduli HTML5 {#html-forms-2}

* Durante l’anteprima di un file XDP come PDF si verifica un comportamento diverso rispetto all’anteprima dello stesso file XDP come HTML in Designer. NPR-28602: Hotfix per CQ-4260239

### Programma di installazione JEE per Forms {#forms-jee-installer-3}

* Il programma di installazione JEE per Forms non contiene nuove correzioni per AEM Forms.

### Bundle OSGi e pacchetti di contenuti inclusi nella versione 6.3.3.4 {#osgi-bundles-and-content-packages-included-in-1}

Elenco dei bundle OSGi inclusi in AEM 6.3.3.4

[Ottieni file](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

Elenco dei pacchetti di contenuti inclusi in AEM 6.3.3.4

[Ottieni file](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Cumulative Fix Pack 6.3.3.3 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.3.3.3 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 3 (6.3.3.0) nel settembre 2018.

AEM Cumulative Fix Pack 6.3.3.3 dipende da AEM 6.3 Service Pack 3. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.3.x dopo aver installato AEM 6.3 Service Pack 3. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Gli elementi di rilievo di **AEM Cumulative Fix Pack** sono:

* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.16.
* La paginazione dell’elenco di impostazioni criteri viene limitata a 50 record per pagina.
* Aggiunta della cache di rep: in nodi ignorabili a livello del listener di sincronizzazione utenti di AEM Communities nelle istanze di pubblicazione.
* Aggiunta dell’attributo aria-label per il pulsante della vista a elenco e a schede.
* Aggiunta di un carattere di escape per la virgola quando viene eseguita una ricerca.
* Abilitazione del supporto delle risorse sintetiche per criteri del contenuto.

#### Risorse {#assets-5}

* Impossibile scaricare più file di tipo .jp2, .max, .oft, .msg. NPR-28002: Hotfix per CQ-4210856
* Le impostazioni di pubblicazione di ImageServer non vengono replicate nella distribuzione ibrida. NPR-28329: Hotfix per CQ-4253030

#### Community {#communities-4}

* Attivazione della navigazione tramite tastiera per i componenti di Attivazione per AEM Communities durante la pubblicazione. NPR-27739: Hotfix per CQ-4253856
* Attivazione della navigazione tramite tastiera per attivare la riproduzione dei contenuti. NPR-27738: Hotfix per CQ-4254026
* Aggiunta dell’attributo aria-label per il pulsante della vista a elenco e a schede. NPR-27736: Hotfix per CQ-4254027
* (Backport) Aggiunta della cache di rep: in nodi ignorabili a livello del listener di sincronizzazione utenti di AEM Communities nelle istanze di pubblicazione. NPR-27841: Hotfix per CQ-4247234
* Ai caratteri speciali viene aggiunto come prefisso il carattere di escape (\) nella casella di ricerca a livello di interfaccia utente. NPR-27839: Hotfix per CQ-4259757
* Errore durante la ricerca di caratteri come ( , +, ? nella ricerca rapida. NPR-28212: Hotfix per CQ-4260969
* Impossibile utilizzare l’API per eliminare i commenti nei contenuti generati dagli utenti (UGC, User-Generated Content). NPR-28075: Hotfix per CQ-4260534
* I commenti pubblicati nella pagina successiva vengono evidenziati in giallo quando viene pubblicato un nuovo commento. NPR-28148: Hotfix per CQ-4259681
* Impossibile aprire messaggi con allegati nella cartella Posta inviata e Posta in arrivo di Outlook. NPR-28559: Hotfix per CQ-4217072

#### Sites {#sites-5}

* Quando si esegue Pulizia delle versioni in AEM 6.3, viene aggiunto un avviso ripetuto nei registri. NPR-27750: Hotfix per CQ-4206870
* Il plug-in dello stile non è supportato nella modalità a schermo intero dell’Editor Rich Text. NPR-27622: Hotfix per CQ-4258674
* L’elenco loaderPromises non viene cancellato dopo il caricamento del frame del contenuto in editor.js. NPR-27768: Hotfix per CQ-4205337
* Impossibile impostare i criteri dei modelli nel componente parsys nidificato senza impostare il componente padre. NPR-27987: Hotfix per CQ-4246095
* Il browser componenti non bonifica l’input dell’utente e si possono quindi verificare errori JavaScript. NPR-27986: Hotfix per CQ-4247590
* La pagina visualizzata è vuota quando l’utente prova a modificare il frammento di contenuto. NPR-27669
* L’evidenziazione dell’annotazione scompare non appena l’utente fa clic sull’annotazione. BPR-27196: Hotfix per CQ-4254423

#### Integrazione {#integration-1}

* ResourceResolver non risolve più domini per il componente Target. NPR-28265: Hotfix per CQ-107847
* L’annullamento dell’ereditarietà Live Copy non funziona correttamente sui contenitori di destinazione in quanto non vengono visualizzate azioni. NPR-28129: Hotfix per CQ-4259813

#### Replica {#replication-1}

* Interruzione della replica con DispatcherFlushRules nella versione 6.3.3.1. NPR-28150: Hotfix per CQ-4261401

#### Campaign - Targeting {#campaign-targeting-1}

* Eccezione NullPointerException in TargetContentManager. Hotfix per CQ-4263485

#### Social - SCORM {#social-scorm}

* Rimozione del riferimento al cloud SCORM (Shared Content Object Reference Model) nel lettore. Hotfix per CQ-4260779

#### DAM - Generale {#dam-general}

* Quando si esegue il download tramite il messaggio e-mail di condivisione del collegamento, viene restituito un file ZIP vuoto o danneggiato. Hotfix per CQ-4259686

#### MAC - Integrazione Test&amp;Target {#mac-test-target-integration}

* L’opzione di configurazione del componente Target non è disponibile per i tipi di pubblico, eccetto quello predefinito. Hotfix per CQ-4261370

#### Traduzione {#translation-1}

* Abilitazione del supporto per il servizio MS Translator in AEM 6.3 dopo l’aggiornamento di MS Translator all’API v3.0. NPR-28365: Hotfix per CQ-4259096

### Forms {#forms-5}

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-5}

#### Forms - Flusso di lavoro {#forms-workflow-1}

* Impossibile eseguire il rendering di PDF Forms nell’area di lavoro HTML5. NPR-28059: Hotfix per CQ-4260373

#### Forms - Servizi basati su documenti {#forms-document-services-2}

* Impossibile visualizzare altri set di criteri oltre ai primi 1000 elencati nella visualizzazione dei set di criteri in Admin Console. NPR-28060, NPR-26047: Hotfix per CQ-4249865
* Viene generata un’eccezione con il nome java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE che impedisce il completamento del processo di breve durata. NPR-28652

#### Forms - Moduli adattivi {#forms-adaptive-forms}

* L’aggiunta o la rimozione di elementi nell’elenco a discesa non viene aggiornata quando si selezionano gli elementi della casella di controllo. NPR-28224: Hotfix per CQ-4252834

### Forms - Programma di installazione JEE {#forms-jee-installer-4}

* Il programma di installazione JEE per Forms non contiene nuove correzioni per AEM Forms.

### Bundle OSGi e pacchetti di contenuti inclusi nella versione 6.3.3.3 {#osgi-bundles-and-content-packages-included-in-2}

Elenco dei bundle OSGi inclusi in AEM 6.3.3.3

[Ottieni file](assets/do-not-localize/6333_bundle_list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.3.3.3

[Ottieni file](assets/do-not-localize/content_package_list_6333.txt)

### Cumulative Fix Pack 6.3.3.2 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.3.3.2 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 3 (6.3.3.0) nel settembre 2018.

AEM Cumulative Fix Pack 6.3.3.2 dipende da AEM 6.3 Service Pack 3. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.3.x dopo aver installato AEM 6.3 Service Pack 3. Per le istruzioni di installazione, consulta le note sulla versione di AEM 6.3 Service Pack 3.

Gli elementi di rilievo di AEM Cumulative Fix Pack sono:

* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.15.
* Aggiunta del supporto per la scheda Regole e la relativa applicazione in Cartella risorse in Schema metadati cartelle.
* Abilitazione del supporto per la paginazione nella pagina di elenco dei gruppi durante la  pubblicazione.
* Abilitazione della notifica unreadCount per la configurazione con qualsiasi numero. Il valore predefinito è impostato su 20.
* Correzioni apportate a Verifica collegamenti esterni.

#### Risorse {#assets-6}

* Il menu a discesa a cascata non è supportato negli elenchi a discesa dinamici. NPR-27044: Hotfix per CQ-4252564
* Miglioramento della query per l’utilizzo della funzione ExpiryNotification. NPR-26999: Hotfix per CQ-4251188
* Migrazione di Regole da Schema metadati a Schema metadati cartelle. NPR-27771: Backport per CQ-4257737, CQ-4257735, CQ-4259822
* Quando si modificano i riferimenti alle risorse, i riferimenti per le risorse che fanno parte di raccolte ResourceCollection Sling non vengono aggiornati. NPR-26759: Hotfix per CQ-4252605
* Quando si esegue il download tramite il messaggio e-mail di condivisione del collegamento, viene restituito un file ZIP vuoto o danneggiato. NPR-27997: Hotfix per CQ-4259686
* La codifica video ibrida non viene completata e non viene creata alcuna miniatura. NPR-27122: Hotfix per CQ-4255080

#### Sites {#sites-6}

* La sospensione della pagina padre rimuove il tipo di mixin cq : LiveRelationship dalla pagina mancante. NPR-26996: Hotfix per CQ-4254113
* (Verifica collegamenti esterni) I collegamenti interni risultano interrotti in singole pagine, ma lo stesso non avviene per i collegamenti esterni. NPR-27481: Hotfix per CQ-4257780
* L’ereditarietà di Configurazione Cloud Service si interrompe quando si modificano altre proprietà della pagina. NPR-27311: Hotfix per CQ-4256785
* Eccezione Null Pointer quando si utilizza un  modulo di Componenti core insieme a un modulo di Foundation. NPR-27333: Hotfix per CQ-4249176
* L’Editor Rich Text rimuove il tag alt vuoto. NPR-26938: Hotfix per CQ-4253267
* (interfaccia classica) Problemi di prestazioni con listener selectionchanged in caso di più elenchi a discesa. NPR-27115: Hotfix per CQ-4237215
* Quando si combina l’Editor Rich Text con più campi, si verifica un errore di tipo “TypeError non rilevato: fieldAPI.getName non è una funzione in foundation.js”. NPR-27146: Hotfix per CQ-4253155, CQ-4259967
* Lo stato attivo o il cursore rimane nell’Editor Rich Text anche quando si fa clic su un pulsante di scelta nel browser Safari. NPR-27144: Hotfix per CQ-4249635
* La pagina visualizzata è vuota quando l’utente prova a modificare il frammento di contenuto. NPR-27669
* Impossibile creare una versione per Frammenti di esperienza. NPR-27689: Hotfix per CQ-4259009

#### Integrazione {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever esamina l’intera struttura per raccogliere i marchi disponibili. NPR-27060: Hotfix per CQ-4255790
* Le azioni   cq : non vengono considerate per un componente di cui è stato eseguito il targeting. NPR-27616: Hotfix per CQ-4257497

#### Sling {#sling}

* Se si utilizza data-sly-use con classi con lo stesso nome, viene prodotto codice non conforme. NPR-27282: Hotfix per Sling-7581

#### Commerce {#commerce-1}

* Aggiornamento ad Apache Felix Http Jetty 4.0.6. NPR-26472: Hotfix per GRANITE-22916

#### DAM - Client DM {#dam-dm-client}

* Dopo la specifica di punti di interruzione nel componente Dynamic Media, non viene visualizzata alcuna immagine. Hotfix per CQ-4256168

#### DAM - Servizi DM {#dam-dmservices}

* MixedMediaSet con video correlato non viene sincronizzato correttamente. Hotfix per CQ-4251650
* La riproduzione video non funziona nell’Editor predefiniti per il visualizzatore di Set di file multimediali diversi. Hotfix per CQ-4251442

#### DAM - Generale {#dam-general-1}

* Il collegamento al modello Frammento di contenuto risulta mancante dopo l’applicazione della patch SP3. Hotfix per CQ-4259029

#### DAM - Interfaccia utente {#dam-ui}

* Errore nell’interfaccia utente di Schema metadati cartelle dopo l’installazione di SP3. Hotfix per CQ-4257737

#### Community {#communities-5}

* Aggiunta del supporto per la paginazione dell’elenco dei gruppi durante la pubblicazione. NPR-26953: Hotfix per CQ-4246525
* Impossibile impostare un valore maggiore di 21 per la notifica del conteggio degli elementi non letti. NPR-27496: Hotfix per CQ-4252829
* Il limite degli abbonamenti utente è limitato a 1000. NPR-27615: Hotfix per CQ-4254689
* Errore durante il caricamento di un allegato in un formato diverso da quello immagine (ad esempio .pdf) nel forum. NPR-27375: Hotfix per CQ-4257753
* Il collegamento per le risposte non funziona quando si fa clic sulla riga. NPR-24556: Hotfix per CQ-4256138
* Le relazioni con contenuti generati dagli utenti (UGC, User-Generated Content) non vengono eliminate in seguito all’eliminazione di tali contenuti. NPR-27631: Hotfix per CQ-4258706
* Impossibile eseguire la ricerca in base al valore dell’indirizzo in Ricerca per parola chiave se la community è impostata con Provider risorsa di archiviazione database (DSRP). NPR-27652: Hotfix per CQ-4253261
* Facendo clic sull’icona del cestino sull’immagine dopo la conferma di eliminazione, l’allegato viene rimosso definitivamente. NPR-27340: Hotfix per CQ-4255150
* I post e le risposte del forum vengono aggiunti all’inizio della seconda pagina e, dopo l’aggiornamento, il post si sposta nella posizione corretta all’inizio della prima pagina. NPR-27341: Hotfix per CQ-4247338
* L’etichetta dello stato per il completamento dell’attivazione di una risorsa SCOR risulta vuota nell’interfaccia utente. NPR-27152: Hotfix per CQ-4249994
* Quando si abilita “Consenti membri privilegiati”, i membri con le autorizzazioni necessarie dovrebbero essere in grado di comporre solo per gli utenti che sono membri della community. NPR-27901: Hotfix per CQ-4251235

#### Manutenzione {#sustenance}

* I registri attività di Gestione pacchetti devono essere estratti in un file di registro separato. NPR-27323: Hotfix per GRANITE-14866

#### Traduzione {#translation-2}

* L’anteprima della traduzione non funziona con i contenuti di esempio we.retail. NPR-27170: Hotfix per CQ-4241179

* Correzioni proattive per platform.login. NPR-26961
* Quando si sceglie Salva e chiudi nelle proprietà della pagina, non viene visualizzata la pagina  corretta in AEM WAR con Tomcat. NPR-27567: Hotfix per GRANITE-23671

* Il testo immesso viene perso tramite la funzione sourceEdit dopo essere stato salvato. Hotfix per CQ-4259273

### Forms {#forms-6}

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-6}

#### Forms - Sicurezza dei documenti {#forms-document-security-1}

* Problema di concorrenza con l’SDK del client JEE. NPR-27572: Hotfix per CQ-4247156

#### Forms - Servizi basati su documenti {#forms-document-services-3}

* Impossibile creare un modello di dati modulo basato su SOAP in WebSphere. NPR-27692: Hotfix per CQ-4253702

#### Forms - Moduli adattivi {#forms-adaptive-forms-1}

* Vulnerabilità di tipo XML Injection con AEM Forms. NPR-27863: Hotfix per CQ-4257315
* Il componente Contenitore di AEM Forms diventa invisibile in seguito alla configurazione del modulo errato nella pagina Sites e alla selezione della casella di controllo “Forms cover the entire width of the page” (I moduli occupano l’intera larghezza della pagina). NPR-25972: Hotfix per CQ-4239287, CQ-4249133

### Programma di installazione JEE per Forms {#forms-jee-installer-5}

#### JEE per Foundation {#foundation-jee-1}

* Impossibile creare un modello di dati modulo basato su SOAP in WebSphere. NPR-27692: Hotfix per CQ-4253702

#### Bundle OSGi e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included}

Elenco dei bundle OSGi inclusi in AEM 6.3.3.2

[Ottieni file](assets/do-not-localize/63332bundle_list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.3.3.2

[Ottieni file](assets/do-not-localize/6332content_package.txt)

### Cumulative Fix Pack 6.3.3.1 {#cumulative-fix-pack-7}

AEM Cumulative Fix Pack 6.3.3.1 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 3 (6.3.3.0) nel settembre 2018.

AEM Cumulative Fix Pack 6.3.3.1 dipende da AEM 6.3 Service Pack 3. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.3.x dopo aver installato AEM 6.3 Service Pack 3. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Gli elementi di rilievo di **AEM Cumulative Fix Pack** sono:

* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.14.
* Miglioramenti delle prestazioni relative a predicati e ricerca.
* Risoluzione di un problema relativo alla gestione di FormData per il valore predefinito.
* Aggiornamento di FormBuilder alla versione più recente di Handlebars.
* Aggiunta del servlet di configurazione per la configurazione di modifica dell’Editor Rich Text in modalità finestra di dialogo.
* Aggiunta del supporto per campi compositi.
* Abilitazione/disabilitazione degli elementi della barra degli strumenti dell’Editor Rich Text con un criterio per contenuti per la finestra di dialogo di modifica.

#### Risorse {#assets-7}

* Quando è abilitata la separazione IDS, il flusso di lavoro Aggiorna risorsa DAM non collega più i riferimenti. NPR-26135: Hotfix per CQ-4250933
* Se si decomprime un archivio creato dal passaggio di annullamento archiviazione con una cartella il cui nome contiene %, l’archivio non viene aperto. NPR-26275: Hotfix per CQ-4251482
* La presenza di virgolette singole impedisce l’aggiornamento dei metadati. NPR-26808: Hotfix per CQ-4254305
* (Omnisearch) Problema di prestazioni durante la ricerca all’interno di una raccolta. NPR-26714: Hotfix per CQ-4253408
* Se si utilizza GQLConverter con una ricerca full-text contenente le lettere “OR” all’interno del testo, l’operazione non viene elaborata correttamente. NPR-26564: Hotfix per CQ-4247362
* Quando si condivide il collegamento delle risorse da più tenant, viene aggiunto l’ID tenant e l’URL risultante non è valido. NPR-26482: Hotfix per CQ-4253540
* Disabilitazione di “Percorso cartella principale della società” nell’interfaccia utente di configurazione cloud per elementi multimediali dinamici. NPR-26361: Hotfix per CQ-4249505
* L’inserimento di file RAW con estensione .mos è prolungato. NPR-26296: Hotfix per CQ-4250661
* Con la condivisione dei collegamenti delle risorse non è possibile aggiungere più utenti interni con ID utente numerico. NPR-26206: Hotfix per CQ-4251466
* Danneggiamento dei file ZIP compressi con l’algoritmo deflate64. NPR-26793: Hotfix per CQ-4253995
* Il processo di generazione delle miniature non funziona correttamente per file PDF complessi e vengono generate miniature in cui parte dell’immagine risulta mancante. NPR-26057: Hotfix per CQ-4250944
* Problema di utilizzo della memoria heap durante la generazione di miniature. NPR-25545: Hotfix per CQ-4246960
* Quando si crea un numero elevato di relazioni su una risorsa, viene generato un errore. NPR-26309: Hotfix per CQ-4250708
* L’opzione “Elimina rappresentazione” non funziona e viene restituito un errore “Nessun elemento da eliminare”. NPR-26007: Hotfix per CQ-4213414
* Impossibile eliminare i valori predefiniti per i campi con più valori. NPR-25116: Hotfix per CQ-4247856
* (DM in modalità ibrida) Interruzione della replica del catalogo per AEM 6.3.2 con Dynamic Media. NPR-26406: Hotfix per CQ-4251306

#### Sites {#sites-7}

* Backport proattivo delle correzioni per Sites. NPR-26963
* I tag vengono creati due volte quando per Titolo e Nome si utilizza una diversa combinazione di maiuscole e minuscole. NPR-26877: Hotfix per CQ-4254134
* Le funzioni dell’Editor Rich Text nella finestra di dialogo di modifica non sono controllate da criteri. NPR-27059, NPR-26750: Hotfix per CQ-4241130
* Domande sui casi in cui adottare o meno la memorizzazione in cache per segment.js in ClientContext. NPR-26622: Hotfix per CQ-4253486
* Quando si attiva la regola del segmento (/etc/segmentation) per le regole figlio in modalità classica, la pubblicazione viene disattivata. NPR-26601: Hotfix per CQ-4253588
* Se si aggiunge un carattere speciale, la finestra di dialogo dell’Editor Rich Text scorre verso l’alto. NPR-26435: Hotfix per CQ-4249869
* (Interfaccia touch) La barra degli strumenti diventa inutilizzabile con più istanze dell’Editor Rich Text quando si passa da una finestra di dialogo a schermo intero a una finestra di dialogo mobile. NPR-25652: Hotfix per CQ-4206008
* Quando si promuove un lancio con più pagine, vengono create più versioni di ogni pagina. NPR-26810: Hotfix per CQ-4254663
* Le operazioni di spostamento dei tag non vengono rilevate  dai campi tag del modello di frammento di contenuto strutturato. NPR-26801: Hotfix per CQ-4251805
* (Interfaccia touch) L’annullamento della pubblicazione della pagina figlia dall’editor pagina non funziona dopo la ridenominazione della pagina nella blueprint. NPR-26774: Hotfix per CQ-4254175
* La pagina di cui è stata annullata la pubblicazione  non funziona con i riferimenti. NPR-26749: Hotfix per CQ-4254372
* Per creare una variante come Live Copy, l’utente deve aggiornare la pagina di conseguenza. NPR-26663: Hotfix per CQ-4254328
* (Interfaccia classica) Quando si torna alle proprietà della pagina, l’immagine miniatura non utilizza più l’ereditarietà, scompare dalla console di amministrazione del sito e dalla barra laterale e viene visualizzata come vuota. NPR-26562: Hotfix per CQ-4252346
* Quando si crea una versione di una pagina e si attiva un confronto, i nodi di /content/ versionshistory sono elencati nell’elenco delle Live Copy per la blueprint. NPR-26506: Hotfix per CQ-4243957
* Gli URL nell’editor di amministrazione di Frammenti di esperienza non consentono sovrapposizioni. NPR-26318: Hotfix per CQ-4252156

#### Platform {#platform}

* Interruzione della sessione in ReplicationEventListener con eventi di test. NPR-25937: Hotfix per CQ-4251090
* Per la replica viene utilizzato il token scaduto per OAuth e vengono generati numerosi errori. NPR-25894: Hotfix per GRANITE-22388

#### Integrazione {#integration-3}

* Interruzione di TSDK incorporato con AEM in seguito a un aggiornamento a Handlebars 4 dovuto all’utilizzo di modelli incompatibili. NPR-26699: Hotfix per CQ-4248974
* Quando si pubblica una pagina con una nuova risorsa, la pagina figlia viene disattivata dall’istanza di pubblicazione senza alcuna notifica. NPR-24869: Hotfix per CQ-4247832
* Per la replica viene utilizzato un token scaduto per  OAuth. NPR-25984: Hotfix per GRANITE-22388

#### Replica {#replication-2}

* Il trasporto HTTP può causare la perdita di dati dalle sessioni aperte. Hotfix per GRANITE-17434
* Eccezioni nei registri quando l’accesso al nodo dei token viene eseguito contemporaneamente da più agenti di replica. NPR-26964: Hotfix per GRANITE-23276, GRANITE-23155

#### ContextHub {#contexthub}

* Il file coral.js include una versione vulnerabile della libreria handlebars.js. Hotfix per CQ-4255377

#### DAM - Client DM {#dam-dm-client-1}

* Quando si elimina una copia di una risorsa immagine, la risorsa immagine originale diventa inutilizzabile. Hotfix per CQ-4251648
* Download ridondante di contenuti immagine aggiuntivi dai server S7. Hotfix per CQ-4248770

#### GRANITE {#granite}

* Il provider OAuth di AEM non esegue la ricerca senza distinzione tra maiuscole e minuscole. NPR-26133: Hotfix per GRANITE-22650
* La funzione di convalida pacchetti non convalida i pacchetti inclusi in CFP/SP. NPR-26775: Hotfix per GRANITE-22825

#### Community {#communities-6}

* Problema relativo al delimitatore nei risultati della ricerca. NPR-27051: Hotfix per CQ-4248939
* Nell’elenco a discesa il valore Dallas diventa Virginia in Provider risorse di archiviazione Adobe. NPR-26936: Hotfix per CQ-4254434
* Abilitazione del supporto per la ricerca di titoli localizzati in SocialTagManager. NPR-26932: Hotfix per CQ-4250276
* La miniatura delle immagini di allegati non viene visualizzata quando si crea un post per forum. NPR-26380: Hotfix per CQ-4253105
* Impossibile caricare più immagini con il plugin Incolla da Word. NPR-26728: Hotfix per CQ-4253638
* Impossibile filtrare i contenuti nella pagina di moderazione. NPR-26697: Hotfix per CQ-4213766
* (Vulnerabilità della sicurezza) Acquisizione dell’account a causa della configurazione errata di JWT. NPR-26440: Hotfix per CQ-4253314
* Il recupero dei dati da Provider risorse di archiviazione Adobe è lento. NPR-26237: Hotfix per NPR-24152
* La pagina di composizione di messaggi privati non funziona correttamente. NPR-26120: Hotfix per CQ-4250923
* Con la notifica “Contrassegna tutto come letto” viene eseguito il rendering solo dei primi 10 messaggi contrassegnati come non letti se non si aggiorna la pagina. NPR-27036: Hotfix per CQ-4254058
* Comportamento di selezione e caricamento pagine per la paginazione della sezione dei commenti di Communities. NPR-27030: Hotfix per CQ-4251228
* (Ricerca nel forum) Facendo clic sul pulsante Indietro, la pagina viene ignorata e viene visualizzata di nuovo la pagina forum.html. NPR-26949: Hotfix per CQ-4254804
* Il limite massimo per la notifica del conteggio degli elementi non letti è 21. NPR-26947: Hotfix per CQ-4251251
* (Processo SearchScheduledPosts) Aggiunta dell’interruttore Abilita/Disabilita in ConfigMgr. NPR-26924: Hotfix per CQ-4250463
* Contesto Tomcat (/aempublish): il percorso viene eliminato durante lo scorrimento nella pagina Assegnazioni. NPR-26919: Hotfix per CQ-4254345
* Eccezione NullPointerException durante la creazione di un gruppo e di un membro. NPR-26778: Hotfix per CQ-4248095
* Il contenuto non in primo piano e sbloccato dal moderatore non è compatibile con il principio di singola responsabilità (SRP) di MySQL. NPR-26767: Hotfix per CQ-4251520
* Problemi della funzionalità di ricerca con alcuni caratteri. NPR-26726: Hotfix per CQ-4247744
* Abilitazione dei collegamenti profondi per le risorse di attivazione e l’interfaccia utente di moderazione. NPR-26705: Hotfix per CQ-4251381
* Problema di ricerca nel componente del forum. NPR-26577: Hotfix per CQ-4251303
* La ricerca con la combinazione di nome e cognome nella messaggistica di Communities non restituisce i risultati previsti. NPR-26377: Hotfix per CQ-4253150
* La paginazione non viene aggiornata in seguito alla rimozione delle risposte. NPR-26327
* L’eliminazione dei post funziona ma viene generato un errore nella console e il post rimane visibile nell’interfaccia utente. NPR-26292: Hotfix per CQ-4252803
* La paginazione non viene aggiornata in modo dinamico e l’elenco delle risposte continua ad allungarsi. NPR-26145: Hotfix per CQ-4251586
* Le impostazioni del gruppo non vengono caricate in un gruppo che contiene da 50.000 a 100.000 utenti. NPR-25642: Hotfix per CQ-4238426
* Errore del lettore risorse del catalogo per i percorsi di contesto. NPR-25640: Hotfix per CQ-4238426
* (Ricerca nel forum) I collegamenti impaginati verso thread con numerosi post non funzionano nelle notifiche. Hotfix per CQ-4254202
* La console di moderazione visualizza solo cinque voci con Firefox. Hotfix per CQ-4254128
* I gruppi non sono visibili durante la creazione di un sito. NPR-27148: Hotfix per CQ-4251788
* Eccezione Null Pointer durante l’aggiunta di gruppi e membri alle impostazioni di Ruolo e abilitando il membro privilegiato nella funzione Blog. NPR-21732, NPR-27176: Hotfix per CQ-4255909
* In seguito alla modifica del sito e all’aggiunta di membri nelle impostazioni di Ruolo viene generata un’eccezione Null Pointer. NPR-27132: Hotfix per CQ-4255909

#### Interfaccia utente {#user-interface}

* Correzioni proattive per l’accesso alla piattaforma. NPR-26961
* (Multifield) Utilizzo di nomi personalizzati consentito per gli elementi compositi. NPR-26493: Hotfix per GRANITE-20568
* Una pagina incollata non viene visualizzata nella vista a colonne finché questa non viene aggiornata. NPR-26030: Hotfix per CQ-4236346
* Correzioni proattive per granite.ui.commons. NPR-26960
* Correzioni proattive per granite.ui.content. NPR-26959
* Correzioni proattive per il registro di CQ o dell’esperienza. NPR-26943
* Backport proattivi dell’interfaccia utente di Foundation. NPR-26942
* (IE11) Nel campo numerico viene visualizzato “NaN” quando si digita un valore negativo. NPR-26701: Hotfix per CQ-100826
* (Coral. Multifield) Nei campi multipli nidificati viene utilizzato il modello errato per la creazione degli elementi. NPR-25649: Hotfix per CUI-6743
* Si devono aggiornare i clientlibs granite coralui2 e coralui3 per rimuovere Handlebars dalla build. NPR-25606: Hotfix per GRANITE-22116

### Forms {#forms-7}

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-7}

#### Forms - Sicurezza dei documenti {#forms-document-security-2}

* Eccezioni di rollover della chiave dell’entità principale nei registri del server per le chiavi inattive. NPR-26748: Hotfix per CQ-4253705
* Impossibile creare o modificare le impostazioni della filigrana per la sicurezza dei documenti. NPR-26267, NPR-26129: Hotfix per CQ-4250234

#### Forms - Servizi basati su documenti {#forms-document-services-4}

* La convalida PDF/A non viene visualizzata come valida con Convalida PDF/A. NPR-25934: Hotfix per CQ-4248558

#### Forms - Comunicazione interattiva {#forms-interactive-communication}

* Le anteprime PDF e HTML della lettera sono visibili e funzionanti nella stessa finestra quando si modifica e si salva un modulo modificabile e quindi si apre/chiude l’anteprima PDF. NPR-26770: Hotfix per CQ-4253217

#### Forms - Flusso di lavoro {#forms-workflow-2}

* L’area di lavoro si blocca in modo intermittente e mostra ripetutamente i punti iniziali. NPR-26461: Hotfix per CQ-4253439
* Viene generata l’eccezione ESAPI nei registri quando nel nome dell’attività si utilizzano parentesi graffe. Hotfix per CQ-4256627
* Viene generata l’eccezione Null Pointer quando si apre il punto iniziale associato al modulo adattivo o al set modulo non precompilato. Hotfix per CQ-4256124
* Impossibile inviare il messaggio e-mail utilizzando l’impostazione globale. NPR-26163: Hotfix per CQ-111110
* Impossibile aprire l’area di lavoro dopo l’applicazione del file axis.jar. NPR-26131: Hotfix per CQ-4251126
* Il pulsante di aggiornamento non consente di sincronizzare i dati più recenti tra il server e i moduli adattivi. Hotfix per CQ-4255670
* Se si imposta un modello di ricerca dall’interfaccia utente di amministrazione e si utilizza lo stesso modello per effettuare ricerche nell’area di lavoro di AEM Forms, viene generata un’eccezione. Hotfix per CQ-4255649
* I dettagli di tracciamento dei processi in applicazioni il cui nome contiene il simbolo delle parentesi non vengono visualizzati nell’area di lavoro HTML. Hotfix per CQ-4242101
* Quando si salvano modifiche nella schermata delle preferenze dell’area di lavoro HTML, viene generata un’eccezione. Hotfix per CQ-4241485
* L’approvazione collettiva viene interrotta in seguito alla configurazione della versione più recente di JEE. Hotfix per CQ-4241486
* Errore della bozza dell’attività o del punto iniziale nella versione più recente del server JEE 6.4. Hotfix per CQ-4241484
* Impostazione del parametro Date().getTime().toString anziché Date.toString() per l’inizializzazione della sessione. Hotfix per CQ-4241483
* Durante l’apertura di /lc/ws, nel parametro HTML viene rilevata un’eccezione di carattere vulnerabile. Hotfix per CQ-4241481

#### Vulnerabilità {#vulnerability-1}

* Vulnerabilità cross-site scripting (XSS) memorizzata nella scheda delle note di Forms Manager. NPR-27157: Hotfix per CQ-4255556

### Programma di installazione JEE per Forms {#forms-jee-installer-6}

#### JEE per Foundation {#foundation-jee-2}

* Revisione del codice per l’API di sicurezza aziendale. Hotfix per CQ-4255638
* Impossibile caricare esapi.properties come risorsa del caricatore di classi in WAS9. Hotfix per CQ-4255631
* Quando si fa clic su Add Authentication (Aggiungi autenticazione) durante la configurazione del dominio, viene generato un errore. Hotfix per CQ-4255634
* JEE per Forms supporta l’autenticazione reciproca PKCS#11. NPR-21372
* Risoluzione dei problemi segnalati nell’analisi del codice statico di Core. Hotfix per CQ-104446
* La distribuzione di adobe.livecycle.weblogic.ear e adobe.livecycle.websphere.ear non riesce durante l’esecuzione di LCM. Hotfix per CQ-4255629, CQ-4255630
* Messaggi di errore non validi in Gestione applicazioni. NPR-23289: Hotfix per CQ-4233163, CQ-4255636
* Quando si fa clic su Add Authentication (Aggiungi autenticazione) durante la configurazione del dominio, viene generato un errore. Hotfix per CQ-4255634

#### Forms - Connettore JEE {#forms-jee-connector}

* Risoluzione dei problemi segnalati nell’analisi del codice statico del connettore. NPR-22260

#### Servizio PDFG {#pdfg-service-1}

* Errore org.jgroups.Message nei registri dopo l’aggiornamento da LiveCycle ad AEM 6.2 Forms. NPR-26795: Hotfix per CQ-4220415
* AEM Forms - Errore durante la migrazione degli stili. Hotfix per CQ-4251969
* Risoluzione dei problemi segnalati nel rapporto di analisi del codice statico di PDFG. NPR-23251: Hotfix per CQ-4213930

#### Bundle OSGi e pacchetti di contenuti inclusi nella versione 6.3.3.1 {#osgi-bundles-and-content-packages-included-in-3}

Elenco dei bundle OSGi inclusi in AEM 6.3.3.1

[Ottieni file](assets/do-not-localize/63sp3cfp1bundlelist.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.3.3.1

### Cumulative Fix Pack 6.3.2.2 {#cumulative-fix-pack-8}

AEM Cumulative Fix Pack 6.3.2.2 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 2 (6.3.2.0) nell’aprile 2018.

AEM Cumulative Fix Pack 6.3.2.2 dipende da AEM 6.3 Service Pack 2. Occorre quindi installare il pacchetto AEM Cumulative Fix Pack 6.3.2.x dopo aver installato AEM 6.3 Service Pack 2. Per le istruzioni di installazione, consulta le [note sulla versione di AEM 6.3 Service Pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html).

Gli elementi di rilievo di **AEM Cumulative Fix Pack** sono:

* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.11.
* Abilitazione delle risorse secondarie e del visualizzatore di risorse con più pagine in Brand Portal.
* Lunghezza del tipo di campo estesa a 255 per supportare tutti i tipi MIME possibili per i diversi tipi di allegati.
* Configurazione del messaggio di errore restituito dal server quando un’immagine viola i criteri di caricamento.
* Aggiunta del supporto per STARTTLS in Day CQ Mail Service (Servizio posta Day CQ).
* Aggiornamento alle versioni più recenti di cq-wcm-content e com.adobe.cq.launches.it.serverside.
* Aggiornamento di com.adobe.granite.ui.coralui3-rte all’ultima versione rilasciata.
* La condizione di rendering restituisce un risultato valido se expressionResolver è null.
* Coral.ColumnView: aggiunta del supporto per Maiusc+clic.

### Risorse {#assets-8}

* Il campo Gruppo utenti chiuso della cartella delle risorse non restituisce il gruppo “tutti”. NPR-23163: Hotfix per CQ-4239377
* La ricerca di ricerche salvate come raccolte avanzate non restituisce tutti i risultati. NPR-23243: Hotfix per CQ-4240355
* (ExpiryNotificationJobImpl) Ottimizzazione della query esistente. NPR-23330: Hotfix per CQ-4205249
* (Profilo metadati) I valori di tag standard impostati durante la creazione non sono disponibili dopo il salvataggio. NPR-23370: Hotfix per CQ-4235458
* (Interfaccia touch) Impossibile spostare più risorse a causa di un errore JavaScript. NPR-23395: Hotfix per CQ-4241279
* La mancata corrispondenza tra le dimensioni del download e le informazioni visualizzate non è corretta e crea confusione per gli utenti. NPR-23418: Hotfix per CQ-4242774
* Il tipo MIME estratto per l’estensione di file LSR e SKETCH non è corretto e causa il download di file non validi. NPR-23644: Hotfix per CQ-4243260
* (Firefox/Chrome) Impossibile scaricare risorse nella pagina Condivisione risorse. NPR-23963: Hotfix per CQ-4244391
* I facet di ricerca dell’amministratore delle risorse scompaiono nei pannelli di ricerca dopo la visualizzazione dell’anteprima. NPR-23964: Hotfix per CQ-4244410
* L’annullamento della pubblicazione del modulo di ricerca causa la rimozione completa del modulo di ricerca predefinito. NPR-23291: Hotfix per CQ-4241382
* (Brand Portal) La ricerca nel predicato di directory deve essere filtrata in base alla replica. NPR-23292: Hotfix per CQ-4241385
* L’azione Pubblica su Brand Portal dell’interfaccia utente non è disponibile. NPR-23293: Hotfix per CQ-4241161
* Il pulsante per la pubblicazione o l’annullamento della pubblicazione su Brand Portal non deve essere disponibile per i frammenti di contenuto. NPR-23318: Hotfix per CQ-4245086
* (Brand Portal) Abilitazione della creazione di risorse secondarie quando viene pubblicata una risorsa. NPR-23331: Hotfix per CQ-4242018
* Nelle richieste Dynamic Media non viene utilizzato il client comune proxy/HTTP. NPR-10727: Hotfix per CQ-45695, CQ-88800
* Impossibile annotare una risorsa video MP4 con rendering singolo in formato Dynamic Media S7 (DMS7). NPR-22046: Hotfix per CQ-4215912
* I dati EmbedXMP sono sempre impostati su “active” per il processo di generazione Ptiff. NPR-22903: Hotfix per CQ-4234498
* Problemi di visualizzazione/selezione delle rappresentazioni dinamiche con un numero elevato di predefiniti immagine. NPR-23151: Hotfix per CQ-4217511
* Problema relativo al modulo di avvio per modifica/ricaricamento di video con codifica Dynamic Media. NPR-23237: Hotfix per CQ-4240260
* Correzione relativa alla gestione dei proxy per il modulo di inoltro HTTP in Dynamic Media S7. NPR-24001: Hotfix per CQ-244140

### Sites {#sites-8}

* Differenze in Query Builder causano una diversa conversione degli xPath tra le versioni 6.2 e 6.3. NPR-23245: Hotfix per CQ-4240396
* La scheda Miniatura nella proprietà della pagina non funziona quando si estende la finestra di dialogo. NPR-22844: Hotfix per CQ-4241474
* Parsys taglia la larghezza del frame del dispositivo dell’emulatore e rimuove eventuali componenti aggiunti al suo interno. NPR-22926: Hotfix per CQ-4238224
* Durante l’esecuzione di più lanci, il lancio viene promosso nell’istanza di creazione, ma le modifiche non vengono replicate nel server dell’istanza di pubblicazione perché mancano le autorizzazioni di replica. NPR-22934: Hotfix per CQ-4234746
* Una pagina bloccata da un utente nella prima sessione può essere modificata da un altro utente in un’altra sessione. NPR-23057: Hotfix per CQ-4199017
* Correzione dell’opzione riordinabile nella vista a elenco. NPR-23065: Hotfix per CQ-4239321
* (Editor pagina) L’immagine in un componente immagine scompare quando si apre di nuovo la finestra di dialogo. NPR-23156: Hotfix per CQ-4239978
* Editor modelli visualizza solo 20 modelli/cartelle e non carica gli altri quando si scorre verso il fondo della pagina. NPR-23185: Hotfix per CQ-4238483
* (Interfaccia classica) Viene generato un errore durante lo spostamento o la ridenominazione delle pagine. NPR-23213: Hotfix per CQ-4240971
* Impossibile modificare/creare segmenti ContextHub. NPR-23218: Hotfix per CQ-4226948
* (Editor Rich Text) Con l’operazione di sostituzione viene modificato il formato di una parola. NPR-23271: Hotfix per CQ-4239677
* Nella scheda Blueprint per le varianti XF manca il pulsante Rollout. NPR-23320: Hotfix per CQ-4240404
* L’interfaccia classica non funziona per la modifica di gruppi utente chiusi (CUG) perché è diventata obsoleta. NPR-24122: Hotfix per 4241823
* Correzione proattiva per la protezione contro promozioni di contenuto indesiderate. NPR-24387: Hotfix per 4244993
* Dopo aver aggiunto circa 80 frammenti in una cartella in Assets, si verificano degli errori quando si attiva il flusso di lavoro dalla console della Timeline. NPR-23393: Hotfix per CQ-4211216
* Impossibile trascinare immagini nella finestra di dialogo Editor Rich Text da Content Finder. NPR-23403: Hotfix per CQ-4242094
* Errore di tipo “Valore del selettore di ricorsione non valido” durante la migrazione di un componente da AEM 6.0 a AEM 6.2. NPR-23532: Hotfix per CQ-4241258
* (Editor Rich Text) Nelle descrizioni è indicato il nome della variabile invece del nome leggibile del plug-in. NPR-23550: Hotfix per CQ-4243269
* Impossibile salvare la finestra di dialogo con il menu a discesa di selezione richiesto nella versione per dispositivi mobili/tablet. NPR-23904: Hotfix per CQ-4243096
* In seguito all’installazione della versione 6.3.2.1, le opzioni di sistema per lo stile vengono visualizzate in tutte le pagine. NPR-23972: Hotfix per CQ-4244394
* L’interfaccia classica non funziona per la modifica di gruppi utente chiusi (CUG) perché è diventata obsoleta. NPR-24122: Hotfix per 4241823
* Correzione proattiva per la protezione contro promozioni di contenuto indesiderate. NPR-24387: Hotfix per 4244993
* I riferimenti alle risorse non vengono aggiornati quando le risorse vengono spostate. NPR-23208: Hotfix per CQ-4239879

### Piattaforma {#platform-1}

* La raccolta avanzata non visualizza i risultati dopo il salvataggio se si utilizza Predicato tag nel facet di ricerca. NPR-23401: Hotfix per GRANITE-21278
* Applicazione della patch a jQuery 1.12.4 da clientlib per includere la correzione di sicurezza. NPR-24128: Hotfix per GRANITE-20058
* Le traduzioni per l’internazionalizzazione vengono aggiornate solo dopo il riavvio del bundle. NPR-23193: Hotfix per Sling-7190
* Risolutore risorse non chiuso in ReplicationEventListener. NPR-23240: Hotfix per CQ-4241350
* Supporto per STARTTLS in “Day CQ Mail Service”. NPR-23941: Hotfix per CQ-4240397
* Il nome del tag di reclamo JCR deve essere compilato automaticamente in base al titolo del tag. NPR-24173: Hotfix per CQ-4199411

### Integrazione {#integration-4}

* (Target) Le campagne non vengono attivate quando si utilizza il tipo di API XML. NPR-23199: Hotfix per CQ-4240936****
* Impossibile eseguire la replica dei riferimenti di configurazione con la struttura di cartelle intermedia. NPR-23485: Hotfix per CQ-4242751

### Vulnerabilità {#vulnerability-2}

* L’integrazione con Salesforce è vulnerabile ad attacchi di tipo SSRF (Server Side Request Forgery). NPR-24289: Hotfix per CQ-424527
* Vulnerabilità cross-site scripting (XSS) nei collegamenti di progetto di Interfaccia utente amministratore. NPR-23272: Hotfix per CQ-4241795

### WCM - Componenti Foundation {#wcm-foundation-components}

* La tabella di Foundation presenta una vulnerabilità cross-site scripting archiviati. NPR-23214: Hotfix per CQ-4240760

### Traduzione {#translation-3}

* Le proprietà di Live Copy non vengono eliminate durante la creazione di copie della lingua. NPR-23123: Hotfix per CQ-4230641

### Interfaccia utente {#user-interface-1}

* DatePicker non supporta l’impostazione manuale di suggerimenti di tipo esterni impostati da un campo nascosto. Se si modifica il valore di hint “type”, viene generato un errore di conversione. NPR-23371: Hotfix per GRANITE-21194
* Coral.ColumnView: aggiunta del supporto per Maiusc+clic. NPR-23404: Hotfix per GRANITE-13338
* La selezione RT non viene convalidata se si seleziona un elemento con valore vuoto. NPR-23405: Hotfix per GRANITE-21283
* (OMEGA) Rapporto “Feature” disponibile solo in inglese. NPR-23990: Hotfix per GRANITE-21231
* Correzioni per l’API di Coral.Autocomplete. NPR-23516

### GRANITE {#granite-1}

* Le connessioni per il tracciamento client Apache HTTP e l’elevato utilizzo dell’heap causano l’arresto anomalo del server AEM. NPR-23906: Hotfix per GRANITE-21056

### Commerce {#commerce-2}

* L’output JSON di Campaign non contiene la directory principale del contesto del servlet. NPR-23733: Hotfix per CQ-4243827

### Community {#communities-7}

* Errore durante la ricerca di alcune parole in Communities. NPR-23256: Hotfix per CQ-4240717
* Impossibile assegnare gruppi per il problema di ruolo dei manager della community. NPR-23317: Hotfix per CQ-4241233, CQ-4221399
* Problemi durante la creazione di risorse con un nome di risorse simile. NPR-23319: Hotfix per CQ-4240700
* (ContextPath) Interruzione della funzionalità dei messaggi per le configurazioni Jetty e restituzione di un errore durante la ricerca di membri del gruppo nell’elenco dei membri del gruppo community. NPR-23336: Hotfix per CQ-4241519, CQ-4242080
* Il caricamento di un’immagine in un forum Communities non viene visualizzato in Provider risorse di archiviazione Adobe (ASRP). NPR-23397: Hotfix per CQ-4242497
* Le idee eliminate vengono visualizzate come collegamenti attivi in Attività. NPR-23406
* Impossibile caricare imsmanifest.xml quando AEM è in esecuzione con la directory principale del contesto. NPR-23483: Hotfix per CQ-4242193
* Vulnerabilità di sicurezza in una versione precedente di Handlebars. NPR-23518: Hotfix per CQ-4243055
* Servizio tunnel non funzionante. NPR-23543: Hotfix per CQ-4242217
* Problemi relativi a componenti di Communities quando si effettua l’accesso tramite dispatcher e Sling Dynamic Include è abilitato. NPR-23586: Hotfix per CQ-4242360, CQ-4241522
* Quando si cerca un termine e la ricerca restituisce numerosi risultati, la paginazione non viene reimpostata se si immette un nuovo termine di ricerca. NPR-23739: Hotfix per CQ-4222593
* Problemi durante l’esecuzione della  ricerca nel componente del forum. NPR-23838: Hotfix per CQ-4243770
* (Segnalazione di moderazione della community) L’accettazione collettiva di messaggi segnalati non funziona. NPR-23845: Hotfix per CQ-4243962
* Il testo del pulsante Ordina non visualizza il  valore nonostante sia selezionato l’ordinamento predefinito. NPR-23881: Hotfix per CQ-4243375
* Le notifiche Web ed e-mail non vengono attivate a causa di un errore del messaggio per i gruppi. NPR-23934: Hotfix per CQ-4242880
* Quando si utilizza la configurazione DSRP, non vengono visualizzati dettagli su utenti e motivi della segnalazione. NPR-23973: Hotfix per CQ-4243205
* I motivi della segnalazione relativi a utenti non segnalati rimangono visibili. NPR-23974: Hotfix per CQ-4243822
* Se si allegano per due volte due file con lo stesso nome a un post di tipo modulo, si verifica un errore del server. NPR-24166: Hotfix per CQ-4244367
* Impossibile memorizzare gli allegati con tipi MIME con più di 15 caratteri utilizzando DSRP (Database Storage Resource Developer). NPR-24174
* Quando si trascina un’immagine che viola i criteri di caricamento nel testo del post, viene generato un errore del server e l’utente riceve un messaggio di errore generico. NPR-24243
* Correzioni per diversi problemi relativi al lato server di AEM Communities. NPR-23971: Hotfix per CQ-4243144, CQ-4242145, CQ-4243365, CQ-4244098
* Correzioni per diversi problemi relativi ad Adobe Social. NPR-24242: Hotfix per CQ-4245054, CQ-4245120, CQ-4245296

### Campaign {#campaign}

* L’output JSON di Campaign non contiene la directory principale del contesto del servlet. NPR-23733: Hotfix per CQ-4243827

### MSM {#msm}

* Durante il rollout della pagina, la Live Copy non mostra le proprietà dei tempi di attivazione/disattivazione ereditate dalla pagina mastro. NPR-23873: Hotfix per CQ-4243431
* Durante l’operazione della Live Copy i nodi secondari dei componenti eliminati non vengono ignorati. NPR-23058: Hotfix per CQ-4211662

### Offload {#offloading}

* Richiesta di un meccanismo per ripulire le risorse dalle istanze del worker dopo l’elaborazione o a intervalli regolari. NPR-23638: Hotfix per GRANITE-21337

## Forms {#forms-8}

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-8}

#### Moduli adattivi {#adaptive-forms-1}

* Spostamento di ReCaptchaConfigService nel pacchetto interno. Hotfix per CQ-4217459
* Il campo numerico non rispetta il valore minimo. NPR-23967: Hotfix per CQ-4244830
* Supporto di più partizioni nell’integrazione di Moduli adattivi con Adobe Sign. NPR-23383

#### Integrazione con il back-end {#backend-integration}

* (FDM)(WebService) Supporto del costrutto per le estensioni di WSDL nel parser WSDL. NPR-23640, NPR:23236: Hotfix per 4205821
* Per includere SDLInvokerParams nell’SDK del client per componenti aggiuntivi di Forms. NPR-23157

### Programma di installazione di JEE per Forms {#forms-jee-installer-7}

#### Gestione processi {#process-management}

* Impossibile aprire l’area di lavoro dopo l’applicazione del nuovo file axis.jar. NPR-23316
* Vulnerabilità cross-site scripting (XSS) di LiveCycle in PMAdmin. NPR-23267
* Dopo l’aggiornamento ad AEM 6.1 Forms, l’area di lavoro HTML si blocca quando si accede all’elenco attività per utenti specifici. NPR-23943

#### Core {#core}

* JEE per Forms supporta l’autenticazione reciproca PKCS#11. NPR-21372

#### Servizio PDFG {#pdfg-service-2}

* Il servizio di acquisizione foglio si arresta in modo anomalo durante l’elaborazione simultanea di file TIFF (dimensioni pari a circa 50 KB). NPR-23556

#### Forms Designer {#forms-designer}

* Output server di AEM Forms - Descrizione alternativa mancante per le annotazioni. NPR-22207
* Aggiunta del supporto per PDF/UA ai moduli XML generati tramite Designer e il servizio Output. NPR-23132

### Bundle OSGi e pacchetti di contenuti inclusi nella versione 6.3.2.2 {#osgi-bundles-and-content-packages-included-in-4}

Elenco dei bundle OSGi inclusi in AEM 6.3.2.2

[Ottieni file](assets/do-not-localize/6_3_2_2_bundle-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.3.2.2

[Ottieni file](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Cumulative Fix Pack 6.3.2.1 {#cumulative-fix-pack-9}

AEM Cumulative Fix Pack 6.3.2.1 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 2 (6.3.2.0) nell’aprile 2018.

Gli elementi di rilievo di **AEM Cumulative Fix Pack** sono:

* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.10.
* Rendering migliorato dei componenti parsys nell’interfaccia classica.
* Aggiornamento dei bundle dei modelli Sling per includere la correzione del set di caratteri.
* Pubblicazione su Brand Portal disponibile in modalità asincrona per tutti i tipi di risorse.
* Aggiornamento di coralui-component-richtexteditor.git dalla versione 0.1.15 alla versione 0.1.16
* Correzioni apportate alla funzionalità Mostra/Nascondi del componente del menu a discesa.
* Abilitazione della riflessione immagine per il componente immagine di base.
* Aggiornamento dei bundle  felix   http per abilitare gli attributi di sessione.

* Rimozione di cache=true nei modelli Sling a causa di problemi di consumo di memoria.

### Risorse {#assets-9}

* Quando si modifica il titolo o l’immagine in miniatura nelle impostazioni di Cartella risorse, il gruppo e le autorizzazioni originali della cartella vengono ignorati. NPR-22171: Hotfix per CQ-4216080
* L’interfaccia utente restituisce il falso errore “Pubblicazione su Brand Portal non riuscita”, laddove il processo viene aggiunto alla coda di replica e le risorse vengono pubblicate su Brand Portal. NPR-22179: Hotfix per CQ-4205273
* (Interfaccia touch) Percorso di caricamento predefinito per le risorse nella vista a colonne. NPR-22465: Hotfix per CQ-4237057
* AEM genera un errore StackOverflow quando si prova a copiare uno schema di risorse da /conf/global a /conf/ mytenant. NPR-22489: Hotfix per CQ-4235875
* Il tentativo di decompressione di un archivio ZIP non riesce per la presenza di uno spazio alla fine del nome della cartella. NPR-22522: Hotfix per CQ-4238036
* L’ordinamento in base alla colonna Titolo risorsa non funziona per i risultati della ricerca. NPR-22908: Hotfix per CQ-4239076
* Il video YouTube è contrassegnato con il percorso completo invece del nome del tag stesso. NPR-22976: Hotfix per CQ-4238669
* Il nuovo ordinamento delle cartelle in una cartella riordinabile non viene mantenuto. NPR-23125: Hotfix per CQ-4231761
* HTTP 504: Errore di timeout del gateway quando si prova a condividere raccolte con il collegamento di condivisione. NPR-21928: Hotfix per CQ-4234507
* I metadati delle parole chiave PDF non vengono estratti correttamente e vengono modificati in modo errato se a una risorsa PDF sono associate più parole chiave. Per risolvere il problema, la proprietà dei metadati del campo Oggetto è stata rimossa per le risorse PDF. Si può, tuttavia, modificare lo schema metadati per aggiungere un campo di testo con più valori al campo Oggetto. NPR-21972: Hotfix per 4215741****
* Se si cambia la cartella selezionata nell’intervallo di visualizzazione tra le due finestra a comparsa, le risorse errate vengono eliminate. NPR-21980: Hotfix per CQ-4233675
* (DAM) Rilevazione di più vulnerabilità cross-site scripting (XSS) durante l’aggiunta alla procedura guidata della raccolta. NPR-22432: Hotfix per CQ-4327086
* Il download delle risorse non riesce quando si utilizza Digital Rights Management in Assets con Safari. Gli utenti non possono scaricare risorse con liberatoria e nomi file lunghi. NPR-22747: Hotfix per CQ-4236460 e CQ-4235274
* Impostazione della condivisione pubblica come opzione predefinita durante la pubblicazione di risorse su Brand Portal. NPR-21931: Hotfix per CQ-4218816

### Sites {#sites-9}

* Il nuovo elemento nella posta in arrivo di Workflow mostra il percorso della pagina invece del titolo della pagina. NPR-21634: Hotfix per CQ-4230672
* I componenti di struttura modificabili perdono i nomi delle classi CSS necessari per la griglia reattiva quando vengono modificati. NPR-21741: Hotfix per CQ-4232374
* (Interfaccia touch) Rilevazione di più vulnerabilità cross-site scripting (XSS) per i componenti HTL. NPR-21899: Hotfix per CQ-4232511
* Impossibile modificare il tipo di risorsa immagine da file multimediali diversi per frammenti di contenuto. NPR-21907: Hotfix per CQ-4233401
* La finestra a schermo intero dell’Editor Rich Text per l’interfaccia utente touch nasconde i plugin dell’Editor Rich Text. NPR-22034: Hotfix per CQ-4235457
* (Interfaccia touch) L’Editor Rich Text rimuove tutti gli attributi dal tag &lt;a>, ad eccezione degli id. NPR-22044: Hotfix per CQ-4234133
* La presenza di più istanze sovrapposte di parsys (più di 6) causate da query con tempi di esecuzione lunghi rallenta l’esecuzione di AEM. NPR-22134: Hotfix per CQ-4233904
* Impossibile modificare le autorizzazioni per nodi il cui nome contiene due punti (:). NPR-22136: Hotfix per CQ-4236221
* (Interfaccia classica) L’output dell’editor rich text aggiunge “list-position-style: inside;” come stile in linea con il tag &lt;ul>. NPR-22145: Hotfix per CRTE-114
* Se il testo è vuoto, come fallback di TreeNode viene impostato l’attributo name. NPR-22146: Hotfix per CQ-4234724/CQ-4236300
* Problemi relativi ai feed RSS, porta -1 a AEM 6.3. NPR-22176: Hotfix per CQ-4233339
* (Interfaccia classica) La scelta rapida da tastiera per incollare il testo (Ctrl+V) non funziona per il componente Testo OOTB (Rich Text). NPR-22224: Hotfix per CQ-4236224
* Il filtro del campo tag  non funziona come previsto durante la digitazione del testo. NPR-22236: Hotfix per CQ-4236655
* (Editor pagina) Quando si incollano dati di testo nel componente Mappa immagine, viene incollato anche il componente Testo. NPR-22264: Hotfix per CQ-4236230
* Il campo richiesto FileUpload della finestra di dialogo causa problemi nell’invio della finestra di dialogo. NPR-22464: Hotfix per CQ-4222192
* Se si esegue uno spostamento senza autorizzazioni di replica, viene avviata una richiesta per un flusso di lavoro di attivazione se la pagina spostata o i relativi referenti non possono essere attivati. NPR-22467: Hotfix per CQ-4211765
* Problemi di prestazioni durante il caricamento di una pagina destinata a un numero elevato di utenti (oltre 2000). NPR-22478: Hotfix per CQ-4209567
* Problemi di persistenza quando ContextHub memorizza il livello di persistenza predefinito della sovrascrittura durante l’inizializzazione. NPR-22479: Hotfix per CQ-4218399
* Quando si esegue il lancio con più pagine, le pagine secondarie non vengono pubblicate nei server di pubblicazione se l’opzione “Includi le pagine secondarie” non è selezionata nella  prima root di contenuto. NPR-22482: Hotfix per CQ-4237818
* [Interfaccia touch] Quando si eliminano lanci tramite la console dell’interfaccia classica, tutte le pagine non sono più modificabili. NPR-22491: Hotfix per CQ-4225074
* Problemi relativi al componente Immagine a causa di spazio eccessivo nella  finestra di dialogo. NPR-22528: Hotfix per CQ-4238183
* Quando si apre il componente con la modalità  in linea, i plug-in caricati in precedenza non sono visibili la seconda volta. NPR-22591: Hotfix per CQ-4236850
* Se si elimina un lancio in un lancio nidificato, i lanci secondari diventano orfani. NPR-22621: Hotfix per CQ-4202639
* (Barra laterale dell’interfaccia classica) La scheda Flusso di lavoro è disabilitata quando la pagina si trova nella fase di blocco del flusso di lavoro. NPR-22722: Hotfix per CQ-4237557
* Dopo aver riflesso un’immagine aggiunta nel componente immagine in una pagina, le modifiche non vengono salvate e nella pagina viene visualizzata l’immagine  originale. È stato aggiunto il supporto per il rendering al componente di base Immagine tramite [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141). NPR-22801: Hotfix per CQ-4221539
* Quando l’utente prova a eliminare l’ancoraggio esistente dal menu di ancoraggio, la finestra del componente Editor Rich Text viene chiusa e le modifiche rimangono non salvate. NPR-22802: Hotfix per CQ-4238167
* Il filtro Omnisearch non visualizza tutte le azioni nella console di Sites. NPR-22804: Hotfix per CQ-4239007
* Problema  relativo all’operazione Copia/Incolla nell’interfaccia touch con gli Appunti del sistema operativo e gli Appunti interni di AEM. NPR-22807: Hotfix per CQ-4220383
* Incoerenza nell’evidenziazione di estratti restituita dalla ricerca Lucene. NPR-22879: Hotfix per CQ-4238513
* Quando si attiva una pagina con istanze di  pubblicazione disattivate, viene visualizzato lo stato verde invece di quello giallo. NPR-22927: Hotfix per CQ-4236310
* (StyleSystem) La posizione dello schermo si sposta durante la selezione dello stile dalla finestra a comparsa. NPR-23183: Hotfix per CQ-4238867
* (Gestisci pubblicazione) Per passare al mese successivo del calendario sono necessari più clic. NPR-23508: Hotfix per CQ-4242732

### Piattaforma {#platform-2}

* Il servlet di esportazione Sling non esporta correttamente i caratteri giapponesi. NPR-22153: Hotfix per CQ-4228920
* Blocco critico del modulo di pianificazione durante l’avvio. NPR-22440: Hotfix per Sling-7004
* Impossibile sincronizzare i gruppi tra due istanze di pubblicazione. NPR-21943: Hotfix per GRANITE-19564
* Problemi di prestazioni relative al risolutore risorse/sessioni condivise org.apache.sling.i18n. NPR-23390: Hotfix per Sling-7543

### Integrazione {#integration-5}

* ResourceResolver non chiuso in com.day.cq.analytics.sitecatalyst. NPR-22323: Hotfix per CQ-4236515
* TargetContentImpl rallenta l’esecuzione di AEM durante le query con tempi di esecuzione lunghi. NPR-22361: Hotfix per CQ-4236907
* Il motore target (mbox.js, at.js) non utilizza URL gestiti e utilizza URL contenenti due punti, che potrebbero non riuscire con determinate implementazioni. NPR-22366: Hotfix per CQ-4237854
* Quando viene fornito un file at.js o mbox.js personalizzato, lo script “include” viene scritto nella pagina in formato testo anziché con tag HTML. NPR-22441: Hotfix per CQ-4203691
* In modalità Target gli autori possono modificare un componente ereditato dalla blueprint senza annullare l’ereditarietà. NPR-22751: Hotfix per CQ-4237907
* PersonalizationDataSource genera un’eccezione Null Pointer perché manca un nodo  jcr : content. NPR-22850: Hotfix per CQ-4222122
* Il targeting AEM non riesce quando si utilizza una lingua  diversa dall’inglese. NPR-22917: Hotfix per CQ-4218213
* Quando si pubblica una pagina con contenuto di destinazione, le risorse correlate risultano mancanti. NPR-23064: Hotfix per CQ-4227119
* Gli utenti non possono visualizzare i valori di test di Parametro statico nella chiamata  mBox visibile quando si esegue il test utilizzando AT.js come libreria client nella configurazione cloud. NPR-21930: Hotfix per CQ-4234520

### WCM - Componenti Foundation {#wcm-foundation-components-1}

* iParsys crea lo spostamento della posizione dopo la deselezione della casella di controllo per annullare/disabilitare l’ereditarietà. NPR-21905: Hotfix per CQ-4230951
* La funzionalità Mostra/Nascondi del componente del menu a discesa del modulo non viene eseguita come previsto. NPR-22327: Hotfix per CQ-4222853
* Il componente CAPTCHA è stato dichiarato obsoleto per una maggiore sicurezza. Se utilizzi il componente CAPTCHA, viene visualizzato il messaggio “Il componente Captcha è obsoleto e non deve più essere utilizzato”. dopo l’installazione della versione 6.3.2.1 o di una versione successiva. Per maggiore sicurezza, si può personalizzare il componente AEM in modo da includere reCAPTCHA. NPR-22151: Hotfix per CQ-4220052

### WCM - Editor pagina {#wcm-page-editor}

* Vulnerabilità cross-site scripting (XSS) rilevabile quando si utilizza un selettore non valido. Hotfix per CQ-4270397

### Traduzione {#translation-4}

* Esame dei problemi relativi alla funzionalità Anteprima. NPR-22114: Hotfix per CQ-4223753

### Interfaccia utente {#user-interface-2}

* Problemi relativi al selettore del mese di calendario di Coral quando si imposta l’intervallo di date “min” e “max”. NPR-22716: Hotfix per CUI-7187
* (Interfaccia classica) Il componente visualizza i valori predefiniti anche se il servizio del modello dati del modulo associato è impostato su un campo vuoto. NPR-22272: Hotfix per GRANITE-19744

### GRANITE {#granite-2}

* Problemi di stabilità dell’istanza del publisher AEM di Condivisione risorse causati da perdite di memoria. NPR-22205, NPR-23178: Hotfix per Sling-5668, Sling-7292 e Sling-7470
* Non si deve utilizzare un ID servizio instabile per i nomi degli attributi di sessione. NPR-22821: Hotfix per GRANITE-21059
* Quando  una sessione whiteboard gestita http viene invalidata, viene invalidata anche la sessione del contenitore se non include altri attributi di sessione. NPR-23059: Hotfix per FELIX-5819
* All’avvio di LogbackManager, potrebbe verificarsi la perdita di alcune configurazioni OSGi. NPR-23060: Hotfix per GRANITE-19791

### Commerce {#commerce-3}

* Abilitazione della creazione del flusso di lavoro nel menu Frammenti di esperienza. NPR-22347: Hotfix per CQ-4221661
* Errori di Frammenti di esperienza riproducibili in WeRetail. NPR-21958: Hotfix per CQ-4220061
* Quando si attiva una pagina contenente un frammento di esperienza eliminato, viene generata un’eccezione NullPointerException. NPR-23179: Hotfix per CQ-4239939

### Progetti {#projects}

* (Progetto multilingue) Il progetto non elenca i processi di traduzione per più di 19 lingue. NPR-22498: Hotfix per CQ-4229978

### Flusso di lavoro {#workflow}

* (Interfaccia classica) L’attivazione o la disattivazione di un modulo di avvio del flusso di lavoro causa un comportamento non corretto. NPR-22907: Hotfix per CQ-4239153

## Forms {#forms-9}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

Gli elementi di rilievo di AEM Forms sono:

* Aggiunta del supporto per il tipo di input HTML5.
* Correzione dell’autenticazione dell’intestazione SOAP di base.
* Aggiunta del supporto per l’attributo title per il collegamento ipertestuale.
* Attivazione dell’identificatore PDF/UA nella struttura di accessibilità di Forms Designer.
* Abilitazione dell’autenticazione dei certificati per gli utenti di Workbench.
* Aggiunta del supporto per la produzione di file PDF conformi allo standard PDF/A-2a o PDF/A-3a.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-9}

#### Forms - Interfaccia utente amministratore {#forms-admin-ui}

* La password è visibile in formato testo normale durante l’esame del campo della password per le pagine di configurazione dei connettori ECM. NPR-22508: Hotfix per CQ-4236065

#### Servizio Forms {#forms-service}

* Quando SSL è abilitato, gli eventi di invio e abbandono non funzionano con Analytics per i moduli. NPR-22637: Hotfix per CQ-4237973

#### User Management {#user-management}

* Impossibile sincronizzare LDAP a causa di una versione non corretta di cglib-nodep. NPR-22493: Hotfix per CQ-4234099

#### Moduli adattivi {#adaptive-forms-2}

* Le funzioni personalizzate per l’editor di regole stanno aggiungendo un ; dopo la chiamata della funzione, per questo non è possibile eseguire la convalida anche se la funzione personalizzata restituisce true. NPR-22481: Hotfix per CQ-4235499
* Indipendentemente dal pattern selezionato per la data, il componente del selettore data non utilizza tale pattern durante la visualizzazione dei messaggi di convalida dei valori minimo e massimo. NPR-22444: Hotfix per CQ-4236269
* Il formato della data che viene inviato nella richiesta di invio deve essere allineato al pattern specificato nel componente del selettore data. NPR-22384
* Nei dispositivi Samsung con Android 6.0 non viene rispettato il numero massimo di caratteri specificato per una casella di testo di modulo adattivo. NPR-22363, NPR-22364: Hotfix per CQ-4235205
* (Microsoft Edge)(IE11) Il valore predefinito visualizzato nel componente Campo testo del modulo adattivo con campo a più righe mostra “Null”, invece di un valore vuoto. NPR-22284: Hotfix per CQ-69107
* Con la codifica di input SOAP UTF-8 in Moduli adattivi vengono errori e la pagina visualizzato non è corretta. NPR-20105: Hotfix per CQ-4222669
* Il componente Contenitore di AEM Forms non è disponibile per la modifica dopo aver configurato il modulo errato nella pagina per Sites. Hotfix per CQ-4237456
* I test di sviluppo non riescono se vengono eseguiti in server JEE. Hotfix per CQ-4222082
* Test AF non riusciti sui server JEE a causa di problemi di minificazione nel framework Calvin. Hotfix per CQ-4217220

#### Forms Manager {#forms-manager}

* (Firefox) Impossibile aggiornare le proprietà dello schema XML di Moduli adattivi perché le opzioni nel DOR (Document of Record) non risultano come già selezionate nella pagina delle proprietà. NPR-22298: Hotfix per CQ-4237402
* I moduli modificati dopo la pubblicazione della pagina non vengono più pubblicati quando si pubblica il sito. NPR-23013: Hotfix per CQ-4236566

#### Integrazione con il back-end {#backend-integration-1}

* L’autenticazione di base OOTB per i servizi SOAP non funziona per l’autenticazione di base nell’integrazione FDM. NPR-23238: Hotfix per CQ-4241308

#### Gestione della corrispondenza {#correspondence-management}

* Se gli XDP OOTB vengono utilizzati all’interno della lettera e visualizzati in anteprima, il contenuto risulta sovrapposto al piè di pagina. Hotfix per CQ-4212414

#### Servizio assemblatore {#assembler-service}

* Discrepanza tra i report di Acrobat DC e AEM sull’errore del controllo di conformità PDF/A-1b. NPR-22051, NPR-22050: Hotfix per CQ-4226128, CQ-4227671

### Programma di installazione JEE per Forms {#forms-jee-installer-8}

#### Workbench {#workbench}

* Abilitazione dell’autenticazione dei certificati per gli utenti di Workbench. NPR-20644: Hotfix per CQ-4214486
* Il download del registro dei server con Workbench funziona solo per un server e non per l’altro. NPR-21079: Hotfix per CQ-4229842

#### Gestione processi {#process-management-1}

* (Workspace HTML) Problemi relativi alle dimensioni dello schermo con le barre di scorrimento. NPR-23288
* (Workspace HTML) I punti iniziali del processo non sono visualizzati in ordine alfanumerico. NPR-22841: Hotfix per CQ-4238944
* (Workspace HTML) La funzione di preparazione dei dati viene attivata alla chiusura del modulo nell’area di lavoro. NPR-21127: Hotfix per CQ-4224574
* (Workspace HTML) Quando si richiama un processo che richiede note con descrizioni lunghe, il pulsante di espansione delle note non funziona. Hotfix per CQ-4241488

#### Core {#core-1}

* Errore durante l’avvio del modulo di pianificazione. NPR-22990
* I browser non possono memorizzare le credenziali immesse nei moduli HTML. NPR-21762: Hotfix per CQ-4206543
* I problemi segnalati nell’analisi del codice statico di Core devono essere risolti. Hotfix per CQ-104446

#### Servizio PDFG {#pdfg-service-3}

* PDF Generator non riesce a produrre documenti PDF con livelli di segnalibri specifici. NPR-22921, NPR-22285: Hotfix per CQ-4230562
* Aggiunta del supporto per la produzione di file PDF conformi allo standard PDF/A-2a o PDF/A-3a. NPR-23021: Hotfix per CQ-4214172

#### Forms Designer {#forms-designer-1}

* Identificatore PDF/UA mancante se salvato in formato PDF da Designer. NPR-23137
* Agli oggetti percorso, ad esempio bordi, sottolineature e collegamenti ipertestuali, non vengono assegnati tag durante il salvataggio in formato PDF da Designer. NPR-23136
* L’oggetto immagine non presenta alcun rettangolo di selezione se viene salvato in formato PDF da Designer. NPR-23134
* Ai collegamenti ipertestuali inline definiti in Designer non vengono assegnati tag né testo alternativo se vengono salvati in formato PDF da Designer. NPR-23133
* Quando si apre il pacchetto dati XML con AEM 6.3 Forms Designer, la formattazione XHTML viene rimossa dall’origine XML. NPR-21178: Hotfix per LC-3917046

#### Installazione di LCM {#install-lcm}

* Aggiornamento dei JAR di Jsafe a Cryptoj 6.1.3.1 nel programma di installazione e in LCM. NPR-21370

#### Servizio Firme {#signatures-service}

* Eccezione durante il tentativo di firma/certificazione digitale di un documento PDF tramite HSM. NPR-21154: Hotfix per CQ-4226978

### Bundle OSGi e pacchetti di contenuti inclusi nella versione 6.3.2.1 {#osgi-bundles-and-content-packages-included-in-5}

Elenco dei bundle OSGi inclusi in AEM 6.3.2.1

[Ottieni file](assets/do-not-localize/bundle-list_002_.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.3.2.1

[Ottieni file](assets/do-not-localize/content_package_comparison.txt)

AEM Cumulative Fix Pack 6.3.1.2 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 1 (6.3.1.0) nell’ottobre 2017.

Gli elementi di rilievo di AEM Cumulative Fix Pack sono:

* Modifica dell’interfaccia utente per supportare l’implementazione delle funzionalità per gruppi utenti chiusi (CUG) in AEM Assets.
* Correzione dei problemi relativi all’interfaccia utente nella pagina di controllo della licenza per migliorare l’esperienza.
* Abilitazione del supporto per le attività del flusso di lavoro OSGi nell’app AEM Forms.

### Risorse {#assets-10}

* Modifica dell’interfaccia utente per supportare l’implementazione delle funzionalità per gruppi utenti chiusi (CUG) in AEM Assets. NPR-19485
* Il caricamento di una risorsa come nodo figlio diretto di se stesso tramite l’interfaccia touch causa un problema. La risorsa viene caricata come elemento figlio diretto della risorsa selezionata in precedenza. NPR-19736
* Il predicato di Intervallo date e il predicato di Intervallo non funzionano quando si carica una ricerca salvata o una raccolta avanzata. NPR-19844: Hotfix per CQ-4220808
* Si riscontrano rallentamenti nell’istanza di AEM quando si pubblicano più di quattro risorse su Brand Portal. NPR-20009: Hotfix per CQ-4213426
* Impossibile scaricare risorse con spazi dalla pagina di controllo della licenza. NPR-20067: Hotfix per CQ-4216557
* Problemi di elaborazione durante il caricamento di file PSB con più livelli alfa. NPR-20250: Hotfix per CQ-4220869
* Gli utenti non possono scaricare risorse definite con nomi file lunghi e liberatoria. NPR-20254
* ProductAssetsUploader lascia i file temporanei della cache JAVA nella cartella TEMP di Java. NPR-20256: Hotfix per CQ-4221801
* Sostituzione del codice di confronto delle versioni con il codice proprietario Adobe a causa di problemi di licenza. NPR-20272: Hotfix per CQ-4223758
* I metadati di una proprietà stringa documentNumber vengono visualizzati sotto forma di data, mentre dovrebbero essere un numero. NPR-20291: Hotfix per CQ-4223991
* L’estrazione del testo si blocca per un PDF danneggiato. NPR-20416: Hotfix per CTG-4150375
* I file compressi che includono risorse con nomi non compatibili con UTF-8 non vengono scaricati correttamente. NPR-20420: Hotfix per CQ-4219961
* Un numero eccessivo di caratteri in OmniSearch causa l’arresto anomalo del server AEM. NPR-20434: Hotfix per CQ-4223602
* Il difetto dei metadati dell’API delle risorse DAM interrompe le API xmp -write-back. NPR-20607: Hotfix per CQ-4220455
* Problemi di prestazioni durante l’aggiunta di utenti alle raccolte. NPR-20699: Hotfix per CQ-4225733
* La pubblicazione su Brand Portal da AEM non deve essere consentita per i set Dynamic Media. NPR-20320: Hotfix per CQ-4221147
* Se il nome del video contiene spazi o accenti, non viene prodotto alcun video per la pagina Rendering. NPR-19961: Hotfix per CQ-4221014
* Risoluzione di diversi problemi di gestione delle cartelle con le API di Assets. NPR-20569
* AEM Dynamic Media Classic (in precedenza Scene7) non riesce a sincronizzare le risorse dal server AEM quando il percorso di destinazione nella configurazione del servizio cloud punta a una sottocartella nel percorso principale. CQ-4228265
* È stato aggiunto il bundle per l’e-mail di Apache Commons `{org.apache.commons/commons-email/1.5}`in sostituzione di `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`

### Sites {#sites-10}

* Problemi relativi all’autorizzazione dell’amministratore: impossibile rimuovere i membri di Gruppo utenti chiuso dalle proprietà della pagina. NPR-20631
* Il nome del flusso di lavoro digitato deve essere disponibile nella casella Notifica quando si pubblica una pagina tramite Gestisci pubblicazione. NPR-20046: Hotfix per CQ-4221586
* Quando si applica testo formattato su due righe nell’Editor Rich Text e si uniscono tali righe in un unico paragrafo, le espansioni formattate vengono rimosse. NPR-20110: Hotfix per CQ-4223051
* Le modifiche apportate alle proprietà di campo in più schede nella finestra di dialogo di modifica delle proprietà talvolta non vengono salvate. NPR-20286
* Tag imprevisto alla fine del contenuto incollato nel frammento di contenuto. NPR-20413: Hotfix per CQ-4224014
* Implementazione di un meccanismo in Adobe Campaign per recuperare i criteri di una risorsa di contenuto da una risorsa di targeting esterna. NPR-20667
* Il plug-in Rich Text non funziona sia per la barra inline che per la barra a schermo intero nell’interfaccia utente touch a più campi. NPR-20973

### Campaign {#campaign-1}

* I segnaposto non sono visibili in una pagina che contiene più componenti parsys. NPR-20436: Hotfix per CQ-4215000

### Commerce {#commerce-4}

* I frammenti di esperienza non vengono visualizzati correttamente in Internet Explorer 11. NPR-20161: Hotfix per CQ-4223319
* Nei flussi di lavoro di Commerce, quando si crea una variante basata su un prodotto primario con più immagini viene inserita automaticamente un’immagine vuota. NPR-20068: Hotfix per CQ-4222048
* Il filtro per tag nelle pagine della raccolta della console Prodotti non funziona. NPR-20292: Hotfix per CQ-4224023

### Community {#communities-8}

* Risultati di ricerca non coerenti con il componente Risultato di ricerca. NPR-20070: Hotfix per CQ-4220913
* Le notifiche e-mail non vengono attivate per nessuna delle attività correlate al moderatore nei componenti pubblicati. NPR-20122
* Per gli utenti anonimi della community viene visualizzata una paginazione vuota senza risultati. NPR-20136: Hotfix per CQ-4220738
* Configurazione dell’attivazione dell’avviso quando un contenuto generato dall’utente (UGC) viene rilevato come spam o quando un utente pubblica in un sito con pre-moderazione dei contenuti. NPR-20274: Hotfix per CQ-96850
* Risoluzione di diversi problemi nelle pagine del sito di AEM Communities, tra cui reindirizzamenti non corretti e problemi di aggiornamento delle pagine. NPR-20344
* CommunityUserOperationExtension viene eseguito in un’eccezione di cast di classe. NPR-20532: Hotfix per CQ-4224385
* Dopo aver creato un sito Communities, gli utenti non possono aprirlo dalla mappa del sito perché il percorso di contesto non viene aggiunto all’inizio dell’URL. NPR-20730

### Integrazione {#integration-6}

* Migrazione delle credenziali esistenti di Analytics all’autenticazione WSSE. NPR-19962: Hotfix per CQ-4218071
* La riattivazione del segmento dopo qualsiasi modifica non riesce e viene generato un errore. NPR-20054: Hotfix per CQ-4218401
* Durante la configurazione del servizio cloud Search&amp;Promote il metodo di recupero del modulo viene ignorato, di conseguenza il modulo diventa inutilizzabile nell’istanza di creazione. NPR-20447: Hotfix per CQ-4206076
* La definizione ambigua del filtro nel pacchetto di contenuti causa la sovrascrittura dei percorsi quando si installa la funzione Search&amp;Promote. NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* Le proprietà dei metadati per le risorse di tipo TXT vengono visualizzate in editor di metadati diversi ogni volta che se ne visualizzano le relative proprietà. NPR-20239

### Piattaforma {#platform-3}

* Risoluzione di un’eccezione relativa al risolutore risorse non chiuso. NPR-19749: Hotfix per GRANITE-19143
* Richiesta relativa alla visualizzazione di schede personalizzate insieme ai controlli di integrità predefiniti nel dashboard operazioni. NPR-20145
* Il livello Annotazione dell’Editor pagina non funziona correttamente in Internet Explorer 11. NPR-20222: Hotfix per CQ-4222818
* Interruzione della sessione quando si imposta l’agente utente come amministratore nell’agente di replica. NPR-20578
* requestAttributes non viene disattivato per le altre istruzioni data-sly-resource. NPR-20639: Hotfix per 4226206
* Risoluzione dei problemi relativi alle richieste di intestazione curl per le risorse OOTB in AEM. NPR-20781: Hotfix per CQ-4221520

### Progetti {#projects-1}

* L’accesso a progetti diversi dalla console Progetti richiede un tempo di caricamento più lungo. NPR-20314
* Quando si installa AEM 6.3.0.1, l’archivio chiavi dell’utente del servizio di aggiornamento DAM viene rimosso. NPR-20018
* In alcune distribuzioni personalizzate, gli utenti che cercano di selezionare l’assegnatario nel modulo addTask impiegano più tempo per compilare l’elenco nel selettore utente. NPR-20283: Hotfix per CQ-4224193

### Interfaccia utente {#user-interface-3}

* Il campo colore è impostato su “always required” (sempre obbligatorio) nonostante gli attributi nella finestra di dialogo. NPR-19702
* La barra di scorrimento non viene visualizzata per il componente a più campi a schermo intero in Internet Explorer 11. NPR-20261: Hotfix per CQ-4219782
* Le query precedenti non vengono interrotte in caso di attivazione di query consecutive e vengono generati risultati non corretti. NPR-20398: Hotfix per GRANITE-19306

### Flusso di lavoro {#workflow-1}

* Gli utenti vengono informati sulle attività del flusso di lavoro ricevute nella casella in entrata. NPR-20213: Hotfix per CQ-4221639
* Il selettore utenti GRANITE OOTB non carica alcun utente quando si fa clic sul menu a discesa nel passaggio del partecipante della finestra di dialogo del modello di flusso di lavoro. NPR-20236

## Forms {#forms-10}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-10}

#### Moduli adattivi {#adaptive-forms-3}

* Manca il supporto per l’espressione di aggregazione relativa ai pannelli ripetuti. NPR-20861
* Il menu a discesa visualizza l’ultimo valore memorizzato anche se il servizio del modello dati del modulo associato non restituisce alcun valore. NPR-20710
* Impossibile modificare le regole esistenti con vincoli booleani nell’editor delle regole. NPR-21128

#### Portale moduli {#form-portal}

* Viene visualizzato il profilo HTML per un modulo adattivo anche quando il relativo tipo di risorsa non è XDP. NPR-20079

#### Integrazione con il back-end {#backend-integration-2}

* Impossibile impostare il valore del componente switch tra true/false. NPR-21111

#### Flusso di lavoro OSGi {#osgi-workflow}

* Con l’invio di Gestisci flusso di lavoro vengono elencate solo dieci applicazioni. CQ-4230193

#### Moduli HTML5 {#html-forms-3}

* Come descrizione comando di un oggetto modulo XDP, ad esempio un sottomodulo, viene visualizzato il relativo nome quando non è definito nelle configurazioni di accessibilità. NPR-20523

### Programma di installazione JEE per Forms {#forms-jee-installer-9}

#### Gestione processi {#process-management-2}

* Il punto iniziale di FormSetPrefillApp non precompila i campi del set modulo nell’app AEM Forms. NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* Installare la libreria CTJPEG2K più recente per una vulnerabilità di sicurezza critica. Questo problema interessa i moduli XMLFM (AEM e IfBA), RM e PDFG. NPR-20625, NPR-21337.

### Feature Pack inclusi {#feature-packs-included}

#### App AEM Forms {#aem-forms-app}

* Abilitazione del supporto per le attività del flusso di lavoro OSGi nell’app AEM Forms. CQ-4222638

### Bundle OSGi e pacchetti di contenuti inclusi nella versione 6.3.1.2 {#osgi-bundles-and-content-packages-included-in-6}

Elenco dei bundle OSGi inclusi in AEM 6.3.1.2

[Ottieni file](assets/do-not-localize/6_3_1_2-bundle-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM 6.3.1.2

[Ottieni file](assets/do-not-localize/6_3_1_2-content-package-list.txt) AEM Cumulative Fix Pack 6.3.1.1 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 Service Pack 1 (6.3.1.0) nell’ottobre 2017.

Gli elementi di rilievo di AEM Cumulative Fix Pack sono:

* Abilitazione dell’azione Pubblica su Brand Portal per il modulo schema metadati predefinito.
* Modifica del comportamento nella visualizzazione dei titoli nella scheda Immagine per un’immagine con la proprietà dc: title impostata su String [] (multifield).
* Sostituzione del rendering del tempo lato server con il componente di tempo di Foundation.
* Abilitazione della pubblicazione di tag da AEM a Brand Portal dalla console tagadmin/tagging.
* Pubblicazione dell’API JSON per l’utilizzo di frammenti di contenuto.
* Aggiornamento dell’archivio incorporato (Apache Jackrabbit Oak) alla versione 1.6.5.

### Risorse {#assets-11}

* Quando si mappano due campi con la stessa proprietà e tipi di campo proprietà diversi, viene generato un errore interno. NPR-19462: Hotfix per CQ-4216828
* dc:title e dc:description non vengono modificati in un valore a più campi in  crx /de. NPR-19570: Hotfix per CQ-4209086
* Il visualizzatore dinamico carica un rendering video di qualità inferiore per testare l’esperienza di riproduzione video in modalità di creazione. NPR-19004
* Non è possibile scaricare il rendering dinamico per le risorse il cui nome contiene spazi. NPR-19433: Hotfix per CQ-4211738
* Impossibile caricare l’elenco completo delle pagine/risorse nella vista a colonne utilizzando Chrome. NPR-19566: Hotfix per CQ-4214248
* L’opzione Pubblica su Brand Portal non è disponibile quando si seleziona uno schema, un facet di ricerca o un predefinito. NPR-19550
* Quando si seleziona una risorsa nella vista a colonne e si fa clic su Modifica, la pagina restituisce un errore. NPR-20301: Hotfix per CQ-4224052
* La visualizzazione della scadenza delle risorse è disattivata quando si attraversano fusi orari positivi e negativi. NPR-20329: Hotfix per CQ-4219333

### Campaign {#campaign-2}

* I componenti cursore di Campaign non vengono visualizzati quando si seleziona l’esperienza predefinita per una campagna. NPR-19213

### Integrazione {#integration-7}

* Il file at.js personalizzato non viene pubblicato se vi si accede con l’utente anonimo. NPR-19542: Hotfix per CQ-4219592
* Il campo Motore di destinazione nella configurazione guidata è impostato su ContextHub (AEM) invece di Adobe Target. NPR-19320: Hotfix per CQ-4218465
* La sezione Pubblico viene danneggiata durante la creazione dell’esperienza. NPR-19110
* La finestra di dialogo Impostazione destinazione non viene visualizzata in modalità di targeting quando un modulo di destinazione viene modificato e salvato più volte. NPR-19144: Hotfix per CQ-4216708
* L’accesso alle proprietà per gli articoli viene impostato in modo errato nell’interfaccia classica di Adobe Digital Publishing Solution. NPR-19367
* Comportamento non corretto della piegatura automatica quando si personalizzano le offerte tramite Campaign se gli utenti hanno accesso a più aree. NPR-19290: Hotfix per CQ-4218029

### Sites {#sites-11}

* I valori dell’elenco a discesa di campi compositi multipli non vengono ricompilati a causa della modifica del codice in Sidekick.js dopo l’aggiornamento dell’istanza ad AEM 6.1SP2-CFP3. NPR-19450: Hotfix per CQ-4194771
* WCMMode.EDIT non funziona per i componenti di destinazione in modalità authoring. NPR-19387
* Pubblicazione dell’API JSON per l’utilizzo di frammenti di contenuto. NPR-19500
* La funzionalità Grassetto, Corsivo e Sottolineato non funziona per i campi dell’Editor Rich Text nella finestra di dialogo di creazione. NPR-19670, NPR-19718: Hotfix per CQ-4219088

### Mobile On-Demand {#mobile-on-demand-1}

* Problemi di rendering relativi alla console degli articoli AEM, la cui esecuzione risulta più lenta quando si utilizzano immagini a dimensione intera. NPR-19088

### Traduzione {#translation-5}

* Impossibile generare l’anteprima per i progetti di traduzione. NPR-19289

### Sicurezza {#security}

* Errore di connessione SSL. Impossibile stabilire una connessione protetta al server. NPR-19628

### Community {#communities-9}

* La posta viene attivata in caso di pubblicazione di contenuto con siti con pre-moderazione. NPR-20008
* Le notifiche e-mail non funzionano per nessuna delle attività relative al moderatore nei componenti pubblicati. NPR-19767: Hotfix per CQ-4218060

### Piattaforma {#platform-4}

* Problemi di stabilità relativi alla distribuzione del server di produzione AEM. NPR-19707
* La libreria Tag personalizzata che fa riferimento a tag implementati come script non viene trovata dopo l’aggiornamento ad AEM 6.3. NPR-19087
* Correzioni di bug HTL per AEM 6.3.1. NPR-19161
* Il campo Rich Text non è modificabile nei componenti a più campi. NPR-19604: Hotfix per GRANITE-16755
* Il servizio Modello e-mail Adobe aggiunge tag ai modelli utente personalizzati. NPR-19190
* Hotfix per Oak 1.6.5. NPR-19148

### Commerce {#commerce-5}

* Il pulsante Avvia flusso di lavoro non ha alcun effetto dopo la selezione di un editor di varianti XF. NPR-19642: Hotfix per CQ-4207796

### Progetti {#projects-2}

* Gli editor di progetti non possono copiare/incollare risorse nella cartella delle risorse del progetto. NPR-19619: Hotfix per CQ-4215321

### Gestione contenuti Web {#web-content-management}

* Nella schermata Rollout, le caselle di controllo corrispondenti alle pagine Live Copy non possono essere selezionate o deselezionate. NPR-19518
* La modifica collettiva di proprietà della pagina non è utilizzabile correttamente, perché al momento tutte le schede e i campi sono disponibili per la modifica collettiva. NPR-19451
* Le proprietà OOTB e le proprietà di allineamento delle immagini non vengono visualizzate quando si modifica un’immagine nell’interfaccia classica. NPR-19488: Hotfix per CQ-4217914

### Interfaccia utente {#user-interface-4}

* Quando si utilizza il browser Google Chrome, gli utenti non riescono a caricare l’elenco completo delle pagine/risorse utilizzando la vista a colonne nell’interfaccia touch. NPR-19566: Hotfix per CQ-4214248

### Brand Portal {#brand-portal-1}

* Impossibile pubblicare da AEM risorse con commenti e annotazioni. NPR-19590: Hotfix per CQ-4218386
* Abilitazione della pubblicazione di tag da AEM a Brand Portal dalla console tagadmin/tagging. NPR-20271: Hotfix per CQ-4223948
* Correzione del campo “abilitato” nell’interfaccia utente di configurazione del servizio cloud di Brand Portal. Hotfix per CQ-4211101
* La replica del modulo di ricerca non riesce. Hotfix per CQ-4220080

## Forms {#forms-11}

Le correzioni per AEM Forms vengono distribuite tramite pacchetti di componenti aggiuntivi e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta Versioni di AEM Forms.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-11}

#### Moduli adattivi {#adaptive-forms-4}

* Con il flusso di lavoro di invio a JEE il parametro di output lato JEE non viene restituito ad AEM e viene visualizzato un messaggio di tipo “Ignorato perché il valore non è primitivo”. NPR-20265
* Il componente Moduli adattivi non consente l’utilizzo di PDF come allegati in Safari. NPR-19625
* RestoreGuideState sovrascrive la mappa customcontextproperty. CQ-4222877
* Durante la configurazione di Google reCaptcha con Cloud Service, in ambienti che richiedono la configurazione di org.apache.http.proxyconfigurator per le connessioni esterne, sembra che le chiamate POST non vengano gestite tramite PROXY. NPR-20454
* I moduli adattivi basati su schemi XSD inviano valori XML errati per i campi numerici in installazioni con impostazioni internazionali che usano separatori decimali diversi da “.” causando errori. NPR-20444
* Le impostazioni proxy specificate per Apache HTTP Components Proxy Configuration (Configurazione proxy per componenti HTTP Apache) non vengono rispettate quando si effettua la richiesta HTTP a un server di terze parti. Problemi di timeout della connessione quando si usano chiamate HTTP GET o POST. NPR-20457, NPR-20456, NPR-20455, NPR-20451

#### Integrazione dei dati Forms {#forms-data-integration}

* I caratteri UTF-8 restituiti dal servizio SOAP non vengono copiati correttamente nei campi di Moduli adattivi per le lingue diverse dall’inglese. NPR-20238, NPR-20103

#### Gestione della corrispondenza {#correspondence-management-1}

* Quando si copia e incolla contenuto dal file di Word, il colore e il font del contenuto vengono persi nell’editor di testo. NPR-19521

#### Servizi assemblatore {#assembler-services}

* Discrepanza tra i risultati di Acrobat e AEM durante una verifica della conformità di un documento rispetto al formato PDFA-1b. NPR-19280

#### Flusso di lavoro {#workflow-2}

* Aggiunta del passaggio per la firma del flusso di lavoro per consentire la connessione di chiamate HTTP tramite il proxy. NPR-20529

#### Moduli HTML5 {#html-forms-4}

* Aggiunta del supporto per l’evento preSubmit. NPR-20604

### Programma di installazione JEE per Forms {#forms-jee-installer-10}

#### Gestione processi {#process-management-3}

* Le schede allegati, note e dettagli del flusso di lavoro non funzionano nell’area di lavoro quando il modulo viene ingrandito o ridotto a icona e salvato come bozza o inoltrato. NPR-20243
* Il campo di testo a più righe (TextArea) non mantiene l’interruzione o il carattere di nuova riga nel testo dopo l’invio dei dati nell’area di lavoro HTML. NPR-20085

#### Reporting processi {#process-reporting}

* Durante il reporting dei processi i dati non vengono recuperati correttamente a causa di un’eccezione Null Pointer. NPR-19759

>[!NOTE]
>
>Per risolvere il problema, installa il pacchetto di incorporazione LiveCycle indicato nell’articolo [Versioni di AEM Forms](aem-forms-releases.md).

#### Servizi standard {#standard-services}

* docConvertor non supporta l’appiattimento delle trasparenza in PDF e non genera un PDF/A. NPR-16228: Hotfix per CQ-4214488

#### Core {#core-2}

* Quando il server AEM Forms in esecuzione in una configurazione cluster nell’applicazione JBoss viene arrestato, il server applicazione viene disconnesso dal database. Questo comportamento può causare problemi di danneggiamento dei dati. NPR-19724

### Feature Pack inclusi {#feature-packs-included-1}

* Non è possibile rendere obbligatorio il campo dello schema metadati dell’elenco a discesa perché per le risorse manca la convalida obbligatoria dei campi. NPR-17882: FP per CQ-4208373

### Bundle OSGi e pacchetti di contenuti inclusi nella versione 6.3.1.1 {#osgi-bundles-and-content-packages-included-in-7}

Elenco dei bundle OSGi inclusi in AEM CFP 6.3.1.1

[Ottieni file](assets/do-not-localize/bundle-list.txt)

Elenco dei pacchetti di contenuti inclusi in AEM CFP 6.3.1.1

[Ottieni file](assets/do-not-localize/content-package-list.txt)

AEM Cumulative Fix Pack 6.3.0.2 è un aggiornamento importante che include diverse correzioni di problemi interni e segnalati dai clienti, introdotte successivamente alla data di disponibilità generale di AEM 6.3 nell’aprile 2017.

Gli elementi di rilievo di AEM Cumulative Fix Pack sono:

* Verificabilità del controllo di accesso degli utenti
* Include la versione 1.6.2 dell’archivio incorporato (Apache Jackrabbit Oak)
* Risoluzione dei problemi relativi al risolutore risorse non chiuso.
* Configurazione semplificata per i servizi di contenuti avanzati
* Risoluzione dei problemi di convalida dei frammenti di contenuto
* Miglioramento della modificabilità degli schemi di metadati sui dispositivi ibridi
* Risoluzione dei problemi di sincronizzazione a livello di componente nelle Live Copy
* Miglioramento dell’usabilità delle pagine ricche di contenuti nella vista a colonne
* Miglioramento della conformità alle convenzioni di denominazione delle pagine per le pagine con titoli lunghi
* Miglioramento dell’esperienza di personalizzazione delle campagne nell’interfaccia utente touch
* Correzioni relative a diversi problemi di sovrapposizione dei progetti

### Piattaforma {#platform-5}

* Hotfix per Oak 1.6.2. NPR-16993
* Quando si apre Omnisearch utilizzando un filtro, il percorso non risulta più impostato. NPR-17398: Hotfix per CQ-4204870
* Requisito relativo alla verificabilità delle modifiche delle autorizzazioni utente in AEM. NPR-17061
* Connessioni in sospeso a DM Cloud Services causano eccezioni di tipo “Troppi file aperti”. CQ-4211407

### Risorse {#assets-12}

* Problemi di usabilità quando si configurano servizi di contenuti avanzati utilizzando opzioni diverse. NPR-18200: Hotfix per CQ-4201557
* Perdita di risorse nei flussi binari indirizzati all’archivio dati S3. NPR-18041: Hotfix per CQ-4209506
* Si verifica un errore quando un file di testo con codifica ASCII/UTF-8 viene caricato in AEM Assets e la generazione delle miniature non riesce. NPR-18006: CFP per CQ-4209345
* Lo schema metadati predefinito causa un errore di convalida del frammento di contenuto. NPR-17769: Hotfix per CQ-4211111
* Risolutore risorse non chiuso in com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner. NPR-17598: CFP per CQ-4209018
* Richiesta di creazione di più agenti di replica per la pubblicazione di risorse su Brand Portal. NPR-17189
* L’attività di revisione delle risorse nella cartella in lingua giapponese non funziona. CQ-4204782
* Si verifica un’eccezione Null Pointer quando una risorsa viene spostata dalla relativa pagina di proprietà. CQ-4204251
* AEM non tiene traccia dei riferimenti successivi a una risorsa nella pagina di proprietà se è collegata più volte a un documento InDesign. CQ-4204186
* Problemi relativi all’aggiunta di nuove schede nel modulo dello schema metadati quando lo schema viene modificato in Chrome su dispositivi ibridi. CQ-4201810
* Quando vengono caricate risorse duplicate, l’opzione Elimina/Mantieni viene applicata a tutte le risorse anche se non è selezionata nella finestra di dialogo Duplicati rilevati. CQ-4201673
* Quando si sposta una cartella di risorse con più di 150 riferimenti in entrata, viene generata un’eccezione Null Pointer. CQ-4200981
* Se per una cartella di risorse scaricata si verifica un conflitto durante l’estrazione del contenuto del file ZIP, l’opzione predefinita visualizzata è Crea versione invece di Mantieni entrambe. CQ-97800
* Gli utenti con autorizzazioni di sola lettura per l’app non possono visualizzare l’anteprima del contenuto dalla gestione dei contenuti di AEM Mobile. NPR-17486: CFP per CQ-4209690
* Il pulsante Crea catalogo non funziona nella vista a colonne della console Catalogo. CQ-4209952

### Sites {#sites-12}

* Problemi relativi all’incorporamento di componenti immagine/video tramite l’attributo data-sly-resource. NPR-18182: CFP per CQ-4212100
* I componenti localizzati modificati non vengono ripristinati nel modulo originale quando viene riapplicata l’ereditarietà in una Live Copy. NPR-18172: Hotfix per CQ-4211379
* Problemi relativi alla navigazione in una pagina ricca di contenuti nella vista a colonne dell’interfaccia utente touch. NPR-17799: Hotfix per CQ-4199611
* Risolutore risorse non chiuso in `com.day.cq.wcm.core.impl.VersionManagerImpl`. NPR-17789: CFP per CQ-4211152
* Il nome della pagina non viene generato conformemente alla convenzione per i titoli di pagina lunghi. NPR-17633: Hotfix per CQ-4209056
* Problemi relativi alla creazione di pagine nell’interfaccia utente touch in AEM 6.3 implementato in Jboss EAP 6.4. NPR-17589: Hotfix di CQ-4210137
* Il provider dello stato del flusso di lavoro causa il blocco dell’istanza quando sono presenti gruppi nidificati. NPR-17556: Richiesta di CFP per CQ-4202056
* Risolutore risorse non chiuso negli oggetti seguenti:

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497: CFP per CQ-4208673
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495: CFP per CQ-4208668
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494: CFP per CQ-4208669
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493: CFP per GRANITE-17404

### Integrations (Integrazioni) {#integrations-1}

* Risoluzione di errori del componente AEM - Ricerca che possono verificarsi quando l’OSGi AEM Day HTTP Client 3.1 è configurato con un proxy che richiede l’autenticazione digest. NPR 18128: Hotfix per NPR-18029
* Problemi relativi alla personalizzazione di campagne e delle esperienze associate tramite l’interfaccia classica. NPR-18127: Hotfix per CQ-4211559
* Quando si imposta un marchio o una zona su una pagina principale di un sito, non è possibile ripristinare l’ereditarietà annullata per le aree nelle pagine secondarie. NPR-17753: Hotfix per CQ-4210139

### Flusso di lavoro {#workflow-3}

* In un flusso di lavoro non transitorio, la cronologia dei processi e le modifiche apportate ai metadati prima di un passaggio del processo esterno non vengono mantenute. NPR-17848: Hotfix per GRANITE-17757
* I valori provenienti dai campi della finestra di dialogo del flusso di lavoro non vengono mantenuti nel nodo dell’elemento di lavoro. NPR-17734: Hotfix per CQ-4210369
* Si verifica un errore di data non analizzabile durante la modifica dell’attività dalla casella in entrata. CQ-4208749

### Progetti {#projects-3}

* Correzioni relative a diversi problemi di sovrapposizione dei progetti. NPR-17733
* La ristrutturazione dei pod nel modulo dei progetti rende il modulo meno configurabile. CQ-4209859
* Il percorso delle risorse viene impostato sui rispettivi siti localizzati quando le pagine vengono aggiunte al processo di traduzione. CQ-4206007

### Sicurezza {#security-1}

* Problemi relativi al caricamento di immagini avatar per gli utenti LDAP. NPR-16561
* Richiesta di utilizzare una versione aggiornata di org.apache.sling.servlets.post servlet (2.3.22) nell’API Sling Apache per prevenire una vulnerabilità XSS. NPR-18963

## Forms {#forms-12}

Le correzioni per AEM Forms vengono distribuite tramite il pacchetto di componenti aggiuntivi per Forms e altri programmi di installazione delle patch forniti con la versione. Per informazioni dettagliate, consulta [Versioni di AEM Forms](aem-forms-releases.md).

Gli elementi di rilievo di AEM Forms sono:

* Le correzioni apportate ai moduli di testo per la gestione della corrispondenza, alle anteprime delle lettere e all’avvio a livello di programmazione dell’interfaccia utente per la gestione della corrispondenza.
* Correzioni relative alla convalida PDF/A-1b e alla conversione di file immagine di grandi dimensioni in formato PDF e di documenti PDF in giapponese in PDF Generator.
* Correzioni relative all’usabilità per la gestione della corrispondenza, la sicurezza dei documenti e il flusso di lavoro per i moduli.
* Aggiunta del supporto per l’acquisizione di eventi di controllo per il campo della firma scarabocchio.

### Pacchetto di componenti aggiuntivi per Forms {#forms-add-on-package-12}

**Gestione della corrispondenza**

* Quando si modifica un frammento di gestione della corrispondenza, l’editor di testo visualizza le condizioni inline insieme al testo elaborato. CQ-4211930
* Quando si crea una lettera di gestione della corrispondenza, la descrizione della lettera non viene salvata. NPR-18089
* Il margine aggiuntivo sopra e sotto un elenco puntato è visibile nell’editor di testo, ma non nel rendering HTML e PDF. NPR-18126
* Quando per l’invio HTML è stato utilizzato il metodo POST, l’interfaccia utente per la corrispondenza non viene avviata. NPR-18202
* Quando un modulo di testo viene salvato e un’espressione nel modulo di testo non contiene tag di espressione di apertura o chiusura, non viene visualizzato alcun messaggio di errore. Il modulo di testo visualizza un messaggio di errore e non riesce a eseguire il rendering nella lettera. NPR-18535
* Quando si aggiunge nuovo contenuto o si preme il tasto Invio, al modulo di testo viene aggiunto un tag div. NPR-18240

**Assemblatore**

* Quando si convalida un documento PDF per la conformità PDF/A-1b, AEM Forms restituisce un errore di convalida: PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED. Il documento PDF non restituisce l’errore se viene convalidato con Adobe Preflight e software di terze parti. NPR-18011
* Quando si convalidano documenti PDF per la conformità PDF/A-1b, AEM Forms restituisce un errore di convalida simile a Form field has multiple appearances (L’aspetto del campo modulo è variabile). I documenti PDF sono conformi allo standard PDF/A-1b. NPR-18013

**Cartella di controllo**

* Quando si seleziona l’opzione per elaborare i file con un flusso di lavoro, durante la creazione di una cartella di controllo viene visualizzato il menu a discesa per la selezione del modello di flusso di lavoro. NPR-17566

**Moduli HTML5**

* AEM Forms non acquisisce eventi di controllo per il campo della firma scarabocchio. NPR-15286

**Forms Manager**

* Nell’interfaccia utente di AEM Forms sono elencate tutte le risorse a partire da quelle meno recenti. Gli utenti non possono riordinare le risorse in modo da visualizzare per prime quelle più recenti. NPR-18450

**Riferimento per API Java**

Aggiunta di JavaDocs per la classe com.adobe.livecycle.content. NPR-18468

### Programma di installazione JEE per Forms {#forms-jee-installer-11}

**PDF Generator**

* Il servizio PDF Generator non riesce a convertire immagini di dimensioni superiori a 100 MB in documenti PDF. Ref. CQ-4208628
* Quando si utilizza il servizio PDF Generator con un OCR in lingua giapponese, viene generato un PDF invertito. NPR-17602

**Gestione processi**

* La variabile TaskContext non viene compilata per i processi AEM Forms. NPR-18199

**Sicurezza dei documenti**

* Microsoft Excel e Microsoft PowerPoint impiegano molto più tempo per aprire i documenti protetti con l’estensione di sicurezza dei documenti AEM per Microsoft Office. CQ-4212358
* Quando viene creato un nuovo criterio ed esiste già un criterio con lo stesso nome, si verifica un errore interno del server. NPR-18247

## Feature Pack inclusi {#feature-packs-included-2}

* Requisito relativo alla verificabilità delle modifiche delle autorizzazioni utente in AEM. NPR-17061

AEM Cumulative Fix Pack 6.3.0.1 è un aggiornamento importante che include diverse correzioni interne e per i clienti a partire dalla disponibilità generale di AEM 6.3 nell’aprile 2017. Le principali caratteristiche del Cumulative Fix Pack AEM sono:

* Miglioramenti nelle aree seguenti:

   * Frammenti di contenuto, Sites e componenti Editor Rich Text, Editor regole ed Editor modelli
   * Accesso social network tramite Facebook e Social Review
   * Configurazione e avvio di processi di traduzione
   * Tempo di risposta per l’accesso alle notifiche in Social community
   * Visualizzazione delle attività di revisione nell’archivio DAM

* Opzione di convalida disponibile in Gestione pacchetti per rilevare i conflitti tra sovrapposizione e CFP

## Istruzioni per il download di CFP tramite Software Distribution {#download-instructions-for-cfp-via-package-share}

Puoi scaricare il pacchetto CFP direttamente da [Software Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8) oppure eseguire i seguenti passaggi:

1. Apri [Software Distribution](https://experience.adobe.com/downloads). Per accedere a Software Distribution è necessario disporre di un Adobe ID.
1. Tocca **[!UICONTROL Adobe Experience Manager]** che si trova nel menu di intestazione.
1. Tocca il nome del pacchetto, seleziona **[!UICONTROL Accetta termini EULA]**, quindi tocca **[!UICONTROL Scarica]**.

## Istruzioni di installazione {#installation-instructions}

Questa sezione descrive i requisiti e i passaggi necessari per installare il CFP.

### Prima dell’installazione {#before-you-install}

>[!NOTE]
>
>I Feature Pack opzionali forniti da Adobe dipendono dalla versione e dal Cumulative Fix Pack disponibili. Se hai installato un Feature Pack, contatta il [team di Assistenza clienti di AEM](https://helpx.adobe.com/it/marketing-cloud/contact-support.html) per verificare la compatibilità con questo Cumulative Fix Pack per AEM 6.3.

>[!NOTE]
>
>Prima di installare il pacchetto, è consigliabile eseguire la convalida su ogni nuovo pacchetto di installazione. La pre-convalida analizza e segnala eventuali errori riscontrati prima dell’installazione avvisando gli utenti di tali errori in modo proattivo.
>
>La documentazione relativa all’opzione Convalida è disponibile al sito [https://docs.adobe.com/content/docs/it-IT/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/it-IT/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* AEM 6.3.3.0 è un prerequisito per il CFP. Per istruzioni dettagliate sull’aggiornamento di un’installazione di AEM ad AEM 6.3, consulta la [documentazione relativa all’aggiornamento.](https://docs.adobe.com/docs/en/aem/6-3/deploy/upgrade.html)
* Per un’implementazione cluster tramite RDBMK o MongoDB, il pacchetto CFP può essere installato in una qualsiasi delle istanze di creazione che utilizza Gestione pacchetti.
* Prima di installare il Cumulative Fix Pack, assicurati di creare uno snapshot o eseguire un backup dell’istanza AEM.
* La disinstallazione del CFP non è supportata.

### Aggiunta di nuovi logger {#adding-new-loggers}

Per configurare la registrazione a livello di debug e recuperare un registro attività durante l’installazione di SP/CFP, puoi effettuare le seguenti operazioni:

* Puoi aggiungere un nuovo logger nel percorso predefinito [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) specificando le seguenti proprietà:

   * Log Level: Debug
   * Additive: false
   * Log File: logs/activity.log
   * Logger: org.apache.jackrabbit.vault.packaging.impl.ActivityLog

Il registro activity.log verrà creato nella cartella crx -quickstart /logs.

### Installare Cumulative Fix Pack tramite Software Distribution {#install-the-cumulative-fix-pack-via-package-share}

Per installare il Cumulative Fix Pack in un’istanza AEM 6.3 esistente, effettua le seguenti operazioni:

1. Fai clic sul collegamento [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) per scaricare il pacchetto.

1. Apri [Gestione pacchetti](http://localhost:4502/crx/packmgr/index.jsp) e fai clic su **[!UICONTROL Carica pacchetto]** per caricarlo.

1. Seleziona il nome del pacchetto e fai clic su **[!UICONTROL Installa]**.

### Installazione automatica {#automatic-installation}

Il CFP può essere installato automaticamente in un’istanza in esecuzione nei seguenti modi:

* Inserisci il pacchetto in `../crx-quickstart/install` mentre il server è in esecuzione. Il pacchetto viene installato automaticamente.
* Utilizza l’[API HTTP da Gestione pacchetti](https://helpx.adobe.com/it/experience-manager/6-3/sites/administering/using/package-manager.html). In questo caso assicurati di utilizzare `cmd=install&recursive=true` in modo che il pacchetto nidificato venga installato.

### Convalidare l’installazione {#validate-installation}

1. La pagina di informazioni prodotto (`/system/console/  productinfo`) dovrebbe ora mostrare la stringa della versione aggiornata “Adobe Experience Manager, versione 6.3.3.8” sotto Prodotti installati.
1. Tutti i bundle OSGi risultano come ATTIVI o FRAMMENTI nella console OSGi (usa la console Web: `/system/console/bundles`).

>[!NOTE]
>
>Dopo l’installazione corretta del pacchetto, nei registri di errore viene visualizzato un messaggio informativo per indicare che il pacchetto di contenuti è stato installato correttamente, ad esempio “Pacchetto di contenuti **AEM-6.3.3-Cumulative-Fix-Pack-7** installato correttamente”.

>[!NOTE]
>
>A partire da AEM 6.3.3.1, il livello registro in Jackrabbit FileVault è cambiato da INFO a DEBUG per la maggior parte dei messaggi. Per ottenere i registri di installazione per un pacchetto di contenuti installato in AEM 6.3.3.1 o versione successiva, abilita il livello di registro DEBUG per org.apache.jackrabbit.vault.package.impl.

### Installare AEM Forms {#install-aem-forms}

>[!NOTE]
>
>Ignora questa sezione se non usi AEM Forms.

#### Installare il componente aggiuntivo per AEM Forms {#install-forms}

1. Assicurati di aver installato il pacchetto CFP di AEM 6.3.3.x.
1. Scarica il pacchetto corrispondente dei componenti aggiuntivi per Forms elencato in [Versioni di AEM Forms](aem-forms-releases.md) per il sistema operativo in uso.
1. Installa il pacchetto dei componenti aggiuntivi per Forms come descritto in [Installazione dei pacchetti aggiuntivi per AEM Forms](https://helpx.adobe.com/it/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html).

#### Installare il pacchetto dei bundle di JEE per AEM Forms {#install-aem-forms-jee-bundles-package}

Le correzioni apportate a JEE per AEM Forms vengono distribuite tramite un programma di installazione separato. Per informazioni sull’installazione di un CFP in JEE per AEM Forms, consulta [Installing Cumulative Fix Packs on AEM Forms JEE](install-cfp-aem-forms-jee.md) (Installazione di Cumulative Fix Pack in JEE per AEM Forms).

#### Programma di installazione di Forms Designer {#designer-installer}

1. Per installare l’aggiornamento, esegui il file Designer 6.2.0_&lt;Lingua>_Cumulative_QF.msp.
1. Nella schermata di benvenuto, fai clic su **Aggiorna**. L’installazione viene avviata.
1. Al termine dell’installazione, fai clic su **Fine**.

## Impostazioni di configurazione di JEE per AEM Forms (JBoss EAP) {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>Se stai installando la versione 6.3.3.0 o una versione successiva, esegui la procedura seguente per configurare le impostazioni per il server applicazioni JBoss. Se stai installando la versione 6.3.3.0 nel server AEM Forms in esecuzione in server applicazioni Oracle WebLogic o IBM WebSphere, non è richiesta alcuna configurazione aggiuntiva. Per ulteriori dettagli, consulta [Note sulla versione di AEM 6.3.3.0](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

## Aggiornamenti della configurazione per l’integrazione di Search&amp;Promote {#configuration-updates-for-search-promote-integration}

Con AEM Cumulative Fix Pack 6.3.0.2 e versioni successive, la configurazione OSGi utilizzata per l’integrazione di Search&amp;Promote è **Apache HTTP Components Proxy Configuration** (Configurazione proxy per componenti HTTP Apache). La configurazione proxy di Day Commons HTTP Client 3.1 non viene più utilizzata.

## Problemi noti {#known-issues}

* Durante l’installazione di AEM CFP 6.3.3.x.x potrebbero essere visualizzati i seguenti errori e avvisi che è possibile ignorare senza problemi:

   * *WARN* [OsgiInstallerImpl]org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallhook-0.0.2-jar-with-dependencies.jar threw runtime exception.
   * *ERROR* [OsgiInstallerImpl]com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] Timeout waiting for reg change to complete unregistered. CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver service missing, cannot service requests , sending status 503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource: cannot check resource[/bin/receive] page manager unavailable
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver: Calling the error handler resulted in an error
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver Original error null
   * org.apache.sling.engine.impl.DefaultErrorHandler Error handler failed:java.io.IOException
   * *ERROR* [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Component: com.day.cq.dam.handler.standard.ps.PostScriptHandler))

**Brand Portal**

* A partire dalla versione 6.3.1.2, il pulsante Pubblica su Brand Portal è stato rimosso per le raccolte avanzate.

**Interfaccia utente**

>[!NOTE]
>
>Nel caso in cui si verifichi uno di questi due problemi, contatta l’[Assistenza clienti AEM](https://helpx.adobe.com/marketing-cloud/contact-support.html).

* È stato notato un utilizzo intensivo della CPU dovuto a un numero elevato di richieste nella funzionalità di ricerca amministrazione. NPR-24229
* PathField non è selezionato in pathBrowser quando si riapre il componente. NPR-24177

## Impostazioni di configurazione richieste per NPR-27692 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>Questa impostazione di configurazione si applica al CFP 6.3.3.2 e versioni successive. Consente di aggiornare le proprietà di delega di avvio nel file di proprietà `sling`

Per aggiornare manualmente le modifiche in adobe- livecycle - cq -author.ear/ cq.war, procedi come segue:

* Arresta il server AEM.
* Passa ad adobe-livecycle-cq-author.ear/cq.war
* Apri adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml per la modifica:

   * aggiorna il valore di param-name in **sling.bootdelegation.ibm** con:

      * com.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * Dopo la modifica precedente, init-param dovrebbe essere simile a:

      * &lt;init-param>\
         &lt;param-name>sling.bootdelegation.ibm&lt;/param-name> &lt;param-value>com.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* Disinstalla il file EAR (Enterprise Archive) precedente dal server applicazioni WebSphere e installa il file EAR aggiornato seguendo la procedura descritta alla Sezione 10.2 del documento [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
* Salva il file e riavvia il server. [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## Impostazioni di configurazione richieste per NPR-23208 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>Questa impostazione di configurazione si applica alla versione 6.3.2.2 e alle versioni successive. Indica di aggiornare manualmente i criteri degli elenchi di controllo accesso (ACL) tramite CRX-DE in quanto gli ACL non vengono aggiornati tramite l’installazione di CFP per la presenza di &quot;merge_preserve&quot; acHandling.

**Documentazione per l’aggiunta manuale di criteri ACL**

Per aggiornare i criteri ACL, aggiungi i seguenti controlli di accesso tramite CRX-DE:

`1)` Nel percorso &quot;/content&quot;\
`a)` Entità principale: servizio-regolazione-riferimento\
Tipo: Consenti\
Privilegi: jcr:read , jcr:modifyProperties\
Restrizioni : rep:glob=&quot;/*/jcr:content&quot;\
`b)` Entità principale: servizio-regolazione-riferimento\
Tipo: Consenti\
Privilegi: jcr:read , jcr:modifyProperties\
Restrizioni : rep:glob=&quot;/*/jcr:content/*&quot;

`2)` Nel percorso &quot;/content/usergenerated&quot;\
`a)` Entità principale: servizio-regolazione-riferimento\
Tipo: Consenti\
Privilegi: jcr:write

`3)` Nel percorso &quot;/etc&quot;\
`a)` Entità principale: servizio-regolazione-riferimento\
Tipo: Consenti\
Privilegi: jcr:read , jcr:modifyProperties\
Restrizioni : rep:glob=&quot;/*/jcr:content&quot;\
`b)` Entità principale: servizio-regolazione-riferimento\
Tipo: Consenti\
Privilegi: jcr:read , jcr:modifyProperties\
Restrizioni : rep:glob=&quot;/*/jcr:content/*&quot;

## Impostazioni di configurazione richieste per NPR-19450 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>Questa impostazione di configurazione si applica al CFP 6.3.1.1 e versioni successive.

**Configura la proprietà CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL.**

La proprietà controlla la profondità massima della sottostruttura del nodo discendente dalla pagina ` /  jcr   :content`. Fino a quel punto i nodi presenti nella directory archivio verranno utilizzati per ottenere le proprietà della pagina. Qualsiasi nodo presente sotto la profondità specificata in questa proprietà viene ignorato.

Il valore predefinito è 1. Il valore può essere  sovrascritto sovrapponendo la proprietà file constants.js (`/libs/cq/ui/widgets/source/constants.js`), rimuovendo il commento dalla proprietà CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL e assegnando il valore richiesto (la profondità massima sotto la proprietà / jcr :content della pagina fino alla quale vengono memorizzati i dati delle proprietà della pagina).

**Se l’utente deve creare più varianti di pagine in modo che il numero di nodi sotto il nodo  / jcr :content della pagina diventi maggiore di 1000, procedi come segue per apportare modifiche alla configurazione:**

* Configurare la proprietà Max results JSON di Apache Sling
* Ottieni il servlet utilizzando `/system/console/  configMgr`
* Imposta il relativo valore su un numero maggiore di 1000 (valore predefinito corrente) in modo che questo numero sia maggiore del numero totale di nodi nella sottostruttura / jcr  :content fino alla profondità configurata sopra.

In questo modo il servlet GET di Sling può restituire tutti i nodi richiesti.

## JAR Uber {#uber-jar}

Il file JAR Uber per 6.3.3.8 è disponibile nell’[archivio pubblico Maven di Adobe](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/).

Per utilizzare il file JAR Uber in un progetto Maven, consulta l’articolo [Come utilizzare il file JAR Uber](https://helpx.adobe.com/it/experience-manager/6-3/sites/developing/using/ht-projects-maven.html) e includi nel POM del progetto la seguente dipendenza:

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## Funzioni rimosse/obsolete {#deprecated}

In questa sezione sono elencate le funzionalità rimosse o dichiarate obsolete in AEM 6.3.

| Area | Funzione obsoleta | Sostituzione | Versione |
|----|-----|-----|-----|
| Integrazione di Assets con Adobe Creative Cloud | La [condivisione cartelle da AEM a Creative Cloud](https://helpx.adobe.com/it/experience-manager/6-3/sites/administering/using/creative-cloud.html) è stata introdotta in AEM 6.2 per consentire agli utenti creativi di accedere alle risorse da AEM. Una nuova funzionalità introdotta nell’applicazione Creative Cloud, Adobe Asset Link, offre un’esperienza utente migliore e un accesso più efficace alle risorse da AEM direttamente da Photoshop, InDesign e Illustrator.<br /> Adobe non apporterà ulteriori miglioramenti alla funzionalità di condivisione cartelle. Sebbene la funzione sia inclusa in AEM, consigliamo ai clienti di utilizzare la funzionalità sostitutiva. | Adobe Asset Link o app desktop. Per ulteriori informazioni, consulta l’articolo sull’[integrazione di AEM con Creative Cloud](https://helpx.adobe.com/it/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html). | AEM 6.3.3.x |

## Bundle OSGi e pacchetti di contenuti inclusi {#osgi-bundles-and-content-packages-included-1}

Nei documenti di testo seguenti sono elencati i bundle OSGi e i pacchetti di contenuti inclusi nel CFP.

* [Elenco dei bundle OSGi inclusi in AEM 6.3.3.8](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [Elenco dei pacchetti di contenuti inclusi in AEM 6.3.3.8](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [Versioni e aggiornamenti per AEM](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates.html?lang=it)
>* [Pagina degli hotfix di AEM 6.3](https://helpx.adobe.com/it/experience-manager/kb/aem63-available-hotfixes.html)
>* [Note sulla versione di AEM 6.3](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [Pagina del prodotto AEM](http://www.adobe.com/it/solutions/web-experience-management.html)
>* [Documentazione di AEM 6.3](https://docs.adobe.com/content/docs/it/aem/6-3.html)
>* Abbonati ad [Adobe priority product update](https://www.adobe.com/subscription/priority-product-update.html)

