# Doporučené publikování

## Kam

Pro první veřejnou verzi je vhodný samostatný veřejný GitHub repozitář. Pracovní název:

```text
relational-agent-harness
```

Bezpečnější publikační cesta vede přes samostatný repozitář, nikoli přes veřejnou větev nebo kopii osobního vaultu. Do repozitáře pak vstupuje pouze zkontrolovaný veřejný balíček.

## Proč GitHub

- Markdown se zobrazuje bez dalšího publikačního systému.
- Historie změn zachovává vývoj rámce.
- Issues nebo Discussions mohou sbírat příklady, námitky a návrhy.
- Releases umožní vydávat stabilní verze.
- `CITATION.cff` umožní strojově čitelnou citaci.
- GitHub Pages může později nabídnout čitelnější web bez změny zdroje.

GitHub doporučuje, aby README vysvětlilo účel, přínos, první kroky, podporu a správce projektu. Licence, citační soubor a pravidla přispívání pomáhají vyjasnit očekávání.

## Navržené fáze

### 1. Soukromá příprava

- schválit český významový základ,
- potvrdit název **Relational Agent Harness**,
- odstranit interní poznámky a placeholdery,
- ověřit odkazy a Markdown.

### 2. Veřejná v0.1

- vytvořit samostatný repozitář,
- nahrát veřejný balíček,
- přidat `LICENSE`, `CITATION.cff` a stručný `CHANGELOG.md`,
- vytvořit release `v0.1.0`,
- zapnout Issues nebo Discussions jen tehdy, pokud existuje kapacita reagovat.

### 3. Anglická verze

- zachovat českou verzi jako významový zdroj,
- přidat `README.en.md` a anglické protějšky hlavních dokumentů,
- neslévat terminologické rozdíly do zdánlivě doslovného překladu.

### 4. Citovatelná verze

Zenodo lze propojit s GitHubem. Nové GitHub releases pak automaticky archivuje a přiděluje jim DOI. Tento krok dává smysl až pro významově stabilní vydání, například `v1.0.0`, nebo dříve, pokud má být v0.1 citovaným výzkumným objektem.

## Licence

Rámec je licencovaný pod `MIT`. Licence umožňuje používání, úpravy, publikování, distribuci, sublicencování a komerční využití. Kopie nebo podstatné části musí zachovat copyright notice a licenční text. MIT nevyžaduje zveřejnění zdrojů odvozeného díla ani zachování stejné licence.

Repozitář obsahuje textový rámec, provozní šablony a případně později i kód. MIT byla zvolená pro jednoduché a široké praktické převzetí celku. Tento dokument není právní stanovisko.

## Autorství a provenience

Citovanými autory rámce jsou **Denisa Faltová & Mark**. `AUTHORS.md` popisuje rozdílné příspěvky obou autorů. `CITATION.cff` poskytuje strojově čitelnou citaci. Denisa Faltová je v MIT licenci uvedená jako lidská držitelka práv a osoba schopná licenci udělit.

Interní historii rozhovoru, osobní kontinuitu a neveřejné zdroje není potřeba publikovat, aby byla spolupráce přiznaná pravdivě. Před přijímáním externích příspěvků je ještě potřeba rozhodnout, kdo schvaluje změny a kdo smí vydat novou verzi.

## Doporučené soubory před vydáním

```text
README.md
FRAMEWORK.md
IMPLEMENTATION.md
EVALUATION.md
RELATED_WORK.md
PUBLISHING.md
templates/
LICENSE
CITATION.cff
AUTHORS.md
CHANGELOG.md
CONTRIBUTING.md        # až pokud jsou příspěvky skutečně vítané
CODE_OF_CONDUCT.md     # při otevření komunitních příspěvků
```

## Co zatím nedělat

- nezakládat automaticky web nebo značku,
- nepublikovat interní vault ani jeho historii,
- nevytvářet organizaci na GitHubu bez potřeby,
- neslibovat bezpečnostní certifikaci,
- nezapínat komunitní kanály bez kapacity je spravovat,
- nepřidělovat DOI verzi, kterou autorka ještě nepovažuje za citovatelnou.

## Provozní zdroje

- [GitHub: About README files](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
- [GitHub: Licensing a repository](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)
- [GitHub: About CITATION files](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files)
- [GitHub Pages: Creating a site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [Zenodo: GitHub integration](https://help.zenodo.org/docs/github/)
- [Zenodo: Archive a GitHub release](https://help.zenodo.org/docs/github/archive-software/github-upload/)

