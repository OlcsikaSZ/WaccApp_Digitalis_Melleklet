WaccApp forráskód – szakdolgozati digitális melléklet

Ez a mappa a WaccApp rendszer leadásra szánt, tisztított forráskódját tartalmazza. A csomag célja, hogy a dolgozatban bemutatott frontend és a működéshez szükséges kiszolgálóoldali környezet újratelepíthető legyen, miközben valódi hozzáférési adatok nem kerülnek a mellékletbe.

A csomag tartalmazza az app.js fájlt, a public mappában lévő HTML-alapú frontend nézeteket, a kérdőívfájlokat, a package.json és package-lock.json állományokat, a .env.example mintakonfigurációt, valamint az üresen megtartott feltöltési és adatkönyvtárakat.

A csomagból szándékosan kimaradt a node_modules mappa, a .git és .idea fejlesztői metaadat, a valódi .env fájl, minden éles API-token, jelszó, SMTP-jelszó, valós ügyféladatot tartalmazó adatbázis, továbbá a korábban feltöltött vagy elküldött médiafájlok. Ezek leadása biztonsági és adatvédelmi szempontból nem lenne helyes.

Futtatás röviden:
1. Telepítsd a Node.js környezetet.
2. Lépj be a 02_forraskod/waccapp mappába.
3. Futtasd az npm install parancsot.
4. Másold a .env.example fájlt .env néven.
5. A .env fájlban add meg a saját Meta/WhatsApp, session és SMTP adataidat.
6. Indítsd el az alkalmazást az npm start paranccsal.
7. Böngészőben nyisd meg a http://localhost:3000 címet.

Teszteléshez a 03_adatbazis mappában található whatsapp_messages_teszt.db használható. Ehhez a .env fájlban a DB_PATH változó például így állítható be:
DB_PATH=../../03_adatbazis/whatsapp_messages_teszt.db

A valódi WhatsApp küldéshez érvényes Meta Developer / WhatsApp Business API adatok szükségesek. Ezek nélkül a frontend nézetek, a helyi működés, a tesztadatbázis és a dokumentált folyamatok vizsgálhatók, de éles üzenetküldés nem várható.
