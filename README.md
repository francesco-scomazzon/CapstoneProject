<img width="1584" alt="Senza titolo" src="https://github.com/user-attachments/assets/42dedc4c-dfac-4bf9-aa1c-4245475634a6">


<h2 style="text-align: center;"><strong>ANALISI SULLO STATO DELL’ENERGIA NUCLEARE IN EUROPA NEL 2022 — RELAZIONE PER IL CAPSTONE PROJECT</strong></h2>
<p style="text-align: center;"><strong>Presentazione e interrogativi dell’analisi</strong></p>

   
   <p>Ho deciso di affrontare questo studio sull’energia nucleare come Capstone project per una serie di motivi</p>
   <ul>
      <li><strong>🌱 Ambiente: </strong>progetti europei come il <em class="markup--em markup--li-em">Fit for 55</em> e, più in generale, la lotta al cambiamento climatico richiedono una pluralità di strategie per la transizione verso fonti a zero emissioni nette (<em class="markup--em markup--li-em">net zero</em>), tra cui l’energia nucleare.</li>
      <li><strong>🔋 Sicurezza energetica: </strong>il mutato contesto internazionale, in seguito all’invasione russa dell’Ucraina, ha riportato alla ribalta il tema dell’approvvigionamento energetico evidenziando la vulnerabilità delle forniture europee e la necessità di diversificare le fonti energetiche.</li>
      <li><strong>👨‍🔬 Innovazione:</strong> l’industria nucleare e il mondo della ricerca stanno sviluppando soluzioni innovative tra cui la flessibilità di installazione dei reattori modulari di piccole dimensioni (<em>Small Modular Reactor</em>) e i reattori di IV generazione, quest’ultimi progettati per minimizzare la produzione di scorie riducendone la durata</li>
   </ul>

   
   <p>Questa relazione è stata redatta per offrire un panorama dell’energia nucleare in Europa, con un approfondimento sulla situazione francese, utilizzando i dati disponibili fino al 2022. L’analisi si concentra su:</p>
   <ul>
      <li>la distribuzione geografica dei reattori</li>
      <li>la capacità installata per coprire parte del fabbisogno elettrico</li>
      <li>l’evoluzione dell’uso dell’energia nucleare negli ultimi dieci anni</li>
      <li>la provenienza dell’uranio, la capacità di arricchimento e la produzione di uranio e plutonio negli impianti di riprocessamento</li>
   </ul>
   
   <p>Per conseguire questi obiettivi, sono stati utilizzati tre strumenti di data analysis appresi nel corso: Python, Excel e Power BI.</p>
   
   
   <p><strong>Dataset utilizzati</strong></p>
   <ul>
      <li>World Nuclear Power Reactors & Uranium Requirements: <a href="https://world-nuclear.org/information-library/facts-and-figures/world-nuclear-power-reactors-and-uranium-requireme" data-href="https://medium.com/r/?url=https%3A%2F%2Fworld-nuclear.org%2Finformation-library%2Ffacts-and-figures%2Fworld-nuclear-power-reactors-and-uranium-requireme" class="markup--anchor markup--li-anchor" data-tooltip="https://medium.com/r/?url=https%3A%2F%2Fworld-nuclear.org%2Finformation-library%2Ffacts-and-figures%2Fworld-nuclear-power-reactors-and-uranium-requireme" data-tooltip-position="bottom" data-tooltip-type="link" target="_blank">link</a></li>
      <li>World Nuclear Energy Generation: <a href="https://www.kaggle.com/datasets/alistairking/nuclear-energy-datasets" data-href="https://medium.com/r/?url=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Falistairking%2Fnuclear-energy-datasets" class="markup--anchor markup--li-anchor" data-tooltip="https://medium.com/r/?url=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Falistairking%2Fnuclear-energy-datasets" data-tooltip-position="bottom" data-tooltip-type="link" target="_blank">link</a></li>
      <li>Nuclear Energy Statistics: <a href="https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Nuclear_energy_statistics#Uranium_supply_security" data-href="https://medium.com/r/?url=https%3A%2F%2Fec.europa.eu%2Feurostat%2Fstatistics-explained%2Findex.php%3Ftitle%3DNuclear_energy_statistics%23Uranium_supply_security" class="markup--anchor markup--li-anchor" data-tooltip="https://medium.com/r/?url=https%3A%2F%2Fec.europa.eu%2Feurostat%2Fstatistics-explained%2Findex.php%3Ftitle%3DNuclear_energy_statistics%23Uranium_supply_security" data-tooltip-position="bottom" data-tooltip-type="link" target="_blank">link</a></li>
      <li>Electricity prices for (non-)household consumers — bi-annual data: <a href="https://ec.europa.eu/eurostat/cache/metadata/en/nrg_pc_204_sims.htm" data-href="https://medium.com/r/?url=https%3A%2F%2Fec.europa.eu%2Feurostat%2Fcache%2Fmetadata%2Fen%2Fnrg_pc_204_sims.htm" class="markup--anchor markup--li-anchor" data-tooltip="https://medium.com/r/?url=https%3A%2F%2Fec.europa.eu%2Feurostat%2Fcache%2Fmetadata%2Fen%2Fnrg_pc_204_sims.htm" data-tooltip-position="bottom" data-tooltip-type="link" target="_blank">link</a></li>
      <li>Population and Demography Database: <a href="https://ec.europa.eu/eurostat/web/population-demography/demography-population-stock-balance/database" data-href="https://medium.com/r/?url=https%3A%2F%2Fec.europa.eu%2Feurostat%2Fweb%2Fpopulation-demography%2Fdemography-population-stock-balance%2Fdatabase" class="markup--anchor markup--li-anchor" data-tooltip="https://medium.com/r/?url=https%3A%2F%2Fec.europa.eu%2Feurostat%2Fweb%2Fpopulation-demography%2Fdemography-population-stock-balance%2Fdatabase" data-tooltip-position="bottom" data-tooltip-type="link" target="_blank">link</a></li>
      <li>Nuclear power stations of EDF SA: <a href="https://opendata.edf.fr/explore/dataset/centrales-de-production-nucleaire-edf/table/?disjunctive.centrale&disjunctive.tranche&disjunctive.sub_sector&sort=-tri" data-href="https://medium.com/r/?url=https%3A%2F%2Fopendata.edf.fr%2Fexplore%2Fdataset%2Fcentrales-de-production-nucleaire-edf%2Ftable%2F%3Fdisjunctive.centrale%26disjunctive.tranche%26disjunctive.sub_sector%26sort%3D-tri" class="markup--anchor markup--li-anchor" data-tooltip="https://medium.com/r/?url=https%3A%2F%2Fopendata.edf.fr%2Fexplore%2Fdataset%2Fcentrales-de-production-nucleaire-edf%2Ftable%2F%3Fdisjunctive.centrale%26disjunctive.tranche%26disjunctive.sub_sector%26sort%3D-tri" data-tooltip-position="bottom" data-tooltip-type="link" target="_blank">link</a></li>
   </ul>
   
   
   <p><strong>Recupero e pulizia dei dati</strong></p>

   
   <p>Nella prima fase del progetto, ho utilizzato un Jupyter Notebook (.ipynb) per raccogliere i dati da una tabella web. La <em>World Nuclear Association</em>, organizzazione indipendente senza fini di lucro, è stata il punto di partenza per ottenere un dataset comprensivo del numero di reattori presenti e futuri, con relative specifiche sulla loro capacità e sulla richiesta di uranio per la loro operatività. Ho usato <em>Beautiful Soup</em> e <em> Pandas </em> per fare scraping della tabella sul loro sito web e, una volta ottenuto il dataframe, ho filtrato solo i paesi europei tramite una merge con la colonna <em>Country</em>.</p>



<img width="240" alt="EmblemaPython" src="https://github.com/user-attachments/assets/4a3f4aab-d1a4-4c2a-a200-6f8b74fdd5f4">

   <p>Per i dati relativi alla generazione di energia elettrica da fonte nucleare, ho utilizzato il <em>Global Power Plant Database</em> su Kaggle.</p>
   <p>Per le altre informazioni, sono ricorso a Eurostat, limitando lo studio ai soli paesi dell’Unione Europea. In particolare, ho recuperato tre file Excel: il primo contenente i dati sul calore nucleare, sulla capacità di arricchimento, sulla produzione di uranio e plutonio negli impianti di riprocessamento e sui paesi che garantiscono l’approvvigionamento di uranio; il secondo sulla popolazione europea per effettuare calcoli pro capite su un arco di tempo decennale; e un terzo sui prezzi dell’elettricità, divisi per utenza domestica e industriale. Inoltre, ho utilizzato il sito di EDF, la maggiore azienda produttrice e distributrice di energia in Francia, che offre molte informazioni utili in formato open data.</p>

<img width="240" alt="EmblemaExcel" src="https://github.com/user-attachments/assets/e17e58fd-2cb4-4a6e-85d8-5fa444f1130e">

   
   <p>In un nuovo file di Excel, ho utilizzato Power Query per recuperare tutte le tabelle precedentemente scaricate. I dati presentavano già un elevato livello di pulizia, quindi la maggior parte del tempo è stata spesa nella gestione dei valori nulli, nel merge delle tabelle e nell’eliminazione delle colonne non rilevanti ai fini dell’analisi. Alcuni limiti si sono manifestati una volta importate le tabelle su Power BI, rendendo necessaria una revisione della pulizia per ottimizzare il modello e, nel caso dei reattori francesi, per correggere i loro nomi al fine di visualizzarli correttamente nelle mappe.</p>
   
   
   <p><strong>Preparazione e creazione del modello dati</strong></p>

   
   <p>Il modello dati preparato su Power BI segue lo schema a stella (star schema). Ho preparato le varie <em>tabelle delle dimensioni</em> affinché si ricollegassero alla chiave primaria della <em>tabella dei fatti</em> tramite la colonna Country. Per fare ciò è stato fondamentale l’impiego della funzione UnPivot presente su Power Query.</p>
   <p>Il dataset riguardante i reattori francesi non è stato incluso direttamente nello schema a stella, bensì collegato con la tabella calendario, che a sua volta era collegata con la tabella principale.</p>
   <p>Le misure create con DAX sono state raccolte in una tabella non inclusa nel modello.</p>

<img width="240" alt="emblema_PowerBI" src="https://github.com/user-attachments/assets/af69a1a7-86cc-4f3b-9211-bbe74bfad32a">


   
   <p><strong>Progettazione e presentazione delle dashboard</strong></p>

   
   <p>Per velocizzare il caricamento delle pagine in Power BI, ho preparato tutti gli elementi statici su Affinity Designer, un software di grafica, e ho disposto le sei immagini come sfondo per ciascuna dashboard. Nella prima pagina sono disposte le metriche fondamentali del report, utili a comprendere la funzione di ciascuna dashboard. Le icone fungono da bottoni per navigare intuitivamente tra le varie analisi. Questa interfaccia viene ripresa anche nelle pagine successive che trattano in ordine le varie domande esplorative.</p>
   <ul>
      <li><strong>Prima pagina:</strong> contiene due grafici a barre e uno a pila, utile a visualizzare più categorie di reattori per nazione. Un limite del lavoro è stata la mancata progettualità nella costruzione della dashboard durante la collezione dei dati, che ha portato a una certa imprecisione nel valutare la quantità di informazioni da visualizzare in ciascuna sezione.</li>
      <li><strong>Seconda pagina:</strong> si concentra sulla capacità dei reattori, ovvero la capacità di immagazzinare carica elettrica. Include un grafico scatter plot che confronta i prezzi dell’elettricità con la percentuale di generazione di energia elettrica da fonte nucleare. Sono stati inclusi due segnalibri che consentono all’utente di modificare il dato nel grafico in base al destinatario del costo (utenza domestica o industriale).</li>
      <li><strong>Terza pagina:</strong> contiene tre grafici a linea, di cui uno ottenuto mediante una misura creata con DAX. Questo linguaggio si è rivelato particolarmente utile per calcolare valori come il totale della popolazione filtrato per determinati anni, la media della produzione elettrica da fonte nucleare e il rapporto tra la somma annua di due variabili.</li>
      <li><strong>Quarta pagina:</strong> visualizza varie metriche relative ai materiali, dall’export di uranio da paesi extra-europei all’import con dati aggiornati al 2024, fino al confronto dei tre paesi che mantengono strutture di arricchimento dell’uranio.</li>
      <li><strong>Ultima pagina:</strong> prende in considerazione diversi parametri. L’impiego delle mappe aiuta a comprendere la distribuzione geografica dei reattori e la concentrazione di capacità elettrica. Il grafico a barre misura il capacity factor dei reattori, ovvero la percentuale di operatività dalla loro connessione alla rete elettrica, mentre i due grafici a torta visualizzano la distribuzione delle tipologie di reattore in termini di capacità e di combustibile impiegato. È stato infine posto un filtro per esplorare questi parametri in base alla data di connessione alla rete.</li>
   </ul>
   
   
   <p><strong>Risultati dell’analisi</strong></p>
   
   
   <p><em>Distribuzione geografica</em></p>
   <p>L’Europa possiede una vasta flotta di reattori nucleari, concentrati prevalentemente in Francia. Negli ultimi decenni, il numero di nuovi reattori costruiti è stato esiguo, mentre molti di quelli esistenti stanno invecchiando. Tuttavia, il 2022 ha segnato un punto di svolta in tema energetico, con il mutare del contesto geopolitico. Si osservano già segni di un cambio di rotta, con nuovi reattori pianificati e un’intensificazione del dibattito politico sull’energia nucleare, evidenziato dal numero crescente di reattori proposti. I dati mostrano anche un maggiore interesse da parte dei paesi dell’Europa orientale, in particolare della Polonia, nell’adozione o nel potenziamento delle loro capacità nucleari, in contrasto con l’abbandono tedesco.</p>
   <p><em>Capacità e prezzi dell’elettricità</em></p>
   <p>La capacità elettrica dei reattori nucleari riflette in gran parte la distribuzione geografica. Le poche incongruenze possono essere spiegate dalla diversa dimensione dei reattori o dalla mancanza di una proposta politica univoca sulla scelta dei reattori. I dati visualizzati nello scatterplot non permettono di stabilire una chiara correlazione tra la percentuale di generazione di energia elettrica da fonte nucleare e il costo in bolletta, poiché sono necessari ulteriori approfondimenti sugli elementi che influenzano queste dinamiche economiche. Ad esempio, il prezzo al kW per il settore industriale in Francia è sostanzialmente inferiore alla media europea, mentre la Slovacchia, pur avendo percentuali di generazione nucleare superiori al 50%, affronta costi molto più elevati.</p>
   <p><em>Analisi temporale</em></p>
   <p>Nel decennio 2013–2022, si è registrato un calo della produzione di energia elettrica da fonte nucleare in rapporto alla popolazione. Questo può essere attribuito all’incremento demografico e alle riduzioni dei contributi nucleari dovute alle prolungate manutenzioni dei reattori francesi nel 2022 e alle condizioni meteorologiche dei fiumi. Il primo grafico a linee mostra la capacità combinata dei tre paesi europei che operano l’arricchimento dell’uranio attraverso aziende specializzate (Orano e Urenco). Dopo un picco nel 2016, i valori di arricchimento si sono stabilizzati. Il riprocessamento del materiale esausto consiste nella separazione e recupero di uranio e plutonio per la fabbricazione di nuovo combustibile, un’operazione eseguita dopo l’utilizzo del combustibile nel reattore. Il grafico a linee mostra come il Regno Unito abbia negli ultimi anni preferito lo stoccaggio al riprocessamento.</p>
   <p><em>Materiali</em></p>
   <p>La sezione dedicata ai materiali evidenzia la domanda di uranio francese, che è almeno sette volte superiore rispetto agli altri paesi europei. La quantità di uranio esportato dai paesi extra-europei vede il Kazakistan al primo posto, seguito dal Niger e dal Canada. Infine, il grafico a torta mostra il confronto tra Francia, Germania e Paesi Bassi, i tre paesi che operano l’arricchimento dell’uranio in Europa.</p>
   <p><em>Il caso francese</em></p>
   <p>In Francia, i reattori sono maggiormente concentrati nelle regioni del Centro-Valle della Loira e dell’Alvernia-Rodano-Alpi, con una capacità elettrica significativa anche nella regione dell’Alta Francia. Il reattore con il più elevato load factor è il Golfech 2, operante al 93,2% del tempo dal suo ingresso in rete. I due grafici a torta finali forniscono un identikit sulla capacità e il combustibile scelti per i reattori PWR (Pressurized Water Reactor). Oltre la metà dei reattori sono di dimensioni più piccole (PWR 900) e nel 62% dei casi utilizzano uranio arricchito.</p>
