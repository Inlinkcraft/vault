---
name: Algorithme de parcours en profondeur dun graph
type: Matière
---
#GLO-2100 

Plusieurs version de l'agorithme existe ici regroupe quelque versions

### Version de base
---
```pseudocode
BEGIN explore(v): // un sommet v d'un grapgh
    POUR TOUT u FAIRE visité[u] = faux;
    visité[v] = vrai;
    P.EMPILER(v)
    
    TANT QUE P != {}:
        u = P.DEPILER();
        
        // DO SOMETHING
        
        FOR u' VOISIN DE u DO
        IF visiter[u'] == faux THEN
            visité[u'] = vrai;
            P.EMPILER(u');
```

### Version recursive
---
```pseudocode
BEGIN explore(v): // un sommet v d'un grapgh
    visiter[v] = vrai;
    
    // DO SOMETHING
    
    FOR TOUT u VOISIN DE v DO
        IF visiter[u] == faux THEN
            CALL explore(u)
```

### Version avec clock
---
```pseudocode
BEGIN explore(v): // un sommet v d'un grapgh
    début[v] = clock;
    clock++;
    visiter[v] = vrai;
    
    FOR TOUT u VOISIN DE v DO
        IF visiter[u] == faux THEN
            CALL explore(u)
    
    fin[v] = clock;
    clock++;
    P.empliler(v)
    
```

> [!Info]
> Trier le résultât par la valeur de fin donne un [[Tri-topologique]]. Le dernier nœud empiler sera une source.
