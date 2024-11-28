---
name: Arbre binaires de recherche
type: Chapter
course: GLO-2100
---

# Arbres binaires de recherche

---

## Arbres binaires de recherche (de tri)
([[Chapitre-8.pdf#page=2&selection=4,0,8,21&color=yellow|Chapitre-8, p.2]])

- Peuvent être utilisés pour implémenter les dictionnaires. 
- Dictionnaire : conteneur d’éléments devant supporter efficacement les opérations suivantes: 
    - Insertion d’un élément 
    - Suppression d’un élément 
    - Trouver un élément (déterminer si un élément est présent) 
- s’effectuent en 𝑂(log 𝑛) lorsque l’arbre de 𝑛 éléments est équilibré

• Ce chapitre portera entièrement sur les arbres binaire de recherche qui supportent efficacement ces opérations en plus de conserver les éléments dans un ordre. 
    ➢ L’affichage des éléments en ordre croissant des valeurs de clé se fait à l’aide du parcours en-ordre. 
• Nous verrons en détail les arbres AVL 
    ➢ Arbres qui restent toujours équilibrés grâce à l’exécution de certaines opérations (rotations) lors des insertions et des suppressions d’éléments

### Implémentation ?

![[Chapitre-8.pdf#page=4&rect=584,285,742,424&color=red|Chapitre-8, p.4]]

```c++
template <typename E> 
class Arbre { 
public: 
    //méthodes publiques 
private: 
    // classe Nœud 
    class Noeud { 
        public: 
            E data; // la donnée est ici la clé 
            Noeud *gauche; 
            Noeud *droite; 
            int hauteur; 
            Noeud(const E & d): 
                gauche(0),data(d),droite(0),hauteur(0) { } 
    }; 
    // Les membres données 
    Noeud * racine; //racine de l'arbre 
    long cpt; // Nombre de noeuds dans l'arbre 
    // méthodes privées }
```
([[Chapitre-8.pdf#page=4&selection=14,0,166,1&color=red|Chapitre-8, p.4]])

#### Implantation par chaînage
- Puisque chaque nœud possède au maximum deux nœuds fils, on maintient un pointeur sur chacun d’eux.
- Avantages:
    - La taille de l’arbre est dynamique.
    - Facile d’opérer sur des pointeurs.
- Inconvénients:
    - On doit éviter les fuites de mémoire et les doubles références. 
    - Le parcours explicite de l’arbre ne se fait que de la racine vers les feuilles.
        - Mais il est possible de remonter vers la racine grâce aux retours d’appels récursifs.
([[Chapitre-8.pdf#page=5&selection=8,0,135,1&color=yellow|Chapitre-8, p.5]])

#### Identifiant des élément d'un arbre de tri
- Attribut data (de type E) de la classe Nœud
    - utilisé pour identifier les éléments dans l’arbre et appliquer la propriété d’ordonnancement de l’arbre de tri.
    - définit la clé (ie. l’identifiant) de l’élément
- Donc, pour tout nœud de l’arbre de tri, sa clé (champ data) doit être:
    - > aux clés des noeuds de son sous arbre de gauche
    - < aux clés des nœuds de son sous arbre de droite
- L’opérateur < doit être surchargé pour le type E.
    - C’est donc operator< du type E qui définit l’ordre utilisé par l’arbre de tri
([[Chapitre-8.pdf#page=6&selection=16,0,48,77&color=yellow|Chapitre-8, p.6]])
- Conteneur associatif: À la place du seul attribut data de la classe nœud, il est possible d’en avoir deux: un attribut clé (utilisé pour l’ordonnancement des éléments) et un attribut valeur (associée à la clé).
    - les éléments sont identifiés par l’attribut clé
([[Chapitre-8.pdf#page=7&selection=16,0,93,0&color=yellow|Chapitre-8, p.7]])

#### Élément équivalent
- Deux éléments a et b sont considérés comme équivalents lorsque nous avons ! (𝑎 < 𝑏) et ! 𝑏 < 𝑎 .
- La présence d’éléments équivalents (duplicatas), est habituellement interdit dans les arbres binaires de recherche.
    - Cas des conteneurs set et map de la STL.
    - C’est ce que nous supposerons dans ce chapitre.
- quand même possible de permettre la présence de duplicatas
([[Chapitre-8.pdf#page=8&selection=12,0,125,10&color=yellow|Chapitre-8, p.8]])
- Moyens possibles:
    - En ajoutant un autre attribut dans la classe nœud qui indique la fréquence de cet élément. 
    - En ajoutant un autre conteneur (ex: liste) pour les éléments équivalents
    - En modifiant la définition d’un arbre de tri comme suit:
        - Toute clé d’un nœud doit être ≥ aux clés de son sous arbre gauche et ≤ aux clés de son sous arbre droit.
        - Mais contribue à augmenter la profondeur de l’arbre et le temps d’exécution pour les opérations sur le conteneur…
([[Chapitre-8.pdf#page=9&selection=12,0,152,1&color=yellow|Chapitre-8, p.9]])

### Implantation d'un arbre binaire par chaînage
```c++
template <typename E> 
class Arbre { 
public: 
    //Constructeurs 
    Arbre(); 
    Arbre(const Arbre& source) ; 
    
    //Destructeur 
    ~Arbre(); 
    
    //Les fonctions membres 
    bool estVide() const; 
    const E& max() const; 
    const E& min() const; 
    
    //Les fonctions membres 
    int nbNoeuds() const; 
    int hauteur() const; 
    bool appartient(const E&) const ; 
    void inserer(const E&); void insererAVL(const E&); 
    void enleverAVL(const E&); 
    std::vector<E> parcoursSymetrique() const; 
    
private: 
    //Attributs internes de Arbre 
    Noeud* racine; //racine de l'arbre 
    long nb_noeuds; 
    
    //.. Les membres méthodes privés (les auxiliaires récursifs) 
    void _auxInserer( Noeud* &, const E&); 
    void _auxInsererAVL(Noeud* &, const E &); 
    void _auxEnleverAVL( Noeud* &, const E&); 
    Noeud* _auxAppartient(Noeud* arbre, const E &) const; 
    
    // Les membres privés propres aux arbres AVL 
    int _hauteur(Noeud*) const; 
    void _balancer(Noeud* &); 
    void _zigZigGauche(Noeud* &); 
    void _zigZigDroit(Noeud* &); 
    void _zigZagGauche(Noeud* &); 
    void _zigZagDroit(Noeud* &);
}
```
([[Chapitre-8.pdf#page=10&color=red|Chapitre-8, p.10]])

#### Parcours en-ordre pour un arbre binaire implémenté par chaînage

```c++
template <typename E> 
void Arbre<E>::_parcoursSymetrique(Noeud* arb, std::vector<E>& parcours) 
{ 
    if (arb!=0) { 
        _parcoursSymetrique(arb->gauche, parcours); // appel récursif 
        parcours.push_back(arb->data); // traitement 
        _parcoursSymetrique(arb->droite, parcours); // appel récursif 
    } 
}
```
([[Chapitre-8.pdf#page=15&selection=22,0,119,1&color=yellow|Chapitre-8, p.15]])

#### Insertion dans un arbre de tri (non AVL)

```c++
void inserer(const E&) 
{
    _auxInserer(racine, data);
}
```
([[Chapitre-8.pdf#page=16&selection=10,0,30,1&color=yellow|Chapitre-8, p.16]])

#### Insertion dans un arbre de tri (non-AVL)

```c++
void _auxInsererAVL(Noeud* & arbre, const E &) 
{ 
    if (arbre == 0) 
    {
        arbre = new Noeud(data); 
        nb_noeuds++; return; 
    } 
    else if( data < arbre->data )
        _auxInserer(arbre->gauche, data); //appel récursif
    else if( arbre->data < data )
        _auxInserer(arbre->droite, data); //appel récursif
    else throw logic_error("Les duplicatats sont interdits");
}
```
([[Chapitre-8.pdf#page=17&selection=10,0,146,1&color=yellow|Chapitre-8, p.17]])

## Complexité de l’insertion/ recherche/ suppression dans un arbre de tri non équilibré

La complexité d’insertion d’un élément est en 𝑶(𝒉(𝒏)), où 𝒉(𝒏) ≡ la hauteur de l’arbre contenant n éléments
([[Chapitre-8.pdf#page=25&selection=34,0,58,28&color=yellow|Chapitre-8, p.25]])

- Meilleur cas: 𝑂(1) 
- Pire cas: 𝑂(𝑛)
([[Chapitre-8.pdf#page=27&selection=17,0,39,1&color=yellow|Chapitre-8, p.27]])

## Synthèse
- Arbres binaires de recherche (de tri)
    - Dictionnaire : conteneur d’éléments devant supporter efficacement les opérations 
        - Insertion, Suppression, Trouver un élément
    - Implantation par chaînage 
        - classe Nœud interne : data (clé): type E
        - Si conteneur associatif : Clé + valeur 
        - operator< du type E surchargé 
        - Sous-arbres :gauche < droit > 
        - Méthodes publiques qui font des appels récursifs de méthodes privées (_m) (ex : parcours en pré-ordre, insertion)
    - Insertion/recherche/suppression dans un arbre de tri non équilibré 
        - Meilleur cas: 𝑂(1)
        - Pire cas: 𝑂(𝑛)
([[Chapitre-8.pdf#page=28&selection=6,0,153,1&color=yellow|Chapitre-8, p.28]])

## Les arbres AVL

- Un arbre binaire de recherche (de tri) doit être équilibré pour supporter efficacement les opérations de recherche, d’insertion et de suppression
- Le facteur d’équilibre d’un nœud est de 𝑘 lorsque
    - |hauteur(sous-arbre droit) - hauteur(sous-arbre gauche)| = 𝑘.
    - Remarque: la hauteur d’un arbre de 0 nœuds = -1. 
- Un arbre est 𝐻𝐵[𝑘] lorsque le facteur d’équilibre de ses nœuds est ≤ 𝑘
([[Chapitre-8.pdf#page=29&selection=10,0,123,2&color=yellow|Chapitre-8, p.29]])

- Les arbres AVL sont des arbres 𝐻𝐵[1]
- Nous verrons que ℎ(𝑛) est en 𝑂(log 𝑛) pour les arbres AVL.
- Le temps d’exécution des insertions/suppressions/recherches sera donc toujours en 𝑂(log 𝑛) pour un arbre AVL de 𝑛 nœuds.
([[Chapitre-8.pdf#page=30&selection=10,0,92,1&color=yellow|Chapitre-8, p.30]])

![[Chapitre-8.pdf#page=31&rect=140,93,843,391&color=yellow|Chapitre-8, p.31]]

### Nœud critique

- Quand il y a un déséquilibre, le nœud le plus profond à partir duquel il y a une différence de 2 ou plus est appelé le nœud critique. ([[Chapitre-8.pdf#page=32&selection=8,0,50,1&color=yellow|Chapitre-8, p.32]])
- Mais ce n’est pas toujours la racine ([[Chapitre-8.pdf#page=33&selection=54,0,58,9&color=yellow|Chapitre-8, p.33]])
- Il peut parfois y avoir plusieurs nœuds débalancés. Dans ce cas, on s’occupe d’abord du plus profond de tous, c’est le nœud critique. ([[Chapitre-8.pdf#page=34&selection=10,0,51,9&color=yellow|Chapitre-8, p.34]])

#### Déséquilibre
- Surviennent lors d’un ajout ou lors d’une suppression.
- S’il y a lieu, le ou les nœuds débalancés engendrés sont toujours sur le chemin de l’ajout ou de la suppression.
([[Chapitre-8.pdf#page=35&selection=6,0,50,18&color=yellow|Chapitre-8, p.35]])

#### Rééquilibrer un arbre déséquilibré
• Quand un déséquilibre apparaît, il faut remodeler la partie de l’arbre dont la racine est le nœud critique.
([[Chapitre-8.pdf#page=36&selection=12,0,41,9&color=yellow|Chapitre-8, p.36]])

##### Trouver le cas de déséquilibre

![[Chapitre-8.pdf#page=41&rect=169,33,699,350&color=yellow|Chapitre-8, p.41]]

- Identifier le genre de déséquilibre
    - Voir de quel côté l’arbre penche à partir du nœud critique. ([[Chapitre-8.pdf#page=37&selection=14,0,42,9&color=yellow|Chapitre-8, p.37]])
- Puis, regarder de quel côté penche l’arbre à partir du nœud sous-critique (l’enfant du nœud critique sur le côté le plus profond) ([[Chapitre-8.pdf#page=38&selection=16,0,55,1&color=yellow|Chapitre-8, p.38]])
- L’arbre sous-critique n’a pas besoin d’être déséquilibré pour qu’on considère qu’il penche. Une différence de 1 suffit pour identifier le cas. ([[Chapitre-8.pdf#page=39&selection=14,0,66,10&color=yellow|Chapitre-8, p.39]])
- L’arbre sous-critique penche vers la droite. ([[Chapitre-8.pdf#page=39&selection=14,0,66,10&color=yellow|Chapitre-8, p.39]])
- Dans cet exemple-ci, un déséquilibre vers la gauche, avec un arbre sous-critique qui penche vers la droite. ([[Chapitre-8.pdf#page=40&selection=16,0,40,10&color=yellow|Chapitre-8, p.40]])
- Quand le sens du déséquilibre principal est différent du sens dans lequel l’arbre souscritique penche (déséquilibre secondaire), alors deux rotations sont nécessaires: cas zig-zag. ([[Chapitre-8.pdf#page=41&selection=15,1,68,4&color=yellow|Chapitre-8, p.41]])
- Quand le sens du déséquilibre principal est le même que le sens du déséquilibre secondaire, ou bien que l’arbre sous-critique ne penche pas du tout, alors une seule rotation est nécessaire: cas zig-zig. ([[Chapitre-8.pdf#page=42&selection=16,0,76,4&color=yellow|Chapitre-8, p.42]])
- Dans notre exemple, nous aurons donc à faire deux rotations. ([[Chapitre-8.pdf#page=42&selection=80,0,95,21&color=yellow|Chapitre-8, p.42]])

#### Les rotations
Cas zig-zag : il faut faire deux rotations, la première sert à faire pencher l’arbre souscritique dans le même sens que l’arbre critique, de façon à nous retrouver dans le cas simple d’une seule rotation.
([[Chapitre-8.pdf#page=43&selection=8,0,59,9&color=yellow|Chapitre-8, p.43]])

![[Chapitre-8.pdf#page=43&rect=198,31,652,248&color=yellow|Chapitre-8, p.43]]
![[Chapitre-8.pdf#page=46&rect=201,39,629,243&color=yellow|Chapitre-8, p.46]]
![[Chapitre-8.pdf#page=48&rect=175,33,626,262&color=yellow|Chapitre-8, p.48]]
![[Chapitre-8.pdf#page=50&rect=169,28,629,239&color=yellow|Chapitre-8, p.50]]
![[Chapitre-8.pdf#page=51&rect=222,31,584,215&color=yellow|Chapitre-8, p.51]]
![[Chapitre-8.pdf#page=53&rect=193,63,626,261&color=yellow|Chapitre-8, p.53]]
![[Chapitre-8.pdf#page=55&rect=257,60,604,261&color=yellow|Chapitre-8, p.55]]

On tasse toute du même coter pour ramener tous du bon coté

: ZIGZIG même sens
: ZIGZAG alterne les direction

## Balancement
![[Chapitre-8.pdf#page=61&rect=18,117,872,430&color=yellow|Chapitre-8, p.61]]
![[Chapitre-8.pdf#page=62&rect=9,103,857,418&color=yellow|Chapitre-8, p.62]]
![[Chapitre-8.pdf#page=63&rect=5,87,958,433&color=yellow|Chapitre-8, p.63]]
![[Chapitre-8.pdf#page=64&rect=22,91,946,430&color=yellow|Chapitre-8, p.64]]

### Implémentation

```c++
template <typename E> 
class Arbre 
{ 
    public: 
        //.. 
    private: 
        // Les membres données 
        Noeud* racine; //racine de l'arbre 
        long nb_noeuds; 
        
        // classe Noeud 
        class Noeud { 
            public: 
                E data; 
                Noeud* gauche; 
                Noeud* droite; 
                int hauteur; 
                Noeud(const E & d) : 
                    gauche(0),data(d),droite(0),hauteur(0) { } 
        }; 
    };
};
```
([[Chapitre-8.pdf#page=65&color=red|Chapitre-8, p.65]])

#### Insertion dans un arbre AVL

```c++
template<typename E>
void Arbre<E>::insererAVL(const E& data) {
    _auxInsererAVL(racine, data);
}
```
([[Chapitre-8.pdf#page=67&selection=10,0,44,1&color=red|Chapitre-8, p.67]])

```c++
template<typename E> 
void Arbre<E>::_auxInsererAVL(Noeud*& arbre, const E& data) 
{ 
    if(arbre == 0) 
    {
        arbre = new Noeud(data);
        nb_noeuds++; 
        return;
    } 
    if(data < arbre->data) 
        _auxInsererAVL(arbre->gauche, data);
    else if( arbre->data < data ) 
        _auxInsererAVL(arbre->droite, data);
    else
        throw logic_error("Les duplicatats sont interdits");
        
    _balancer(arbre); //balancer et mise à jour des hauteurs 
}

```
([[Chapitre-8.pdf#page=68&selection=10,0,153,1&color=red|Chapitre-8, p.68]])

```c++
template<typename E> 
void Arbre<E>::_balancer(Noeud*& arbre) 
{
    if (_debalancementAGauche(arbre)) {
        
        // Lorsque le débalancement est à gauche, on fait un 
        // zigZig lorsque le sousArbre penche à gauche OU est balancé.
        if (_sousArbrePencheADroite(arbre->gauche))
            { _zigZagGauche(arbre); } 
        else 
            { _zigZigGauche(arbre); } 
        
    }
    else if (_debalancementADroite(arbre)) 
    {
        
        // Lorsque le débalancement est à droite, on fait un 
        // zigZig lorsque le sousArbre penche à droite OU est balancé 
        if (_sousArbrePencheAGauche(arbre->droite)) 
            { _zigZagDroit(arbre); } 
        else 
            { _zigZigDroit(arbre); } 
            
    }
    else 
    { 
        //aucun débalancement; seulement m.à.j. des hauteurs 
        if (arbre!=0) 
        {
            arbre->hauteur = 1 + std::max(
                    _hauteur(arbre->gauche),
                    _hauteur(arbre->droite)
                ); 
        } 
    } 
}
```
([[Chapitre-8.pdf#page=69&selection=0,2,246,1&color=red|Chapitre-8, p.69]])

```c++
template <typename E> 
int Arbre<E>::_hauteur(Noeud* arbre) const 
{
    if (arbre == 0) 
    {
        return -1; // la hauteur du vide = -1 
    } 
    
    return arbre->hauteur; 
    
}
```
([[Chapitre-8.pdf#page=70&selection=10,0,69,1&color=red|Chapitre-8, p.70]])

```c++
template<typename E> 
bool Arbre<E>::_debalancementAGauche(Noeud* arbre) const 
{ 
    if (arbre == 0) 
    {
        return false; 
    } 
    
    return 1 < _hauteur(arbre->gauche) - _hauteur(arbre->droite); 

} // similairement pour _debalancementADroite()
```
([[Chapitre-8.pdf#page=71&selection=10,0,87,1&color=red|Chapitre-8, p.71]])

```c++
template<typename E> 
bool Arbre <E>::_sousArbrePencheADroite(Noeud* arbre) const 
{
    if (arbre == 0) 
    {
        return false; 
    } 
    return _hauteur(arbre->gauche) < _hauteur(arbre->droite); 
    
} // similairement pour _sousArbrePencheAGauche()
```
([[Chapitre-8.pdf#page=72&selection=10,0,84,2&color=red|Chapitre-8, p.72]])

#### Implémentation de ZIG-ZIG-Gauche
```c++
template <typename E> 
void Arbre<E>::_zigZigGauche(Noeud*& K2) 
{
	Noeud* K1 = K2->gauche; 
	K2->gauche = K1->droite; 
	K1->droite = K2; 
	K2->hauteur = 
		1+ max(_hauteur(K2->gauche),_hauteur(K2->droite)); 
	K1->hauteur = 
		1 + max(_hauteur(K1->gauche), K2->hauteur); 
	K2 = K1;
}
```
([[Chapitre-8.pdf#page=73&selection=10,0,132,0&color=red|Chapitre-8, p.73]])
#### Implémentation de ZIG-ZIG-Droit
```C++
template <typename E> 
void Arbre<E>::_zigZigGauche(Noeud*& K2) 
{ 
	Noeud* K1 = K2->droite; 
	K2->droite = K1->gauche; 
	K1->gauche = K2; 
	K2->hauteur = 
		1 + max(_hauteur(K2->droite), _hauteur(K2->gauche)); 
	K1->hauteur = 
		1 + max(_hauteur(K1->droite), K2->hauteur); 
	K2 = K1; 
}
```
([[Chapitre-8.pdf#page=74&selection=10,1,135,0&color=red|Chapitre-8, p.74]])
#### Implémentation de ZIG-ZAG-Gauche
```c++
template <typename E> 
void Arbre<E>::_zigZagGauche(Noeud*& K3) 
{ 
	_zigZigDroit(K3->gauche); 
	_zigZigGauche(K3); 
}
```
([[Chapitre-8.pdf#page=75&selection=10,0,50,1&color=red|Chapitre-8, p.75]])
#### Implémentation de ZIG-ZAG-Droit
```c++
template <typename E> 
void Arbre<E>::_zigZagDroit(Noeud*& K3) 
{ 
	_zigZigGauche(K3->droite); 
	_zigZigDroit(K3); 
}
```
([[Chapitre-8.pdf#page=76&selection=10,0,51,1&color=red|Chapitre-8, p.76]])

### Synthèse
 - Arbres AVL : équilibrés 
	 - pour supporter efficacement les opérations de recherche, d’insertion et de suppression 
	 - facteur d’équilibre 
		 - |hauteur(sous-arbre droit) - hauteur(sous-arbre gauche)|= 𝑘 
		 - 𝐻𝐵[𝑘] lorsque ≤ 𝑘 
		 - AVL → arbres 𝐻𝐵[1] 
	 - Déséquilibre → balancement 
		 - Nœud critique 
		 - Rotations : zigzig droit/gauche, zigzag droit/gauche 
		 - Implémentation
([[Chapitre-8.pdf#page=77&selection=7,0,104,14&color=red|Chapitre-8, p.77]])

#### Analyse: complexité pour l’insertion dans AVL 
- Les opérations suivantes se font en temps 𝑂(1) : 
	- Insertion d’une donnée à partir d’une feuille 
	- Vérification du débalancement (lecture des hauteurs) d’un noeud 
	- Mise à jour de la hauteur d’un noeud 
	- Le rebalancement (zigZig et zigZag) à une position donnée
- Soit ℎ(𝑛) = hauteur de l’arbre AVL de 𝑛 nœuds. 
- Or, la profondeur de la feuille la moins profonde dans un arbre AVL de hauteur ℎ est ≥ ⌈𝒉/𝟐⌉ (voir exercices). 
- Les opérations suivantes se font donc en O(ℎ(𝑛)) : 
	- trouver le point d’insertion (de la racine à une feuille) 
	- Remonter du point d’insertion jusqu’à la racine (en rebalançant lorsque nécessaire) 
- L’insertion se fait donc en 𝑂(ℎ(𝑛)) 
- Or, nous allons voir que ℎ(𝑛) ∈ 𝑂(log 𝑛) pour un arbre AVL. 
- L’insertion d’une donnée dans un arbre AVL se fait donc en 𝑂(log 𝑛)
([[Chapitre-8.pdf#page=78&selection=0,2,294,0&color=yellow|Chapitre-8, p.78]])

# Enlèvement dans un arbre AVL
- Premier cas simple: le nœud à supprimer est une feuille. 
	- Dans ce cas, il suffit de le supprimer directement. 
- Deuxième cas simple: le nœud à supprimer possède un seul enfant. 
	- Dans ce cas, il suffit de le remplacer par son seul enfant. 
- Cas compliqué: le nœud à supprimer possède deux enfants. 
	- Dans ce cas, il faut d’abord échanger ce nœud avec son successeur minimal à droite, ce qui nous mènera nécessairement à l’un des deux cas simples car ce successeur minimal à droite n’a pas d’enfant à gauche!
([[Chapitre-8.pdf#page=84&selection=37,0,199,7&color=yellow|Chapitre-8, p.84]])

![[Chapitre-8.pdf#page=86&rect=115,125,837,422&color=yellow|Chapitre-8, p.86]]
![[Chapitre-8.pdf#page=87&rect=111,120,893,430&color=yellow|Chapitre-8, p.87]]![[Chapitre-8.pdf#page=88&rect=125,115,845,426&color=yellow|Chapitre-8, p.88]]
##### Implémentation
```c++
template <typename E> 
void Arbre<E>::enleverAVL(const E & data) 
{ 
_auxEnleverAVL(racine, data);
}
```
([[Chapitre-8.pdf#page=114&selection=12,0,55,1&color=red|Chapitre-8, p.114]])

```c++
template <typename E> 
void Arbre<E>::_auxEnleverAVL(Noeud*& noeud, const E& valeur) 
{
	if (noeud==0) throw logic_error("Tentative d’enlever une donnée absente");
	if (valeur < noeud->data) _auxEnleverAVL(noeud->gauche, valeur); 
	else if(noeud->data < valeur) _auxEnleverAVL(noeud->droite, valeur);
	// valeur == noeud->data: ici on doit enlever le noeud pointé par noeud
	else if(noeud->gauche != 0 && noeud->droite != 0) 
	{ //Cas complexe: chercher le successeur minimal droit et l‘enlever 
		_enleverSuccMinDroite(noeud); 
	} 
	else 
	{ //Cas simples: un ou zéro enfant 
		Noeud* vieuxNoeud = noeud; 
		noeud = (noeud->gauche != 0) ? noeud->gauche : noeud->droite; 
		delete vieuxNoeud; 
		--nb_noeuds; 
	} 
	//dans tous les cas: rebalancer et mise à jour des hauteurs
	_balancer(noeud);  
}
```
([[Chapitre-8.pdf#page=115&selection=0,3,270,1&color=red|Chapitre-8, p.115]])

```c++
template <typename E> 
void Arbre<E>::_enleverSuccMinDroite(Noeud* noeud) 
{ 
	Noeud* temp = noeud->droite; 
	Noeud* parent = noeud; 
	while ( temp->gauche != 0) 
	{ 
		parent = temp; 
		temp = temp->gauche; 
	} 
	noeud->data = temp->data; //écrasement par le successeur minimal à droite
	// enlever nœud (cas simple) 
	if (temp == parent->gauche) 
		_auxEnleverAVL(parent->gauche, temp->data); 
	else 
		_auxEnleverAVL(parent->droite, temp->data); 
}
```
([[Chapitre-8.pdf#page=116&selection=12,0,177,1&color=red|Chapitre-8, p.116]])

**Complexité:**  𝑂(log 𝑛) pour un arbre AVL
([[Chapitre-8.pdf#page=117&selection=0,3,221,3&color=yellow|Chapitre-8, p.117]])
**Toujours re-balancer ?:** Changement d'algorithme (arbre rouge et noir) (Même croissance asymptotique)

## Recherche d'un élément

```c++
template<typename E> 
bool Arbre<E>::appartient(const E& data) const 
{ 
	return _auxAppartient(racine, data) != 0; 
}
```
([[Chapitre-8.pdf#page=119&selection=8,0,51,1&color=red|Chapitre-8, p.119]])

```c++
template<typename E> 
typename Arbre<E>::Noeud* Arbre<E>::_auxAppartient(Noeud* arbre, const E& data) const 
{ 
	if (arbre == 0) 
		return 0; //si data n’est pas dans l’arbre 
		
	if (data < arbre->data) 
		return _auxAppartient(arbre->gauche, data);
	else if (arbre->data < data) 
		return _auxAppartient(arbre->droite, data); 
	else 
		return arbre; //car arbre->data == data 
}
```
([[Chapitre-8.pdf#page=120&selection=8,0,145,1&color=red|Chapitre-8, p.120]])

##### Trouver l'élément maximal
```c++
template<typename E> const E& Arbre<E>::max() const 
{ 
	if(nb_noeuds<=0) 
		throw logic_error("Doit être non vide"); 
		Noeud* temp = racine; 
		while (temp->droite!=0) 
			temp = temp->droite; 
		return temp->data; 
}
```
([[Chapitre-8.pdf#page=121&selection=71,0,154,1&color=red|Chapitre-8, p.121]])

**Dans la stl :** [[Set]], [[Map]], etc

## SET
- La valeur d’un élément dans un set est son identifiant et doit être unique et non modifiable. 
- Les élément sont ordonnés selon operator< défini par le type T des éléments du set 
	- Il est possible d’utiliser un foncteur lors de la création du set pour définir l’opérateur de comparaison 
- On utilise iterator pour accéder aux élements 
	- la méthode begin () retourne un itérateur pointant sur le premier (i.e. le plus petit) élément et end() retourne un iterator pointant sur un élément (sentinelle) après le dernier
([[Chapitre-8.pdf#page=124&selection=10,0,147,16&color=yellow|Chapitre-8, p.124]])

- On utilise insert(const T&) pour ajouter un élément et ça retourne un objet de type pair<iterator,bool> où le membre bool nous indique si l’insertion a échoué (élément déjà dans le set) ou a été effectué avec succès (dans ce cas iterator pointe sur l’élément inséré). 
- On utilise erase(const T&) ou erase(iterator) pour enlever un élément du set. 
- On utilise find(const T&) pour obtenir un iterator pointant sur l’élément recherché s’il est trouvé ou pointant sur la sentinelle à la fin du set si cet élément n’est pas dans le set.
([[Chapitre-8.pdf#page=125&selection=10,0,158,4&color=yellow|Chapitre-8, p.125]])

### Example
```c++
#include <iostream> 
#include <set> 
int main() 
{
	std::set<int> myset; 
	std::set<int>::iterator it; 
	myset.insert(30); 
	myset.insert(10); 
	myset.insert(20); 
	myset.insert(5); 
	myset.insert(15); 
	it = myset.begin(); 
	myset.erase(it); //enlève le plus petit élément 
	it = myset.end(); 
	myset.erase(--it); //enlève le plus grand 
	std::cout << "myset contains:"; 
	for (it = myset.begin(); it != myset.end(); ++it) 
		std::cout << ' ' << *it; //affiche 10 15 20 
	std::cout << std::endl; 
	return 0; 
}
```
([[Chapitre-8.pdf#page=126&selection=12,0,205,1&color=yellow|Chapitre-8, p.126]])

## Map
- Est un ensemble ordonné de paires de type pair<KeyType,ValueType> 
- Les élément sont ordonnés selon operator< défini par le type KeyType 
	- Il est possible d’utiliser un foncteur lors de la création du map pour définir l’opérateur de comparaison 
- Pour accéder aux éléments, on peut utiliser un iterator ou, plus simplement, l’opérateur d’indexation [ ] dont le prototype est: 
	- ValueType & operator[] (const KeyType & key)
([[Chapitre-8.pdf#page=127&selection=10,0,122,6&color=yellow|Chapitre-8, p.127]])

- Fonctionnement: Si key est dans le map alors une référence à la valeur associé à key est retournée. Si key n’est pas dans le map, key est inséré dans la map avec une valeur associé par défaut (défini par le constructeur sans paramètre de ValueType). 
	- operator[] est un modificateur: il est donc inutilisable dans une fonction où le map est passé par référence constante. 
- Il est donc généralement plus prudent de tester d’abord si une clé est dans le map avant de lui associer une valeur. Pour cela on utilise find(const KeyType & key) qui retourne un itérateur pointant sur la paire pair<key,value> si key est dans le map (et value est la valeur associé à key). Sinon, l’itérateur retourné pointe sur un élément de map passé le dernier.
([[Chapitre-8.pdf#page=128&selection=10,0,226,21&color=yellow|Chapitre-8, p.128]])

#### EXAMPLE
```c++
std::map<string, unsigned int> tailles; 
//insère éventuellement une paire <‘’Julie’’,162> dans tailles
tailles["Julie"] = 162;
std::cout << tailles["Julie"] << endl; //affiche 162
std::cout << tailles["Robert"] << endl; //insère une paire <‘’Robert’’,0> 
	//dans tailles et affiche 0
```
([[Chapitre-8.pdf#page=129&selection=80,0,172,12&color=red|Chapitre-8, p.129]])

 - Le deuxième énoncé: tailles[‘’Julie’’] insère d’abord <‘’Julie’’,0> dans tailles et retourne par référence la valeur associée de 0 . Cette valeur est ensuite écrasée par 162 avec l’opérateur d’affectation =. 
 - Le dernier énoncé insère <‘’Robert’’,0> dans tailles et affiche 0
([[Chapitre-8.pdf#page=129&selection=12,1,78,12&color=yellow|Chapitre-8, p.129]])

```c++
std::map<std::string, unsigned int>::const_iterator itr; 
itr = tailles.find("Robert"); 
if(itr==tailles.end()) 
	std::cout << "Absent de notre base de donnée" << endl; 
else 
	//affiche la valeur associée à la clé Robert
	std::cout << itr->second << endl; 
```
([[Chapitre-8.pdf#page=130&selection=56,0,147,5&color=yellow|Chapitre-8, p.130]])

- À la place de ce dernier énoncé, on peut d’abord vérifier si ‘’Robert’’ est dans le map et, si c’est le cas, afficher sa taille:
([[Chapitre-8.pdf#page=130&selection=12,0,54,7&color=yellow|Chapitre-8, p.130]])

#### Synthèse
- Dans la STL 
	- set, map, multiset et multimap ✓ insert erase find Iterator begin end ✓ Clés non modifiables ✓ Arbres rouge et noir 
- set (duplicatas interdits), multiset (duplicatas autorisés) ➢ operator< défini par le type T (data) 
- map (duplicatas interdits), multimap (duplicatas autorisés) ➢ pair<KeyType,ValueType> ➢ operator< défini par le type KeyType ➢ operator[
([[Chapitre-8.pdf#page=131&selection=6,0,82,9&color=yellow|Chapitre-8, p.131]])