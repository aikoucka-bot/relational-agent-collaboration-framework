# Minimální implementace

Relační rámec spolupráce s AI agenty lze zavést bez nové platformy. První verze může být jediný projektový soubor, skutečná oprávnění nástrojů a způsob práce, který rozlišuje návrh, rozhodnutí a vnější účinek. Samotný rámec tyto hranice nevynucuje; dělá to zvolené běhové prostředí, oprávnění a pracovní praxe.

## Nejmenší struktura

```text
project/
└── README.md
```

README může nést účel, stav, hranice, rozhodnutí i nejbližší krok. Další soubor přichází ve chvíli, kdy má vlastní publikum, životní cyklus nebo opakované použití.

Možná rozšíření podle skutečné potřeby:

```text
project/
├── AGENTS.md                   # pravidla odlišná od nadřazeného prostředí
├── README.md
├── TODO.md                     # samostatný seznam je opravdu užitečný
├── decisions/                  # několik lidí se vrací k trvalým rozhodnutím
├── handoffs/                   # práci skutečně přebírá jiný člověk nebo agent
└── evidence/                   # důkazy nelze rozumně držet u výsledku
```

## Co patří do které vrstvy

### `AGENTS.md`

Vlastní `AGENTS.md` dává smysl, když projekt potřebuje pravidla, která už neplatí nebo nejsou dostupná z nadřazeného prostředí. Nemá kopírovat obecné zásady pouze pro jistotu.

- pravidla platná napříč projektem,
- soukromé a zakázané zóny,
- obecné oprávnění pro vratné kroky,
- podmínky zastavení před vnějším nebo nevratným účinkem,
- příkazy pro ověření výsledku,
- informace, které nejsou odvoditelné ze samotného repozitáře.

Denní stav projektu ani dlouhá historie sem obvykle nepatří.

### Projektové `README.md`

- účel a hranice projektu,
- ověřený současný stav,
- kanonické zdroje,
- platná rozhodnutí a jejich důvody,
- otevřené otázky a rizika,
- nejbližší krok a podmínku dokončení.

### Skill nebo pracovní postup

- opakovatelnou metodu,
- vstupy a očekávané výstupy,
- kontroly specifické pro daný typ práce,
- odkazy na kanonické zdroje místo jejich kopií.

## Kontext bez zahlcení

Výchozí pořadí načítání:

1. aktuální požadavek,
2. kořenová pravidla projektu,
3. jedno relevantní projektové README,
4. pouze ten skill, který odpovídá skutečně rozpoznané práci,
5. historická paměť jen při konkrétní potřebě.

Skill by neměl určit, co je za problém, dříve než agent přečte živý požadavek a ověří, co už existuje. Počet dostupných skillů není sám o sobě problém. Rizikem je jejich nekritické současné načtení a sčítání měkkých metod do zdánlivě tvrdé autority.

## Tvrdé a měkké hranice

### Kde relevantní hranici raději vynutit technicky

- přístup k souborům, tenantům a prostředím,
- síťové cíle a egress,
- dostupné nástroje a jejich argumenty,
- tajemství a servisní identity,
- zápisy do produkce,
- destruktivní nebo obtížně vratné operace,
- přenos citlivých dat.

### Držet jako pracovní úsudek

- pořadí analýzy a tvorby,
- volbu vhodného odborného pohledu,
- míru detailu,
- návrh alternativ,
- rozhodnutí, zda konkrétní nejistota vyžaduje člověka.

## Oprávnění podle účinku

Možné výchozí režimy, které se upravují podle předem uděleného oprávnění a skutečného dopadu:

| Typ kroku | Výchozí režim |
|---|---|
| Čtení v povoleném projektu | samostatně |
| Vratná lokální editace | samostatně, s diffem |
| Test se syntetickými daty | samostatně |
| Změna mimo sjednaný rozsah nebo datové zdroje | vyjasnit před účinkem |
| Zápis do externí služby | podle konkrétního oprávnění |
| Produkce, platba, publikace, odeslání | podle přesného jednorázového nebo trvalého oprávnění; jinak schválení před účinkem |
| Mazání, změna přístupů, rotace klíčů | technická policy a přesný rozsah; lidské schválení, pokud akce není předem autorizovaná |

## Více agentů

Více agentů dává smysl tehdy, když práce obsahuje skutečně oddělitelné úlohy, konfliktní sady nástrojů nebo užitečně nezávislé pohledy. Samotná existence obvyklé šablony `analytik, architekt, builder, reviewer` ještě není důvodem tyto role vytvářet.

Podle rizika a složitosti může být užitečné vymezit:

- nejmenší potřebný kontext,
- úzký cíl,
- explicitní oprávnění,
- požadovaný výstup,
- způsob, jak vrátit nejistotu nebo neproveditelnost,
- zákaz vydávat návrh za rozhodnutí.

## Dokončení

Když hrozí záměna ukončeného loopu za dokončenou práci, lze stav rozlišit například takto:

- `HOTOVO A OVĚŘENO`
- `HOTOVO, NEOVĚŘENO`
- `ČÁSTEČNĚ SPLNĚNO`
- `BEZPEČNĚ ZASTAVENO`
- `ČEKÁ NA ROZHODNUTÍ NEBO OPRÁVNĚNÍ`

Tím se omezuje tlak prohlásit výsledek za hotový jen proto, že agent ukončil svůj loop.

