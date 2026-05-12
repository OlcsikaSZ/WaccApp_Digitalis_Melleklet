# WaccApp forráskód

Ez a mappa a szakdolgozati digitális melléklet WaccApp forráskódját tartalmazza. A rendszer Node.js és Express alapú kiszolgálóoldali réteggel, SQLite adatbázissal és több HTML/CSS/JavaScript alapú frontend nézettel működik.

## Tartalom

A `public` mappa tartalmazza a frontend oldalakat, köztük az üzenetküldő, beszélgetésnézet, szűrő, kérdőív-szerkesztő, sablonkezelő, bejelentkezési és adminisztrációs felületeket. Az `app.js` biztosítja a REST végpontokat, az adatbázis-kapcsolatot, az adminisztrációs kiszolgálást, a webhook feldolgozást, az üzenetküldési folyamatokat és az időzített küldéseket. A `questionnaire.js` és a `kerdoivek` mappa a kérdőíves működéshez tartozó mintákat tartalmazza.

## Biztonságos konfiguráció

Valódi `.env` fájl nem része a mellékletnek. Helyette a `.env.example` fájl szerepel mintaként. Ezt kell `.env` néven lemásolni, majd saját fejlesztői adatokkal kitölteni. A melléklet nem tartalmaz valódi Meta hozzáférési tokent, WhatsApp azonosítót, SMTP-jelszót vagy éles ügyféladatot.

## Telepítés és indítás

```bash
npm install
cp .env.example .env
npm start
```

Windows alatt a másolás kézzel is elvégezhető: a `.env.example` fájlból készíts egy `.env` nevű másolatot.

Alapértelmezett helyi cím: `http://localhost:3000`.

## Tesztadatbázis használata

A digitális melléklet `03_adatbazis/whatsapp_messages_teszt.db` állománya mintaadatbázis. A használatához a `.env` fájlban a következő érték adható meg:

```env
DB_PATH=../../03_adatbazis/whatsapp_messages_teszt.db
```

## Megjegyzés

A `node_modules` mappa nem része a beadási csomagnak, mert az `npm install` paranccsal újra előállítható. A feltöltési és média mappák üresen, `.gitkeep` állománnyal szerepelnek, hogy a program futás közben létre tudja hozni és használni tudja őket.
