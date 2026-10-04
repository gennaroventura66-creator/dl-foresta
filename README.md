# DL Foresta

App per la **direzione dei lavori di utilizzazione forestale** (Basilicata, Campania, Calabria): verifica in bosco del piedilista di martellata, ceppaie, danni e aree di saggio, con report e relazione di direzione lavori. Collegata a QGIS / QField / QFieldCloud come PAF Campo e Martellata Campo.

- **Web:** https://gennaroventura66-creator.github.io/dl-foresta/
- **Android (APK):** https://github.com/gennaroventura66-creator/dl-foresta/releases/latest/download/DL-Foresta.apk

## Cosa fa
- **Importa il piedilista di Martellata Campo** (GeoPackage, Piedilista.csv o **PDF** del piedilista / fascicolo di martellata e matricinatura) e crea il cantiere con piante martellate, matricine/riserve e aree; distingue **ceduo** e **alto fusto**.
- **Verifica pianta per pianta**: tagliata / in piedi / non trovata; diametro e altezza della ceppaia (confronto con il diametro di martellata, rapporto atteso impostabile), qualità del taglio (regolare, ceppaia alta, slabbrata, danneggiata), foto, posizione GPS; piante tagliate senza contrassegno con motivo.
- **Danni** alle piante rilasciate (scortecciatura / ferita al fusto, rottura di rami o cimale, sradicamento / inclinazione), al suolo e alla rinnovazione (solchi, compattamento, smottamenti, piste non autorizzate, rinnovazione distrutta): grado %, gravità, **evitabile / inevitabile**, causa, superficie, foto.
- **Aree di saggio** conformi alla norma regionale: nel ceduo matricine rilasciate per specie e classe e ceppaie per qualità del taglio (matricine/ha rispetto alle prescritte, % ceppaie irregolari); nell'alto fusto piante rilasciate.
- **Censimento integrale delle matricine** (da PC): importa uno shapefile / GeoJSON di punti (LiDAR, ortofoto, GNSS) oppure **rileva le cime direttamente dal CHM o da DSM + DTM in GeoTIFF** del volo drone / LiDAR (massimi locali sopra una soglia di altezza, dentro le sezioni di taglio), con ortofoto GeoTIFF come sfondo in mappa per controllare e scartare i falsi positivi; conteggio per sezione di taglio e a ettaro, confronto con le prescritte, classi di altezza, esportazione in QGIS (layer *Matricine censite*).
- **Verifiche di conformità** automatiche (piante non trovate, tagli senza contrassegno, ceppaie anomale o alte, danni evitabili oltre soglia, matricine/ha, periodo di taglio).
- **Documenti**: report di verifica e relazione di direzione lavori (Word / PDF con carta, grafici e foto), verbale di sopralluogo, piedilista di verifica, fascicolo fotografico, Excel, CSV.
- Scambio con QGIS tramite `dlforesta.gpkg` + `DLForesta.qgz`; sincronizzazione QFieldCloud a più operatori (unione a tre vie, foto incluse) e divisione del lavoro per aree.

## Firma dell'APK
Per installare gli aggiornamenti sopra la versione precedente serve il secret `ANDROID_KEYSTORE` (Settings → Secrets and variables → Actions), da inserire a cura del proprietario del repository (stessa chiave di PAF Campo e Martellata Campo).
