---
cssclasses:
  - scopo-base
  - base
sbilanciamento: proiezione
categoria: base
stato: originale_v2
titolo: Proiezione, Base
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
#proiezione #invadenza #percezione #vincoli

- **L'Imposizione di Garanzie e Necessità Soggettive**
	La proiezione si manifesta quando l'individuo insiste per ottenere garanzie o imporre qualcosa che è percepito come assolutamente necessario per sé, anche se gli altri non ne condividono l'importanza o la necessità. Di fronte all'indifferenza altrui, si percepisce un profondo senso di esclusione, come se gli altri siano indifferenti alle nostre esigenze, senza accorgersi che gli si sta chiedendo di aderire ad una visione della realtà che non appartiene  a loro. È un tentativo di forzare le proprie necessità o desiderio di sicurezza sul mondo circostante.

- **La Prevaricazione della Libertà di Scelta Altrui Attraverso il Proprio Filtro Percettivo**
	Un aspetto negativo distintivo di questa proiezione è la tendenza ad applicare il proprio filtro percettivo e la propria visione del mondo agli altri, senza che questi siano coinvolti attivamente nel processo. Questo significa privare l'altra persona della propria libertà di scegliere come desidera gestire e migliorare la propria realtà. Non si concede spazio all'interazione o alla partecipazione attiva, imponendo una direzione che si ritiene giusta, ma che, in realtà, annulla l'autonomia e la capacità di decisione altrui nel proprio contesto.

### ⚖️ Influenza sulla Percezione
#proiezione #invadenza #percezione #doppio_standard

Una profonda e talvolta inconscia mancanza di fiducia nelle proprie fondamenta è all'origine di questa proiezione. La sensazione di incertezza, che si annida nella percezione di un ambiente non sempre equo o affidabile, crea un bisogno impellente di sicurezza. Spesso, questa fragilità interiore deriva da esperienze passate, dove l'impegno profuso non ha trovato il dovuto riconoscimento o dove le regole sembravano sbilanciate. Tale disagio sottile impedisce di sentirsi serenamente nella propria "base sicura".

Da questa insicurezza latente deriva una insistenza per garanzie e sicurezza. L'individuo, mosso da una percezione interna di necessità a volte irragionevoli, tende a imporre agli altri ciò che ritiene indispensabile. Anche se gli altri non ne condividono la medesima importanza, si cerca di forzare questa visione sul mondo esterno. Questo crea incomprensioni da parte degli altri, che si sentono obbligati ad aderire a una realtà che non appartiene loro.

Questa necessità percepita porta ad applicare il proprio filtro percettivo e la propria visione del mondo agli altri. Si tenta di modellare l'ambiente circostante secondo i propri bisogni di sicurezza, senza dare agli altri modo di partecipare attivamente a comprendere e scegliere come gestire e migliorare la loro realtà in quella direzione. Ci si dimentica di garantire spazio all'interazione o alla partecipazione, si cerca di realizzare una visione ritenendola l'unica giusta o possibile, negando di fatto l'autonomia altrui.

Tale comportamento si traduce nella prevaricazione della libertà di scelta altrui. Si impedisce all'altra persona di gestire e migliorare la propria realtà a modo loro, di scegliere ed eventualmente sbagliare liberamente e di conseguenza imparare dagli errori. Questa proiezione priva gli altri della capacità di esprimere il loro potenziale, costringendoli a conformarsi. Non si riconosce che esista un modo altrettanto valido per raggiungere obiettivi comuni.

Invece di contribuire a un ambiente di uguaglianza, dove la reciprocità è riconosciuta e valorizzata, la proiezione genera attrito, per difendersi da una minaccia fantasma. Le energie, che dovrebbero essere investite per normalizzare situazioni problematiche o per espandere la propria base sicura, vengono dissipate in una costante vigilanza. 

### ♻️ Utilità se Consapevole
#osservatore #propositivo #tolleranza #indipendenza

La proiezione relativa alla base, se gestita consapevolmente, può essere un motore per raggiungere l'equilibrio interiore. Invece di proiettare all'esterno un'insistenza per garanzie e sicurezza, l'individuo può riconoscere questo bisogno come un segnale di una mancanza di fiducia nella propria "base sicura" interiore. L'aspetto cruciale è reindirizzare questa energia.

Si tratta di lavorare attivamente per costruire una propria serenità interna, un rifugio sicuro che non dipenda dalle imposizioni sugli altri. Questo processo implica l'identificazione dei propri veri bisogni di sicurezza e l'investimento di energie per consolidare la propria base sicura. In questo modo, la tendenza a cercare sicurezze esterne si trasforma in un processo di auto-consolidamento. Questo espande la propria capacità di sentirsi tranquilli e in equilibrio, indipendentemente dall'ambiente esterno, e porta a non prevaricare la libertà altrui.