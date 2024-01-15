# GIT CHEAT SHEET

Git er det gratis og open source distribuerede versionsstyringssystem, der er ansvarlig for alt, hvad der er relateret til GitHub, der sker lokalt på din computer. Denne cheat sheet indeholder de vigtigste og mest almindeligt anvendte Git-kommandoer for nem reference.

## INSTALLATION & GUIS
Med platformsspecifikke installatører til Git giver GitHub også en grafisk brugergrænseflade til daglig interaktion, gennemgang og synkronisering af depotet.

- [GitHub til Windows](https://windows.github.com)
- [GitHub til Mac](https://mac.github.com)
- [Git til alle platforme](http://git-scm.com)

## SETUP
Konfiguration af brugeroplysninger, der bruges på tværs af alle lokale depoter.

- `git config --global user.name “[fornavn efternavn]”`: Indstil et navn, der kan identificeres for kredit ved gennemgang af versionshistorik.
- `git config --global user.email “[gyldig-email]”`: Indstil en e-mail-adresse, der vil være forbundet med hver historisk markør.
- `git config --global color.ui auto`: Indstil automatisk kommandolinjefarvning for Git for nem gennemgang.

## STAGE & SNAPSHOT
Arbejde med øjebliksbilleder og Git-staging-området.

- `git status`: Vis ændrede filer i arbejdsområdet, klar til din næste commit.
- `git add [fil]`: Tilføj en fil, som den ser ud nu, til din næste commit (staging).
- `git reset [fil]`: Fjern en fil fra staging-området og bevar ændringerne i arbejdsområdet.
- `git diff`: Diff af hvad der er ændret, men ikke staged.
- `git diff --staged`: Diff af hvad der er staged, men ikke endnu committed.
- `git commit -m “[beskrivende besked]”`: Commit dine stagede ændringer som et nyt commit snapshot.

## BRANCH & MERGE
Isolering af arbejde i branches, ændring af kontekst og integration af ændringer.

- `git branch`: Vis dine branches. Et * vil vises ved siden af den aktuelt aktive branch.
- `git branch [branch-navn]`: Opret en ny branch ved det aktuelle commit.
- `git checkout [branch]`: Skift til en anden branch og tjek den ud i dit arbejdsområde.
- `git merge [branch]`: Merge den specificerede branchs historik ind i den nuværende.
- `git log`: Vis alle commits i den aktuelle branchs historik.

## SETUP & INIT
Konfiguration af brugeroplysninger, initialisering og kloning af depoter.

- `git init`: Initialiser en eksisterende mappe som et Git-depot.
- `git clone [url]`: Hent et helt depot fra en hostet placering via URL.

## INSPECT & COMPARE
Undersøgelse af logs, diffs og objektinformation.

## SHARE & UPDATE
Hent opdateringer fra et andet depot og opdater lokale depoter.

- `git log`: Vis commit-historik for den aktuelt aktive branch.
- `git log branchB..branchA`: Vis commits på branchA, der ikke er på branchB.
- `git log --follow [fil]`: Vis commits, der ændrede filen, selvom den blev omdøbt.
- `git diff branchB...branchA`: Vis forskellen på det, der er i branchA, men ikke i branchB.
- `git show [SHA]`: Vis ethvert objekt i Git i en menneskelig læsbar format.
- `git remote add [alias] [url]`: Tilføj en Git-URL som en alias.
- `git fetch [alias]`: Hent alle branches fra den Git-remote.
- `git merge [alias]/[branch]`: Merge en fjernbranch ind i din aktuelle branch for at opdatere den.
- `git push [alias] [branch]`: Overfør lokale branch-commits til fjernrepositoryets branch.
- `git pull`: Hent og merge eventuelle commits fra den trackede fjernbranch.

## TRACKING PATH CHANGES
Versionering af filfjernelser og stive stiændringer.

## REWRITE HISTORY
Omskrivning af branches, opdatering af commits og rydning af historik.

## TEMPORARY COMMITS
Midlertidig opbevaring af ændrede, fulgte filer for at skifte branches.

- `git rebase [branch]`: Anvend eventuelle commits fra den nuværende branch foran den specificerede.
- `git reset --hard [commit]`: Ryd staging-området, omskriv arbejdsområdet fra det specificerede commit.
- `git rm [fil]`: Slet filen fra projektet og stage fjernelsen til commit.
- `git mv [eksisterende-sti] [ny-sti]`: Ændre en eksisterende filsti og stage flytningen.
- `git log --stat -M`: Vis alle commit-logs med indikation af eventuelle stier, der er flyttet.
- `git stash`: Gem ændringer midlertidigt.
- `git stash list`: Vis stakrækkefølgen af gemte filændringer.
- `git stash pop`: Skriv arbejdet fra toppen af stash-stakken.
- `git stash drop`: Kassér ændringerne fra toppen af stash-stakken.

## IGNORING PATTERNS
Forebyggelse af utilsigtet staging eller commit af filer.

- Opret en fil med ønskede mønstre som `.gitignore` med enten direkte strengmatches eller wildcard-globs.
- `git config --global core.excludesfile [fil]`: Systembred ignoremønster for alle lokale depoter.

---