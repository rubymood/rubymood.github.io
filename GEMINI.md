# Projekt Konfiguráció: Jekyll Blog a GitHub Pages-en

## Összefoglaló

Ez a projekt egy Jekyll alapú statikus weboldal, ami a `rubymood/rubymood.github.io` repository-t használja és a GitHub Pages szolgáltatja.

A build folyamat lokálisan történik, a GitHub Actions **nem** végez buildelést.

## Branch-elési Stratégia

-   `dev`: Az alapértelmezett fejlesztési branch. Minden forráskód (Markdown posztok, Jekyll konfiguráció, stíluslapok stb.) ezen a branch-en található.
-   `main`: A production branch. Ez a branch tartalmazza a Jekyll által legenerált statikus weboldalt (a `_site` mappa tartalmát). A GitHub Pages ezt a branch-et használja a weboldal publikálásához.

## Fejlesztési és Publikálási Folyamat

1.  **Fejlesztés:** Mindig a `dev` branch-en dolgozz.
    ```bash
    git checkout dev
    ```
2.  **Módosítások:** Írj új bejegyzést, módosítsd a stílusokat, stb.
3.  **Lokális Build:** Generáld le a statikus oldalt a `_site` mappába.
    ```bash
    jekyll build
    ```
4.  **Commit:**
    -   A forráskód változásait commitold a `dev` branch-re.
    -   A legenerált `_site` mappa tartalmát commitold a `main` branch-re.
5.  **Push:** Töltsd fel mindkét branch-et a remote repository-ba.
    ```bash
    git push origin dev
    git push origin main
    ```

**Fontos:** A `main` branch-re soha ne kerüljön közvetlenül forráskód, csak a `jekyll build` parancs kimenete.

## Aktuális Teendők

Az aktuális feladatok és a megvalósítási terv a `gemini_action_plan.txt` fájlban található. Kérjük, ellenőrizd ezt a fájlt a folyamatban lévő munkához és a következő lépésekhez.
