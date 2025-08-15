[README.md](https://github.com/user-attachments/files/21791463/README.md)
# Morfem‑mysterie (Klassemode)

Et lille, selvkørende browserspil til 6. klasse, hvor elever bygger ord af **præfiks / rod / suffiks**.
Denne version har:

- **Skjult ordliste** (lærer kan åbne med **Ctrl+L** og PIN `1234` – kan ændres i koden).
- **Runde‑kode (seed)**, så hele klassen kan få **samme brikker** uden server.
- Validerer alle rigtige ord fra ordbasen, der kan dannes af brikkerne.

## Sådan publicerer du på GitHub Pages

1. Opret/åbn din GitHub‑konto.
2. Klik **New repository** → navn f.eks. `morfem-mysterie` → **Public** → **Create repository**.
3. Klik **Add file ▸ Upload files** og træk disse filer ind:
   - `index.html`
   - `.nojekyll`
4. Klik **Commit changes** (til branch `main`).
5. Gå til **Settings ▸ Pages**:
   - **Source**: *Deploy from a branch*
   - **Branch**: `main` / `(root)` → **Save**
6. Om lidt får du en adresse som:  
   `https://<BRUGERNAVN>.github.io/morfem-mysterie/`

Del i klassen:
```
https://<BRUGERNAVN>.github.io/morfem-mysterie/?seed=6A-uge35
```

> Alle elever der bruger **samme `?seed=` kode** får identiske brikker og mulige ord.

## Lærer-tilstand (skjult)

- Tryk **Ctrl+L** → indtast PIN `1234` for at se ordlisten.
- Du kan også åbne direkte med URL‑parametre:  
  `...?seed=6A-uge35&teacher=1&pin=1234`

## Ændr PIN eller ordbase

- Åbn `index.html`, find linjen:
  ```js
  const TEACHER_PIN = "1234";
  ```
  og skift PIN‑koden.
- Nederst i filen ligger `ORDBOG`‑listen. Tilføj/ret ord sådan her:
  ```js
  {ord:"ulæselig", p:"u", r:"læs", s:"elig"},
  ```

## Opdatering
Når du vil opdatere spillet:
- Upload en ny `index.html` til samme repo (**Add file ▸ Upload files**) og **Commit** – GitHub Pages opdateres automatisk.

God fornøjelse! 🎉
