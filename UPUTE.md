# Upute: kako raditi i predati zadaću

Tekst opisa zadaće je u `README.md`. Ovdje piše kako postaviti alate, raditi u repozitoriju i predati zadaću.

## 1. Instalirajte alate

1. **IntelliJ IDEA**, besplatna verzija: [jetbrains.com/idea](https://www.jetbrains.com/idea/download/).
2. **Git**, ako ga nemate: [git-scm.com](https://git-scm.com/downloads). Na macOS-u i Linuxu je obično već instaliran.
3. **GitHub nalog**, ako ga nemate: [github.com](https://github.com).

## 2. Isključite AI u IntelliJ-u

Zadaća se radi **bez AI-ja**, i to uključuje dopunjavanje koda u editoru.

1. Otvorite **Settings** (Windows/Linux: `Ctrl+Alt+S`, macOS: `Cmd+,`).
2. U polje za pretragu gore lijevo upišite **inline completion** i isključite sve opcije koje se pojave.
3. U **Settings → Plugins → Installed** potražite **AI** i isključite (Disable) sve AI dodatke, npr. *JetBrains AI Assistant*, *GitHub Copilot* i slične.
4. Restartujte IntelliJ.

Obično dopunjavanje (lista prijedloga dok kucate ime funkcije) smije ostati. Isključuje se samo ono što predlaže cijele linije ili blokove koda.

## 3. Preuzmite svoj repozitorij

1. Otvorite link zadaće na **Classmojiju** i prihvatite zadaću. Dobit ćete svoj repozitorij na GitHubu.
2. Na stranici repozitorija kliknite zeleno dugme **Code** i kopirajte HTTPS adresu.
3. U IntelliJ-u, na početnom ekranu, izaberite **Clone Repository** (ili **File → New → Project from Version Control**).
4. Zalijepite adresu i kliknite **Clone**. Ako traži prijavu, prijavite se na GitHub.

## 4. Prvo pokretanje

1. Nakon otvaranja, IntelliJ prvi put učitava projekat (Gradle). To može potrajati nekoliko minuta i zahtjeva Internet. Sačekajte da nestane progress bar na dnu.
2. Otvorite `src/main/kotlin/Main.kt`.
3. Kliknite zelenu strelicu pored `fun main()` i izaberite **Run**.
4. Dole se treba ispisati `Hello, Kotlin!`. Ako jeste, sve je spremno.

Sav kod pišete u `src/main/kotlin/`. Model podataka ide u `Model.kt`, a čitanje podataka, upiti i ispis u `Main.kt`. Ako želite, možete dodati još file-ova. Folder `data/` s CSV file-ovima koristi samo verzija C.

## 5. Commit i push

Radite commit **kako napredujete**, a ne samo na kraju. Potrebno je najmanje 5 commit-a.

1. **Git → Commit** (Windows/Linux: `Ctrl+K`, macOS: `Cmd+K`).
2. Označite file-ove koje ste mijenjali i napišite kratku poruku šta ste uradili.
3. Kliknite **Commit and Push**, pa **Push**.

Primjeri dobrih poruka:
- `Model: predmet i tip predmeta`
- `Unos podataka`
- `Prosjek i ECTS`
- `Nepoloženi i najbolja ocjena`
- `Ispis po semestru`

Na stranici repozitorija na GitHubu provjerite da se vaši commit-ovi vide.

## 6. Predaja

- Predaja je **zadnji push prije roka**. Commitovi nakon roka se ne računaju.
- Ništa ne šaljete mailom. To neće biti pregledano niti ocjenjeno.

## Česti problemi

| Problem | Rješenje |
|---|---|
| "No JDK" ili "Project JDK is not defined" | **File → Project Structure → Project → SDK → Download JDK**, izaberite verziju 21. |
| Crvene linije svuda nakon otvaranja | Sačekajte da Gradle završi učitavanje. Ako ne prođe, kliknite ikonu slona (**Load Gradle Changes**) ili **File → Reload All from Disk**. |
| Push traži lozinku i ne prihvata je | GitHub ne prima lozinku. U IntelliJ-u se prijavite kroz **Settings → Version Control → GitHub → Add Account → Log In via GitHub**. |
| Zelena strelica ne postoji | Provjerite da je `Main.kt` u `src/main/kotlin/` i da ima `fun main()`. |
