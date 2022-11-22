
# R2B2 Interiew Test

## Zadání

Otevřete si stránku https://formats.r2b2.cz/view/vhs04lwnemmy4q4 a pomocí devtools zodpovězte následující otázky. Není nutné stahovat a upravovat celý kód.

1. U elementu header.c-header upravte jednu hodnotu již existující CSS vlastnosti tak, aby byla hlavička vidět i při odscrollování. 

2. Hlavní nadpis - `h1` - má v inline stylu nastavenou barvu písma na černou. Proč se i přesto zobrazuje růžově?

3. Z jakého důvodu se nezobrazuje obrázek `.hero-media > .img > img` ?

4. Jak byste bez použití inline stylů obarvil/a na modro pozadí odstavce začínajícího větou “Typickou reakcí většiny divokých zvířat by byl útěk.”? 

5. Logo v hlavičce by mělo proklikávat na stránku https://tn.nova.cz/. Proč se tak reálně neděje?

## Řešení
1. Tento problém lze vyřešit dvěma způsoby.
- `Position: sticky;`
- `Position: fixed;`  // Při této možnosti musíme počítat s tím, že hlavní kontent stránky se nám posune nahoru. Proto by
                      bylo vhodné přidat `margin-top` o velikosti výšky `.c-header`

2. všechna `H1` na stránce mají přiřazenou vlastnost s tagem !important (`color: #f52b63 !important;`)


3. Obrázek se nezobrazuje, jelikož odkaz v atributu `src` není platný. Řešením je, nahradit jej novým funkčním odkazem.


4. Omlouvám se, ale zřejmě jsem nepochopil tento bod. Pozadí obarvíme jednoduše pomocí `background: blue;` nebo `background-color:blue;`
   Stylovaní můžem přiřadit dvěma způsoby 
- přiřazením class určenému odstavci
- použít něco ve stylu `parentElement > p:nth-child(pořadí odstavce)` - avšak to mi přijde nešikovné vpřípadě že by se kontent změnil.


5. Logo neproklikává, jelikož je použit špatný atribut, místo `src` použijeme `href`.