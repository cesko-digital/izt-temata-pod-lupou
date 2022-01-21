## Idea Témata pod Lupou 
Přidanou hodnotou Témat pod lupou je dát čtenářům možnost reálně něco změnit ve svém okolí a zároveň si vybudovat důvěru v novináře a média. Na straně druhé dát novinářům možnost poznat, co lidi opravdu nejvíce zajímá a zaměřit se tak na témata, která jim přinesou nejvíce čtenářů. Inspiraci našel tým u novináře Johna D. Suttera ze CNN, který takto zmobilizoval desetitisíce čtenářů. 

## Inovace Zpravodajského Storytellingu
Projekt vznikl ve spoluprácí Nadačního fondu nezávislé žurnalistiky a Česko.Digital. Cílem bylo navrhnout prototyp, který by dostat zpravodajství k lidem, kteří zprávy nečtou (dle [výzkumu](https://www.nfnz.cz/studie-a-analyzy/cesi-a-zpravodajstvi/) se jedná o více než 30 % populace). Zapojili jsme 150 expertních dobrovolníků a novináře z 10 redakcí. Ověřovali jsme si hypotézy, ptali se novinářů i mediálních domů. Idea chatbota zvítězila v konkurenci téměř stovky nápadů.

## Koncept v kostce
Témata pod Lupou je způsob, jak umožnit čtenářům participovat na výběru témat, které redakce zpracovávají. Redakce si vloží formulář pro sběr témat například na svou webovou stránku nebo do speciálního článku, kde vyzve čtenáře, aby se podělil o zajímavé téma ke zpracování, o čem se má psát. Po ukočení sběru vyhlásí redakce hlasování o nejlepší témata. Nejlepší témata pak redakce zpracuje a poděkuje autorům vítězných témat. Témata pod Lupou umožňuje sběr témat, včetně nahrání doprovodného materiálu jako jsou fotky či videa, a umožní redakcím procházet či stáhnout zaslaná témata.

<img width="642" alt="obrazek" src="https://user-images.githubusercontent.com/69157075/150546148-f84c7413-791d-47fe-a166-98ee9ad24ac6.png">

## Jak to funguje
Jak jsme náš prototyp testovali s redakci Drbna.cz najdete buď ve zkratce v [prezentaci](https://docs.google.com/presentation/d/1G5xDPy9cBN-K8Sk93r8C4FAU9HwOow2n/edit#slide=id.p4) nebo [případové studii](https://docs.google.com/document/d/1qQwiHLGnEgOeArn54oMb6n9xuWjT1cMnLMRvIdFVqDg/edit?usp=sharing).


# Návod k použití

Tato sekce obsahuje návod pro správnou konfiguraci systému, vytvoření a provoz sběru témat a stažení výsledků. Kroky potřebné k prvnotní instalaci platformy jsou uvedeny v dalších sekcích.

## Onboarding nové redakce

Jedna instalace platformy Témata pod lupou může obsluhovat i více redakcí. Pro každou redakci je nutné vytvořit prvotní obsah a dát členům redakce přístup k jejich části dat.

1. V sekci `Content` vytvořte dokument typu `Media` (= redakce)
    - Pro velké redakce můžete volitelně z dokumentů typu `Media` vytvořit hierarchii a lépe tak členit obsah a přístupová práva
1. Každé redakci (dokumentu typu `Media`) na nejvyšší úrovni (a nikoliv tedy vnořeným dokumentům téhož typu) přiřaďte doménu s unikátní cestou
    - Pravým tlačitkem kliněte na zvolenou redakci a stiskněte `Culture and Hostnames`
    - Do domén vložte požadovaný záznam ve tvaru `domena/cesta` např. `sber-temat.cz/zpravodaj-z-kocourkova`, vyberte požadovaný jazyk a kliněte na `Save`
1. V sekci `Media` vytvořte složky (`Folder`) tak, aby jejich struktura odpovídala struktuře dokumentů typu `Media` v sekci `Content`
    - Pod každou takto vytvořenou složkou vytvořte další stejného typu s názvem `Obsah od čtenářů`, kam se bude nahrávat uživatelský obsah z odeslaných formulářů 
1. V sekci `Users` vytvořte nové uživatele pro členy redakce
    - Členy vytvořte s právy skupiny `Editors`
    - V poli `Content start nodes` vyberte nově vytvořené relevantní dokumenty typu `Media` ze sekce `Content`
    - V poli `Media start nodes` vyberte nově vytvořené relevantní složky typu `Folder` ze sekce `Media`

## Vytvoření formuláře

Formulář pro sběr témate se vytvoří následovně:

1. Klikněte pravým tlačítkem na redakci, pod kterou chcete formulář vytvořit
1. Klikněte na `Create...`
1. Vyberte `Submission Widget`
1. V záhlaví formulář pojmenujte
1. Vyplňte všechna povinná pole
1. Stiskněte `Save and Publish`

Formulář si můžete prohlédnout a vyzkoušet kliknutím na odkaz v boxu `Links` pod kartou `Info`.

### Nastavení formuláře

Samotný formulář má spoustu polí, které je potřeba vyplnit, ale většinou se jedná o znění jednotilvých položek formuláře, doprovodného textu, tlačítek a výzev, a jejich zadání je vcelku jasné. Je zde ale pár speciálních polí, které mají vliv na fungování samotného sběru.

*Configuration*
- **Target Element ID**: ID elementu, před který se formulář vloží, viz kapitola Vložení formuláře na web

*Call to Action*
- **Display Call to Action**: Pokud je zaškrtnuto, formulář se nejprve zobrazí jako banner s výzvou k vyplnení formuláře. Po stisknutí tlačítka na banneru se rozbalí samotný formulář. Tato volba je vhodná zejména pokud má být formulář zobrazen u jiného obsahu, např u článku či v postranním panelu. Pokud tato volba není zaškrtnuta, formulář se zobrazí rovnou celý. To je vhodné například pokud je formulář vložen na svojí vlatní stránku na webu redakce.

*Media*
- **Media Store Folder**: Zde je třeba vybrat příslušnou složku ze sekce `Media`, do které se budou ukládat soubory odeslané spolu s formulářem.

## Vložení formuláře na web redakce

Redakce má na výběr ze tří možností, jak formulář uživateli nabídnout.

1. Přesměrovat uživatele přímo na stránku formuláře (adresa formuláře je v boxu `Links` pod kartou `Info`).
1. Zobrazit přímo na stránce redakce banner s výzvou, a po kliknutí rozbalit formulář pod tímto bannerem
    - Je nutné identifikovat místo ve zdrojovém kódu webové stránky, kam se bude banner vkládat, a nastavit pole `Target Element ID` daného formuláře. Příklad: Chceme banner vložit před komentáře. Jejich zdrojový kód začíná `<div id="comments">`, do pole `Target Element ID` tedy dáme `comments`.
    - Do zdrojového kódu webu redakce umístíme nový `script` tag pro vložení formuláře. Adresa skriptu začíná adresou foruláře a je k ní přidáno `/embed`. Příklad: `<script src="https://sber-temat.cz/zpravodaj-z-kocourkova/prvni-formular/embed" />`
1. Zobrazit formulář na samostatné stránce redakce
    - Postupujte jako při kroku 2., ale v nastavení formuláře odškrtněte volbu `Display Call to Action`

## Výsledky

Odeslané odpovědi se uloží jako nové dokumenty pod samotný formulář. Tyto odpovědi lze upravovat a mazat dle potřeby.

Odpovědi je také možné stáhnout ve formátu CSV a dále zpracovávat např v Excelu či Google Sheets, a to výběrem položky `Download Submissions` pro stisku relevantního formuláře pravým tlačítkem.

# Instalace pro ostrý provoz

K instalaci je potřeba pomoc od IT oddělení - odborníka, ale instalace samotná není složitá. Jedná se o klasický ASP.NET MVC projekt a může běžet jak v cloudu (Azure) nebo na vlastním serveru (IIS). 

Tato platforma používá CMS systém Umbraco 8 a z tohoto důvodu vyžaduje operační systém Windows. V době psaní tohoto návodu je již dostupné Umbraco verze 9, které běží na Linuxu, ale tato platforma zatím na verzi 9 nebyla aktualizována.

Pro databázi se doporučuje MS SQL Server. Pro menší redakce je ale možné použít vestavěný SQL CE. Je nutné ale ověřit správné nastavení v souboru Web.config a po prvnotním spuštení a natavení systému spustit uSync, který v prázdné databázi vytvoří všechny stavební bloky platformy Témata pod lupou.

# Vývoj

## Nástroje

- IDE, vyber jeden z:
  - Visual Studio 2019 Community Edition, behem instalace vybrat
    - ASP.NET and web development workload
  - JetBrains Rider
  - VS Code (nezkouseno, budou potreba nejake plugins)

## Instalace

1) Otevri slozku src\TemataPodLupou.Web\App_Data
1) Vytvor kopii souboru UmbracoSeed.sdf jmenem Umbraco.sdf
1) Otevri solution (src\TemataPodLupou.sln) ve svem oblibenem IDE
1) Spust projekt TemataPodLupou.Web
1) Otevre se prohlizec s URL webu, napr https://localhost:44367
1) Prihlas se do backoffice na `/umbraco`
    - Uzivatel: `admin@tematapodlupou.cz`
    - Heslo: `H78WFWRUdyFUVMb0IFBW`
1) V sekci Users si vytvor vlastniho uzivatele
1) Prihlas se pod vlastim uzivatelskym uctem
1) V sekci Settings klikni na `uSync` a pak na tlacitko `Import`

## Testovací obsah

1) V sekci `Media` vytvor slozku a pojmenuj ji Uploads
1) V sekci `Content` vytvor obsah typu `Media`, ktery reprezentuje redakci
    1) Pro ulozeni je potreba kliknout na `Save and Publish`
1) Pod redakci vytvor obsah typu `Submission Widget`
    1) Vypln vsechny pole, v poli `Media Store Folder` vyber predem vytvorenou slozku Uploads
    1) Klikni na `Save and Publish`
1) Zobraz formular v prohlizeci
    1) Po ulozeni se preklinki na zalozku `Info` a klikni na odkaz v boxu `Links`
1) Vypln formular a odesli
1) Odeslana data se zobrazi v sekci `Content` pod formularem, ktery byl odeslan
    1) Muze byt nutne zmacknout na formular pravym tlacitkem a vybrat `Reload` 

V případě problémů založte issue.
