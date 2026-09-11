---
cssclasses:
  - mente-gioco
  - gioco
sbilanciamento: escapismo
categoria: gioco
stato: originale_v2
titolo: Escapismo, Gioco
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
#escapismo #distrazioni #emozioni #vincoli

- Cessione del Ruolo Attivo di Co-autore della Propria Felicità
	Si ricorre all'utilizzo di distrazioni o intrattenimento, spesso cercate per noia o accolte passivamente da proposte esterne, usati come palliativi per evitare di riconoscere o affrontare situazioni sgradevoli, pensieri opprimenti o la propria infelicità.
	Si cede passivamente il proprio ruolo attivo di co-autore della propria felicità e del proprio modo di sentirsi liberi a chi fornisce l'intrattenimento. Questo implica che la responsabilità di generare stimoli positivi viene trasferita a fonti esterne, anziché essere prodotta autonomamente.

- Senso di Colpa e Deresponsabilizzazione a Fonti Esterne
	Il senso di colpa che segue la distrazione, spinge a cercare di legittimare la distrazione cercando capri espiatori o attribuendo la colpe a fattori esterni o inevitabili. Questo serve a evitare di ammettere a se stessi una profonda infelicità o la riluttanza ad affrontare una determinata situazione, trasformando una mancanza di volontà di affrontare il problema in un'abitudine giustificata.

### 💔Esperienze Spiacevoli
#escapismo #distrazioni #emozioni #inconsapeovle

La mancanza di coinvolgimento creativo nello svolgimento di una attività, porta a cercare gratificazioni esterne superficiali e poco soddisfacenti, poiché la parte spontanea responsabile della gratificazione naturale "non partecipa".

L'escapismo, in questo contesto, spesso viene chiamato intrattenimento, rappresenta una forma semplicistica e pervasiva di distrazione ed evasione dalla realtà. A differenza del gioco autentico, che promuove l'esplorazione e la sperimentazione personale.

L'intrattenimento incoraggia a cedere il proprio ruolo attivo nella ricerca e creazione di gratificazione personale a persone, attività o servizi esterni che ci forniscono uno stimolo piacevole facile da consumare con poco sforzo ma che non nasce più da noi.

Si può manifestare come una ricerca costante o circostanziale a stress esterni, di gratificazioni sensoriali o emotive provenienti da diverse fonti come videogiochi, narrativa, cibo, socialità, sesso, sostanze d'abuso e in molte altre attività dalla socialità superficiale.

Diventa un lenitivo o un surrogato per evitare di riconoscere un problema o affogare i dispiaceri di situazioni difficili che non si vuole affrontare o non si sa come superare. Offre una pausa temporanea da ciò che si percepisce come opprimente o faticoso, senza risolvere realmente il problema alla radice.

Si è spesso consapevoli di questo fenomeno, ma si sceglie di attribuirne la colpa o la responsabilità a fattori esterni (come la tentazione) o a una parte interna incontrollabile (l'ego o le pulsioni dell'inconscio) che servono come capro espiatorio per non razionalizzare realmente il nostro ruolo e la possibilità di fare scelte migliori.

### ♻️ Utilità se Consapevole
#consapevolezza #indipendenza #stato_di_flusso #obiettività

Il superamento di questo escapismo passa per la consapevolezza del meccanismo di distrazione e del disagio sottostante che questa va a lenire. 

La via d'uscita consiste nell'imparare a rendere le attività che si affronta, intrinsecamente coinvolgenti e gratificanti attraverso stimoli realmente vicini alle nostre preferenze, e modalità di esecuzione libere da sensi di colpa o obblighi impliciti.

Riprendendo il ruolo attivo di co-autori== della propria felicità e appagamento, riducendo così l'appetibilità di un conforto esterno generico e impersonale.