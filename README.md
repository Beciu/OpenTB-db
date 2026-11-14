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

Si lista parcului STB, in zilele in care s-a schimbat:

- `parc/parc_stb_ZZ.LL.AAAA.csv`: toate vehiculele STB, in coloanele
  `fleet_no,transport_type,model,sub_model,original_model,registration,year_built,depot,history,notes`.
  Tramvaiele vin din fisierul de modele al OpenTB; autobuzele si
  troleibuzele sunt cele vazute live, cu modelul dupa numarul de parc si
  numarul de inmatriculare (de la mo-bi sau confirmat de 2 calatori).

Fisierele sunt copiate automat de workflow-ul
`.github/workflows/copy-weekly-files.yml`, luni dupa miezul noptii si la
fiecare 6 ore. Un fisier deja publicat nu mai este inlocuit.
