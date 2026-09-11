---
cssclasses:
  - abilità-spirito
  - spirito
sbilanciamento: sabotatore
categoria: spirito
stato: originale_v2
titolo: Sabotatore, Spirito
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
#sabotatore #idealismo #depotenziante #vincoli

- **Punto di Ingresso per Messaggi Esterni e Convinzioni**
	Succede che pensieri, ideologie, precetti morali e mentalità di gruppo vengano interiorizzati come "buoni consigli". Queste influenze esterne, se assimilate in modo acritico, possono radicare regole apparenti o vincoli impliciti, influenzando la capacità di interpretare ed esprimersi nel mondo, una colonizzazione di concetti che invadono il nostro sistema di valori, simboli e significati.
	
- **Alterazione dell'Interpretazione e Modello Limitante**
	L'incapacità di gestire gli eventi in momenti di vulnerabilità e il nostro ruolo di interpreti del passato, e l'assimilazione di false speranze o giustificazioni esterne cristallizzano un significato a volte limitato o impreciso dei ricordi difficili e delle emozioni che proviamo. Compromettendo il ruolo neutrale del nostro modello della realtà, si perde una visione oggettiva degli eventi se questi sono incoerenti al modello interiorizzato.

### 👁️ Influenza sull'Immagine di Se
#sabotatore #idealismo #depotenziante #autocritica

Questo sabotatore, diversamente dagli altri, può accogliere in modo acritico gli eventi esterni comportandosi come una "breccia", attraverso cui pensieri e convinzioni possono introdursi e mettere radici nel nostro mondo interiore. Sfruttando un ingresso incustodito, precetti morali, ideologie di gruppo e mentalità collettive si infiltrano nel nostro sistema di valori. 

L'eco interiore di queste interferenze esterne, influenzano la percezione della realtà, perché dal momento in cui si prendono per vere o si accettano determinati schemi di pensiero, le regole apparenti che questi portano dietro entrano nel nostro modello della realtà. L'individuo perde il suo ruolo di interprete neutrale, e aderendo a regole implicite, finisce senza saperlo in un labirinto di specchi e di illusioni, che alterano la realtà che percepisce e lo distolgono da ciò che gli serve o che può realizzare.

Questa assimilazione acritica di influenze esterne e una interpretazione distorta di esperienze passate conduce alla creazione di regole illusorie. Queste consolidano convinzioni o consuetudini non necessarie, dove ciò che dovrebbe essere una scelta personale si trasforma in "automatismo" o una abitudine. Se il proprio mondo interiore ha integrato "regole illusorie", queste offuscano, prevengono o alterano le intenzioni o i pensieri più spontanei e naturali, e senza accorgersene si perdono la presenza mentale e l'obiettività.

Questi vincoli interiori influenzano ed ostacolano la libertà di scelta e l'espressione senza filtri del proprio mondo interiore. Lo fanno ogni volta che una convenzione non necessaria, radicata nel mondo interiore, altera le sensazioni relative ad una attività con convinzioni che la giustificano, la prevengono o la fanno sentire inappropriata anche in assenza di regole formali e obblighi reali.

### ♻️ Utilità se Consapevole
#alleato_interiore #mediazione #rinnovamento #obiettività

È necessario ricoprire il ruolo di custode della soglia, il cui compito non è impedire il passaggio, ma valutare ciò che entra o è già entrato nel nostro modello della realtà. Rivalutando attivamente concetti, regole, convenzioni o luoghi comuni già assimilati. Accorgersi dei conflitti interiori nati da queste incongruenze, e soppesando l'influenza delle relazioni e dei vincoli che abbiamo interiorizzato, prestare attenzione a quando il nostro modello di realtà  entra in conflitto con la quotidianità o ne sembra incompatibile.

Rimuovendo uno specchio deformante alla volta dal nostro modello, guadagneremo maggiore flessibilità e capacità di esprimere e fare da mediatori tra il nostro mondo interiore e la nostra quotidianità. Con un regolare lavoro di "pulizia" possiamo rivalutare queste premesse limitanti, dismettere le regole superflue e recuperarne il significato simbolico originale o l'intenzione positiva che le ha originate.

Creando nuove regole, abitudini e convenzioni migliori, più personali e bilanciate, è possibile fare riemergere desideri precedentemente considerati irrealizzabili, raggiungendo un punto di equilibrio interiore stabile che spontaneamente mantenga in armonia la nostra vita quotidianità e il nostro giardino interiore.
