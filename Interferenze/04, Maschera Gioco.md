---
cssclasses:
  - mente-gioco
  - gioco
categoria: gioco
sbilanciamento: maschera
stato: esordiente_v2
titolo: Maschera, Gioco
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
#maschera #depersonalizzazione #contesto #vincoli

- **L'adesione a un divertimento fittizio e non gratificante che nega la propria spontaneità:**
	L'individuo, aderendo a un ruolo o a un'immagine che manifesta felicità all'esterno, si convince che l'attività svolta sia stata divertente, anche se manca una distensione e una liberazione dalle routine. Questa forzatura che tende nel tempo a diventare un'abitudine nega la possibilità di riconoscere ciò che gratifica realmente, poiché la gratificazione viene inconsciamente cercata nei riscontri esterni. Si investe tempo ed energie in una direzione non corretta. Il mantenere questa immagine finta e vuota dentro ritarda il recupero della capacità di godersi il momento e di interagire con gli altri in modo gratificante.

- **L'emergere dell'esigenza di un contatto sincero con le proprie preferenze fallisce nel risolvere l'impasse:**
	L'esigenza di una visione sincera delle proprie preferenze si manifesta quando le attività, svolte per abitudine o per compiacere gli altri, non generano soddisfazione genuina. Quando l'attività è percepita come scomoda o spiacevole, la mente cerca scorciatoie esterne o distrazioni per ottenere facilmente piacere. Queste forme di intrattenimento sono un palliativo che maschera il problema senza risolverlo. Esse agiscono come una fuga dalla consapevolezza e fanno cedere il ruolo attivo di coautori della nostra felicità, impedendo di re-imparare a goderci il momento o di affrontare attivamente la situazione opprimente.

### ⚓ Influenza dal Contesto
#maschera #depersonalizzazione #contesto #stereotipo

Nella quotidianità capita spesso di indossare un'immagine di facciata per dimostrare un apparente gradimento durante le attività svolte in compagnia. Si fa finta di essere appagati e coinvolti, spinti dal desiderio che le persone vicine si trovino di buon umore e traggano piacere dalla situazione. Tuttavia, questa gioia riflessa non nasce da un'esigenza autentica, ma dal bisogno di conformarsi a ciò che gli altri apprezzano. Al termine dell'esperienza non rimane il desiderio di ripeterla, bensì un senso di stanchezza sottile che spinge a convincersi forzatamente che l'evento sia stato comunque piacevole. Questa dinamica rivela quanto la maschera sociale possa insidiosamente sostituirsi alla verità dei nostri vissuti.

Il punto di rottura affiora quando ci si rende conto che il tempo dedicato allo svago non produce alcuna reale distensione. Riemerge allora il ricordo di una dimensione spontanea in cui il provare e persino lo sbagliare risultavano gratificanti, senza il peso di dover raggiungere un risultato o rendere conto a un pubblico. In assenza di questa freschezza interiore, si tenta di gestire la sofferenza aumentando la frequenza degli impegni o cercando distrazioni artificiali. Come chi tenta di studiare in modo passivo senza interagire con la materia attraverso colori o schemi creativi, ci si limita a ripetere routine vuote. La mancanza di coinvolgimento diretto trasforma ogni azione in un dovere, lasciando che le aspettative altrui guidino le scelte e soffochino ogni slancio genuino.

Senza il recupero della propria sensibilità, il disagio primario è destinato ad aggravarsi progressivamente. Le ore trascorse a recitare una finta felicità generano un'accumulazione di rimuginazioni velate, dove ci si scopre a valutare cosa si sarebbe potuto fare diversamente o quanto sarebbe stato meglio accorciare la durata dell'impegno. L'insoddisfazione non riconosciuta agisce come un'interferenza silenziosa che rimanda continuamente la possibilità di apprendere da se stessi. Il peso di questo meccanismo diviene nel tempo insostenibile, trasformando il tempo libero in un'ulteriore fonte di pressione psicologica. Diventa quindi indispensabile fare un passo indietro e trovare uno spazio autonomo in cui riallinearsi con le proprie preferenze reali.

### ♻️ Utilità se Consapevole
#ruolo #obiettività #presenza_mentale #indipendenza

Una strada per l'evoluzione è acquisire onestà intellettuale e iniziare a lavorare su sé stessi per recuperare il contatto con la parte spontanea. È possibile dedicarsi a sperimentare senza l'obbligo di un obiettivo, concentrandosi sul godersi il momento e l'attività. L'azione pratica consiste nel prestare attenzione al motivo per cui si ricorre alla distrazione, per identificare il problema opprimente che si sta evitando. Diventando interlocutori attivi, si può trasformare un'attività anonima in una più gratificante, fornendo attivamente stimoli positivi prodotti da noi. Questo coinvolgimento attivo nella propria realtà, libero da influenze e riscontri esterni, porta a generare gratificazione spontaneamente, riducendo la necessità di ricorrere a surrogati e facilitando un equilibrio interiore stabile e imperturbabile.