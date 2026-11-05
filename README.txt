ØSTERGADES POS 1.0 – TESTVERSION

Åbn index.html i Chrome/Edge for at teste med det samme.
PIN medarbejder: 1234
PIN administrator: 9999

Windows-app (kræver Node.js på en Windows-computer):
1. Pak ZIP-filen ud.
2. Åbn terminalen i mappen.
3. Kør: npm install
4. Kør: npm start
5. For at bygge installationsfil: npm run dist

VIGTIGT:
Dette er en lokal prototype, ikke et produktionsklart POS-system.
PIN-koder er hårdkodede og ikke sikre.
Supabase/PakkeTracker-synkronisering er IKKE implementeret.
Data gemmes i localStorage på den enkelte computer. Tag JSON-backup.
Printeren bruger Windows' normale printdialog; direkte HS-58CUB-integration er ikke testet.
Ingen lovpligtig kasselogning/SAF-T eller automatisk MobilePay-afstemning.
Brug ikke prototypen som lovpligtigt kassesystem.
