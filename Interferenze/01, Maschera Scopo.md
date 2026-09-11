---
cssclasses:
  - scopo-base
  - scopo
categoria: scopo
sbilanciamento: maschera
stato: esordiente_v2
titolo: Maschera, Scopo
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
#maschera #frustrazione #contesto #vincoli

- **Forzarsi a Mantenere un'Immagine Esteriore Rigida Porta ad un Logoramento Interiore:**
	L'abitudine ad aderire a un ruolo o a un'immagine di sé che si è accettata come modello vincola le scelte, facendole sembrare automatiche o inconsapevoli. Quando l'individuo si sente in dovere di fare qualcosa, questa pressione lo spinge a forzarsi, sacrificando risorse o rinunciando a qualcosa a cui terrebbe, in favore di un obiettivo desiderato. L'attività stessa, se richiede uno sforzo eccessivo anziché una fatica sostenibile, diventa sgradita, poiché si è forzati a realizzarla contro la propria volontà.

- **La necessità di una visione chiara e non parziale che fallisce nel risolvere l'impasse:**
	Quando emerge il bisogno di una visione chiara e non parziale, ci si rende conto, con il senno di poi, che le scelte fatte istintivamente non sono state le migliori. Se l'immagine che si crede di avere di sé condiziona le azioni, diventa estremamente difficile affrontare la situazione considerando i propri limiti e le proprie vulnerabilità. L'incapacità di depositare il ruolo difensivo e di accogliere le osservazioni altrui per trovare un punto di incontro porta alla creazione di due fazioni. In assenza di un'apertura al dialogo e alla capacità di conciliare differenze, non viene naturale raggiungere l'armonia.

### ⚓ Influenza dal Contesto
#maschera #frustrazione #contesto #stereotipo

La manifestazione del disagio è spesso percepita quando ci si accorge, ripensando alle proprie reazioni, che non ci è piaciuto il modo in cui ci siamo comportati istintivamente, o che un'alternativa sarebbe stata preferibile. Questa percezione deriva dal fatto che le azioni sono state vincolate da un "pilota automatico". L'individuo agisce non per una scelta libera, ma perché l'immagine che ha di sé condiziona attitudini e comportamenti, portandolo a vestire un ruolo.

Questa adesione a un ruolo non scelto spontaneamente culmina nel sentirsi in dovere di svolgere attività e nel sacrificarvi risorse, concentrando l'energia su un obiettivo esterno senza gestirle correttamente. Se questa sensazione di sacrificio deriva da uno scambio non consapevole, e la ricompensa o l'esito sperato non arriva, ne consegue un profondo senso di insoddisfazione e frustrazione. In quel momento, l'attività, che richiede uno sforzo, non è più sopportabile.

Il momento critico che spinge verso la necessità di una visione chiara e non parziale si manifesta quando si deve affrontare la realtà in modo efficace, non seguendo semplicemente un modello precostituito. Si riconosce l'assenza della capacità di trovare un punto di incontro quando l'atteggiamento rigido impedisce di considerare il punto di vista degli altri, incluse le proprie vulnerabilità. La difficoltà maggiore emerge quando ci si sente minacciati, rendendo difficile distaccarsi per gestire la cosa razionalmente e non ricorrere a reazioni automatiche difensive.

Se si mantiene un ruolo difensivo per proteggere qualcosa di caro, si impedisce l'accoglimento di osservazioni esterne, creando fazioni e bloccando la conciliazione. La spesa energetica per sostenere un ruolo o un'immagine porta ad abusare della forza di volontà, anziché investire le energie per ottenere un miglioramento permanente delle condizioni di vita. Il non riconoscere il valore onesto dell'impegno crea una situazione di sforzo continuo, dove si perde la libertà di scegliere e l'attività smette di dare piacere, portando al limite della sopportazione. È necessario ridimensionare il dovere di rispecchiare un'immagine per raggiungere una forma più reale e oggettiva.

### ♻️ Utilità se Consapevole
#ruolo #obiettività #reciprocità #mediazione

Una strada per superare il senso di rinuncia e l'insoddisfazione è iniziare a smontare i modelli di ruolo e le credenze auto-imposte, cercando una forma più oggettiva e reale di sé. È possibile accogliere le osservazioni esterne in modo prudente, depositando il ruolo difensivo, per trovare un punto di incontro e integrare nel proprio modello i frammenti di verità che potrebbero essere utili. L'impegno e la fatica sono riconosciuti come importanti quando si impara a gestire correttamente le proprie risorse e a rivalutare rapidamente le scelte se l'attività diventa troppo gravosa. Riconoscere l'utilità del dialogo e la capacità di conciliare differenze permette di intervenire in modo equilibrato e assertivo, richiedendo chiarezza e reciprocità in situazioni poco trasparenti. Questo porta a un consolidamento reale delle proprie risorse, dove il lavoro e l'investimento energetico sono in linea con un rapporto di scambio equo e riconosciuto.