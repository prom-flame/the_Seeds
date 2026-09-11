---
cssclasses:
  - abilità-spirito
  - abilità
sbilanciamento: sabotatore
categoria: abilità
stato: originale_v2
titolo: Sabotatore, Abilità
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
#sabotatore #ruminazione #depotenziante #vincoli

- **Il "Giudice" e la Collezione di Critiche**
	Questo sabotatore spesso definito il "giudice", si manifesta come una collezione persistente di critiche che rinfaccia fallimenti passati e compiti non completati, sedimentate durante la crescita ed il confronto con gli altri. Mina la motivazione a provare e toglie visibilità ai propri pregi o successi. È una critica costante ma poco specifica, priva di utilità reale per il miglioramento.

- **Procrastinazione e Perdita di Motivazione**
	Evidenziando unicamente gli aspetti negativi, l'effetto più dannoso è l'abbassamento dell'autostima, che disperde la volontà di agire o di migliorare. Si stratifica un senso di insicurezza e incertezza sulle proprie abilità, che causano e rafforzano la procrastinazione, ostacolando qualsiasi attività di cui non ci si sente all'altezza. Rendendo l'azione stessa difficile o fonte di ansia.

### 👁️ Influenza sull'Immagine di Se
#sabotatore #ruminazione #depotenziante #autocritica

Questo sabotatore affonda le sue radici in una stratificazione di ricordi negativi, di critiche interiorizzate nel corso del tempo. Una ruminazione generalizzata che assume la forma di una voce interiore giudicante e sempre scontenta, ha assorbito fallimenti passati ed aspettative deluse, trasformandole in una descrizione limitata e svilente di cosa crediamo di poter valere, accettandola senza metterla in discussione.

L'effetto dannoso e depotenziante di questo sabotatore è la sua capacità di agire come un filtro negativo omnicomprensivo, una mentalità negativa che impedisce di riconoscere gli aspetti positivi o i propri progressi, evidenziando solo i difetti e le difficoltà. Porta ad una demotivazione ad ampio spettro che soffoca la volontà di fare o di migliorare su attività pratiche per cui potremmo sentirci giudicati.

La mente, che naturalmente cerca riconoscimento, gratificazioni e conferme durante l'apprendimento, si blocca di fronte ad una costante negatività. Se ogni sforzo genera uno stimolo negativo auto-prodotto, anche in assenza di critiche esplicite questa sarà l'impressione più frequente che impoverirà qualsiasi esperienza, drenando lo slancio a fare o migliorare. A causa del sabotatore, l'individuo perde la capacità di auto-sostegno, di conseguenza l'asse dell'immagine di se si ribalta dal riconoscimento personale alla validazione sociale. 

Il valore dell'impegno personale e della gratificazione interna viene oscurato, spingendo l'individuo a cercare validazione esterna. La persona inizia a cercare riconoscimenti esterni e complimenti, spingendosi a creare traguardi o a sostenere carichi di lavoro, a volte inutili, principalmente per ottenere l'apprezzamento altrui e mantenere un'immagine di se e una reputazione di cui essere contento.  Questa dipendenza dal riscontro esterno cementa indirettamente l'insicurezza, poiché la stima di sé non è più generata internamente, ma diviene precaria e legata alle fluttuazioni delle opinioni altrui.

### ♻️ Utilità se Consapevole
#alleato_interiore #mediazione #oggettività #obiettività

Il sabotatore, percepito per abitudine come un giudice interiore, proprio tramite le voci e i ricordi del passato che utilizza per renderci consapevoli dell'immagine che abbiamo maturato di noi, ci regala spesso preziosi indizi sulle relazioni e i vincoli del passato non ancora risolti. 

È nostro compito diventare un interlocutore comprensivo e consapevole con questa voce del passato, e invece di subirne le critiche o prenderla sul personale, richiedere una qualità di informazione migliore, ricordando in modo esplicito che il passato non c'è più, è stato superato, e che adesso abbiamo intenzione di cambiare le cose.

L'obiettivo è trasformare questo eco interiore in un collaboratore interno, accettando le difficoltà vissute nel passato e chiedendo "alla nostra esperienza", quali siano i passi più efficienti e concreti, per fare in modo che nel nostro presente non si manifestino più perché non più necessarie. Usando la tendenza a notare i problemi, ma in una direzione propositiva, proponendo strategie per gestirli e risolverli, promuovendo un equilibrio in cui il pensiero critico diventa uno strumento di crescita e miglioramento pratico.