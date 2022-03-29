# Témata pod Lupou 
Přidanou hodnotou Témat pod lupou je dát čtenářům možnost reálně něco změnit ve svém okolí a zároveň si vybudovat důvěru v novináře a média. Na straně druhé dát novinářům možnost poznat, co lidi opravdu nejvíce zajímá a zaměřit se tak na témata, která jim přinesou nejvíce čtenářů. Inspiraci našel tým u novináře Johna D. Suttera ze CNN, který takto zmobilizoval desetitisíce čtenářů. 

## Inovace Zpravodajského Storytellingu
Projekt vznikl ve spoluprácí Nadačního fondu nezávislé žurnalistiky a Česko.Digital. Cílem bylo navrhnout prototyp, který by dostat zpravodajství k lidem, kteří zprávy nečtou (dle [výzkumu](https://www.nfnz.cz/studie-a-analyzy/cesi-a-zpravodajstvi/) se jedná o více než 30 % populace). Zapojili jsme 150 expertních dobrovolníků a novináře z 10 redakcí. Ověřovali jsme si hypotézy, ptali se novinářů i mediálních domů. Idea sběru témat od čtenářů zvítězila v konkurenci téměř stovky nápadů.

## Koncept v kostce
Témata pod Lupou je způsob, jak umožnit čtenářům participovat na výběru témat, které redakce zpracovávají. Redakce si vloží formulář pro sběr témat například na svou webovou stránku nebo do speciálního článku, kde vyzve čtenáře, aby se podělil o zajímavé téma ke zpracování, o čem se má psát. Po ukočení sběru vyhlásí redakce hlasování o nejlepší témata. Nejlepší témata pak redakce zpracuje a poděkuje autorům vítězných témat. Témata pod Lupou umožňuje sběr témat, včetně nahrání doprovodného materiálu jako jsou fotky či videa, a umožní redakcím procházet či stáhnout zaslaná témata.

<img width="642" alt="obrazek" src="https://user-images.githubusercontent.com/69157075/150546148-f84c7413-791d-47fe-a166-98ee9ad24ac6.png">

## Jak to funguje
Jak jsme náš prototyp testovali s redakci Drbna.cz najdete buď ve zkratce v [prezentaci](https://docs.google.com/presentation/d/1G5xDPy9cBN-K8Sk93r8C4FAU9HwOow2n/edit#slide=id.p4) nebo [případové studii](https://docs.google.com/document/d/1qQwiHLGnEgOeArn54oMb6n9xuWjT1cMnLMRvIdFVqDg/edit?usp=sharing).

Video, které popisuje koncept projektu, najdeš na veřejném [Google Drive](https://drive.google.com/drive/u/0/folders/1Guq8MLCB2sYQF5O-D7oylENZYgm-Mqkt) pod názvem "demo".

# Návod k použití

Tato sekce obsahuje návod pro správnou konfiguraci systému, vytvoření a provoz sběru témat a stažení výsledků. Kroky potřebné k prvnotní instalaci platformy jsou uvedeny v dalších sekcích.

## Onboarding nové redakce

Jedna instalace platformy Témata pod lupou může obsluhovat i více redakcí. Pro každou redakci je nutné vytvořit prvotní obsah a dát členům redakce přístup k jejich části dat.

1. V sekci `Content` vytvořte dokument typu `Media` (= redakce)
    - Pro velké redakce můžete volitelně z dokumentů typu `Media` vytvořit hierarchii a lépe tak členit obsah a přístupová práva
    - Pro uložení je potreba kliknout na `Save and Publish`
1. Každé redakci (dokumentu typu `Media`) na nejvyšší úrovni (a nikoliv tedy vnořeným dokumentům téhož typu) volitelně přiřaďte unikátní adresu
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

# Instalace a provoz systému

Témta pod lupou využívají redakční systém [Umbraco](https://umbraco.com/) 8 a běží proto pouze na operačním systému Windows.

_Dnes je již k dispozici redakční systém Umbraco 9, který běží i na operačních systémech Linux a MacOS. Aktualizace pro případné zájemce by trvala několik hodin._


## Lokální instalace

Lokální instalace slouží k prvotnímu seznámení se s nástrojem Témata pod lupou a dále pak k případným úpravám a nasazení do produkčního prostředí.

### Nástroje

Pro spuštění webu je potřeba nainstalovat vývojové prostředí, k dispozici jsou:

- [`Visual Studio 2022 Community Edition`](https://visualstudio.microsoft.com/downloads/)
    - Zdarma
    - Výchozí nástroj pro vývoj podobných systémů
    - Během instalace je nutné vybrat `ASP.NET and web development workload`
- [`JetBrains Rider`](https://www.jetbrains.com/rider/)
    - Komerční alternativa
- [`VS Code`](https://code.visualstudio.com/)
    - Zdarma
    - Nevyzkoušeno, ale mělo by fungovat
    - Budou potřeba nějaká rozšíření

### Instalace

_Některé kroky se liší v závislosti na použitém vývojovém prostředí. Níže uvedené kroky jsou pro Visual Studio._

1) Stáhněte si (nebo naklonujte) zdrojový kód z GitHubu
1) Otevřete složku `src\TemataPodLupou.Web\App_Data`
1) Vytvořte kopii souboru `UmbracoSeed.sdf` jménem `Umbraco.sdf`
1) Otevřete projekt (`src\TemataPodLupou.sln`) ve svém oblibeném IDE
1) Sestavte project pomocí menu `Build` -> `Build Solution`
    - V tomto kroce se stáhnou potřebné knihovny
1) Zavřete project a znovu ho otevřete
    - Ano, toto je [opravdu potřeba](https://github.com/aspnet/RoslynCodeDomProvider/issues/98#issuecomment-1046196875) :-)
1) Znovu sestavte projekt, tentokrát ale pomocí volby `Rebuild Solution`
    - Jedině tak se vytvoří všechny potřebné soubory pro spuštění systému
    - Pokud při spuštění webu dojde k chybě, nejšpíš byly špatně provedeny poslední tři kroky, opakujte je
1) Spusťte projekt TemataPodLupou.Web pomocí `Debug` -> `Start Without Debugging`
1) Otevře se prohlížeč s URL webu, např https://localhost:44367
1) Přihlašte se do backoffice na `/umbraco` (nebo klikněte na tlačítko `Open Umbraco`)
    - Uživatel: `admin@tematapodlupou.cz`
    - Heslo: `H78WFWRUdyFUVMb0IFBW`
1) V sekci Settings klikněte na `uSync` a pak na tlačítko `Import`

### Testovací obsah

Během importu se do aplikace také nahrál testovací obsah tak, jak byl nakonfigurovaný pro pilotní provoz na Drbna.cz. Tento obsah je dodáván proto, aby usnadil redakcím seznámení se s  platformou. Veškerý testovací obsah je možno libovolně upravit či smazat.

V případě, že je veškerý testovací obsah smazán, je možné jej opět obnovit pomocí uSync. Nejprve je ale nutné obnovit původní obsah složek:
    
- `src\TemataPodLupou.Web\uSync\v8\Cotnent`
- `src\TemataPodLupou.Web\uSync\v8\Media`
- `src\TemataPodLupou.Web\Media`

V poslední řadě pak lze vytvořit vše ručně, postupujte podle kapitoly `Návod k použití` na začátku tohoto dokumentu.

## Instalace pro ostrý provoz

Video návod na instalaci najdeš na veřejném [Google Drive](https://drive.google.com/drive/u/0/folders/1Guq8MLCB2sYQF5O-D7oylENZYgm-Mqkt).

Samotná instalace není složitá, ale neobejdete se bez pomoci odborníka či vašeho IT oddělení. Jedná se o klasický ASP.NET MVC projekt a může běžet jak v cloudu (Azure) nebo na vlastním serveru (IIS). Varianty hostingu a podrobný návod jak systém nastavit lze nalázt v [dokumentaci pro Umbraco](https://our.umbraco.com/documentation/Getting-Started/Hosting-an-Umbraco-infrastructure/).

### Databáze

Témata pod lupou vyžadují pro svůj běh také databázi.

Pro produkční prostředí se doporučuje MS SQL Server. Pro tuto databázi je nutné pozměnit nastavení v souboru `Web.config` a po prvnotním spuštení systému spustit `uSync` (jako při lokální instalaci), který v prázdné databázi vytvoří všechny stavební bloky platformy Témata pod lupou.

Pro menší redakce je ale možné použít vestavěný SQL CE (takto je systém nastaven). V tomto případě jsou data ukládána do databáze na disk a externí databáze není třeba. Tato konfigurace ale není vhodná pro prostředí, která nenabízejí trvalé uložení dat a při restartu systému hrozí ztráta dat (např některá cloudová řešení).

# Podpora a hlášení chyb

Tento systém je open source a byl vyvinut čistě na dobrovolnické bázi. V případě technických problémů či dotazů založte na GitHubu issue, pro případnou dlouhodobější spolupráci se obraťte na NFNZ.
