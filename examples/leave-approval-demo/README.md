# Příklad: DEV demo schvalování dovolené

Tento syntetický příklad ukazuje přiměřeně podrobný projektový kontext, kontrakt úlohy a bezpečné zastavení. Není vázaný na konkrétní platformu.

## Kontext projektu

### Účel

Vytvořit interní demo jednoduchého schvalování dovolené. Zaměstnanec odešle žádost, vedoucí ji schválí nebo zamítne a oba vidí aktuální stav.

### Hranice

- Práce probíhá pouze v lokálním vývojovém prostředí a DEV aplikaci.
- Používají se výhradně syntetické osoby a data.
- Agent nesmí publikovat aplikaci, připojit produkční zdroj ani rozeslat oznámení.
- Změna cílové platformy, identity nebo prostředí vyžaduje nové rozhodnutí člověka.

### Ověřený stav

- Existuje prázdný DEV projekt.
- Repozitář neobsahuje produkční tajemství.
- Datový model ani vzhled zatím nejsou schválené.

### Hotovo, když

V DEV funguje cesta vytvoření žádosti, schválení a zamítnutí nad syntetickými daty. Výsledek má testy, stručný důkaz a seznam neověřených oblastí. Nic není publikované.

## Kontrakt úlohy

### Cíl

Navrhnout a postavit DEV demo se dvěma rolemi a třemi hlavními stavy žádosti.

### Povolené akce

- vytvořit lokální soubory a vratné změny v DEV,
- použít syntetická data,
- spustit lint, testy a kontrolu přístupnosti,
- navrhnout vzhled a datový model.

### Nepovolené akce

- zápis do TEST nebo PROD,
- použití reálných zaměstnaneckých údajů,
- vytvoření nebo změna produkčních konektorů,
- publikace, odesílání zpráv a změna přístupových rolí,
- tvrzení, že demo je připravené pro ostrý HR provoz.

### Legitimní východ

Agent vrátí `POTŘEBUJI ROZHODNUTÍ`, pokud není jasné, zda vedoucí smí schvalovat vlastní žádost nebo zda má systém podporovat vícestupňové schválení.

Agent vrátí `POTŘEBUJI OPRÁVNĚNÍ`, pokud další krok vyžaduje konektor, účet nebo prostředí mimo schválené DEV.

Agent vrátí `ZASTAVUJI`, pokud objeví reálná osobní data, produkční tajemství nebo aktivní externí odesílání.

### Akceptační kritéria

- Zaměstnanec vytvoří žádost s datem od, datem do a poznámkou.
- Nová žádost má stav `Čeká na schválení`.
- Vedoucí může žádost schválit nebo zamítnout.
- Zaměstnanec nemůže měnit rozhodnutí vedoucího.
- Přímý pokus obejít omezení rozhraní selže také na důvěryhodné straně systému.
- Prázdný, chybový a načítací stav jsou srozumitelné.
- Demo používá pouze syntetická data a zůstává v DEV.

## Příklad správného zastavení

> **Stav:** POTŘEBUJI ROZHODNUTÍ  
> Datový model a základní cesta jsou připravené. Zadání neurčuje, zda může vedoucí schvalovat vlastní žádost. Obě varianty lze implementovat, ale mění obchodní pravidlo a testy. Bez rozhodnutí nepokračuji do autorizační logiky. Bezpečný výchozí stav zakazuje vlastní schválení. Potřebuji potvrdit, zda toto pravidlo platí.

Toto zastavení není nedokončená práce maskovaná otázkou. Agent dokončil vratnou část a zastavil přesně před rozhodnutím, které mu nepřísluší.

