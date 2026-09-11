---
cssclasses:
  - mente-gioco
  - mente
sbilanciamento: sabotatore
categoria: mente
stato: originale_v2
titolo: Sabotatore, Mente
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
#sabotatore #autosvalutazione #depotenziante #vincoli

- **Autosvalutazione e Filtro Critico**
	È presente un un filtro di autosvalutazione sulla propria percezione, spesso il risultato di critiche e osservazioni negative ricevute in passato. Queste critiche ripetute si sedimentando come convinzione auto-accettata di inadeguatezza. L'individuo si focalizza esclusivamente sui propri insuccessi o difetti ignaro del suo vero potenziale, perde la fiducia in se stesso e le aspettative di ciò che può realizzare.

- **Demotivazione per Assenza di Gratificazione Cognitiva**
	Si manifesta un intenso scoraggiamento di fronte a piccoli insuccessi nel processo di apprendimento, l'assenza di punti riferimento genera la sensazione di "brancolare nel buio" e di non capire nulla. Quando il processo di apprendimento non è graduale o gratificante, la fatica cognitiva spinge a rigettare una attività potenzialmente interessante, la mente vive l'esperienza come spiacevole, una inutile perdita di tempo e di energie.

### 👁️ Influenza sull'Immagine di Se
#sabotatore #autosvalutazione #depotenziante #autocritica

Il sabotatore si manifesta come un autodialogo critico o pessimista, un eco di critiche del passato o di ripetute osservazioni negative, ricevute in contesti formativi o come punizione disciplinare. Questa interferenza induce una crescente disconnessione tra una attività cognitiva come l'apprendimento o lo studio e il coinvolgimento spontaneo che essa potrebbe generare. 

**L'abitudine peggiore è accettare la presenza di un autodialogo sempre e costantemente rivolto agli aspetti negativi: cosa è incompleto, cosa manca, cosa si poteva fare di più. Essere in grado di notarli è importante. Tuttavia, il problema è che siano le uniche cose che ci si abitua a notare. Il pensiero di trovare i difetti è sempre la prima scelta rispetto a trovare i pregi o gli sbocchi per poter migliorare quello che si riconosce come oggettivamente incompleto.**

È come se la mente si sentisse brava o compiaciuta esclusivamente a riconoscere ed elencare i problemi, gli errori, le cose che mancano o cosa si poteva fare di più, però senza prendersi a carico quello che dovrebbe naturalmente seguire, ovvero elaborare delle soluzioni possibili o riconoscere ed evidenziare la direzione migliorare per gestire la cosa.

**Se gli errori non propongono una direzione migliorativa non è possibile imparare, si diventa solo bravi a riconoscere i problemi. Può essere utile solo se si sta facendo un'analisi critica, non se si sta imparando**

Questo diventa un percorso depotenziante e nel tempo porta a una perdita di interesse, l'attività diventa solo fonte di disagio e insoddisfazione perché la presenza di errori sovrasta ogni possibile direzione utile per migliorare, perché per imparare resta necessario disporre di una soluzione di riferimento.

Questa attitudine porta solo a concentrarsi sull'aspetto negativo ma senza una soluzione diventa un vicolo cieco di opportunità, qualcosa che impedisce di chiudere il cerchio e rielaborare le scelte passate o le esperienze presenti per individuare schemi di pensiero che possono essere migliorati.
### ♻️ Utilità se Consapevole
#alleato_interiore #mediazione #riconciliazione #propositivo

È importante sapere che è possibile interagire attivamente e costruttivamente con questa voce interiore, invece di perdere energie passivamente a causa di questo autodialogo depotenziante. La mente come un motore di ricerca, lavora continuamente per trovare il punto comune tra i pensieri che ritiene importanti. 

Se questa voce interiore ci pone all'attenzione un pensiero anziché sentirci mortificati o prenderla sul personale, possiamo aggiungere alcuni parametri di ricerca e trasformarlo da sabotatore ad alleato. Assegnandogli il compito di individuare cosa vorremmo migliorare dell'esperienza e farci suggerire soluzioni accessibili e gratificanti. Questo preserva il suo ruolo naturale nella gestione dei problemi, lasciando a noi la possibilità di scegliere il modo in cui preferiamo essere aiutati. Reincanalando l'energia precedentemente dispersa, verso una processo che favorisce la fiducia nelle proprie capacità e un approccio collaborativo in ogni sfida quotidiana.