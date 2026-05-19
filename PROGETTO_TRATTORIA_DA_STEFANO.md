# 🍝 Trattoria Da Stefano — Stato Progetto
**Ai Partners Web** · Aggiornato: Maggio 2025

---

## 📍 Dati Cliente

| Campo | Valore |
|---|---|
| **Nome** | Trattoria Da Stefano |
| **Indirizzo** | Lo 04 An Thuong 29, Ngu Hanh Son, Da Nang, Vietnam |
| **Tel (chiamate VN)** | +84 336 069 894 |
| **WhatsApp (IT)** | +39 370 145 6206 |
| **Orari** | Tutti i giorni 10:30 – 22:30 |
| **Google Place ID** | `0x314217a1b3621ecb:0x80d5d98cd4a903e6` |
| **Google Review Link** | `https://search.google.com/local/writereview?placeid=0x314217a1b3621ecb:0x80d5d98cd4a903e6` |
| **Facebook** | https://www.facebook.com/people/Trattoriadastefanodanang/61587987500409/ |
| **TripAdvisor** | https://www.tripadvisor.com/Restaurant_Review-g298085-d34174590 |

---

## 🌐 Deploy & Dominio

| Campo | Valore |
|---|---|
| **Dominio** | `trattoriadastefano.com` (GoDaddy) |
| **Hosting** | Vercel |
| **URL Vercel** | `trattoria-stefano.vercel.app` |
| **DNS A record** | `76.76.21.21` |
| **DNS CNAME www** | `359d911eaab74045.vercel-dns-017.com` |
| **SSL** | Let's Encrypt (automatico Vercel) |

### File da aggiornare su Vercel
Solo `index.html` — le immagini in `img/` non cambiano.

---

## 📁 Struttura File

```
trattoria-da-stefano/
├── index.html          ← sito completo (125 KB)
├── sitemap.xml         ← multilingual, 4 URL
├── robots.txt          ← con Sitemap link
├── vercel.json         ← cache headers + redirect 301
└── img/
    ├── hero.jpg        (137 KB)
    ├── interior.jpg    (82 KB)
    ├── facade.jpg      (90 KB)
    ├── amatriciana.jpg (54 KB)
    ├── carbonara.jpg   (50 KB)
    ├── vongole.jpg     (39 KB)
    ├── pizza.jpg       (77 KB)
    └── qr_google_review.png
```

---

## 🏗️ Struttura Sito (sezioni in ordine)

1. **Nav** — logo tricolore 🇮🇹, 5 link, lang switcher dropdown, CTA "Book a Table"
2. **Hero** — fullscreen con `img/hero.jpg`, parallax, animazioni
3. **Trust Bar** — Google ⭐5.0, Open Daily, ~40 seats
4. **Menu** — 8 tab: Starters · Pasta · Mains · Pizza · Sides · Desserts · Wine · Cocktails
5. **Story** — narrativa Stefano romano
6. **About** — 6 card info (posti, orari, vini, eventi, asporto, zona)
7. **Gallery** — 5 foto reali
8. **Reviews** — 3 card Google + badge 5.0 + QR recensione
9. **Contact** — box WhatsApp + 4 shortcut rapidi + mappa Google Maps
10. **Footer** — logo tricolore, link rapidi, contatti
11. **Badge fluttuante** — WhatsApp fisso in basso a destra

---

## 🌍 Lingue

| Lingua | Codice | Auto-detect |
|---|---|---|
| English | `en` | Default + tutti gli altri |
| Tiếng Việt | `vi` | Browser `vi-*` |
| Русский | `ru` | Browser `ru-*` |
| 한국어 | `ko` | Browser `ko-*` |

- Rilevamento automatico da `navigator.language`
- Preferenza salvata in `localStorage` chiave `tds_lang`
- Menù: nome italiano sempre visibile + traduzione nella lingua selezionata sotto

---

## 🍽️ Menù Attuale (da foto maggio 2025)

### Starters
| Piatto | Prezzo |
|---|---|
| Bruschette Rustiche Miste | 89k |
| Tagliere Italiano di Salumi e Formaggi | 265k |
| Carpaccio di Manzo con Rucola e Parmigiano (Wagyu) | 185k |
| Caprese con Mozzarella | 179k |
| Parmigiana di Melanzane | 159k |
| Sauté di Cozze e Vongole | 199k |

### Pasta
| Piatto | Prezzo |
|---|---|
| Fettuccine al Burro e Parmiggiano ⭐ | 175k |
| Rigatoni Carbonara ⭐ | 215k |
| Rigatoni Amatriciana ⭐ | 205k |
| Lasagna Classica | 275k |
| Spaghetti alle Vongole | 195k |
| Spaghetti al Cartoccio di Mare | 265k |

### Mains
| Piatto | Prezzo |
|---|---|
| Involtini alla Romana | 245k |
| Trippa alla Romana | 245k |
| Pollo all'Arancia | 195k |
| Costolette di Agnello allo Scottadito ⭐ | 450k |
| Bistecca di Manzo alla Griglia | 490k |
| Baccalà alla Romana | 290k |

### Pizza
| Piatto | Prezzo |
|---|---|
| Focaccia | 129k |
| Margherita | 175k |
| Patate e Funghi ⭐ | 185k |
| Quattro Formaggi | 235k |
| Vegetariana | 205k |
| Mortadella Pistacchio e Brie ⭐ | 260k |
| Napoli | 195k |
| Capricciosa | 260k |
| Funghi e Prosciutto Crudo | 230k |
| Parma | 195k |

### Sides
| Piatto | Prezzo |
|---|---|
| Insalata Mista | 69k |
| Patate al Forno | 79k |
| Verdure Grigliate | 89k |
| Chips di Patate con Pecorino e Pepe | 99k |
| Fagiolini all'Agro | 79k |

### Desserts
| Piatto | Prezzo |
|---|---|
| Tiramisù Classico ⭐ | 109k |
| Pannacotta alla Fragola | 99k |
| Gelato Italiano | 89k |
| Bella Coppia & Limoncello ⭐ | 165k |

### Wine
**Red:** Terre Forti 480k · Il Pumo 590k · Modà 590k · Vanità 690k · Neprica 790k · Chianti 890k · Etna Rosso 1.150k · Barbera 1.190k · Amarone 1.980k

**White:** Terre Forti 480k · Trebì 550k · Vigneti Romio 590k · Luccarelli 610k · Orvieto 610k · Tormaresca 750k · Vitiano 750k · Pecorino 850k · Anthilia 990k

**Rosé:** Cerasuolo 570k · Remole Frescobaldi 670k

**Sparkling:** Novebolle 570k · Cavalieri Reali 590k · Tommasi Filodora 850k

### Cocktails
Negroni 149k · Aperol Spritz 149k · Campari Spritz 149k · Americano 139k · Gin & Tonic 99k · Espresso Martini 139k · Mojito 109k · Cuba Libre 99k

---

## 📈 SEO

- **Title:** `Italian Restaurant Da Nang Danang | Trattoria Da Stefano — Authentic Roman Cuisine`
- **Canonical:** `https://trattoriadastefano.com/`
- **hreflang:** en · vi · ru · ko · x-default
- **Keywords:** `Italian restaurant Da Nang`, `이탈리안 레스토랑 다낭`, `итальянский ресторан дананг`, `nhà hàng Ý Đà Nẵng`
- **Schema:** Restaurant + LocalBusiness + BreadcrumbList
- **aggregateRating:** 5.0 / 5 recensioni reali Google
- **sitemap.xml** e **robots.txt** inclusi

---

## 💬 WhatsApp Booking

- **Numero:** `+39 370 145 6206` (wa.me/393701456206)
- **Numero chiamate:** `+84 336 069 894`
- Tutti i CTA del sito aprono WhatsApp direttamente
- Messaggi pre-compilati in 4 lingue
- 4 shortcut rapidi: tavolo x2 · tavolo x4 · evento privato · asporto
- Badge fluttuante con animazione pulse

---

## ✅ Checklist post-deploy

- [ ] Google Search Console → aggiungi `trattoriadastefano.com` → invia sitemap
- [ ] Google Business Profile → aggiorna URL sito con `https://trattoriadastefano.com`
- [ ] Testa schema su `search.google.com/test/rich-results`
- [ ] Aggiorna canonical da Vercel a dominio quando attivo
- [ ] Verifica mappa Google Maps (Place ID reale inserito)

---

## 🔧 Tecnologia

- **HTML5** monopagina (no framework, no build step)
- **CSS vanilla** con variabili custom
- **JavaScript vanilla** (lang switcher, tab menu, scroll reveal, parallax)
- **Tailwind** usato nella versione artifact React (non nel file di produzione)
- **Font:** Abril Fatface · Lora · Be Vietnam Pro (Google Fonts)
- **Palette:** Rosso `#cc2200` · Oro `#f0b429` · Verde `#2e7d32` · Dark `#1c0800`
