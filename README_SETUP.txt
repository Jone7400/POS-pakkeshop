Østergades POS v1.7 – opsætning

1. Tag en JSON-backup fra v1.6 først.
2. Åbn Supabase > SQL Editor i projekt paqeijcqyjvcsehnxzww.
3. Kør indholdet af SUPABASE_SETUP.sql én gang.
4. Upload appfilerne til GitHub Pages. SQL-filen må gerne ligge lokalt; den bruges kun i SQL Editor.
5. Åbn POS og log ind med PakkeTracker e-mail/adgangskode.
6. Åbn Administration (bekræft adgangskode), derefter Backup > Overfør lokale data til ny cloud.
7. Kontrollér at status viser Synkroniseret. Test ved at genindlæse siden.

VIGTIGT:
- Dette er en første cloud-integration, IKKE et produktionssikkert multi-medarbejder-kassesystem.
- Hele POS-tilstanden gemmes som ét JSON-dokument pr. Supabase-bruger.
- Der er ingen sikker adskillelse af medarbejderrettigheder: medarbejdere arbejder
  i samme indloggede browsersession. Admin-bekræftelse er en UI-barriere.
- Hvis to enheder ændrer samtidig, stopper revisionstjekket overskrivning, men
  konflikter skal løses manuelt. Brug kun én POS-enhed til skrivning.
- Billeder er endnu indlejret i JSON, ikke i Supabase Storage. Større billeder
  kan gøre synkronisering langsom. Kvitterings-PDF eksport er fortsat manuel.
- Hvis cloudstatus ikke siger Synkroniseret, er ændringer ikke sikkert cloud-gemt.
- Gem regelmæssige JSON-backups; test først med fiktive salg.
