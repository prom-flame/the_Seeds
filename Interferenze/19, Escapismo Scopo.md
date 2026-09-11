---
cssclasses:
  - scopo-base
  - scopo
sbilanciamento: escapismo
categoria: scopo
stato: originale_v2
titolo: Escapismo, Scopo
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
#escapismo #rassegnazione #emozioni #vincoli

- **Passività nell'Affrontare e Ristrutturare l'Esterno**
	Questo tipo di escapismo è caratterizzato dall'incapacità di affrontare sfide o situazioni che richiedono di mettere in discussione le regole esistenti per ricostruire interazioni funzionali con l'esterno. Porta ad adottare atteggiamenti evasivi e a non essere in grado di trasmettere o esprimere le proprie intenzioni o i propri bisogni agli altri, culminando nell'abbandono di discussioni importanti, rimanendo passivi di fronte agli eventi.

- **Evitare la Responsabilità del Miglioramento Attivo**
	Si manifesta come un'incapacità di rendere migliore la propria realtà o il proprio contesto legato allo scopo, non si è in grado di affrontare forme di autorità o accettare alcune responsabilità necessarie ad un miglioramento. Questo spinge a cercare una zona di comfort, a cambiare ambiente o condizioni pur di non vivere emozioni negative.

### 💔Esperienze Spiacevoli
#escapismo #rassegnazione #emozioni #inconsapeovle

L'escapismo è una condizione in cui si manifesta una incapacità di affrontare sfide o situazioni che richiedono di confrontarsi con le proprie paure o insicurezze, ridiscutere ruoli o affrontare figure autoritarie. Questo implica una difficoltà nel mettere in discussione le dinamiche esistenti per ricostruire un rapporto con l'ambiente esterno equilibrato e privo di preoccupazioni.

Questa attitudine porta a un comportamento remissivo e passivo, con una tendenza ad evitare qualsiasi tipo di conflitto o confronto diretto. Nel tempo si consolida la perdita della capacità di esprimere i propri bisogni e le proprie intenzioni, e non si riesce a comunicarli efficacemente o spontaneamente agli altri (aspettandosi a volte che siano loro ad accorgersene). Ciò conduce, ad una crescente incapacità di soddisfare le proprie aspettative e i propri desideri.

Di fronte a situazioni percepite come spiacevoli, si tende a cercare una zona di comfort o a dipendere da essa. C'è una propensione a essere pronti a cambiare ambiente o condizioni pur di evitare di vivere emozioni negative o di affrontare un contesto sgradito.

Si rinuncia inconsapevolmente alla possibilità di cambiare la propria realtà, a portare equilibrio nel contesto a favore di un sollievo apparente. Senza la capacità di affrontare responsabilità necessarie al cambiamento, si genera un senso di impotenza e frustrazione nel non riuscire mai davvero ad ottenere una serenità duratura o ciò che si desidera.

Si presenta una marcata tendenza ad abbandonare la discussione o a non esporre i propri pensieri o bisogni in modo assertivo. Ne consegue un atteggiamento passivo e il mantenimento di una certa distanza emotiva dai problemi e l'assenza di una revisione delle relazioni interpersonali che potrebbero portare a cambiamenti significativi, utili o necessari.

### ♻️ Utilità se Consapevole
#consapevolezza #indipendenza #impegno #mediazione

A volte la scelta consapevole di introdurre nelle proprie abitudini elementi quali fatica, impegno o rinuncia a vantaggi momentanei può essere sufficiente a rendersi conto che per realizzare un miglioramento permanente della situazione non serve fare sacrifici, ma piuttosto fare un passo nella direzione giusta affrontabile e costante.

Anzi quando si termina un lavoro impegnativo, che ci ha fatto sentire realizzati, che ha avuto uno scopo, di cui possiamo serenamente e sinceramente essere soddisfatti e gratificati, la percezione del tempo dedicato a quella attività diventa significativo ed importante, lo sentiamo come un investimento.

Il significato che diamo alle conseguenze delle nelle nostre scelte e azioni ci fa capire a livello intuitivo che la responsabilità consapevole è l'altra faccia del merito e della soddisfazione personale, e che quando il nostro impegno viene investito in qualcosa di costruttivo e duraturo, i nostri orizzonti ricominciano ad espandersi.