
  
# 2. Skupinová práce - Dokumentace k řešení

## Nejde kliknout na zavřít po uložení na mobilu

  

  

  

### Oprava tlačítka

Při editaci firmy na mobilu tlačítko nereaguje. Stačilo smazat jednu část css konkrétně v souboru <em>css/forms-style.css.</em> a tlačítko normálně fungovalo.
  

```css
.form .label {
 font-weight: bold;
  color: black;
  padding-top: 0; 
  padding-left: 0;
  letter-spacing: 0.025em;
  font-size: 1.125em;
  line-height: 1.25; position: relative;
  /* z-index: 100; */ // Tento řádek je potřeba smazat pro normální funkci tlačítka
```

  

  
  

  
  

## Tlačítko vyhledávače šoupnout do leva aby bylo vidět při editaci firmy

  
Cílem tohoto úkolu bylo nastavit tlačítko, Vyhledávací pole není vidět při editaci firmy. Upravili jsme část tohoto kódu: 


```css
 #basic_filter label 
{ 
position: absolute;
left: 0vw;
top:60px; 
min-width: 125px;
max-width: 130px; }

 #basic_filter input 
 { 
 min-width: 105px;
 max-width: 110px; }
 
 #basic_length.dataTables_length
 { 
 margin-bottom: 57px; }

```

## Vyhledávátko u událostí 

U událostí po vymazání vyhledávaného slova se nic nestane se seznamem firem. Zrušit tam pamatování uloženého. Takto jsme vyřešili daný problém:

Lehce jsme editovali tableEvents.php file, neliknovalo se css tím pádem to celý nefungovalo, stačilo doplnit tečku na 7. řádek, aby se správně linklo css php a potom to začalo fungovat.

 
```html
<link rel="stylesheet" href="../min/style.min.css"> //Editovany radek
```

  

## Lepší menu
Posledním úkolem bylo, že položky menu jsou na sebe namačkané a celkově menu je nepřehledné. V souboru css jsme editovali řádek 117 a upravili margin z 0px na 2px.

```css

#basic_wrapper  .bn49, #basic_filter  input, #delete-btn, #export-btn, #basic_wrapper select, #basic_wrapper option, #basic_wrapper  label 
{ 
border: 0;
 text-align: center;
  padding: 8px;
  margin: 2px; /* zlepseni menu */ 
  font-size: 14px;
  max-height: 50px;
  color: #ffffff;
  background-color: #36a2eb;
  border-radius: 8px;
  font-family: "proxima-nova-soft", sans-serif; 
  font-weight: 600;
  text-decoration: none;
  transition: box-shadow 200ms ease-out; } 
```

