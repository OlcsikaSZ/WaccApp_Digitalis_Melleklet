WaccApp forráskód - szakdolgozati digitális melléklet

Ez a mappa a WaccApp rendszer leadásra szánt, tisztított forráskódját tartalmazza.
A csomagból szándékosan kimaradtak az automatikusan újragenerálható, helyi fejlesztői
környezethez kötődő vagy biztonsági szempontból érzékeny állományok.

Nem része a csomagnak:
- node_modules/
- .git/
- .idea/
- valódi .env fájl
- valódi API-tokenek, jelszavak, SMTP-jelszavak
- éles felhasználói adatokat tartalmazó adatbázis
- korábban feltöltött vagy elküldött médiafájlok

Futtatás röviden:
1. Telepítsd a Node.js környezetet.
2. A 02_forraskod/waccapp mappában futtasd: npm install
3. Másold a .env.example fájlt .env néven.
4. A .env fájlban add meg a saját Meta/WhatsApp, session és SMTP adataidat.
5. Indítás: npm start
6. Böngészőben: http://localhost:3000

Teszteléshez a 03_adatbazis mappában található whatsapp_messages_teszt.db használható.
