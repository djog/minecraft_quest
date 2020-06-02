# minecraft_quest

Minecraft wedstrijd.

## Doel

 * Samenwerken
 * Gebruiken GitLab

## Server

 * `djog.hosthorde.net`

## Scheidsrechters

 * Joshua
 * Richel

## Moderators

 * Daan
 * Joshua
 * Richel

## Hoe

### Bijeenkomst

Bijeenkomsten zijn wekelijks, op Discord.
Dit is het tijdschema:

Tijd       |Taak
-----------|---------------------------
18:00-18:15|Binnenkomst
18:15-18:45|Server open: warming up
18:45-19:00|Server dicht, voor herstart met nieuwe wereld
19:15-20:00|Server open voor wedstrijd
20:00-20:05|Winnaar wordt bekend gemaakt

Elk team heeft een eigen voicechatkanaal op de De Jonge Onderzoekers
Discord server.

### Teams

Er zijn twee teams: het rode en blauwe team. 

De wereld is verdeeld in twee helften:

 * `Rood`: gaat Rechts oftwel oostwaards
 * `blauW`: gaat West oftewel links

### Quest

De Quest is vantevoren bekend: deze wordt bepaalt door stemmen op GitLab.
Een voorbeeld: 'verzamel de meeste appels'.
Het team me de meeste punten wint.

### Moderators

Moderators zorgen ervoor dat je op de Minecraft server kunt inloggen.
Dit omdat we een whitelist hebben.

### Scheidsrechters

Scheidsrechters lopen vrij rond. 
ze hebben een groene skin.
Scheidsrechters kijken alleen maar.

Een scheidsrechter is altijd ook een moderator.

### Gedrag

 * Gedraag je als een goed teamlid
 * Teams zijn gescheiden
 * We zijn zuinig op de spullen van het team

## Vragen

### Hoe wordt de server ingesteld?

 * Spigot versie 1.15.2
 * Survival mode
 * Easy mobs
 * Geen cheats
 * Geen command blocks

### Waarom zo kort?

Deze tijd is expres kort, zodat je wel goed samen moet werken.

### Hoe worden de quests bepaalt?

Door te stemmen op de `minecraft_quest` GitLab.

### Wat is het maximaal aantal spelers?

16.

### Ik heb geen Minecraft

Helaas pindakaas :+1:

### Ik heb geen Minecraft Java Edition

Helaas pindakaas :+1:

### Voor welke leeftijd is dit?

Van 8 t/m 18 jaar.

### Ik wil meedoen, maar ik ben geen deelnemer van De Jonge Onderzoekers

Geen probleem: als er plek is, ben je welkom om mee te doen.

# Hoe maak je Teams aan

Commands voor de Minecraft Quest

## Maak de teams aan

```
/team add blauw "Blauw"
/team add rood "Rood"
/team add mod "Moderator"
```

## Zet de kleuren van de teams

```
/team modify blauw color blue
/team modify rood color red
/team modify mod color green
```

## Voeg enventueel nog een prefix toe

Let op de spatie achter de `[x] `: hierdoor zien de namen er mooier uit.

```
/team modify blauw prefix "[B] "
/team modify rood prefix "[R] "
/team modify mod prefix "[MOD] "
```

## Voeg iemand aan het team toe

```
/team join blauw spelernaam`
/team join rood spelernaam`
/team join mod spelernaam`
```

# Hoe maak je hoedjes voor de teams

Credits naar Joshua en Youri voor dit

## Hoedjes voor de teams

1e command block, zet op REPEAT & ALWAYS ACTIVE: (Voor team rood)

```
/replaceitem entity @a[team=rood] armor.head minecraft:leather_helmet{display:{Name:"{\"text\":\"Team rood\"}",color:16711680},Unbreakable:1,HideFlags:63,Enchantments:[{id:"minecraft:binding_curse",lvl:1}]}
```

2e command block, verbonden met 1e, zet op CHAIN & ALWAYS ACTIVE: (Voor team blauw)

```
/replaceitem entity @a[team=blauw] armor.head minecraft:leather_helmet{display:{Name:"{\"text\":\"Team blauw\"}",color:65535},Unbreakable:1,HideFlags:63,Enchantments:[{id:"minecraft:binding_curse",lvl:1}]}
```

3e command block, verbonden met 2e, zet op CHAIN & ALWAYS ACTIVE: (Voor moderators)

```
/replaceitem entity @a[team=mod] armor.head minecraft:leather_helmet{display:{Name:"{\"text\":\"Moderator hoed\"}",color:49706},Unbreakable:1,HideFlags:63,Enchantments:[{id:"minecraft:binding_curse",lvl:1}]}
```


## Haal de hoedjes weg

Doe met deze command of in een command block:

```
/replaceitem entity @a armor.head air
```

