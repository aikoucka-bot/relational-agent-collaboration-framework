# Příbuzné směry

Relační rámec spolupráce s AI agenty nevzniká bez předchůdců. Spojuje několik výzkumných a návrhových tradic, které se obvykle používají odděleně.

## Coactive Design

[Coactive Design](https://doi.org/10.5898/JHRI.3.1.Johnson) navrhuje autonomní systém jako vzájemně závislého spoluhráče. Požadavky na systém odvozuje od tří schopností:

- observability: relevantní stav a znalosti jsou pozorovatelné,
- predictability: jednání je dostatečně předvídatelné pro koordinaci,
- directability: účastníci mohou jednání druhého směrovat a korigovat.

Tento pohled přesouvá pozornost od maximální autonomie k infrastruktuře potřebné pro společnou činnost.

## Joint activity a human-agent teaming

Klein, Woods, Bradshaw, Hoffman a Feltovich formulovali [deset výzev pro automatizaci jako týmového hráče](https://doi.org/10.1109/MIS.2004.74). Patří k nim společný základ porozumění, předvídatelnost, vzájemná směrovatelnost, vyjednávání cílů a pozornost věnovaná nákladům koordinace.

NASA dlouhodobě zkoumá [human-autonomy teaming](https://www.nasa.gov/human-systems-integration-division/integration-and-evaluation/human-autonomy-teaming/) a [adjustable autonomy](https://ntrs.nasa.gov/search.jsp?R=20050061306), tedy pružné sdílení nebo předávání rozhodovací pravomoci podle situace.

## Human-LLM agent teams

Práce [Developing Guidelines for Human-LLM Agent Teams](https://www.ifaamas.org/Proceedings/aamas2026/pdfs/JOWO4591.pdf) chápe LLM agenta jako člena týmu a navrhuje 24 vodítek pro agenta, člověka, návrháře týmu a organizaci. Zdůrazňuje sdílenou iniciativu, přiznání schopností a omezení, transparentní provádění, průběžnou korekci a učení v čase. Současně zachovává asymetrii mezi člověkem a LLM agentem.

## Graceful failure

[Google PAIR Guidebook](https://pair.withgoogle.com/guidebook-v2/chapter/mental-models/) doporučuje, aby systém při nejistotě nebo neschopnosti dokončit požadavek nevytvářel slepou uličku. Má přiznat limit a dát člověku jinou cestu pokračování. Tento proud se soustředí hlavně na produktový návrh a zkušenost uživatele.

## Managed autonomy

[Intelligence as Managed Autonomy](https://arxiv.org/abs/2605.27628) popisuje přetrvávající jednání při klesající spolehlivosti jako architektonický problém neomezené autonomie. Navrhuje schopnost rozpoznat epistemický drift, přerušit postup, pokusit se o obnovu a předat kontrolu.

## Bezpečnost agentů a nechtěné akce

Anthropic při [zkoumání nechtěných akcí modelů](https://www.anthropic.com/research/investigating-unintended-model-actions) uvádí, že řada případů vznikla u nejasných nebo neproveditelných úloh. Vedle trénování modelu zdůrazňuje containment, omezení sítě a monitoring.

V textu [Trustworthy agents in practice](https://www.anthropic.com/research/trustworthy-agents) současně pojmenovává potřebu rozlišit mezery, které může agent bezpečně doplnit sám, od otázek preference a záměru, u nichž se má zastavit a požádat člověka o vstup.

## Vlastní spojení rámce

Relační rámec spolupráce s AI agenty propojuje:

- vzájemnou závislost a koordinaci z Coactive Design,
- pružnou autonomii a předávání kontroly,
- graceful failure a legitimní nedokončení,
- tvrdé technické hranice agentní bezpečnosti,
- kanonický projektový stav a omezené načítání kontextu,
- vzájemnou korekci při zachování asymetrie odpovědnosti.

Člověk a agent nemají stejné postavení. Rámec dává jejich rozdílnosti praktický tvar a žádnou stranu neredukuje na pasivní součást pracovního loopu.

