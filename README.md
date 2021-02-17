# 01-04-01-GlassPaiting
Osztályhierarchia. Tulajdonságok. 
Poharak festése projekt.     
Poharak festése (GlassPainting)    
Egy nagyüzemben poharakat festenek egy színnel. A megrendelések különböző számú poharakra vonatkoznak, amelyeket ugyan avval a színnel kell befesteni. A tervezők feladata annak a színmennyiségnek a megbecsülése, amely a poharak festéséhez szükséges. Ehhez a projekthez fejlesztünk ki egy osztályt.     
A poharak alja egy kör, oldala egy hengerszerű alakzat oldala (palást). A pohár festése előtt ismert a pohár aljának sugara és a pohár magassága centiméterben. A pohárnak füle nincs.    
A szakértők a következő képlettel határozzák meg:   
```
festékmennyiség=(((kör területe+ hengerszerű alakzat területe) * 0,005 liter ) *1,1)*db     
```
(mivel 5 ml festék kerül egy négyzetcentiméter felületre, 10%-al többet kell rakni a gépbe, hogy megfelelően működjön).     
Készítse el a PaintedGlasses osztályt, amelynek két ismert adata a kör sugara és a pohár magassága, valamint a poharak darabszáma. Az osztálynak legyen egy requiredPaintQuantity tulajdonsága, amely egy lekérhető tulajdonságú adat, és megadja a szükséges festék mennyiséget.     
A segédszámítások elvégzésére használjon egy kör (circle) osztályt, amely sugarával meghatározható, és amelynek két leolvasható metódusa a kör területe (area) és a kör kerülete (district).    

![Henger felszíne](https://cms.sulinet.hu/get/d/c5ce84d6-1630-408b-ab4a-b1653a8a2484/1/6/b/Normal/c06aa006.jpg)

Teszt kód:
```
double radius=2.5;
Circle c=new Circle(radius);
Console.WriteLine(c);
glassesHeight=4;
numberOfGlasses=50;
PaintedGlasses pg=new PaintedGlasses(c,glassesHeight,numberOfGlasses)
Console.WrtiteLine(pg);
```


Kimenetek:
A kiírások előtt a számított eredményeket egy tizedes jegyre kerekítse.
1.
Console.WriteLine(c); kód esetén:
A kör sugara 2.5 cm, a kör kerüte xx.xx cm, a területe xx.xx nétgyzetcentiméter.
2.
Console.WrtiteLine(pg); kód esetén:
50 db, 4 cm magas pohár szükséges festékmennyisége xx.xx liter.
