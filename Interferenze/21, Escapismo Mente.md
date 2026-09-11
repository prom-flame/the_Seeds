---
cssclasses:
  - mente-gioco
  - mente
categoria: mente
sbilanciamento: escapismo
stato: esordiente_v2
titolo: Escapismo, Mente
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
#escapismo #resistenza_al_cambiamento #emozioni #vincoli

- **Il sistema di convinzioni si irrigidisce per paura del dispendio energetico:**
	Il costo di energia legato al cambiamento viene percepito come fatica sprecata o come inutile. L'incapacità di accettare che il proprio modello di pensiero non sia perfetto o che presenti lacune porta l'individuo a una rigida difesa delle proprie convinzioni. Per evitare di affrontare la ristrutturazione onerosissima della propria immagine interiore, si tende a preferire schemi di pensiero che non mettano in discussione ciò in cui si crede, mantenendo un modello intellettuale rigido e immutabile. Tale autolimitazione si manifesta come una risposta interna del tipo: "siamo fatti così", "sono abituato a essere così", una conseguenza di abitudini radicate.

- **L'autogestione della gratificazione si scontra con l'incertezza e lo stallo:**
	La necessità di generare spontaneamente gratificazione dalla propria attività mentale, senza dipendere da forme di distrazione o scorciatoie esterne, è la chiave per l'autonomia. Tuttavia, il tentativo di non affidarsi a stimoli artificiali è reso difficile dal timore di dover firmare un assegno in bianco in termini di energie, senza conoscere il ritorno dell'investimento. In questa situazione, si alimenta l'illusione che parlare di un argomento che si conosce molto bene o sfogarsi sia sufficiente a progredire, quando in realtà è solo un meccanismo per alleggerire alcune tensioni o costrizioni, mantenendo di fatto uno stato di stallo forzato.

### 💔Esperienze Spiacevoli
#escapismo #resistenza_al_cambiamento #emozioni #inconsapeovle

L'abitudine all'evasione mentale, o la ricerca di una distrazione che alleggerisca un pensiero opprimente, è il sintomo di una resistenza a mettere in discussione il proprio modello cognitivo. Questo fenomeno si manifesta soggettivamente attraverso punti ciechi, cioè informazioni che ci vengono fatte notare dall'esterno ma che noi troviamo irragionevoli e scartiamo subito, negando l'utilità di ciò che non ci interessa. Il costo di energia legato al cambiamento può essere percepito come inutile, e per questo non lo si vuole affrontare senza un valido motivo. Quando l'opinione esterna fa emergere lacune nel nostro modello, ci si sente minacciati e la mente reagisce insistendo e negando determinate considerazioni per mantenere la solidità di un'idea.

La ricerca della ricompensa cognitiva è l'elemento che spinge verso il cambiamento, ma per riuscire a generare piacere dalla propria attività, è necessario accogliere la visione non filtrata della realtà, ovvero accettare che il proprio modello possa avere lacune e non essere perfetto. L'assenza di questa disponibilità a considerare altre prospettive impedisce di fare tesoro delle osservazioni altrui, mantenendo il modello intellettuale obsoleto. La mente, incapace di aggiornare la propria visione della realtà, tende a rimanere entro schemi noti e a interpretare soggettivamente ciò che viene detto come una critica o una minaccia.

Se si è troppo convinti di difendere il proprio credo, si reagisce in modo acceso e si cade nella polarizzazione, applicando un filtro che interpreta negativamente le opinioni diverse. In assenza di un'analisi senza filtri dei fatti, il problema non può migliorare, anzi la sensazione di incongruità aumenta. La fuga dalla consapevolezza tramite la distrazione serve a evitare di ammettere di essere infelici o di non vedere una soluzione. È cruciale rendersi conto che la solidità di un'idea dipende dalla sua capacità di resistere in contesti apparentemente contraddittori. Solo così si può rompere lo stallo e permettere al proprio modello di evolvere.

### ♻️ Utilità se Consapevole
#consapevolezza #indipendenza #adattabilità #obiettività

Una strada per superare la tendenza a evitare l'impegno mentale è riuscire a riqualificare le attività che risultano noiose o scomode, trasformandole in qualcosa di gratificante. Si può cominciare a prestare attenzione al motivo per cui si scarta un'informazione, ammettendo che il confronto attivo e costruttivo con l'esterno obbliga a migliorare il modello interiore. È possibile prendere nota delle osservazioni e provare a interagire per trovare punti di incontro con chi la pensa diversamente, usando la critica ricevuta come stimolo al miglioramento. Riscoprire la capacità di accogliere prospettive differenti permette di espandere il repertorio di soluzioni, rendendo il proprio approccio più flessibile e permettendo all'attività di generare gratificazione spontaneamente. In questo modo, il modello interiore può aggiornarsi, diventando coerente con il mondo reale e aumentando la libertà di scegliere come affrontare i percorsi di apprendimento.