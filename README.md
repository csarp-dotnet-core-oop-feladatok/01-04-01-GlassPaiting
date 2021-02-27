# 01-04-01-GlassPaiting
Osztályhierarchia. Tulajdonságok. 
Poharak festése projekt.     
Poharak festése (GlassPainting)    
Egy nagyüzemben poharakat festenek egy színnel. A megrendelések különböző számú poharakra vonatkoznak, amelyeket ugyan avval a színnel kell befesteni. A tervezők feladata annak a színmennyiségnek a megbecsülése, amely a poharak festéséhez szükséges. Ehhez a projekthez fejlesztünk ki egy osztályt.   
A poharak alja egy kör, oldala egy hengerszerű alakzat oldala (palást). A pohárnak füle nincs.    
A segédszámítások elvégzésére használjon egy kör (circle) osztályt, amely sugarával meghatározható, és amelynek két leolvasható metódusa a kör területe (area) és a kör kerülete (district).  
Készítse el a PaintedGlasses osztályt. A pohár alja egy kör. Adott egy pohár magassága valamint a poharak darabszáma.  
Készítsen konstruktort.  
Az osztálynak legyen egy RequiredPaintQuantity tulajdonsága, amely egy lekérhető tulajdonságú adat, és megadja a szükséges festék mennyiséget.     
A szakértők a következő képlettel határozzák meg a festékmennyiség kiszámítására:    
```
festékmennyiség=(((kör területe+ hengerszerű alakzat területe) * 0,05 liter ) *1,1)*db    
```
(mivel 5 cl festék kerül egy négyzetcentiméter felületre, 10%-al többet kell rakni a gépbe, hogy megfelelően működjön).     


![Henger felszíne](https://cms.sulinet.hu/get/d/c5ce84d6-1630-408b-ab4a-b1653a8a2484/1/6/b/Normal/c06aa006.jpg)

Teszt kód:
```
            double glassesHeight = 4;
            int numberOfGlasses = 50;
            Circle c = new Circle(2.5);
            Console.WriteLine(c);
            PaintedGlasses pg = new PaintedGlasses(c, glassesHeight, numberOfGlasses);
            Console.WriteLine(pg);
```
Kimenetek:  
A kiírások előtt a számított eredményeket egy tizedes jegyre kerekítse.  
1.  
Console.WriteLine(c); kód esetén:  
A kör sugara 2.5 cm, a kör kerüte 15,7 cm, a területe 19,6 nétgyzetcentiméter.  
2.  
Console.WrtiteLine(pg); kód esetén:  
50 db, 4 cm magas pohár szükséges festékmennyisége 226,8 centiliter. 
