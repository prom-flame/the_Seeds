---
cssclasses:
  - abilità-spirito
  - spirito
sbilanciamento: maschera
categoria: spirito
stato: originale_v2
titolo: Maschera, Spirito
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
#maschera #suggestionabilità #contesto #vincoli

- **Assimilazione di Mentalità Astratte**
	Si origina dall'assimilazione di ideologie, mentalità di gruppo e forme-pensiero, che indirettamente influenzano i propri valori e la propria identità, spingendo a diventare attori che recitano un copione anziché interpreti della propria realtà, compromettendo nel tempo la capacità di interpretare ed esprimere liberamente se stessi.

- **Perdita di Identità Reale e Separazione Interna**
	Questo processo causa un allontanamento dalla parte spontanea e dalla propria identità reale, creando una separazione interna (simile al concetto di ombra) dove si escludono elementi genuini del sé estraniati o negati da modelli appresi, elementi che non venendo integrati o espressi liberamente, portando l'individuo a sentirsi "inquinato" da parti di se ritenute sbagliate, sporche o inadeguate.

### ⚓ Influenza dal Contesto
#maschera #suggestionabilità #contesto #stereotipo

La maschera relativa allo spirito agisce in profondità, influenzando l'immagine che abbiamo di noi stessi, non tanto in relazione agli altri, quanto nel nostro mondo interiore. Si radica nei nostri valori e nella propria identità, plasmando il modello del mondo che abbiamo assimilato. Questa maschera è straordinariamente sfuggente, e per questo, difficile da percepire, poiché si fonde con ciò che crediamo essere, il nostro carattere e il come siamo.

L'origine di questa distorsione risiede nell'assimilazione, spesso inconsapevole, di ideologie, mentalità di gruppo o modelli sociali. Che anche se inizialmente sembrano positive, influenzano e vincolano le scelte nel tempo. Accogliendole, crediamo di rispecchiarci in esse, ma diventiamo attori che recitano un copione piuttosto che interpreti autentici delle proprie convinzioni. Quando l'individuo si abitua a pensarsi in un certo modo, crederà che "sarebbe strano comportarsi diversamente". 

L'inquinamento del proprio modello interiore diventa nel tempo sempre più difficile da riconoscere. Il dialogo interiore, che dovrebbe essere un alleato e un sostegno per la nostra volontà e fonte di autostima, viene compromesso dalla maschera. Il nostro modello del mondo, anziché essere flessibile e in costante evoluzione, diventa rigido. Non esponendo più le proprie incertezze al confronto attivo e costruttivo con gli altri, proprio quella frizione necessaria con l'esterno, pur scomoda, è ciò che consente al modello interiore di evolvere e diventare più obiettivo.

La maschera impedisce di accettare questa frizione, lasciando le idee e i concetti in una forma acerba e non definitiva. Si perde la capacità di valorizzare l'impegno dedicato a crescere, rendendo superfluo il riconoscimento intrinseco dei propri sforzi. La gratificazione interna cede il passo alla ricerca di approvazione esterna, anche se superficiale o non sincera. Si finisce per preferire le opinioni altrui alla propria realizzazione personale, rinunciando alla libertà di scegliere e alla capacità di trovare piacere nella propria presenza mentale e nel confronto con il proprio autodialogo.

La maschera dello spirito porta a una dipendenza dalle idee esterne, dal conformismo alle norme sociali, all'adeguarsi a qualcosa che è generico ed impersonale. Il suo effetto più insidioso è proprio questa inibizione del riconoscere la differenza tra le proprie intenzioni e qualcosa che non è realmente necessario, rendendo l'individuo meno capace di adattarsi alla realtà o di esprimere pienamente la propria identità autentica, finendo per adeguarsi al "così fan tutti".

### ♻️ Utilità se Consapevole
#ruolo #obiettività #autenticità #propositivo

La maschera relativa allo spirito, pur essendo molto sottile e legata all'immagine che abbiamo di noi stessi nel nostro mondo interiore, può essere gestita consapevolmente per favorire un equilibrio interno. Si tratta di coltivare un auto-dialogo che agisca come un alleato e un sostegno, riconoscendo il valore dell'impegno dedicato a crescere e a migliorare. Questo porta a un sostegno autogestito, rendendoci indipendenti dalla necessità di un riconoscimento esterno.

Tuttavia, per raffinare e rendere più obiettivo il proprio modello interiore, che altrimenti sarebbe puramente legato alle nostre esperienze private, è fondamentale esporre le proprie idee al confronto attivo e costruttivo con gli altri. Questa "frizione" esterna, sebbene possa essere scomoda, ci obbliga a migliorare i nostri concetti, rendendoli più solidi e facili da condividere, e a integrarli con il mondo reale. In questo modo, il nostro modello diventa più flessibile e resistente, favorendo una profonda presenza mentale e un piacere intrinseco nello stare con sé stessi.