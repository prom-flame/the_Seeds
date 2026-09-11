---
cssclasses:
  - scopo-base
  - base
categoria: base
sbilanciamento: maschera
stato: originale_v2
titolo: Maschera, Base
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
#maschera #generalizzazione #contesto #vincoli

- **Deformazione delle Priorità e Generalizzazione dei Bisogni**
	Questa maschera induce a privilegiare l'idea di un bene superiore o collettivo, basato su presunzioni, luoghi comuni o standard generalizzati, a scapito dell'attenzione per le specifiche e diverse necessità legate alla base sicura potenzialmente diversa in ciascun individuo. Emerge una incapacità nel notare le necessità individuali, applicando una "ricetta standard generica" che ignora le differenze e le esigenze personali. L'individuo si conforma a ciò che la società propone come desiderabile per tutti, non vedendo la perdita della propria unicità.

- **Produzione di Soluzioni Impersonali e Inefficaci**
	Si tende a creare o a preferire soluzioni suggestive, concettualmente nobili o universalmente condivisibili sulla carta, ma sterili e di difficile utilizzo nella realtà del singolo, perché basate su idee astratte o idealistiche anziché su dinamiche concrete e tangibili. Delle "soluzioni apparenti" che servono principalmente a manifestare una intenzione o a mettere in pace la coscienza, per sentirsi buoni ed impegnati su una causa, ma senza verificare quanto questo impegno rappresenti un reale cambiamento o beneficio per i reali destinatari, essendo spesso.

### ⚓ Influenza dal Contesto
#maschera #generalizzazione #contesto #stereotipo

Questa maschera induce alla permeabilità da ideologie morali o aspettative sociali, l'individuo accoglie ciò che la collettività reputa desiderabile e adatta le sue priorità verso un "bene ideale" o il "fare la cosa giusta". Cavalca il desiderio di tutti di aiutare il prossimo, ma a volte questa attitudine impedisce di riconoscere o ascoltare i bisogni specifici degli altri, perché questi mettono alla luce le difficoltà realizzative reali e la necessità di cambiare le priorità personali. Si preferisce una generalizzazione dei bisogni, "ricette generiche e universali" per il benessere personale o altrui, spesso presentate in modi che le fanno sembrare facili da applicare. 

Questa apparente comodità, lascia la porta aperta a regole morali e luoghi comuni che non rispecchiano bisogni reali, ma ne sono spesso una versione stereotipata di come "dovrebbero" essere le dinamiche sociali, ottime per catturare l'attenzione collettiva, ma povere della capacità di risolvere qualcosa nella pratica, cosa ben più impegnativa della sola idea di farlo. Invece di investire energie per un miglioramento concreto delle condizioni proprie o sociali, lo sforzo viene dirottato verso un'azione che non porta a una stabilità autentica. La ricerca della serenità è ostacolata da questa dinamica, non si affrontano i problemi reali, ma si perpetua un'illusione. 

È a quel punto che la propria base sicura, luogo interiore e personale di riposo e recupero, viene inevitabilmente compromessa dal suo stesso istinto naturale di essere di aiuto. Perché la maschera incoraggia ad ignorare la diversità delle esigenze individuali, incoraggiando un atteggiamento che impedisce di riconoscere cosa fa perdere tempo ed energie, ostacola la capacità di agire per il proprio benessere o di legittimare la difesa del proprio spazio individuale.

Come diretta conseguenza, la maschera incoraggia soluzioni superficiali, costruite su aspettative astratte e suggestive, soluzioni apparenti che alla fine risultano incomplete o inefficienti, che consumano tempo, risorse e motivazione ma sono incapaci di portare a un cambiamento reale. A volte nemmeno apprezzate perché troppo impersonali per offrire un sostegno tangibile, l'efficacia è compromessa dalla loro natura universale, la differenza tra una aspettativa astratta rispetto a ciò che soddisfa un bisogno tangibile e realmente necessario.
### ♻️ Utilità se Consapevole
#ruolo #obiettività #ascolto #mediazione

Una via concreta e realistica di miglioramento, che segue il punto di crisi generato dalla sterilità delle finte soluzioni, è legata alla riscoperta della capacità di conciliare le prospettive divergenti. È possibile cominciare a lavorare sulla singola persona, assicurandosi che stia sperimentando ciò che desidera, piuttosto che imporre un ideale astratto. Una ristrutturazione interna richiede di smettere di ricorrere ai luoghi comuni e alle ideologie morali che sono prevalenti, per concentrarsi sul notare le autentiche differenze e le necessità individuali. 

In termini pratici, la strada migliore è rappresentata dal gesto più semplice: chiedere direttamente come potremmo essere di aiuto. Questo sposta l'attenzione dal ricorrere a soluzioni impersonali alla creazione di un punto sicuro fatto di cose reali e accessibili. Tale approccio richiede di interrogare e rivedere le convinzioni comuni e di coltivare una comprensione autentica delle esigenze specifiche, proprie e altrui, superando l'illusione di una normalità universale o ideale.