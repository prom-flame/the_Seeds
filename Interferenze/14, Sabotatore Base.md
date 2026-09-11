---
cssclasses:
  - scopo-base
  - base
sbilanciamento: sabotatore
categoria: base
stato: originale_v2
titolo: Sabotatore, Base
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
#sabotatore #insicurezza #depotenziante #vincoli

- **Paura dell'Ignoto e Rinuncia al Cambiamento**
	Esiste un timore profondo della perdita e la paura di rinunciare a qualcosa che diventa schiacciante e più spaventosa dalle opportunità che potrebbero arrivare mettendosi in gioco. È un meccanismo che rende incapaci di agire o di decidere, poiché qualsiasi cambiamento è percepito come un rischio e automaticamente scartato. Si tratta di una vera e propria paralisi decisionale e comportamentale, causata dalla paura di perdere qualcosa di importante.

- **Autolimite Acritico Ereditato e Stagnazione**
	Timori e preoccupazioni ereditate da figure di riferimento, vengono assimilate come regole di vita, assolute e incontestabili, un autolimite acritico sempre attivo. Questa paura primordiale induce una una paralisi decisionale generalizzata, in cui l'individuo per non perdere, non partecipa. Imprigionati dalla paura del cambiamento e trovando impossibile affrontare situazioni nuove o migliorare il proprio contesto, anche quando questo è insoddisfacente o doloroso.

### 👁️ Influenza sull'Immagine di Se
#sabotatore #insicurezza #depotenziante #autocritica

Questo sabotatore è una forma di insicurezza ereditata, originata probabilmente da eccessive preoccupazioni o da atteggiamenti apprensivi di un familiare o di una figura di riferimento. L'intenzione di proteggere o di prevenire potenziali rischi finisce per trasmettere un senso di urgenza e di pericolo, che viene assimilata inconsciamente. Da queste sensazioni emerge il desiderio di non mettere mai a rischio la propria "zona sicura". Questo non è un trauma, ma una regola interiore depotenziante, un freno che limita costantemente l'azione dell'individuo.

Questa costante insicurezza deriva dall'incapacità di accettare di perdere o abbandonare qualcosa, anche se superfluo o irrilevante. Non si tratta solo di un timore profondo legato alla perdita, ma una preoccupazione generalizzata che spinge a scartare ogni forma di rischio percepito, la "base sicura", intesa come la fonte di serenità e le sue risorse sono considerate intoccabili anche a noi stessi!

Questa paura paralizzante si traduce direttamente in una incapacità di agire o di cambiare, l'individuo si trova bloccato da ogni rischio di una possibile perdita, un perenne di scacco matto. Questa non è più una "base sicura" ne una zona di comfort, ma un limbo da cui non si percepisce via d'uscita. La base, che dovrebbe naturalmente espandersi, si restringe a causa di questa immobilità.

L'impatto si estende anche al concetto di scopo, perché questo richiede di investire energie per ottenere qualcosa di duraturo. La paura indotta da questo sabotatore, frena la motivazione impedendo qualsiasi investimento necessario. La serenità della base, che dovrebbe permettere di affrontare i problemi con calma, diventa la fonte stessa dalla percezione di minaccia.

### ♻️ Utilità se Consapevole
#alleato_interiore #mediazione #pragmatismo #indipendenza

Per mitigare consapevolmente questo sabotatore, è fondamentale riconoscere che le minacce non sono assolute e che i problemi possono essere suddivisi e "porzionati". Ciò significa che esporre all'incertezza piccole parti delle proprie risorse, accertandosi che queste siano facili da ottenere tramite l'impegno e una gestione responsabile può diventare accettabile.

Un approccio graduale permette di esplorare l'incertezza con più calma e con uno scopo chiaro, se quello a cui si rinuncia è riconosciuto come uno scambio necessario a fare esperienza, questa esperienza diventa un investimento. Si costruirà nel tempo una maggiore familiarità con queste dinamiche, riducendo il timore di affrontare l'ignoto.

Perché tramite la pratica si matura esperienza diretta e diventerà più facile riconoscere cosa sappiamo gestire senza problemi e come tutelare i nostri margini di sicurezza. Non si tratta di infrangere nessuna "regola assoluta", semplicemente ci saremo abituati a preparare un contesto sicuro e gestibile in cui la paura non è più necessaria.