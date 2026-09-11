---
cssclasses:
  - abilità-spirito
  - spirito
categoria: spirito
sbilanciamento: proiezione
stato: esordiente_v2
titolo: Proiezione, Spirito
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
#proiezione #parzialità #percezione #vincoli

- **L'attrito generato dalla percezione di un modello interiore più reale della realtà esterna:**
	L'attrito emerge quando il nostro modello della realtà si scontra con ciò che esprimono gli altri, percependo come una minaccia la loro visione differente. Tale tendenza ad un doppio standard evidenzia una mancanza di equilibrio. Ci si trova ad applicare una metrica di valutazione differente tra ciò che si ritiene accettabile e ciò che appare fuori luogo.  L'attrito è un segnale di incoerenza tra il proprio pensiero e quello che si ascolta.

- **L'emergenza di un approccio orientato all'equilibrio che soccombe alle pretese di dogmatismo:**
	Il desiderio di cercare un punto di equilibrio per normalizzare la situazione si scontra con l'incapacità di non essere vincolati da ciò che succede esternamente. Quando il modello interiore è troppo rigido, si insiste nel ribattere con le proprie motivazioni, negando considerazioni altrui. Si tende a creare due fazioni, impedendo una vera conciliazione. Se si cerca un lavoro equilibrato ma si è troppo convinti di dover difendere ciò in cui si crede, si impedisce l'evoluzione del modello, rendendolo obsoleto e inadatto al confronto. 
### ⚖️ Influenza sulla Percezione
#proiezione #parzialità #percezione #doppio_standard

La proiezione dello spirito interviene nel momento in cui l'individuo percepisce come minacciato il suo modello interiore del mondo. Questo si manifesta come una sensazione di attrito o incoerenza nel momento in cui la nostra idea della realtà sembra dissonante rispetto a quella percepita da altri. Ciò che per noi è fondamentale nel nostro modello interiore può risultare marginale o immotivato per gli altri, creando una polarizzazione. Non volendo ammettere che la nostra comprensione non è completamente "a prova di bomba", si ricorre al doppio standard, una visione dualistica che applica metriche diverse tra ciò che riteniamo accettabile e ciò che scartiamo.

Il momento critico che spinge verso la necessità di un approccio costruttivo e di un lavoro equilibrato si manifesta quando ci si accorge che la propria interpretazione non è condivisibile. In questo momento emerge l'assenza della qualità persa di cui si sente la mancanza: l'obiettività, ovvero la capacità di mantenere un punto di vista non vincolato ai limiti della nostra esperienza e di filtrare quello che viene dall'esterno. Senza questa capacità di distacco, il modello interiore non può essere oggettivo, essendo legato unicamente alle nostre esperienze e rielaborazioni private. L'obiettivo non dovrebbe essere quello di difendere la propria idea, ma di cercare un punto di equilibrio, perché un modello troppo rigido non può evolvere e rischia di diventare obsoleto. La tendenza è invece quella di negare l'utilità delle informazioni discordanti e insistere nel ribattere con le proprie motivazioni, trasformando un confronto utile in una semplice presa di posizione difensiva.

Quando il modello interiore non viene esposto all'esterno e al confronto, non si possono chiarire e rafforzare le relazioni tra i concetti. L'attrito che nasce dall'interazione è in realtà un indizio utilissimo che dovrebbe spingere a lavorare sul concetto e migliorare il modello interiore. Se non riusciamo a dialogare in modo equilibrato perché siamo troppo convinti della validità delle nostre regole fondamentali, il nostro castello di carte non regge il confronto. Rinunciamo ad applicare il pensiero critico e accettiamo concetti acriticamente pur di sostenere una visione del mondo incompleta. Questo logoramento continuo nel difendere la propria realtà personale impedisce di fare pulizia dalle regole superflue e ritarda il raggiungimento di una visione più chiara, poiché i concetti rimangono acerbi o in uno stato non definitivo. È la nostra responsabilità riconoscere la necessità di smussare il modello interiore per renderlo più coerente con la realtà.

### ♻️ Utilità se Consapevole
#osservatore #propositivo #pensiero_critico #obiettività

Una strada per l'evoluzione è acquisire una posizione più distaccata, scegliendo di diventare interlocutori attivi del proprio mondo interiore. Si può cominciare a valutare i concetti e le idee emerse tramite la riflessione, esponendole all'esterno tramite un confronto attivo e costruttivo. È possibile utilizzare i punti di vista differenti non per accettarli, ma per far emergere gli elementi di troppo e le parti troppo fantasiose nel nostro modello. L'azione pratica consiste nel lavorare su due punti di vista apparentemente incompatibili cercando il minimo comune denominatore. Questo processo ci abitua a fare la tara e a non essere radicali su un argomento. Lavorando con pazienza per discriminare e far emergere ciò che il modello ci mostra, si rende la propria visione più oggettiva e coerente con il mondo, permettendo di esprimere i concetti importanti in modo molto più semplice e chiaro.