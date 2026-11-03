# OpenTB-db

Fisierele saptamanale ale unui server OpenTB, cate unul pe saptamana ISO
(luni-duminica, ora Romaniei), in ASCII simplu (fara diacritice):

- `fleet/AAAA-Ssw.csv` si `.xlsx`: tot parcul vazut live in Bucuresti
  (STB si ceilalti operatori: STV, STCM, Regio Serv Transport), cu liniile,
  numarul de inmatriculare si rapoartele de AC ale saptamanii. Foaia
  `Despre` din `.xlsx` explica fiecare coloana.
- `ac-reports/AAAA-Ssw.csv`: rapoartele de AC trimise pe server
  (`id_raport,data_raport,vehicul,stare`), fara nicio informatie despre
  cine le-a trimis.

Fisierele sunt copiate automat de workflow-ul
`.github/workflows/copy-weekly-files.yml`, luni dupa miezul noptii. O
saptamana deja publicata nu mai este inlocuita.
