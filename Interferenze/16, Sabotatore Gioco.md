---
cssclasses:
  - mente-gioco
  - gioco
sbilanciamento: sabotatore
categoria: gioco
stato: originale_v2
titolo: Sabotatore, Gioco
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
#sabotatore #senso_di_colpa #depotenziante #vincoli

- **Mortificazione del Piacere Autentico**
	Ripetute esperienze negative dai toni aggressivi o violenti e il senso di mortificazione a seguito di rimproveri o richiami, punizioni disciplinari pubbliche, sperimentate a seguito di espressioni di gioia spontanea o entusiasmo per una attività. Stratificano un condizionamento di questi eventi traumatici, che inibisce la ricerca o l'espressione del proprio piacere, facendo sentire sbagliato o inappropriato ciò che dovrebbe essere liberatorio.

- **Blocco Qualitativo della Felicità e della Spontaneità**
	Ci si sente distanti delle proprie emozioni più sincere e genuine, la perdita di qualcosa di fondamentale della propria vita, come il piacere, la felicità e la libertà di esprimersi. La sensazione di essere eternamente giudicati che frena la persona dal vivere le attività con creatività, partecipazione attiva e coinvolgimento. Quello che rimane è un entusiasmo artificiale o una sterilità emotiva, l'incapacità di godere appieno il momento.

### 👁️ Influenza sull'Immagine di Se
#sabotatore #senso_di_colpa #depotenziante #autocritica

Se nell'infanzia o durante la crescita, in un momento liberatorio di genuina spontaneità o spensieratezza, si è stati vittima di richiami aggressivi, punizioni immotivate o critiche severe. Aver vissuto forti emozioni negative, ha associato un profondo senso di mortificazione all'attività. Queste memorie, cariche di un'intensa firma emotiva, non svaniscono ma si cristallizzano, trasformandosi in un ripetitore interno di moniti e divieti costanti il cui scopo è evitare di stare male.

Questo porta a una ruminazione di sensi di colpa, un pensiero ciclico in cui la serenità e la spensieratezza vengono percepite come sensazioni "sbagliate" o non giustificate. La persona si trova così a inibire attivamente la ricerca e l'espressione del piacere, sentendosi in colpa per attività che dovrebbero essere liberatorie.

L'effetto più subdolo di questa dinamica interiore è la penalizzazione del piacere autentico e una compromissione della qualità emotiva. Invece di provare gioia, leggerezza o un genuino senso di appagamento durante una attività, l'individuo percepisce un possibile giudizio esterno pronto a dare uno schiaffo emotivo, sviluppando senso di colpa per ciò che avrebbe dovuto essere fonte di gioia.

 La riduzione qualitativa del contatto con le proprie emozioni più spontanee e genuine.  Viene innalzato un autolimite interno che ostacola la capacità di sperimentare o ritiene sbagliato l'appagamento, la spontaneità e l'apertura a farsi trasportare. 

Questa austerità emotiva finisce per soffocare l'entusiasmo spontaneo e la capacità di godersi il momento, frenando la persona dal vivere le attività con creatività, partecipazione attiva e coinvolgimento. La paura di essere colpevolizzati perché ci si sta il divertendo continua a minare la possibilità di vivere e sperimentare esperienze pienamente appaganti.

### ♻️ Utilità se Consapevole
#alleato_interiore #mediazione #spontaneità #propositivo

Il sabotatore che genera il senso di colpa, può essere affrontato consapevolmente per ripristinare l'equilibrio interiore. È possibile dialogare attivamente con questa voce limitante che ci trattiene dal goderci le attività quotidiane, per tornare a farci coinvolgere da esse o a lasciarci andare allentando un po il controllo.

Anziché subire passivamente il senso di colpa, si può domandare a questa voce quali situazioni, quali luoghi o persone permetterebbero di esprimere liberamente e senza filtri i propri interessi con spontaneità. E se non è in grado di immaginare e proporre una alternativa stabile in cui questo sia possibile, deve essere in grado di ammettere che è disposto ad imparare, altrimenti perde il diritto di essere un collaboratore e diventa un ostacolo che possiamo ignorare.

L'obiettivo è recuperare la libertà di espressione nel gioco o in altre attività, definendo nuove regole e convenzioni personali che rendano l'esperienza adeguata al contesto e legittima. Questo approccio trasforma la limitazione in un'opportunità di riscoperta di sé, portando a un maggiore benessere emotivo e senso di libertà.