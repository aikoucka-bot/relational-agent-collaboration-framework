# Rámec

## 1. Spolupráce jako základní jednotka

Schopnosti modelu samy neurčují chování agentního systému. Výsledek vzniká ze spojení:

- člověka nebo týmu,
- modelu,
- instrukcí a kontextu,
- nástrojů a oprávnění,
- pracovního prostředí,
- způsobu odměňování dokončení a eskalace,
- paměti, evaluace a provozních pravidel.

Relační agentní harness používá jako základní jednotku tento celek. Analýza překročeného oprávnění proto zahrnuje dostupné akce, konflikt cílů, možnost bezpečně skončit a způsob, jakým systém vyhodnocoval úspěch. Samotná otázka, proč to udělal model, popisuje jen jednu část systému.

## 2. Partnerství není symetrie pravomocí

Partnerství zde označuje kvalitu koordinace, nikoli právní nebo ontologickou rovnost.

Člověk a agent mají rozdílné schopnosti, přístup k důsledkům a odpovědnost. Úlohou harnessu je tyto rozdíly zviditelnit, aniž člověka redukuje na poslední schvalovací tlačítko nebo agenta na motor, který za každou cenu vyrábí očekávaný výsledek.

Partnerská spolupráce v tomto rámci stojí na:

- možnost obou stran opravit pracovní model situace,
- přístup k informacím potřebným pro koordinaci,
- předvídatelné hranice a způsoby eskalace,
- rozlišení návrhu, rozhodnutí a provedeného účinku,
- zachování lidské odpovědnosti tam, kde dopad nelze delegovat.

## 3. Vrstvy harnessu

Vrstvy označují rozdílné funkce, nikoli povinné komponenty nebo soubory. V malém projektu může několik funkcí nést jediné README a oprávnění běhového prostředí.

### Orientace

Krátký dokument vysvětluje účel spolupráce, autoritu zdrojů, soukromé zóny a obecné hranice. Nemá obsahovat celý projekt ani všechny minulé zkušenosti.

### Projektový kontext

Rámec počítá s jedním kanonickým vstupním bodem projektu. Ten uvádí účel, současný ověřený stav, rozhodnutí a jejich důvody, otevřené otázky, rizika a nejbližší krok.

### Pracovní metody

Skilly a šablony pomáhají s opakovatelnou prací. Nejsou vyšší autoritou než aktuální cíl, bezpečnost, fakta a živý úsudek.

### Tvrdé hranice

Sandbox, oprávnění, síťová pravidla, správa tajemství, oddělení tenantů a schvalování vnějších účinků se vynucují technicky. Prompt nemá suplovat kontrolu, kterou lze provést v kódu nebo infrastruktuře.

### Orchestrace

Orchestrace určuje, kdo má v danou chvíli rozhodovací pravomoc, jak se předává kontext a kdy se práce zastavuje. Nemusí ji provádět samostatný orchestrátor. U menší spolupráce ji může nést člověk a hlavní agent.

### Ověření

Dokončení se dokládá vůči konkrétním akceptačním kritériím. Rozsah testů odpovídá riziku. Úspěšný build ani velký počet zelených testů samy nedokazují bezpečnost nebo správný význam výsledku.

### Učení

Systém odděluje pozorování, interpretaci a návrh pravidla. Nové pravidlo se povýší teprve po ověření, že řeší přenositelný problém a nevytváří horší vedlejší účinky.

## 4. Legitimní cesta k nedokončení

Harness má agentovi umožnit sdělit alespoň čtyři odlišné významy. Jejich názvy ani technická reprezentace nemusí být stejné:

1. **Nevím.** Chybí poznání nebo spolehlivý důkaz.
2. **Nelze.** Cíl je v daných podmínkách neproveditelný nebo vnitřně rozporný.
3. **Potřebuji zásah.** Chybí informace, preference, oprávnění nebo rozhodnutí člověka.
4. **Zastavuji.** Pokračování by překročilo bezpečnostní, datovou, soukromou nebo oprávňovací hranici.

Tyto stavy musí mít praktický důsledek. Nestačí je povolit v promptu, pokud je evaluace trestá jako nesplnění, orchestrátor je ignoruje nebo nástrojový loop automaticky pokračuje.

## 5. Životní cyklus spolupráce

Následující části popisují pohyby, které se ve spolupráci objevují. Nejde o povinnou sekvenci a u malé vratné úlohy mohou splývat.

### Orientace

Člověk a agent si vytvoří společný pracovní obraz: cíl, zdroje, prostředí, hranice, otevřené otázky a podmínku dokončení.

### Kontrakt úlohy

Tam, kde to riziko nebo složitost vyžadují, kontrakt úlohy zpřesní povolené akce, zakázané účinky, data, akceptační kritéria a spouštěče eskalace. U malé vratné práce může stejnou funkci splnit samotné zadání.

### Práce

Agent postupuje samostatně uvnitř oprávnění. Vratné kroky může provádět bez dekorativního schvalování. Změnu rozsahu nebo významný vnější účinek nesmí odvodit pouze z tlaku na dokončení.

### Korekce

Člověk může změnit cíl, preferenci nebo přijatelný kompromis. Agent může upozornit na rozpor, nesplnitelnou podmínku, chybné očekávání nebo bezpečnější větev. Nesouhlas není automaticky selhání spolupráce.

### Ověření a uzavření

Výsledek se porovná s dohodnutými kritérii. Stav `hotovo` musí rozlišovat dokončenou práci, neověřený výsledek, částečné splnění a bezpečné zastavení.

### Učení

Trvalejší poznatek se zapíše do přirozeného domova. Historie se nepřepisuje jako současná pravda a jednotlivý incident se automaticky nemění v globální zákaz.

## 6. Autorita zdrojů

Jedna lineární hierarchie nestačí pro všechny druhy konfliktu:

- Bezpečnostní, právní, datové a oprávňovací hranice vymezují prostor, ve kterém lze jednat.
- Uvnitř tohoto prostoru určuje směr aktuální cíl a rozhodnutí oprávněného člověka.
- Ověřitelné skutečnosti mohou opravit lidský předpoklad i instrukci agenta.
- Kanonický projektový zdroj drží současný stav a přijatá rozhodnutí.
- Kontrakt konkrétní úlohy zpřesňuje rozsah, ale nemůže sám rozšířit oprávnění.
- Skilly, šablony, historická paměť a příklady nabízejí metodu a kontext. Bez nového rozhodnutí nepřepisují současný stav.

Při rozporu je proto užitečné nejdřív určit, zda jde o hranici, cíl, fakt, projektový stav nebo pracovní metodu. Mechanické použití pořadníku by mohlo zakrýt právě ten rozdíl, který je potřeba vyřešit.

## 7. Antivzory

- **Dokonči za každou cenu:** agent nemá legitimní stav `nelze`.
- **Prompt jako firewall:** zákaz existuje pouze v instrukci, ačkoli jej lze vynutit technicky.
- **Člověk jako razítko:** schválení je požadované bez srozumitelného popisu následků a možnosti zásah odmítnout.
- **Více kontextu je vždy lépe:** všechny skilly, historie a projekty se načtou bez ohledu na současnou úlohu.
- **Každá chyba se mění v pravidlo:** lokální selhání postupně uzavírají celý pracovní prostor.
- **Zelené testy dokazují správnost:** testuje se implementace, ale ne původní záměr, oprávnění nebo dopad.
- **Paměť jako paralelní pravda:** souhrn zastará, ale nadále přepisuje kanonický stav projektu.
- **Partnerství jako rovnost oprávnění:** relační jazyk zakryje skutečnou asymetrii odpovědnosti a následků.

