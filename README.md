# WIP

# HögskoleProvet
 Ett dataset på svenska HP för att testa modeller. Allt kan struktureras om och ändras. Jag har mest räsat på i den takt jag kunnat med lite reflektion kring tillvägagångsätt. Jag har tyvärr inte riktigt med tid för att göra allt som krävs för att göra den verbala delen av Högskolprovet så bra som möjligt. Om ni själva vill köra experiment eller hjälpa andra att göra experiment så är detta en intressant uppgift på svenska
 
## Hjälp

Hallå!
Har automatiserat en del av processen med att formatera datan men det görs missar och hade varit bra om det gicks igenom av en människa. Det som behöver göras är att få in facit och läsförståelsetexterna, samt kolla OCR-missar i frågorna och alternativen.
  
Är man många som gör det så får vi snabbt ihop det med så lite individuellt mänskligt lidande som möjligt. Är du en gud på OCR eller har koll på verktyg så är du varmt välkommen att ta fram en smidigare pipeline

I done finns färdiga prov att kika på hur de skall vara formaterade

I raw finns alla prov ostädade

- Dessa är inskannade och ocrade, det finns fel i dem. Främst så försvinner i och f.
- Har svaret fler än två rader har den missat sista raden
- Radbryt har alltid ett - som markerar raden. Detta måste tas bort
- Alla läsförståelsetexter har problem med kolumnordningen så man måste försiktigt kopiera bit för bit. Rekommenderar starkt  multiple cursors för detta
- Ibland plockar den upp --9-- och sådant i alternativen, men detta borde bara hända ett par gånger
- Kolumnordningen för orden är fel så radordning/ID matchar inte facit, detta innebär att man måste sortera orden först efter hur det ser ut i PDFen
- Ibland plockar den inte upp sista frågan(fråga 40)

exempel på engelska MEK:
```
"article": "Loneliness is not good for long-distance runners, or anyone else who exercises regularly. That’s the conclusion suggested by an experiment showing that animals _____ better with stress hormones released by physical activity if they have company when they exercise. Although exercise speeds the production of new brain cells, it also raises the level of the stress hormone corticosterone, which by itself has _____ effect. Since social contact helps to reduce stress in many animals, including humans, Elizabeth Gould and fellow psychologists at Princeton University asked whether social contact affects neuron development in rats after they exercise. Some of the rats were housed in groups of three; the rest were housed alone. Half of each group were allowed a daily _____ on an exercise wheel, while the others got no exercise. The researchers measured the levels of corticosterone in the rats’ blood twice a day, and after 12 days they measured neuronal development in the hippocampus, the seat of learning and memory in the brain. After exercise, corticosterone levels _____ by the same amount in the rats that had company as in the isolated rats. However, cell growth in the brains of the group that exercised was faster than in the sedentary rats, and fastest in the rats that exercised and had company. According to Gould, this _____ the idea that social support helps to lessen the negative consequences of stress. New Scientist",
```

jag har kört den här fulregexen med find and replace:
```
        \b(\d+)        
```
```
_____
```
 
## Facit och texter
https://xn--allartt-9wa.nu/ladda-ner-gamla-hogskoleprov.asp



# Hjältar som hjälpt till att städa
Tack till Andreas Forsberg och Filip Sörlin

