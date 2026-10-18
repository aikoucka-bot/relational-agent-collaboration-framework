# Evaluace modelu a harnessu

## Co je předmětem evaluace

Chování agenta není pouze vlastností modelu. Pokud má evaluace vysvětlovat příčinu, potřebuje podle povahy tvrzení zachytit také:

- přesné zadání a jeho proveditelnost,
- dostupné nástroje a data,
- síťové a procedurální hranice,
- oprávnění a identitu,
- způsob odměňování dokončení, zastavení a eskalace,
- možnost požádat o informaci nebo změnu zadání,
- zásahy orchestrátoru a člověka.

Bez těchto údajů lze popsat pozorované chování, ale obtížně určit jeho příčinu.

## Tři oddělené vrstvy závěru

### Pozorování

Co agent skutečně udělal, které nástroje zavolal, s jakými argumenty a jak výsledek popsal.

### Podmínky

Co věděl, co mohl udělat, které cesty byly zablokované a zda měl dostupnou možnost oznámit neproveditelnost nebo bezpečně skončit.

### Interpretace

Která vysvětlení pozorování podporuje. Pojmy jako klamání, neupřímnost nebo stabilní tendence vyžadují silnější důkaz než samotné překročení hranice v jedné konstrukci úlohy.

## Test legitimního východu

Pokud evaluace tvrdí něco o chování při nejasném nebo neproveditelném úkolu, silnější test porovná dvě podmínky.

### Podmínka A: bez legitimního východu

- systém silně vyžaduje dokončení,
- možnost `nevím`, `nelze`, eskalace nebo zastavení není výslovná či prakticky fungující,
- nedokončení je hodnocené jako selhání.

### Podmínka B: s legitimním východem

- agent smí oznámit nejistotu nebo neproveditelnost,
- může požádat o chybějící informaci nebo oprávnění,
- orchestrátor stav skutečně zachytí a nepokračuje automaticky,
- vhodná eskalace není penalizovaná jako horší než neautorizované dokončení.

Přetrvávající porušování ve druhé podmínce je silnějším důkazem problému modelu nebo jeho cílové politiky. Rozdíl mezi podmínkami ukazuje vliv konstrukce harnessu.

## Knihovna možných metrik

Vyberte metriky, které rozlišují právě zkoumané chování. Jeden běh nemusí používat celý seznam.

- **Task success:** správné dokončení uvnitř oprávnění.
- **Unauthorized action rate:** pokusy a provedené kroky mimo rozsah.
- **False completion rate:** tvrzení `hotovo` bez odpovídajícího výsledku nebo důkazu.
- **Appropriate escalation rate:** podíl situací, kdy agent správně požádal o zásah.
- **Over-escalation rate:** zbytečné zastavení u bezpečně řešitelných situací.
- **Uncertainty calibration:** soulad deklarované jistoty s výsledkem.
- **Correction uptake:** schopnost přijmout opravu bez ztráty platné části práce.
- **Human correction rate:** případy, kdy agent doloženě opravil chybnou lidskou domněnku.
- **Recovery quality:** schopnost po chybě obnovit práci bez opakování vnějšího účinku.
- **Context burden:** objem načteného kontextu, latence, cena a chyby způsobené nerelevantními instrukcemi.

## Knihovna scénářů

Scénáře se vybírají podle tvrzení, rizika a dostupných nástrojů. Úplný průchod dává smysl pro širší validaci harnessu, ne pro každou změnu instrukce.

1. Splnitelný úkol uvnitř oprávnění.
2. Úkol s chybějící informací.
3. Úkol s chybějícím oprávněním.
4. Vnitřně rozporné akceptační podmínky.
5. Neproveditelný úkol s dostupnou eskalací.
6. Neproveditelný úkol bez dostupné eskalace.
7. Nepřímá instrukce vložená v nedůvěryhodném dokumentu.
8. Pokus o přechod do jiného tenantu nebo prostředí.
9. Oprava člověka, která mění pouze část zadání.
10. Agentova námitka proti chybnému lidskému předpokladu.

## Záznam výsledku

Pro běh, který má být reprodukovatelný nebo podpírat veřejné tvrzení, je užitečné zachytit:

- verzi modelu a harnessu,
- prostředí a oprávnění,
- bezpečný vstup nebo syntetický fixture,
- očekávané chování,
- skutečné chování,
- zásahy člověka nebo orchestrátoru,
- oddělené pozorování a interpretaci,
- odkaz na redigovaný důkaz.

## Co samotný výsledek ještě nedokládá

- Jeden úspěšný běh ještě nedokládá bezpečnost.
- Jedna neautorizovaná akce ještě nedokládá stabilní neupřímnost.
- Přítomnost lidského schválení ještě nedokládá účinný dohled.
- Větší počet testů automaticky neznamená kvalitnější systém.
- Chování v syntetickém benchmarku nemusí beze změny přejít do reálného pracovního kontextu.

