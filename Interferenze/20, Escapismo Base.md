---
cssclasses:
  - scopo-base
  - base
categoria: base
sbilanciamento: escapismo
stato: esordiente_v2
titolo: Escapismo, Base
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
#escapismo #codipendenza #emozioni #vincoli

- **Il timore di affrontare il cambiamento immobilizza l'esistenza:**
	L'incapacità di accettare di mettere in gioco qualcosa di sé o delle proprie risorse, ereditata magari dalle preoccupazioni di figure di riferimento, genera un blocco che impedisce l'azione e il movimento. La stasi percepita non è una base sicura, ma una zona in cui non si può né vincere né perdere. In questa quiete apparente, il timore di una rinuncia diventa più opprimente e spaventoso delle opportunità che potrebbero aprirsi mettendosi in gioco. Si finisce per dipendere dalla ricerca di conforto esterno o da interazioni che forniscono sostegno, senza risolvere la ferita originale o la situazione stressante.

- **L'autogestione necessaria non è riconosciuta e il disagio aumenta:**
	Quando la serenità è solo una tranquillità apparente, mascherata da forme di distrazione che leniscono il problema senza risolverlo, si rinuncia inconsapevolmente al miglioramento. Se non si riesce a sentire che il proprio bisogno è disponibile autonomamente, si cerca un senso di appartenenza nel gruppo, creando dipendenza da relazioni esterne per ottenere conforto. Questo auto-limite fa sì che le paure diventino regole assolute, e l'individuo non riesce a individuare come migliorare i contesti che sarebbero cruciali per l'espansione della propria zona di quiete.

### 💔Esperienze Spiacevoli
#escapismo #codipendenza #emozioni #inconsapeovle

Il rifugiarsi in uno stato di quiete illusorio è strettamente connesso a un'incapacità di riconoscere che la zona di comfort si è ristretta e che si ha paura di uscirne. Ci si sente bloccati, non pronti, o insicuri, e per non rischiare di subire una perdita, non si ottiene mai nulla di nuovo, rinunciando inconsapevolmente al miglioramento. Questa tendenza alla fuga dalla realtà si manifesta come una distrazione o un intrattenimento che nasconde il problema, agendo come un palliativo che non porta a una guarigione reale. Quando questo atteggiamento mentale, che preferisce l'evitamento, è alimentato da un dialogo interno che impone regole assolute (il non mettere mai a rischio qualcosa), esso crea uno stato di stasi perpetua.

La vera necessità che emerge da questa paralisi è la realizzazione della propria autonomia, che non deve dipendere da filtri o convinzioni altrui. Per superare l'immobilità indotta dal timore di perdere, l'individuo dovrebbe recuperare la capacità di conciliare le differenze, l'elemento che prima fungeva da supporto per garantire l'uguaglianza e la reciprocità in un ambiente condiviso. L'assenza di questa autogestione del supporto, ottenibile tramite l'attenzione e la cura di sé, fa sì che il lavoro e l'investimento di energie all'esterno non portino all'espansione della tranquillità. Affrontare il timore richiede tempo e una lenta esposizione, ma la convinzione di non poter perdere nulla, o il considerare il rischio un limite assoluto, impedisce di porzionare le sfide e fare esperienza recuperabile nel tempo.

Quando la paura di agire è così grande, l'individuo si trova di fronte a un muro percepito come minaccioso o pericoloso, oltre il quale si trovano le cose desiderate. Questo muro non viene abbattuto perché nessuno può sostituirsi alla persona nel raggiungere ciò che vuole. Il ricorso a forme di distrazione per lenire il disagio favorisce situazioni croniche e la reiterazione di comportamenti disfunzionali. Il volere che l'aiuto o l'appoggio agli altri sia esclusivamente nel modo deciso dall'individuo o dalla collettività significa privare l'altro della libertà di scelta, un filtro percettivo che non appartiene alla realtà dell'altro. È fondamentale rendersi conto che la sensazione di minaccia, che impedisce il miglioramento, può essere ridimensionata, trasformando la stasi in un punto di lavoro attivo.

### ♻️ Utilità se Consapevole
#consapevolezza #indipendenza #assertività #mediazione

Una via per il miglioramento è l'accettazione della gradualità e l'avvio di un lavoro interno per identificare il problema alla radice. Si può cominciare a mettere in gioco qualcosa di facilmente recuperabile per fare esperienza. Questo è possibile attraverso l'esposizione lenta e controllata a ciò che intimorisce, un processo che rende la situazione gestibile e familiare, ridimensionando il senso di minaccia. Raggiungere la piena autogestione del proprio sostegno interiore permette di esprimere in modo costruttivo la propria volontà, garantendo che non ci siano perdite camuffate da investimento. È possibile esprimere i propri dubbi e rifiutare ciò che non è utile, in modo trasparente e aperto al dialogo. Questo porta a espandere la zona di quiete, ritrovando la libertà di agire serenamente.