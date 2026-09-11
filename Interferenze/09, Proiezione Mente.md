---
cssclasses:
  - mente-gioco
  - mente
categoria: mente
sbilanciamento: proiezione
stato: esordiente_v2
titolo: Proiezione, Mente
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
#proiezione #pregiudizio #percezione #vincoli

- **La reazione accesa che nega l'utilità delle idee altrui a causa dell'assenza di un punto di incontro:**
	La reazione accesa verso opinioni diverse significa che siamo troppo convinti di difendere ciò in cui crediamo. Sentirsi minacciati indica che notiamo indirettamente lacune nel concetto che abbiamo interiorizzato. La tendenza a negare l'utilità di qualcosa e scartare subito le informazioni che non vogliamo sentire crea un filtro mentale (polarizzazione) che mette in una "lista nera" le idee esterne, trovandole irragionevoli. L'incapacità di cercare un punto di incontro con chi la pensa diversamente o di accogliere osservazioni utili porta a un attrito che impedisce al modello interiore di diventare flessibile e rende il nostro pensiero rigido e obsoleto.

- **L'emergere di un'intenzione costruttiva che fallisce per la superficialità della discussione:**
	A volte parlare di un argomento ci convince che stiamo facendo progressi. Questa illusione è problematica perché l'interazione verbale alleggerisce le tensioni, facendo sembrare di uscire dallo stato di stallo. Tuttavia, questa esposizione verbale non sostituisce la fatica di ristrutturare il modello interiore. Il desiderio di un approccio costruttivo o di un confronto attivo che porti a un miglioramento nei fatti fallisce se si mantengono convinzioni rigide e si insiste a negare le considerazioni altrui. L'azione che mira a normalizzare la situazione può degenerare in presa di posizione difensiva, sprecando tempo ed energie che andrebbero invece investite in nuove opportunità.
### ⚖️ Influenza sulla Percezione
#proiezione #pregiudizio #percezione #doppio_standard

La proiezione della mente si manifesta come un senso di fastidio nei confronti di chi esprime qualcosa che non vogliamo sentire. Questa reazione, non è segno di tranquillità interiore, ma indica che il concetto assimilato non è gestito in modo equilibrato. Quando l'opinione esterna espone le lacune del nostro modello, non ci piace e ci sentiamo minacciati. Diventa più importante aggrapparsi al significato del concetto e difendere a tutti i costi ciò in cui crediamo, escludendo a priori la possibilità che pareri discordanti siano utili. Questo comportamento alimenta un filtro mentale o pregiudizio che scarta rapidamente informazioni che troviamo irragionevoli o fuori luogo. Rischiamo di cadere nel doppio standard, applicando una metrica diversa per valutare ciò che ci piace e ciò che respingiamo.

Il momento critico che spinge verso il bisogno di un approccio costruttivo si manifesta quando ci accorgiamo che, nonostante il desiderio di migliorare o normalizzare la situazione, le nostre azioni non portano a progressi concreti. Si inizia a riconoscere l'assenza della capacità di trovare un punto di incontro che potrebbe ampliare la nostra comprensione. La mente, infatti, cerca naturalmente di massimizzare le ricompense con il minimo sforzo, e se il ristrutturare la propria idea costa troppa energia, si preferisce l'illusione di aver fatto progressi parlando o sfogandosi, alleggerendo la tensione. Non è il parlare o lo sfogarsi la parte che ci aiuterà ad uscire dallo stallo, ma è l'affrontare la fatica per rielaborare il modello.

Quando non si è disposti a rivedere il proprio modello, si creano due fazioni, e si insiste a ribattere con le proprie motivazioni, impedendo che si arrivi a una conciliazione. Questo circolo vizioso ci spinge a mantenere convinzioni rigide e immutabili. Se si continua a perdere energie a alleviare il proprio sconforto tramite interazioni superficiali, si perde l'opportunità di provare nuove opzioni. La riluttanza a spendere energia nel cambiamento mantiene l'attività mentale inutile, poiché l'associazione azione-ricompensa (la soddisfazione del comprendere) viene meno. Solo se si interrompe la tendenza ad aggrapparsi al vecchio modello e si può incominciare a lavorare su una revisione del proprio modello di conoscenze in modo più completo.

### ♻️ Utilità se Consapevole
#osservatore #propositivo #trasparenza #mediazione

Una strada per l'evoluzione è acquisire onestà intellettuale, iniziando a lavorare attivamente per abbassare quel filtro che scarta le informazioni. Si può cominciare a valutare le opinioni altrui non per accettarle, ma per capire il motivo profondo per cui sono ritenute utili. È possibile, attraverso il dialogo e l'approfondimento, integrare nel proprio modello interpretativo i frammenti di verità che altrimenti sfuggirebbero. Questo esercizio, che sfrutta l'attrito per elaborare i concetti, permette di trasformare le critiche percepite in spunti di miglioramento qualitativo. Il modello di pensiero personale diventa più flessibile, non più rigido, e si riduce la necessità di difenderlo. Rielaborando e chiarendo i concetti, si rende il proprio modo di vedere le cose più oggettivo e coerente con il mondo reale. Questo permette di esprimere i concetti importanti in modo molto più semplice e libero da vincoli.