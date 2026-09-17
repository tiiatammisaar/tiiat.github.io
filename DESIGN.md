# Rajajoon — disainisüsteem

## 1. Eesmärk

See dokument kirjeldab veebilehe **„Treeningpaigad rullitajatele”** visuaalset keelt ja kasutajaliidese reegleid. Leht aitab leida rulluisutajatele sobivaid treeningpaiku Tallinnas ja Harjumaal: spordisaale, võimlaid, jõusaale, aeroobikasaale, välialasid ja muid toetavaid treeningukohti.

Disain peab mõjuma:

- õhulise, aktiivse ja usaldusväärsena;
- sportliku, kuid mitte agressiivse ega võistlusliku kujundusena;
- selge ja inimliku veebilehena, mitte geneerilise AI-mallina;
- fotokesksena, sest päris treeningpaigad ja nende kasutuskontekst on sisu kõige olulisem osa.

Kujunduse läbiv identiteedielement on vabalt kulgev **sinine rajajoon**, mis meenutab uisutaja liikumisteekonda.

## 2. Disaini põhimõtted

### 2.1 Sisu enne dekoratsiooni

Fotod, objekti nimi, asukoht, tüüp ja praktilised omadused peavad olema kiiresti loetavad. Dekoratiivne rajajoon ei tohi läbida teksti, nuppe, filtrite nimetusi ega muid interaktiivseid elemente.

### 2.2 Päris ja usaldusväärne

Kasuta eelistatult päris spordiobjektide kvaliteetseid fotosid. Väldi ühtlaseid AI-illustratsioone, liigset klaasiefekti, neoonhelendust, suuri värvilisi gradiente ja ebavajalikke 3D-elemente.

### 2.3 Selge hierarhia

Ühel vaatel peab olema üks selge põhifookus. Pealkirjad on kompaktsed ja tugevad, kirjeldav tekst rahulik ning tegevused lihtsalt eristatavad.

### 2.4 Mõõdukas pehmus

Nurgad on kergelt ümardatud, kuid mitte ümarate „mullide” kujul. Suured pinnad on valged, lehe taust väga hele hallikassinine ning varje kasutatakse tagasihoidlikult.

### 2.5 Liikumise tunne

Rajajoon, fotod ja väikesed hõljutusanimatsioonid annavad lehele liikumise. Animatsioonid peavad olema lühikesed ja rahulikud ning arvestama kasutaja `prefers-reduced-motion` seadistust.

## 3. Brändielemendid

### 3.1 Sinine rajajoon

Rajajoon on orgaaniline, vabakäeline ja pehmelt kaarduv. See võib ilmuda:

- päises;
- hero-foto kohal;
- helesinises vahevöös;
- sektsiooni väikese dekoratiivse detailina.

Reeglid:

- joone põhipaksus on `0.1875rem` ehk ligikaudu 3 px;
- hero-alal võib joon olla veidi paksem, ligikaudu `0.32rem`;
- joone otsad on ümarad (`stroke-linecap: round`);
- joon ei tohi varjata sisu ega vähendada teksti kontrasti;
- joone vasak osa kasutab põhisinist `#2878FF`;
- paremal, uisutaja poole liikudes, muutub joon väga heledaks, peaaegu valgeks;
- hajumine peab olema sujuv, mitte järsu värviastmega;
- heledal ühevärvilisel taustal võib kasutada ka põhisinist joont väiksema läbipaistvusega.

Soovituslik SVG-gradient:

```html
<linearGradient id="route-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
  <stop offset="0%" stop-color="#2878FF" />
  <stop offset="58%" stop-color="#A9D8FF" />
  <stop offset="100%" stop-color="#F7FCFF" />
</linearGradient>
```

### 3.2 Fotograafia

Fotod peavad olema heledad, loomulikud ja piisavalt kvaliteetsed. Eelistada vaateid, mis näitavad ruumi tegelikku kasutusvõimalust, põrandat ja mõõtkava.

Hero-foto puhul:

- tekst jääb vasakule heledale ja kontrastsele alale;
- uisutaja jääb paremale;
- pildi kadreering peab näitama nii kleiti kui ka uiske;
- ära kasuta kärbet, mis lõikab ära jalad, uisud või olulise kehaosa;
- vali `background-position` iga foto järgi, mitte ära eelda alati täpset keskpunkti;
- kui `cover` kärbib sportlase ära, kasuta sobivamat paigutust, näiteks eraldi `<img>` elementi koos `object-fit: contain`, või suuremat hero-ala;
- teksti loetavuse jaoks kasuta vasakult valget läbipaistvat kihti, mis hajub foto poole.

Objektikaartide fotod kasutavad `object-fit: cover`, sest neis on oluline ühtlane kaardirütm. Pildi soovituslik kuvasuhe on ligikaudu 16 : 9.

## 4. Disainitokenid

### 4.1 Värvid

| Token | Väärtus | Kasutus |
|---|---:|---|
| `--color-ink` | `#173B57` | põhitekst, pealkirjad ja tumedad ikoonid |
| `--color-primary` | `#2878FF` | põhitegevused, valitud olekud ja rajajoon |
| `--color-primary-hover` | `#1765E8` | põhinupu hover |
| `--color-primary-active` | `#0E50C7` | aktiivne olek ja tugevam sinine tekst |
| `--color-primary-soft` | `#E8F3FF` | filtrid, infosõnumid ja pehmed taustad |
| `--color-accent-soft` | `#A9D8FF` | helesinine aktsent ja sekundaarse nupu aktiivne olek |
| `--color-canvas` | `#F4F7F8` | lehe üldtaust |
| `--color-surface` | `#FFFFFF` | kaardid, sektsioonid ja muud pinnad |
| `--color-border` | `#D8E0E5` | neutraalsed piirjooned |
| `--color-muted` | `#617485` | abitekst ja teisene info |
| `--color-disabled-bg` | `#EDF1F3` | keelatud elemendi taust |
| `--color-disabled-text` | `#8C9AA5` | keelatud elemendi tekst |
| `--color-error` | `#C53B45` | vead |
| `--color-error-soft` | `#FFF0F1` | vea taust |
| `--color-success` | `#187454` | õnnestumine |
| `--color-success-soft` | `#EAF7F1` | õnnestumise taust |
| `--color-warning` | `#8B5A10` | hoiatus |
| `--color-warning-soft` | `#FFF7E5` | hoiatuse taust |

Kaardi lisavärvid:

- vesi: `#CFEAFF`;
- maa: `#E9F4E8`;
- kaardi põhitaust: `#DFF1E6`;
- teed: valge.

### 4.2 Tüpograafia

Pealkirjad kasutavad **Manrope** kirjatüüpi kaaluga 600. Sisu ja kasutajaliidese tekst kasutab **Inter** kirjatüüpi kaaludega 400, 500 või 600.

Varufondid: `Arial, sans-serif`.

| Tase | Suurus | Reavahe | Kaal | Kasutus |
|---|---:|---:|---:|---|
| XS | `0.875rem` / 14 px | 1.6 | 400–600 | sildid, abitekst, metaandmed |
| SM | `1rem` / 16 px | 1.6 | 400–600 | väike sisutekst, nupud, väljade sildid |
| MD | `1.125rem` / 18 px | 1.6 | 400–600 | põhitekst ja kaardi pealkiri |
| LG | `1.25rem` / 20 px | 1.2–1.6 | 400–600 | juhtlõik ja H3 |
| XL | `1.625rem` / 26 px | 1.2 | 600 | H2 |
| 2XL | `2.125rem` / 34 px | 1.2 | 600 | H1 ja suur pealkiri |
| Hero | `clamp(2rem, 4vw, 3.5rem)` | 1.2 | 600 | avalehe põhisõnum |

Suurtähelised abipealkirjad kasutavad `0.06em` tähevahet. Ära kasuta suurtähtedes pikki tekstilõike.

### 4.3 Vahed

Alussamm on 4 px.

| Token | Väärtus |
|---|---:|
| `--space-0` | 0 |
| `--space-1` | 4 px |
| `--space-2` | 8 px |
| `--space-3` | 12 px |
| `--space-4` | 16 px |
| `--space-5` | 20 px |
| `--space-6` | 24 px |
| `--space-8` | 32 px |
| `--space-10` | 40 px |
| `--space-12` | 48 px |
| `--space-16` | 64 px |

Kasuta ainult seda skaalat, välja arvatud väga väikesed märgiste sisemised vahed.

### 4.4 Nurgad, piirjooned ja varjud

| Token | Väärtus | Kasutus |
|---|---:|---|
| `--radius-sm` | 6 px | väiksed pinnad, navigeerimise lingid |
| `--radius-md` | 10 px | nupud, väljad, kaardid ja sektsioonid |
| `--radius-pill` | 999 px | filtrid ja sildid |
| `--border-thin` | 1 px | tavaääris |
| `--border-strong` | 2 px | tugev rõhutus vajadusel |
| `--shadow-card` | `0 10px 30px rgba(23,59,87,.08)` | hover ja esiletõstetud kaart |
| `--shadow-float` | `0 16px 40px rgba(23,59,87,.14)` | ainult selgelt hõljuv element |

Varje ei kasutata igal pinnal. Vaikimisi eraldavad pindu taust ja 1 px piirjoon.

### 4.5 Mõõdud ja liikumine

- sisu maksimaalne laius: `76rem` ehk 1216 px;
- juhtnupu või sisendvälja minimaalne kõrgus: `2.75rem` ehk 44 px;
- tavapärane üleminek: `150ms ease`;
- klaviatuurifookus: `0 0 0 3px rgba(40,120,255,.24)`;
- keelatud elemendi läbipaistvus: `0.62`;
- dekoratiivse vahevöö kõrgus: `5rem`.

## 5. Lehe struktuur

Soovituslik avalehe järjekord:

1. päis ja lehe nimi;
2. hero-foto, pealkiri ja lühike väärtuspakkumine;
3. treeningpaiga tüübi kiirfiltrid;
4. objektikaardid;
5. sama valikut kajastav kaardivaade;
6. täiendavad otsingu- ja filtreerimisvõimalused;
7. andmeallikas ja uuendamise kuupäev.

Lauavaates paiknevad objektikaardid ja asukohakaart kõrvuti suhtes ligikaudu 2 : 1. Kaartide ruudustikus võib olla kolm tulpa. Mobiilis muutub kogu sisu üheveeruliseks ja kaart paigutub tulemuste järele.

## 6. Komponendid

### 6.1 Nupud

Kõigi nuppude minimaalne kõrgus on 44 px, nurk 10 px ja tekst poolpaks.

**Põhinupp**

- vaikimisi: sinine taust ja valge tekst;
- hover: `#1765E8`;
- active: `#0E50C7` ja 1 px allapoole liikumine;
- focus: nähtav sinine fookusrõngas;
- disabled: helehall taust, hall tekst, `not-allowed` kursor.

**Teisene nupp**

- vaikimisi: valge taust, sinine tekst ja sinine piirjoon;
- hover: `#E8F3FF` taust;
- active: `#A9D8FF` taust ja tumesinine tekst;
- focus ja disabled järgivad põhinupu reegleid.

### 6.2 Kiirfiltrid

Kiirfilter on pillikujuline nupp, milles on alati ikoon ja tekst. Minimaalne kõrgus on 44 px.

- vaikimisi: tumesinine tekst ja helesinine taust;
- hover: sinine piirjoon;
- valitud: sinine taust ja valge sisu;
- ikoon peab kasutama `currentColor`, et olekud töötaksid automaatselt;
- ära kasuta ainult ikooni ilma nähtava tekstisildita.

### 6.3 Sisendväljad

Väli koosneb nähtavast sildist, sisendist ja vajadusel abi- või veatekstist.

- minimaalne kõrgus: 44 px;
- taust: valge;
- piirjoon: `#D8E0E5`;
- hover: piirjoon muutub tumedamaks;
- focus: sinine piirjoon ja fookusrõngas;
- error: punane piirjoon, väga hele punane taust ja selgitav veatekst;
- disabled: helehall taust ja hall tekst.

Placeholder ei asenda välja silti.

### 6.4 Objektikaardid

Objektikaart on tervikuna klikitav ja sisaldab:

1. päris fotot;
2. objekti tüüpi ja piirkonda;
3. objekti nime;
4. aadressi;
5. vajadusel pindala, põrandamaterjali ja muid olulisi omadusi.

Vaikimisi kasutatakse valget tausta, 1 px halli piirjoont ja 10 px nurki. Hover-olekus muutub piirjoon siniseks, lisandub õrn vari ja kaart liigub 2 px üles. Valitud kaart saab sinise piirjoone või vasakpoolse sinise rõhujoone. Keelatud kaart on hall ja väiksema läbipaistvusega.

Pikkadel nimedel peab olema lubatud murduda mitmele reale. Nime täpsust ei tohi visuaalse mugavuse nimel kärpida.

### 6.5 Sildid

Sildid on kompaktsed pillid, mida kasutatakse piirkonna, objekti tüübi, põrandamaterjali või andmeoleku näitamiseks.

- tekst: 14 px, kaal 600;
- minimaalne kõrgus: 28 px;
- vaikimisi: hele sinine taust ja helesinine piirjoon;
- valitud: põhisinine taust ja valge tekst;
- viga: punane tekst, helepunane taust ja punane piirjoon;
- disabled: hall.

### 6.6 Navigatsioon

Navigatsioon kasutab rahulikku heledat tausta ja ümardatud sisemisi linke.

- hover: valge taust ja sinine tekst;
- aktiivne leht: sinine taust ja valge tekst;
- focus: nähtav fookusrõngas;
- keelatud link eemaldatakse tab-järjekorrast ja märgitakse `aria-disabled="true"`.

### 6.7 Teated

Teatel on 3 px vasak rõhujoon, 10 px nurgad, tugev lühike pealkiri ja selgitav tekst.

- info: sinine;
- success: roheline;
- warning: pruunikas-kollane;
- error: punane ja vajadusel `role="alert"`;
- disabled: hall.

### 6.8 Kaardivaade

Kaardivaade peab vastama samale aktiivsele filtrile ja valikule nagu objektikaardid. Markerid kasutavad põhisinist, valget äärist ja piisavat suurust. Kaardil peab olema ligipääsetav tekstiline nimetus või alternatiivne kirjeldus.

## 7. Responsiivsus

### Kuni 44rem / 704 px

- lehe külgmine vahe: 16 px;
- päise elemendid lähevad üksteise alla;
- sektsiooni sisuvahe väheneb 24 × 16 px-ni;
- kõik peamised ruudustikud muutuvad üheveeruliseks;
- kiirfiltrid paiknevad kahe tulbana ja lähevad väga kitsal ekraanil ühte tulpa;
- objektikaardi foto kõrgus on ligikaudu 12rem;
- nupud täidavad rea laiuse;
- navigatsioon muutub üheveeruliseks;
- hero pealkiri kasutab `clamp(1.8rem, 9vw, 2.7rem)`;
- hero kadreeringut kontrollitakse eraldi, et uisud ei kaoks ekraanilt.

### Kuni 24rem / 384 px

- lehe külgmine vahe: 12 px;
- sektsiooni horisontaalne sisuvahe: 12 px;
- filtrid lähevad ühte tulpa;
- hero minimaalne kõrgus on 18rem ainult siis, kui sportlane jääb tervikuna nähtavaks; vajadusel suurenda kõrgust;
- objektikaardi foto kõrgus on ligikaudu 10rem.

## 8. Ligipääsetavus

- Kõik tegevused peavad töötama klaviatuuriga.
- Kasuta `:focus-visible` olekut; ära eemalda fookust ilma asenduseta.
- Interaktiivse elemendi puuteala peab olema vähemalt 44 × 44 px.
- Ikoonidel on nähtav tekstisilt; dekoratiivsed SVG-d saavad `aria-hidden="true"`.
- Sisendväljal on alati programmiline ja nähtav silt.
- Veateade seotakse väljaga `aria-describedby` abil ning vigane väli saab `aria-invalid="true"`.
- Aktiivne navigatsioonilink kasutab `aria-current="page"`.
- Kaart peab saama tekstilise alternatiivi.
- Teksti ei asetata otse kirjule fotoalale ilma piisava kontrastkihita.
- Animatsioonid ja üleminekud lülitatakse `prefers-reduced-motion: reduce` puhul sisuliselt välja.
- Värv ei tohi olla ainus oleku või vea edasiandmise viis.

## 9. Sisureeglid

- Kasuta objektide ametlikke ja täpseid nimesid.
- Objektikaardi pealkiri peab viitama konkreetsele saalile või sportimispaigale, mitte ainult hoonele, kui andmed seda võimaldavad.
- Asukoht esitatakse ühtses järjekorras: tänav, asula või linnaosa, omavalitsus.
- Näita andmeallikat ja andmete kuupäeva.
- Kasuta lihtsat eesti keelt ning lühikesi tegevussõnu: „Vaata”, „Ava”, „Otsi”, „Vali”.
- Väldi turunduslikku liialdamist ja ebamääraseid väiteid.

## 10. Mida vältida

- liigsed sinakas-lillad gradiendid;
- suured helendavad varjud ja neoon;
- klaasjad läbipaistvad kaardid;
- igal sektsioonil eri värvi taust;
- juhuslikud dekoratiivsed ikoonid;
- liiga suured pillikujulised konteinerid;
- ümarad nurgad kõikjal ja ilma hierarhiata;
- kaartide ülemäärane hõljumine;
- fotode agressiivne tumendamine või värvimine;
- hero-foto kärpimine viisil, mis lõikab uisutaja kleidi või uisud ära;
- sinise rajajoone paigutamine teksti või nupu peale;
- automaatselt genereeritud välimusega abstraktsed taustakujundid.

## 11. Rakendusreeglid AI-agentidele ja arendajatele

Uue vaate või komponendi loomisel:

1. kasuta olemasolevaid tokeneid, ära lisa peaaegu samasugust uut sinist või vahet;
2. eelista semantilist HTML-i (`header`, `main`, `nav`, `section`, `article`, `aside`);
3. rakenda kõigile interaktiivsetele komponentidele vähemalt vaikimisi, hover-, focus-, active- ja disabled-olek, kui need on asjakohased;
4. kontrolli tulemust vähemalt laiustel 1440 px, 768 px, 390 px ja 320 px;
5. testi pikki eestikeelseid objekti- ja aadressinimesid;
6. ära paiguta olulist sisu ainult fotole või kaardile;
7. säilita maksimaalne sisulaius 1216 px ja 4 px vahede alusvõrk;
8. kasuta rajajoont säästlikult — üks tugev visuaalne joon vaate kohta on tavaliselt piisav;
9. hero-foto puhul kontrolli alati visuaalselt, et uisutaja kleit ja uisud oleksid nähtavad;
10. rajajoone parempoolne osa peab uisutaja juures olema väga hele ja õrn.

## 12. CSS-i lähteplokk

```css
:root {
  --font-heading: "Manrope", "Arial", sans-serif;
  --font-body: "Inter", "Arial", sans-serif;

  --text-xs: 0.875rem;
  --text-sm: 1rem;
  --text-md: 1.125rem;
  --text-lg: 1.25rem;
  --text-xl: 1.625rem;
  --text-2xl: 2.125rem;
  --line-tight: 1.2;
  --line-normal: 1.6;

  --color-ink: #173B57;
  --color-primary: #2878FF;
  --color-primary-hover: #1765E8;
  --color-primary-active: #0E50C7;
  --color-primary-soft: #E8F3FF;
  --color-accent-soft: #A9D8FF;
  --color-canvas: #F4F7F8;
  --color-surface: #FFFFFF;
  --color-border: #D8E0E5;
  --color-muted: #617485;
  --color-error: #C53B45;
  --color-success: #187454;
  --color-warning: #8B5A10;

  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.25rem;
  --space-6: 1.5rem;
  --space-8: 2rem;
  --space-10: 2.5rem;
  --space-12: 3rem;
  --space-16: 4rem;

  --radius-sm: 0.375rem;
  --radius-md: 0.625rem;
  --radius-pill: 999px;
  --control-height: 2.75rem;
  --content-width: 76rem;
  --focus-ring: 0 0 0 0.1875rem rgba(40, 120, 255, 0.24);
  --shadow-card: 0 0.625rem 1.875rem rgba(23, 59, 87, 0.08);
  --transition-fast: 150ms ease;
}
```

---

Lähtefail: `stardikomplekt(1).html`. Dokument kajastab lähtefaili disainisüsteemi ning hilisemaid täpsustusi hero-foto kadreeringu ja paremale väga heledaks hajuva rajajoone kohta.
