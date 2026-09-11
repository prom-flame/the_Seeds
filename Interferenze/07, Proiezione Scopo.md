---
cssclasses:
  - scopo-base
  - scopo
categoria: scopo
sbilanciamento: proiezione
stato: esordiente_v2
titolo: Proiezione, Scopo
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
#proiezione #impulsività #percezione #vincoli

- **La reazione istintiva che compromette l'obiettivo a causa della dipendenza dal giudizio altrui:**
	L'insorgere di una risposta accesa o un'azione quasi istintiva evidenzia l'incapacità di gestire razionalmente la situazione quando si percepisce una minaccia a ciò che si ritiene caro. Quando l'immagine di sé come competenza è messa in discussione, si possono scatenare reazioni automatiche, portando a forme di espressione distorte o eccessive. Questa reazione difensiva è amplificata dalla perdita della libertà di dire di no a ciò che non è accettabile, rendendo l'individuo schiavo della percezione di un giudizio anche silenzioso. Si trascura che la forza interiore dovrebbe essere utilizzata per difendere ciò che si ha di caro, non per essere vincolati da ciò che succede esternamente.

- **L'emergere di un'intenzione costruttiva che fallisce per la mancanza di distacco emotivo:**
	Il desiderio di un lavoro equilibrato per normalizzare la situazione o di un confronto attivo per migliorare nei fatti si scontra con il bisogno di difendere la propria posizione. La tendenza a forzare le proprie convinzioni sugli altri o a essere irragionevoli perché non si vuole cambiare innesca negli altri la stessa opposizione. È difficile depositare il ruolo difensivo per accogliere le osservazioni in modo prudente, e in assenza di un punto di vista distaccato, l'azione che mira a un miglioramento reale degenera in attrito o conflitto, impedendo una vera evoluzione del proprio approccio.

### ⚖️ Influenza sulla Percezione
#proiezione #impulsività #percezione #doppio_standard

La manifestazione di un atteggiamento impulsivo si avverte spesso come una sensazione di fastidio verso chi si impone o prevarica con le proprie convinzioni. Quando si avverte una minaccia o si reagisce in modo acceso, significa che il concetto interiore non è gestito in modo equilibrato, e le lacune di ciò che si è compreso vengono esposte dalle opinioni esterne, cosa che non piace. A volte, si nota, con il senno di poi, di non aver gradito il modo in cui ci si è comportati quasi istintivamente, come se le proprie scelte fossero vincolate da un "pilota automatico" o da un ruolo non scelto liberamente.

Il momento critico che spinge verso la necessità di un approccio costruttivo emerge con il desiderio di affrontare la situazione in modo efficace, considerando i propri limiti, anziché forzarsi in un modello rigido. In questo contesto, l'assenza della libertà dalle interferenze esterne è lampante, poiché l'individuo si sente minacciato quando qualcuno usa le componenti dell'obiettivo (assertività, convinzione) in modo non equilibrato. Se la consapevolezza dell'impegno viene meno, il riconoscimento esterno (reputazione) prende il sopravvento, e si perde l' autostima auto-sostenuta. Per questo, si rischia di interpretare ogni osservazione come una critica, anche se non intenzionale.

Il lavoro equilibrato e orientato all'obiettivo, in assenza di questo sostegno interiore, fallisce perché si è troppo convinti di dover difendere ciò in cui si crede. Si può arrivare a insistere per avere garanzie dagli altri, applicando un filtro percettivo unilaterale. Senza la capacità di filtrare ciò che viene dall'esterno e di deporre il ruolo difensivo, si creano due fazioni, bloccando la possibilità di conciliazione. L'obiettivo di gestire correttamente le risorse si perde quando l'azione diventa un sacrificio, e l'individuo si sente infastidito se lo scambio atteso non si concretizza. L'abitudine a non affrontare attivamente le sfide o a perdere tempo a sfogare il proprio sconforto ritarda la ristrutturazione interiore necessaria. Pertanto, è fondamentale fare pulizia delle proprie convinzioni per trasformare l'apparente giudizio in opportunità, ottenendo una visione non vincolata ai limiti della propria esperienza.

### ♻️ Utilità se Consapevole
#osservatore #propositivo #chiarezza #indipendenza

Una strada per l'evoluzione è acquisire onestà intellettuale, lavorando attivamente per smontare i modelli ereditati che vincolano le scelte. È possibile accogliere le osservazioni esterne con prudenza, trasformando l'apparente giudizio in un'opportunità di miglioramento. L'individuo si può concentrare sul chiedere esplicitamente i punti da chiarire e sul dialogare per scavare oltre la superficie dell'opinione altrui. Imparare a non prendere le critiche sul personale permette di avviare una conciliazione e un contatto aperto e costruttivo. Se il dialogo non è funzionale, si può tranquillamente interromperlo senza perdere nulla. Questo esercizio permette di raggiungere una forma più oggettiva della realtà e di semplificare l'espressione dei concetti importanti in modo più trasparente e libero da vincoli, mantenendo un equilibrio tra ciò che si desidera fare e il contesto esterno.