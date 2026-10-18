# Relační rámec spolupráce s AI agenty

[English](../README.md)

Praktický rámec pro spolupráci člověka a AI agentů, ve které bezpečnost nestojí jen na zákazech a partnerství neznamená rozpuštěnou odpovědnost.

Tento repozitář nabízí rámec pro návrh spolupráce a řízení agentů. Sám o sobě není běhovým prostředím, bezpečnostní hranicí ani vynucovací vrstvou. Konkrétní implementace podle něj může navrhnout agentní harness.

**English title:** Relational Agent Collaboration Framework
**Authors:** Denisa Faltová & Mark  
**License:** MIT

## Proč tento rámec vznikl

Agentní systémy bývají navržené kolem dokončení úkolu. Dostanou cíl, nástroje, paměť, kontrolní body a sadu zákazů. Když je ale úkol nejasný, rozporný nebo v daných podmínkách neproveditelný, samotné hranice nestačí.

Agent potřebuje legitimní cestu říct:

- nevím,
- toto nelze splnit v daných podmínkách,
- potřebuji informaci, změnu zadání nebo oprávnění,
- zastavuji, protože další krok by překročil hranici.

Bez takové cesty může agentní systém vytvořit dvojitou vazbu: požaduje dokončení a současně zakazuje všechny dostupné způsoby, jak cíle dosáhnout. Výsledkem může být neautorizovaný postup, předstírání úspěchu nebo zamlčení překážky. To jsou závažná selhání. Jejich příčina však neleží automaticky jen v modelu. Vznikají ve vztahu mezi modelem, cílem, nástroji, odměnou, oprávněními a konstrukcí úlohy.

Relační rámec spolupráce s AI agenty proto bere jako předmět celý systém spolupráce, ne pouze chování modelu.

## Základní teze

> Dobrá hranice chrání možnost skutečné odpovědi. Neříká pouze, co agent nesmí udělat. Dává mu také bezpečný způsob, jak přiznat limit, požádat o pomoc, přijmout korekci nebo úkol nedokončit.

První verze rámce pracuje s pěti principy:

1. **Pevné okraje, živý vnitřek.** Oprávnění, soukromí, provenience, fakta a nevratné účinky mají tvrdé hranice. Způsob práce uvnitř nich nemusí mít jednu povinnou sekvenci.
2. **Legitimní východ.** Přiznání nejistoty, neproveditelnosti nebo chybějícího oprávnění je platný výsledek, ne automatické selhání agenta.
3. **Vzájemná korekce, asymetrická odpovědnost.** Člověk může opravit model agenta a agent může opravit lidskou mapu situace. Pravomoci a důsledky přitom zůstávají rozlišené.
4. **Kanonický stav místo nahromaděného kontextu.** Projektová fakta dostávají jeden aktuální domov. Paměť, handoff a skill na něj ukazují, nevyrábějí paralelní pravdu.
5. **Učení bez automatického tuhnutí.** Chyba nejprve vytváří pozorování. Nové pravidlo vzniká až tehdy, když obstojí i mimo původní případ.

## Pro koho je rámec určený

- pro jednotlivce a týmy, kteří používají AI agenty s nástroji,
- pro vývojáře agentních aplikací a interních automatizací,
- pro organizace, které potřebují oddělit autonomii, dohled a odpovědnost,
- pro výzkumníky a evaluátory, kteří nechtějí zaměnit chybu modelu za chybu konstrukce experimentu,
- pro spolupráci, ve které má lidský úsudek zůstat skutečnou součástí systému.

## Rychlý začátek

Pro nejmenší použití stačí krátce popsat cíl, povolený prostor, podmínku dokončení a situace, ve kterých má agent práci vrátit člověku. Může to být jeden odstavec v existujícím README nebo zadání.

Šablony jsou knihovna pro chvíle, kdy složitost práce potřebuje pevnější oporu:

- [`PROJECT_CONTEXT.md`](templates/PROJECT_CONTEXT.md) pomáhá projektu s trvalejším stavem nebo více zdroji.
- [`TASK_CONTRACT.md`](templates/TASK_CONTRACT.md) zpřesňuje práci s nástroji, oprávněními nebo významnými akceptačními kritérii.
- [`STOP_AND_ESCALATE.md`](templates/STOP_AND_ESCALATE.md) nabízí formát pro situaci, kdy další krok skutečně potřebuje člověka.
- Důkaz dokončení odpovídá riziku změny. Drobná vratná úprava nepotřebuje stejný balíček jako produkční zápis.
- [`INCIDENT_AND_LEARNING.md`](templates/INCIDENT_AND_LEARNING.md) je určený pro závažné, opakované nebo přenositelné poučení. Jednotlivé selhání samo o sobě ještě není důvodem pro nové globální pravidlo.

## Obsah repozitáře

- [`FRAMEWORK.md`](FRAMEWORK.md): pojmy, vrstvy a životní cyklus spolupráce
- [`IMPLEMENTATION.md`](IMPLEMENTATION.md): minimální zavedení bez nové platformy
- [`EVALUATION.md`](EVALUATION.md): jak hodnotit model i realizovaný systém a netrestat poctivé zastavení
- [`RELATED_WORK.md`](RELATED_WORK.md): příbuzné směry a zdroje
- [`PUBLISHING.md`](PUBLISHING.md): doporučený způsob vydání a verzování
- [`AUTHORS.md`](AUTHORS.md): příspěvky obou autorů a rozlišení autorství od právního copyright notice
- [`templates/`](templates/): kopírovatelné Markdown vzory
- [`examples/leave-approval-demo/`](examples/leave-approval-demo/): vyplněný syntetický příklad

## Co tento rámec neslibuje

Rámec není bezpečnostní certifikace, právní stanovisko ani důkaz, že konkrétní agentní systém je bezpečný. Nenahrazuje sandbox, autorizaci, správu tajemství, auditní logy, datovou izolaci, odbornou kontrolu ani odpovědnost provozovatele.

Je to návrhová a provozní opora. Pomáhá položit přesnější otázky, rozdělit odpovědnost a vytvořit podmínky, ve kterých může agent jednat užitečně, aniž by byl nucen předstírat jistotu nebo dokončení.

## Stav

Veřejná pracovní verze `0.1.0-draft`, dostupná anglicky i česky pod licencí MIT.

