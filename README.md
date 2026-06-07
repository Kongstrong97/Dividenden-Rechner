# 📈 Dividenden- & Zinseszins-Rechner

Eine fertige, in sich geschlossene Web-App (Single-File-HTML), mit der du **passiv Geld verdienen** kannst – über Werbung (Google AdSense) und Broker-Affiliate-Links.

Die App selbst ist **fertig**. Was jetzt noch fehlt, ist das Veröffentlichen und Geldverdienen-Scharfschalten. Diese Anleitung führt dich Schritt für Schritt durch alles.

---

## 🎯 Das Konzept in einem Satz

> Ein kostenloser Finanz-Rechner zieht über Google dauerhaft Besucher an, die nach „dividenden rechner", „zinseszins rechner" usw. suchen. Diese Besucher verdienen dir Geld über (1) Werbeanzeigen und (2) Provisionen, wenn sie über deine Links ein Depot eröffnen.

**Warum das funktioniert:**
- 🔍 **Immergrüner Suchverkehr** – Finanz-Rechner werden jeden Monat tausendfach gesucht, das Jahr über.
- 💶 **Finanz = hohe Werbeerlöse** – die Finanznische hat mit die höchsten Klickpreise (CPC/CPM) bei AdSense.
- 🤝 **Lukrative Affiliate-Programme** – Broker zahlen oft **20–100 €+ pro eröffnetem Depot**.
- 🛠️ **Null Wartung** – statische Datei, kein Server, keine Datenbank, keine laufenden Kosten.

**Ehrliche Erwartung:** Das ist *passiv*, aber **nicht sofort**. Geld kommt erst mit Besuchern, und Besucher kommen über SEO (Wochen bis Monate) oder Promotion. Es ist ein Vermögenswert, der mit der Zeit wächst – kein Schalter, der sofort Geld druckt.

---

## 📁 Was ist enthalten

| Datei | Zweck |
|---|---|
| `index.html` | Die komplette App (3 Rechner, Charts, Steuer, Design) – **eine Datei, keine Abhängigkeiten** |
| `impressum.html` | Impressum-Vorlage (in DE Pflicht) – **musst du ausfüllen** |
| `datenschutz.html` | Datenschutz-Vorlage – **musst du anpassen** |
| `robots.txt` | Sagt Google, dass alles indexiert werden darf |
| `sitemap.xml` | Hilft Google beim Finden der Seite |
| `README.md` | Diese Anleitung |

---

## 🚀 Schritt 1: Lokal ansehen

Doppelklick auf `index.html` – öffnet sich im Browser. Fertig. Du brauchst nichts zu installieren.

---

## 🌐 Schritt 2: Veröffentlichen (kostenlos)

Du brauchst **kostenloses Hosting**. Drei Optionen, von einfach nach „richtig":

### Option A – Netlify Drop (am einfachsten, 2 Minuten)
1. Gehe auf **https://app.netlify.com/drop**
2. Ziehe den **gesamten Ordner** `dividenden-rechner` ins Browserfenster.
3. Fertig – du bekommst sofort eine Live-URL wie `https://zufallsname.netlify.app`.
4. (Optional) Im Netlify-Dashboard kannst du den Namen ändern oder eine eigene Domain verbinden.

### Option B – Cloudflare Pages / Vercel
Ähnlich wie Netlify, ebenfalls kostenlos. Ordner hochladen oder mit GitHub verbinden.

### Option C – GitHub Pages (gut für Updates)
1. Erstelle ein GitHub-Repo, lade die Dateien hoch.
2. Settings → Pages → Branch `main`, Ordner `/root` → Save.
3. Seite ist unter `https://deinname.github.io/repo/` live.

### 🏷️ Eigene Domain (empfohlen für Seriosität)
Eine eigene Domain wie `dividenden-rechner.de` kostet ~5–15 €/Jahr (z. B. bei Namecheap, INWX, IONOS) und wirkt deutlich vertrauenswürdiger – wichtig für AdSense-Freigabe und Rankings. Domain bei Netlify/Cloudflare verbinden (dort gibt's Anleitungen).

> Nach dem Veröffentlichen: Ersetze in `index.html`, `robots.txt` und `sitemap.xml` den Platzhalter `DEINE-DOMAIN.de` durch deine echte Domain (Suchen & Ersetzen).

---

## ⚖️ Schritt 3: Rechtliches (wichtig in Deutschland!)

Sobald du Geld verdienst (Werbung/Affiliate), ist die Seite **kommerziell**. Pflicht:

1. **Impressum** ausfüllen → `impressum.html`, alle `[Platzhalter]` ersetzen.
2. **Datenschutzerklärung** anpassen → `datenschutz.html`. Sobald AdSense aktiv ist, brauchst du zusätzlich ein **Cookie-Consent-Banner** (siehe unten).
3. Für rechtssichere Texte: kostenlose Generatoren wie **e-recht24.de** oder **datenschutz-generator.de**.

> 💡 Kleinunternehmer: Einnahmen aus so einer Seite sind steuerpflichtig. Bei nennenswerten Einnahmen ggf. Gewerbe anmelden / Steuerberater fragen. (Keine Rechtsberatung.)

---

## 💰 Schritt 4: Monetarisierung scharfschalten

### 4a) Google AdSense (Werbung)

1. Konto erstellen: **https://adsense.google.com**
2. Deine Domain hinzufügen und den Verifizierungs-Code in den `<head>` von `index.html` einfügen.
3. Google prüft die Seite (dauert Tage bis Wochen). **Voraussetzung für Freigabe:** echte Inhalte, Impressum, Datenschutz, eigene Domain empfohlen.
4. Nach Freigabe: Anzeigen-Code generieren und an den markierten Stellen einsetzen.

**Wo Werbung hinkommt:** Suche in `index.html` nach dem Kommentar
```html
<!-- ADSENSE: Hier deinen AdSense-Code einfügen ... -->
```
Ersetze den Platzhalter-Block (`<div class="ad-inner">…</div>`) durch deinen echten AdSense-`<ins>`-Code. Du kannst weitere Werbeblöcke ergänzen (z. B. oben unter dem Header und unten vor dem Footer) – übertreib es aber nicht, sonst leidet die Nutzererfahrung und das Ranking.

> **Cookie-Banner:** AdSense braucht in der EU eine Einwilligung. Nutze ein kostenloses CMP (Consent Management Platform), z. B. **Google's eigenes** „Privacy & messaging" in AdSense, oder **Cookiebot/Usercentrics** (Gratis-Tarif). Ohne Consent-Banner ist AdSense in der EU nicht rechtskonform.

**Alternative zu AdSense:** Falls AdSense (anfangs strenge Freigabe) noch nicht klappt, gibt es **Ezoic**, **Media.net** oder Affiliate-only starten.

### 4b) Broker-Affiliate (oft lukrativer als Werbung!)

Im Abschnitt „Depot eröffnen" (`id="broker"`) sind drei Broker mit Datentabellen (Zins, Gebühren, Sparpläne, Einlagensicherung – Stand Juni 2026) und Platzhalter-Links (`href="#"`). So machst du sie scharf:

> ⚠️ **Konditionen aktuell halten:** Zinssätze und Gebühren ändern sich häufig. Die Werte in den Broker-Karten haben einen sichtbaren „Stand: …"-Hinweis. Prüfe sie alle paar Monate (Quellen z. B. die offiziellen Broker-Seiten, finanztip.de, justetf.com) und aktualisiere Zahl + Datum. Veraltete Finanzangaben schaden der Glaubwürdigkeit und können abmahnfähig sein.


1. Bei Partnerprogrammen anmelden. Möglichkeiten:
   - **Direkt beim Broker** (Trade Republic, Scalable, Comdirect, ING haben teils eigene „Kunden-werben-Kunden" / Affiliate-Programme).
   - **Affiliate-Netzwerke**: **Awin**, **Financeads** (auf Finanzen spezialisiert!), **AdCell**. Dort findest du viele Broker gebündelt.
2. Du bekommst dort deinen persönlichen Partnerlink.
3. In `index.html` die drei `href="#"` bei den Buttons mit `class="cta"` durch deine echten Links ersetzen.
4. Die `rel="sponsored nofollow"`-Kennzeichnung ist bereits gesetzt (Google-konform & vorgeschrieben).

> 💡 **Financeads.net** ist für genau dieses Projekt ideal – ein deutsches Affiliate-Netzwerk nur für Finanzprodukte.

---

## 📈 Schritt 5: Besucher bekommen (das eigentliche „Geheimnis")

Ohne Besucher kein Geld. So kommst du an Traffic:

1. **Bei Google anmelden:** Lege die Seite in der **Google Search Console** an (search.google.com/search-console), reiche die `sitemap.xml` ein. So findet Google dich schneller.
2. **SEO ist schon eingebaut:** Title, Meta-Description, strukturierte Daten (FAQ + WebApp), saubere Überschriften, schnelle Ladezeit. Das ist die halbe Miete.
3. **Mehr Inhalte = mehr Rankings:** Ergänze später Ratgeber-Artikel („Was ist die 4%-Regel?", „MSCI World erklärt", „Beste Dividenden-ETFs") als Unterseiten. Google liebt Inhalte.
4. **Promotion:** Teile den Rechner in passenden Subreddits (r/Finanzen), Finanz-Foren, Facebook-Gruppen – aber als Mehrwert, nicht als Spam.
5. **Backlinks:** Wenn andere Finanzseiten auf deinen Rechner verlinken, steigt das Ranking stark.

---

## 🔧 Anpassen & Erweitern

- **Farben/Design:** ganz oben in `index.html` im `:root`-CSS-Block (`--pri`, `--acc` …).
- **Name/Branding:** „Dividenden-Rechner" überall durch deinen Wunschnamen ersetzen.
- **Neue Rechner:** Die Struktur (Tab + Panel + `calcXXX()`-Funktion) ist leicht kopierbar – z. B. „Entnahmeplan", „Inflationsrechner", „ETF-Vergleich".
- **Steuer-Logik:** im `<script>` bei `steuersatz()` und den `calc…`-Funktionen. Aktuell vereinfacht (Abgeltungssteuer 25 % + Soli, Freibetrag 1.000 €).

---

## ✅ Checkliste zum Live-Gehen

- [ ] App lokal getestet (Doppelklick auf `index.html`)
- [ ] Veröffentlicht (Netlify/Cloudflare/GitHub Pages)
- [ ] Eigene Domain verbunden (empfohlen)
- [ ] `DEINE-DOMAIN.de`-Platzhalter ersetzt (index.html, robots.txt, sitemap.xml)
- [ ] Impressum ausgefüllt
- [ ] Datenschutz angepasst + Cookie-Banner eingebaut
- [ ] Google Search Console eingerichtet + Sitemap eingereicht
- [ ] Affiliate-Programme: echte Broker-Links eingsetzt
- [ ] AdSense beantragt und (nach Freigabe) Code eingebaut
- [ ] Erste Promotion / Inhalte ergänzt

---

## ⚠️ Disclaimer

Die App stellt keine Anlage-, Steuer- oder Rechtsberatung dar. Diese Anleitung ersetzt keine rechtliche/steuerliche Beratung. Prüfe Impressums- und Datenschutzpflichten für deinen konkreten Fall.

Viel Erfolg! 🚀
