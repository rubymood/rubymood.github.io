# Projekt Konfiguráció: Jekyll Blog a GitHub Pages-en

## Összefoglaló

Ez a projekt egy Jekyll alapú statikus weboldal, ami a `rubymood/rubymood.github.io` repository-t használja és a GitHub Pages szolgáltatja.

A build folyamat a GitHub Actions segítségével történik.

## Branch-elési Stratégia

-   `dev`: Az alapértelmezett fejlesztési branch. Minden forráskód (Markdown posztok, Jekyll konfiguráció, stíluslapok stb.) ezen a branch-en található.
-   `master`: A production branch. Ez a branch tartalmazza a Jekyll által legenerált statikus weboldalt (a `_site` mappa tartalmát). A GitHub Pages ezt a branch-et használja a weboldal publikálásához.

## Fejlesztési és Publikálási Folyamat

1.  **Fejlesztés:** Mindig a `dev` branch-en dolgozz.
    ```bash
    git checkout dev
    ```
2.  **Módosítások:** Írj új bejegyzést, módosítsd a stílusokat, stb.
3.  **Commit:**
    -   A forráskód változásait commitold a `dev` branch-re.
4.  **Push:** Töltsd fel a `dev` branch-et a remote repository-ba.
    ```bash
    git push origin dev
    ```



## Aktuális Teendők

Az aktuális feladatok és a megvalósítási terv a `gemini_action_plan.txt` fájlban található. Kérjük, ellenőrizd ezt a fájlt a folyamatban lévő munkához és a következő lépésekhez.
