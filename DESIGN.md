---
name: "Rajajoon"
description: "Hele ja jahedatooniline spordiobjektide kasutajaliides, mille läbiv 3 px sinine rajajoon väljendab liikumist ja teekonda."
colors:
  bg: "#F4F7F8"
  surface: "#FFFFFF"
  ink: "#173B57"
  accent: "#2878FF"
  support:
    accent_hover: "#1765E8"
    accent_active: "#0E50C7"
    accent_soft: "#E8F3FF"
    accent_light: "#A9D8FF"
    border: "#D8E0E5"
    muted: "#617485"
    disabled_bg: "#EDF1F3"
    disabled_text: "#8C9AA5"
    error: "#C53B45"
    error_soft: "#FFF0F1"
    success: "#187454"
    success_soft: "#EAF7F1"
    warning: "#8B5A10"
    warning_soft: "#FFF7E5"
typography:
  heading:
    family: "Manrope, Arial, sans-serif"
    weight: 600
    sizes: ["34px", "26px", "20px"]
    line_height: 1.2
  body:
    family: "Inter, Arial, sans-serif"
    weights: [400, 500, 600]
    sizes: ["20px", "18px", "16px", "14px"]
    line_height: 1.6
spacing:
  space_0: "0px"
  space_1: "4px"
  space_2: "8px"
  space_3: "12px"
  space_4: "16px"
  space_5: "20px"
  space_6: "24px"
  space_8: "32px"
  space_10: "40px"
  space_12: "48px"
  space_16: "64px"
rounded:
  small: "6px"
  medium: "10px"
  pill: "999px"
components:
  - "color-swatch"
  - "type-sample"
  - "primary-button"
  - "secondary-button"
  - "text-input"
  - "card"
  - "tag"
  - "navigation"
  - "notice"
  - "route-line"
dials:
  variance: "1 accent hue, 3 radii, 6 type sizes"
  density: "44px minimum control height, 352px input-column minimum, 16px base spacing, 32px desktop section padding, 16px mobile section padding"
  motion: "150ms ease; 0.01ms with prefers-reduced-motion"
---

# Overview

Rajajoon on Tallinna ja Harjumaa spordiobjektide jaoks loodud hele kasutajaliidese süsteem. Põhitaust on `#F4F7F8`, sisupinnad on `#FFFFFF` ja põhitekst on `#173B57`. Ainus põhitooni aktsent on `#2878FF`.

Süsteemi iseloomustav motiiv on üksik looklev sinine joon. Joone laius on `3px` (`0.1875rem`), otsad on ümardatud ning joon kuvatakse päises, `80px` kõrguses rajavöös ja sektsioonide juures. Dekoratiivsed SVG-jooned kasutavad `aria-hidden="true"`.

Kõik värvid, fondipered, kirjasuurused, vahed ja nurgaraadiused on määratud `:root` CSS-muutujatena.

# Colors

## Põhivärvid

| Token | Väärtus | Kasutus |
| --- | --- | --- |
| `--color-canvas` | `#F4F7F8` | Lehe põhitaust |
| `--color-surface` | `#FFFFFF` | Päis, sektsioonid, kaardid ja väljad |
| `--color-ink` | `#173B57` | Põhitekst ja tugevad detailid |
| `--color-primary` | `#2878FF` | Põhinupp, aktiivne olek, fookus ja rajajoon |
| `--color-primary-hover` | `#1765E8` | Põhinupu hõljutusolek |
| `--color-primary-active` | `#0E50C7` | Põhinupu aktiivne olek |
| `--color-primary-soft` | `#E8F3FF` | Hele aktsenttaust |
| `--color-accent-soft` | `#A9D8FF` | Teisese nupu aktiivne taust ja sildi piir |
| `--color-border` | `#D8E0E5` | Piirjooned |
| `--color-muted` | `#617485` | Abitekst ja metaandmed |

## Olekute tugivärvid

| Token | Väärtus | Kasutus |
| --- | --- | --- |
| `--color-disabled-bg` | `#EDF1F3` | Keelatud elemendi taust |
| `--color-disabled-text` | `#8C9AA5` | Keelatud elemendi tekst |
| `--color-error` | `#C53B45` | Viga |
| `--color-error-soft` | `#FFF0F1` | Vea taust |
| `--color-success` | `#187454` | Õnnestumine |
| `--color-success-soft` | `#EAF7F1` | Õnnestumise taust |
| `--color-warning` | `#8B5A10` | Hoiatus |
| `--color-warning-soft` | `#FFF7E5` | Hoiatuse taust |
| `--color-focus` | `#2878FF` | Fookuse piir |
| `--color-overlay` | `rgba(23, 59, 87, 0.08)` | Varju toon |

Fookuserõngas on `0 0 0 3px rgba(40, 120, 255, 0.24)`. Keelatud elementide läbipaistvus on `0.62`. Rajajoone põhiosa läbipaistvus on `0.9` ja sektsioonide õrna joone läbipaistvus `0.22`.

# Typography

Google Fontsist laaditakse `Manrope` kaaluga `600` ja `Inter` kaaludega `400`, `500` ja `600`. Varufont on mõlemal `Arial`, mille järel kasutatakse üldist `sans-serif` perekonda.

| Roll | Font | Kaal | Suurus | Reavahe |
| --- | --- | ---: | ---: | ---: |
| Lehe pealkiri / suur näidis | Manrope | 600 | `34px` | `1.2` |
| Sektsiooni pealkiri | Manrope | 600 | `26px` | `1.2` |
| Kaardi pealkiri | Manrope | 600 | `20px` | `1.2` |
| Juhttekst | Inter | 400 | `20px` | `1.6` |
| Põhitekst | Inter | 400 | `18px` | `1.6` |
| Väike tekst | Inter | 400 | `16px` | `1.6` |
| Silt ja metaandmed | Inter | 600 | `14px` | `1.6` |

Siltide tähevahe on `0.06em` ja tekst on suurtähtedes. Nuppude kaal on `600`; navigatsiooni ja kaardi detailteksti kaal on `500`.

# Layout

- Sisu maksimaalne laius on `1216px` (`76rem`).
- Lehe horisontaalne välimine vahe on üle `704px` vaates mõlemal küljel `24px`, vahemikus `385–704px` mõlemal küljel `16px` ja kuni `384px` vaates mõlemal küljel `12px`.
- Päise vertikaalne sisevahe on `32px`.
- Põhisisu ülemine vahe on `48px` ja alumine vahe `64px`.
- Sektsiooni sisevahe on üle `704px` vaates `32px`. Vahemikus `385–704px` on vertikaalne sisevahe `24px` ja horisontaalne sisevahe `16px`. Kuni `384px` vaates on horisontaalne sisevahe `12px`.
- Sektsioonide alumine vahe on `48px`.
- Paletivõrgu minimaalne veerulaius on `176px`; vahe on `16px`.
- Komponendivõrgu minimaalne veerulaius on `208px`; vahe on `24px`.
- Sisendväljade võrgu minimaalne veerulaius on `352px` (`22rem`); vahe on `24px`. `1216px` sisulaiuse juures mahub ühte ritta kuni kolm sisendvälja.
- Virnaelementide vahe on `12px`; olekunäite sisemine vahe on `8px`.
- Põhiline mobiili murdepunkt on `704px` (`44rem`) ja kitsa mobiili murdepunkt `384px` (`24rem`).
- Juhtelemendi minimaalne kõrgus on `44px`.
- Rajavöö kõrgus on `80px`.

Vahede skaala on `0`, `4`, `8`, `12`, `16`, `20`, `24`, `32`, `40`, `48` ja `64px`. Uusi vahesid ei lisata skaalaväliselt.

## Mobile setup

| Vaate laius | Välimine külgvahe | Sektsiooni sisevahe | Põhisisu vertikaalvahe | Võrgud |
| --- | ---: | ---: | ---: | --- |
| `705px` ja rohkem | `24px` | `32px` | `48px 64px` | Automaatne mitmeveeruline |
| `385–704px` | `16px` | `24px 16px` | `32px 48px` | Üks veerg |
| `320–384px` | `12px` | `24px 12px` | `32px 48px` | Üks veerg |

Kuni `704px` vaates rakenduvad järgmised reeglid:

- Päis muutub vertikaalseks, elementide vahe on `16px` ja vertikaalne sisevahe `24px`.
- Päise metateksti `max-width` piirang eemaldatakse.
- Rajavöö kõrgus väheneb `80px` → `64px`.
- Sektsioonide alumine vahe väheneb `48px` → `32px`.
- Paleti- ja komponendivõrgud kasutavad `minmax(0, 1fr)` üheveerulist paigutust.
- Komponendivõrgu vertikaalne vahe on `32px`.
- Navigatsioon muutub üheveeruliseks; iga link täidab `100%` laiuse ja joondub vasakule.
- Nupud täidavad `100%` laiuse, nende horisontaalne sisevahe on `16px` ja pikk tekst murdub mitmele reale.
- Kaardi pealkiri, kaardi tekst, teate pealkiri, teate tekst, abi- ja veatekst kasutavad `overflow-wrap: anywhere`.
- Väli, virn, olekunäide, kaart ja teade kasutavad `min-width: 0`, et sisu ei suruks võrku vaateaknast välja.
- Sisend kasutab `min-width: 0`; selle `18px` kirjasuurus väldib iOS-is fookustamisel automaatset suumimist.
- Nupud ja lingid kasutavad `touch-action: manipulation`.
- Nupu, sisendi ja navigatsioonilingi minimaalne kõrgus on `44px`.
- Silt on `28px` kõrge ainult mitteinteraktiivse märgisena. Interaktiivse filtri puhul tuleb silt paigutada vähemalt `44px` kõrguse vajutatava ala sisse.

Kuni `384px` vaates väheneb lehe külgvahe `12px`-ni, sektsiooni horisontaalne sisevahe `12px`-ni ja teate horisontaalne sisevahe `16px`-ni. Kirjasuurusi ei vähendata.

Kontrolli paigutust täpselt laiustel `320px`, `360px`, `390px`, `412px`, `704px` ja `705px`. Ühelgi neist laiustest ei tohi tekkida horisontaalset kerimist, lõigatud teksti ega alla `44px` vajutatavat nuppu, sisendit või navigatsioonilinki.

# Elevation & Depth

- Tavaline piirjoon on `1px solid #D8E0E5`.
- Tugev piirjoon on `2px`.
- Rajajoon ja teate vasak piir on `3px`.
- Kaardi hõljutusvari on `0 10px 30px rgba(23, 59, 87, 0.08)`.
- Valitud kaardil on `3px` sisemine vasak vari värviga `#2878FF`.
- Fookuserõngas on `0 0 0 3px rgba(40, 120, 255, 0.24)`.
- Taustade hierarhia on `#F4F7F8` → `#FFFFFF` → olekupõhised heledad taustad.

Varju kasutatakse ainult kaardi hõljutusolekus. Nupud, sisendid, sildid, navigatsioon ja teated eristuvad piirjoone või taustavärviga.

# Shapes

- Väike raadius on `6px`; seda kasutavad navigatsioonilingid.
- Põhiraadius on `10px`; seda kasutavad sektsioonid, nupud, väljad, kaardid, navigatsioon ja teated.
- Sildi raadius on `999px`.
- Rajajoonel on `3px` joon, `round` jooneotsad ja täiteta SVG-rada.
- Sektsiooni vasak aktsent on `3px × 40px`.
- Sektsiooni parempoolne kõver on `128px × 32px`, `3px` ülemise piiriga, `50%` raadiusega, `-6deg` pöördega ja `0.22` läbipaistvusega.
- Värvinäidise minimaalne kõrgus on `128px`; värvipinna kõrgus on `72px`.
- Kaardi minimaalne kõrgus on `160px`.

# Components

## Buttons

Nupu minimaalne kõrgus on `44px`, sisevahe `12px 20px`, piir `1px` ja raadius `10px`.

- Primary default: taust `#2878FF`, tekst `#FFFFFF`.
- Primary hover: taust `#1765E8`.
- Primary active: taust `#0E50C7`, vertikaalne nihe `1px`.
- Secondary default: taust `#FFFFFF`, tekst ja piir `#2878FF`.
- Secondary hover: taust `#E8F3FF`.
- Secondary active: taust `#A9D8FF`, tekst `#173B57`, vertikaalne nihe `1px`.
- Focus: `3px` fookuserõngas.
- Disabled: taust `#EDF1F3`, tekst `#8C9AA5`, piir `#D8E0E5`, läbipaistvus `0.62`.

## Text input

Sisendi minimaalne kõrgus on `44px`, sisevahe `12px 16px`, piir `1px` ja raadius `10px`. Töölaual on sisendvõrgu veeru minimaalne laius `352px`; kuni `704px` vaates täidab sisendväli üheveerulise konteineri kogu laiuse.

- Default: pind `#FFFFFF`, piir `#D8E0E5`.
- Hover: piir `#617485`.
- Focus: piir `#2878FF` ja `3px` fookuserõngas.
- Error: piir `#C53B45`, taust `#FFF0F1`.
- Disabled: taust `#EDF1F3`, tekst `#8C9AA5`.
- Abi- ja veateksti suurus on `14px`.

## Card

Kaardi minimaalne kõrgus on `160px`, sisevahe `20px`, piir `1px` ja raadius `10px`.

- Hover: piir `#2878FF` ja vari `0 10px 30px rgba(23, 59, 87, 0.08)`.
- Selected: piir `#2878FF` ja vasakul `3px` sisemine aktsent.
- Disabled: taust `#EDF1F3`, tekst `#8C9AA5`, läbipaistvus `0.62`.

## Tag

Sildi minimaalne kõrgus on `28px`, sisevahe `4px 12px`, piir `1px`, raadius `999px`, teksti suurus `14px` ja kaal `600`.

- Default: taust `#E8F3FF`, piir `#A9D8FF`, tekst `#173B57`.
- Hover: taust `#A9D8FF`.
- Selected: taust ja piir `#2878FF`, tekst `#FFFFFF`.
- Error: taust `#FFF0F1`, piir ja tekst `#C53B45`.
- Disabled: taust `#EDF1F3`, piir `#D8E0E5`, tekst `#8C9AA5`, läbipaistvus `0.62`.

## Navigation

Navigatsiooni välimine sisevahe ja elementide vahe on `8px`; taust `#F4F7F8`, piir `1px`, raadius `10px`. Lingi minimaalne kõrgus on `44px`, sisevahe `8px 16px`, raadius `6px`, teksti suurus `16px` ja kaal `500`.

- Hover: tekst `#2878FF`, taust `#FFFFFF`.
- Focus: `3px` fookuserõngas.
- Active: taust `#2878FF`, tekst `#FFFFFF`.
- Disabled: tekst `#8C9AA5`, läbipaistvus `0.62`.

## Notice

Teate sisevahe on `16px 20px`, üldpiir `1px`, vasak piir `3px` ja raadius `10px`. Pealkiri ja tekst on `16px`.

- Info: taust `#E8F3FF`, piir `#2878FF`.
- Success: taust `#EAF7F1`, piir ja tekst `#187454`.
- Warning: taust `#FFF7E5`, piir ja tekst `#8B5A10`.
- Error: taust `#FFF0F1`, piir ja tekst `#C53B45`.
- Disabled: taust `#EDF1F3`, piir `#D8E0E5`, tekst `#8C9AA5`, läbipaistvus `0.62`.

# Do's and Don'ts

## Do

- Kasuta lehe taustaks `#F4F7F8` ja sisupindadeks `#FFFFFF`.
- Kasuta põhitekstiks `#173B57` ja interaktiivseks aktsendiks `#2878FF`.
- Kasuta pealkirjades `Manrope 600` ning muus tekstis `Inter 400`, `500` või `600`.
- Hoia kirjasuurused skaalal `14`, `16`, `18`, `20`, `26` ja `34px`.
- Hoia vahed skaalal `0`, `4`, `8`, `12`, `16`, `20`, `24`, `32`, `40`, `48` ja `64px`.
- Kasuta komponentidel `10px` põhiraadiust ja navigatsioonilinkidel `6px` raadiust.
- Näita klaviatuurifookust `3px` sinise fookuserõngaga.
- Kasuta liikumiseks `150ms ease` üleminekut ja vähenda see `0.01ms`-ni, kui kasutaja eelistab vähendatud liikumist.
- Hoia rajamotiiv ühe `3px` paksuse lookleva sinise joonena.
- Testi iga muudatust laiustel `320`, `360`, `390`, `412`, `704` ja `705px`.
- Lase pikkadel nupu- ja kaarditekstidel murduda; hoia nende konteineritel `min-width: 0`.
- Hoia kõik interaktiivsed nupud, sisendid ja navigatsioonilingid vähemalt `44px` kõrged.

## Don't

- Ära lisa uusi aktsentvärve väljaspool dokumenteeritud HEX- ja RGBA-väärtusi.
- Ära kasuta suuremat pealkirja kui `34px`.
- Ära kasuta väiksemat põhiteksti kui `18px` ega väiksemat silti kui `14px`.
- Ära lisa skaalaväliseid vahesid ega nurgaraadiusi.
- Ära lisa rohkem kui ühte paralleelset rajajoont, rattamärke, rulluisuillustratsiooni ega ikoone.
- Ära kasuta varju mujal kui kaardi hõljutusolekus.
- Ära eemalda fookuserõngast ilma samaväärse `3px` nähtava asenduseta.
- Ära kasuta keelatud olekus aktiivse oleku sinist tausta ega täisläbipaistmatust.
- Ära kasuta mobiilis fikseeritud komponendilaiust, mis ületab konteineri laiuse.
- Ära vähenda mobiilis teksti alla dokumenteeritud `14px` miinimumi.
- Ära looda tegevuse selgitamisel ainult hõljutusolekule; puutevaates peab tegevus olema arusaadav ilma hover'ita.
