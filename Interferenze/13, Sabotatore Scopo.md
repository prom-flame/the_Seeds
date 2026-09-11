---
cssclasses:
  - scopo-base
  - scopo
sbilanciamento: sabotatore
categoria: scopo
stato: originale_v2
titolo: Sabotatore, Scopo
---

```dataviewjs
let meta = dv.current().file.frontmatter;

let cat_tag = meta['categoria'];
let titoloCompleto = meta['titolo'];
let sbilanciamento = meta['sbilanciamento'] || "default";

if (!titoloCompleto) titoloCompleto = dv.current().file.name;

// 🔍 Percorso SVG dal vault
let fileSVG = app.vault.getAbstractFileByPath(`assets/${sbilanciamento}.svg`);
let svgPath = fileSVG ? app.vault.getResourcePath(fileSVG) : null;
console.log("Percorso immagine:", svgPath);

// 🧱 Contenitore principale (immagine + titolo affiancati)
let wrapper = dv.el("div", "", { 
    cls: "title-wrapper", 
    style: "display: flex; align-items: center; gap: 10px;"
});

// 🖼️ Immagine SVG (solo se trovata)
if (svgPath) {
    let img = document.createElement("img");
    img.src = svgPath;
    img.width = 45;
    img.height = 45;
    img.style.objectFit = "contain";
    img.style.display = "inline-block";
    wrapper.appendChild(img);
} else {
    console.warn("⚠️ Immagine non trovata:", `assets/${sbilanciamento}.svg`);
}

// 🧾 Titolo
let [titolo, parolaDaColorare] = titoloCompleto.split(",").map(s => s.trim());
let titleElement = document.createElement("h1");
titleElement.classList.add("custom-title");
titleElement.style.display = "inline-block";
titleElement.style.margin = "0";  // elimina spazio verticale

if (parolaDaColorare && parolaDaColorare.toLowerCase() === cat_tag.toLowerCase()) {
    titleElement.innerHTML = `${titolo}, <span class="${cat_tag}">${parolaDaColorare}</span>`;
} else {
    titleElement.textContent = titoloCompleto;
}

wrapper.appendChild(titleElement);
```
### 🗝️ Vincoli da Dissolvere
#sabotatore #sacrificio #depotenziante #vincoli

- **Sostituzione Inconsapevole del Dovere all'Obiettivo**
	All'origine del sabotatore, ci sono figure di riferimento che hanno nobilitato lo sforzo o il sacrificio, persuadendoci ad abusare della determinazione, come la soluzione a tutto. Se la rinuncia o il sacrificio diventano più importanti dell'effettivo raggiungimento dell'obiettivo, l'azione si trasforma in un obbligo autoimposto che prosciuga la motivazione e distorce le intenzioni iniziali.

- **Regole Assolute Ereditate e "Dover Fare"**
	La rigidità nelle scelte e nei comportamenti, privano della libertà di esplorare approcci alternativi e di adattarsi alle circostanze. Se certe convinzioni o regole si impongono come necessarie, impedendo di rimetterle in discussione anche se non sono funzionali all'obiettivo, diventano un codice di condotta che decide per noi cosa possiamo fare, rendendo la parola "dover fare"  parte del nostro autodialogo.

### 👁️ Influenza sull'Immagine di Se
#sabotatore #sacrificio #depotenziante #autocritica

Il sabotatore, originato dagli insegnamenti di figure autoritarie o di riferimento incontrate nel corso della crescita, che hanno enfatizzano o celebrato la necessità dello sforzo, la sopportazione, la fatica e la dedizione ad una causa, trasformandoli in valori intrinseci. L'assimilazione di tali precetti, in un periodo di apertura alle regole e dinamiche sociali, porta l'individuo a internalizzare queste "forme pensiero" come vere e proprie regole di comportamento personale.

La priorità viene data all'azione stessa piuttosto che al risultato atteso, l'individuo si impegna perché si sente in obbligo o per abitudine, a volte perdendo di vista cosa desidera ottenere dalle energie investite. Questa prospettiva limitata influenza la libertà di scelta e le decisioni non sono più completamente autonome ma condizionate dal senso di responsabilità che si crede di dover rispecchiare, o da abitudini e reazioni automatiche con un pregiudizio sul concedersi delle pause o cercare alternative migliori e semplici.

Ne deriva una tendenza ad essere troppo esigenti con sé stessi, e l'abitudine di abusare della propria forza di volontà, che spinge l'individuo a sforzarsi al di là dei propri limiti e a sacrificare il proprio benessere o la propria serenità per soddisfare le aspettative imposte da sé stessi o da altre persone.

Si crea un circolo vizioso in cui la rigidità comportamentale impedisce di apprezzare l'attività stessa, trasformando la dedizione in uno sforzo eccessivo e insoddisfacente. Questo processo può portare ad una profonda avversione nell'impegnarsi in qualcosa, generando frustrazione e insofferenza per le energie spese e l'assenza di gratificazioni in tutto ciò che la riguarda.

### ♻️ Utilità se Consapevole
#alleato_interiore #mediazione #proattività #indipendenza

Questo sabotatore emerge da convinzioni o scelte, divenute nel tempo abitudini o regole di condotta personale, è quindi fondamentale soppesare queste regole ereditate dal passato e se necessario metterle in discussione, dissolvere le convenzioni e ricostruirle in una forma migliore e più efficiente.

Questo processo consapevole permette di riconoscere che non esiste un modo assoluto di fare qualcosa, e che l'obiettivo da raggiungere è il vero fulcro. Quando l'obiettivo torna ad essere prioritario, si recupera la capacità di scegliere volta per volta, con quale priorità agire, in equilibrio con le proprie intenzioni, senza l'obbligo di sacrificare componenti importanti della propria vita o quotidianità.

Rimuovendo gli obblighi impliciti, si evita che l'attività diventi spiacevole o non più gratificante, recuperando il piacere intrinseco del fare e dell'agire. La chiave è trasformare il "sacrificio" in "fatica gestibile", garantendosi delle pause quando necessarie e rivalutando le scelte iniziali se l'attività non è più gratificante. Questo approccio consente di smantellare le clausole invisibili che condizionano la quotidianità, ripristinando la libertà e la soddisfazione nel perseguire i propri obbiettivi come asse portante della propria motivazione.