---
cssclasses:
  - mente-gioco
  - mente
categoria: mente
sbilanciamento: maschera
stato: esordiente_v2
titolo: Maschera, Mente
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
#maschera #dogmatismo #contesto #vincoli

- **Aggrapparsi alle convinzioni per mascherare le fragilità cognitive:**
	Ci si lega troppo all'immagine interiore di chi crediamo di essere o si assume un atteggiamento difensivo per non essere screditati riguardo alle proprie convinzioni. Questo forzare la mano nel sostenere un determinato concetto, senza accettare pareri discordanti, serve a compensare le lacune del nostro modello, ma allo stesso tempo rendendolo rigido e difficile da aggiornare.  È frequente l'abitudine a preferire la conferma esterna.

- **La pretesa di immutabilità che ignora i punti ciechi:**
	Il rifiuto di accogliere considerazioni esterne per paura di ammettere le proprie imperfezioni, spinge verso la negazione dell'utilità di ogni nuova informazione, se percepita come irragionevole. Mantenere una visione rigida e immutabile del mondo comporta il rischio di diventare obsoleti, poiché un modello non duttile non evolve. Si ha la tendenza a soppesare i pareri esterni e ad evitare punti di incontro con chi la pensa diversamente.

### ⚓ Influenza dal Contesto
#maschera #dogmatismo #contesto #stereotipo

L'interferenza si manifesta come un atteggiamento spesso supponente o difensivo, volto a preservare l'immagine di solidità e competenza su cui abbiamo costruito la nostra idea di noi stessi. Aderiamo a convenzioni e protocolli, auto-convinendoci che l'immagine interiore che abbiamo di noi stessi sia perfetta e debba rimanere invariata.

Quando qualcuno mette in discussione o esprime dubbi sulle nostre convinzioni, tendiamo a non prestare attenzione alle osservazioni esterne, bensì a ribattere per rafforzare la solidità di ciò in cui crediamo. Questa reazione, che può essere a volte eccessiva o fuori luogo, è sintomatica del fatto che il modello che abbiamo interiorizzato non è completamente solido e presenta delle lacune che vengono fatte emergere da opinioni esterne. La vera sfida è distinguere tra un parere costruttivo e una critica superficiale, per evitare di applicare un filtro che assegni il valore di critica a qualsiasi cosa che non ci dà immediata soddisfazione.

Dipendere dalla convalida esterna o dalle lusinghe per l'immagine di competenza ci distoglie dalla gratificazione interiore. Per tornare a un punto di vista concreto e accessibile, dobbiamo uscire dall'abitudine di preferire ciò che rispecchia i nostri schemi di pensiero, anche se ristrutturare il modello interiore costa energia. L'obiettivo non deve essere avere ragione ma ampliare la nostra capacità di affrontare i concetti, unendo prospettive differenti per individuare una forma più completa. Il confronto con altri, sebbene possa essere scomodo, ci obbliga a migliorare il modello interiore, rendendo i concetti man mano più facili da condividere.

Se ci ostiniamo a mantenere un modello rigido e immutabile, e se perdiamo il ruolo di sostegno e ascolto autogestito, le incongruenze tra le nostre aspettative e la vita reale non possono che peggiorare, portando il nostro filtro interiore a diventare obsoleto. In questo modo, il nostro mondo interiore diventa difficile da condividere con gli altri, creando una polarizzazione. Se la volontà di applicare idee rigide persiste in assenza di auto-sostegno, l'abitudine porta a una rigidità o un automatismo. Il lavoro per ritrovare l'equilibrio deve mirare a rendere il modello interiore più coerente con la realtà, sfruttando i punti di vista esterni.

### ♻️ Utilità se Consapevole
#ruolo #obiettività #flessibilità_mentale #indipendenza

Una via concreta di miglioramento si apre non appena si decide di prendere nota e fare tesoro delle osservazioni esterne, ammettendo che il proprio modello possa non essere perfetto. È possibile iniziare a spogliarsi un pochino del ruolo difensivo e accogliere in modo prudente le osservazioni, valutandole come opportunità di arricchimento anziché come minacce o perdite di tempo. Il confronto attivo e costruttivo con gli altri è necessario per raffinare il modello interiore, perché ci costringe a migliorarlo anche quando non lo sentivamo necessario. 

Si può lavorare per rendere il nostro modello interiore più duttile, evitando che rimanga rigido e superato dagli eventi. Incominciando a soppesare meglio i concetti e cercando un punto di equilibrio, si estende la percezione della realtà. L'obiettivo è creare elementi essenziali e comuni, definendo le variazioni, rendendo il pensiero meno radicale e più adattabile a ogni nuova interazione. Si può espandere il repertorio di soluzioni, migliorando l'approccio e la libertà di affrontare nuovi percorsi in modo più duttile e creativo.