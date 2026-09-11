---
cssclasses:
  - abilità-spirito
  - abilità
sbilanciamento: maschera
categoria: abilità
stato: originale_v2
titolo: Maschera, Abilità
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
#maschera #reputazione #contesto #vincoli


- **Priorità alla Quantità rispetto alla Qualità**
	La maschera induce l'individuo a porre un'importanza eccessiva sulla reputazione e sul giudizio altrui, preferendo pareri positivi generici e superficiali, abituandosi a concentrarsi sulla quantità dei riconoscimenti rispetto alla qualità o sincerità. La spinta principale diventa ottenere riconoscimenti per il proprio impegno, questo condiziona le scelte portano ad assumere carichi di lavoro non motivati da autentica passione, ma dal desiderio di mantenere la popolarità raggiunta.

- **Inaridimento della Complicità con la Parte Creativa**
	La tendenza ad impegnarsi in attività primariamente per la validazione esterna, porta ad un progressivo distacco dalla propria sfera creativa e spontanea. Le attività, sebbene connesse alle proprie capacità o competenze, vengono eseguite in maniera più impersonale e distaccate dalle proprie preferenze. Questo si traduce in una perdita della spontaneità e in una frattura della relazione con la propria capacità di vivere il momento, raffreddando l'entusiasmo e la motivazione.

### ⚓ Influenza dal Contesto
#maschera #reputazione #contesto #stereotipo

La maschera, nel contesto dell'Abilità, distorce il modo in cui l'individuo vive e percepisce il proprio valore e quello del proprio operato. La propria autostima diventa fragile, legata a complimenti o pressioni esterne. Si sperimenta un logoramento legato all'esposizione a eventi stressanti e il confronto con gli altri si trasforma in una fonte di emozioni come ostilità, invidia, senso di inferiorità o nascondono una necessità performativa indiretta.

Queste emozioni spiacevoli vengono alleviate dall'apprezzamento per le attività in cui riusciamo ad essere apprezzati o riceviamo riconoscimento o popolarità. La spinta principale nel tempo diventa la ricerca di riconoscimenti ed apprezzamenti provenienti dall'esterno, anziché dall'appagamento che deriva da una attività impopolare o dall'affinare il proprio stile personale. Se l'individuo inizia a dare maggiore importanza alla reputazione e al giudizio altrui, la sua attenzione finirà per concentrarsi sul creare e consolidare questa immagine di sé da mostrare agli altri, finalizzata a risultare d'effetto e ad accrescere la propria reputazione. Finendo per dare eccessiva importanza a ciò che pensano gli altri e lasciando che le opinioni esterne influenzino le proprie scelte.

Questa dipendenza dall'esterno porta ad un inaridimento della complicità con la propria parte creativa e la gioia spontanea nel fare, l'entusiasmo iniziale, si raffredda, le attività vengono eseguite in modo impersonale e disconnesso da quello che sono le proprie preferenze. Non c'è più un dialogo o la complicità con la proprie risorse interiori capaci di creare e sperimentare. L'attività si trasforma in un dovere e l'individuo finisce per inseguire un'immagine che non appartiene più a lui, ma ad una aspettativa esterna o una validazione effimera.

Finendo per inseguire obiettivi dettati dall'immagine esteriore, orientando la crescita personale non sui propri valori autentici, ma su desideri e obiettivi costruiti o dipendenti dall'esterno. Questa divisione ostacola il miglioramento qualitativo autentico, la ricerca di conferme porta a trascurare le critiche costruttive, scegliendo al loro posto apprezzamenti generici, perdendo di vista la qualità del riconoscimento che si riceve. Questo impoverisce le opportunità di ridiscutere le proprie priorità e spegne l'interesse di sperimentare su argomenti non popolari, rischiando di rimanere ancorati ad un livello di mediocrità che piace agli altri ma è lontano da ciò che ci ha fatti appassionare.

### ♻️ Utilità se Consapevole
#ruolo #obiettività #minimalismo #propositivo

Per raggiungere un equilibrio interiore con la maschera legata all'Abilità, è essenziale riposizionare la fonte della gratificazione. Anziché cercare incessantemente lodi esterne, si deve imparare a riconoscere e valorizzare l'impegno e i progressi personali. Questo significa spostare il focus dalla reputazione al piacere intrinseco del fare.

È fondamentale cercare feedback qualitativi, accogliendo anche la critica costruttiva come opportunità di miglioramento autentico, piuttosto che accontentarsi di semplici complimenti. La maschera può essere usata consapevolmente per imparare dagli altri, vedendo le loro competenze come stimoli e occasioni di scambio, non come minacce. Si tratta di superare i propri limiti con una progressione personale, ponendosi obiettivi raggiungibili. Infine, coltivare un dialogo interiore di supporto, che riconosca il proprio valore e fatica, rende indipendenti dal giudizio esterno, fornendo un sostegno stabile all'autostima.