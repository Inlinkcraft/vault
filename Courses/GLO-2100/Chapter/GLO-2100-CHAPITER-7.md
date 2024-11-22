---
name: Arbres et monceau
type: Chapter
course: GLO-2100
---


## Heapsort
```c++
template <typename Comparable> 
void heapsort(vector<Comparable>& heap ) 
{ 
    // construction du monceau 
    if (heap.size() > 1) { heapBottumUp(heap); 
    
        for(size_t i = heap.size() - 1; i > 0; i--) 
        { 
            // positionner la racine dans le tableau trié 
            swap(heap[0], heap[i]); 
            //reconstruction du tas sans l’élément i 
            percDown(heap, 0, i); 
        } 
    } 
}
```
([[Chapitre-7.pdf#page=151&selection=14,0,141,1&color=note|Chapitre-7, p.151]])

## Synthèse
• Monceau/Tas
    - Arbre binaire complet dont la valeur de la clé d’un nœud est toujours supérieure où égale à celle de ses enfants (propriété du tas_max)
- Utilités 
    - File à priorité
    - Tri par tas
- Hauteur d’un tas de 𝑛 noeuds
- Nombre de feuilles d’un tas de 𝑛 nœuds 
- Construction bas vers le haut 
    - en 𝑂(𝑛) dans tous les cas
- Insertion
    - nombre maximal de comparaisons requises $⌊𝑙𝑜𝑔2(𝑛 + 1)⌋$
- Enlever la racine
    - nécessite au plus $𝑂(log 𝑛)$ comparaisons
- Tri par tas (« Heapsort »)
    - s’exécute donc en $𝑂(𝑛 log(𝑛))$ en pire cas et en $𝑂(𝑛)$ en meilleur cas
([[Chapitre-7.pdf#page=178&color=yellow|Chapitre-7, p.178]])

## Monceaux dans la STL 
([[Chapitre-7.pdf#page=180&selection=4,0,4,20&color=yellow|Chapitre-7, p.180]])

Fonctions pour créer et manipuler des monceaux définies dans `<algorithm>`

 Pour réarranger des éléments d’un conteneur se situant entre debut et fin (incluant debut et excluant fin) : `make_heap(Iterator debut, Iterator fin)`
 Fonctions pour insérer et retirer un élément dans l’intervalle \[debut, fin\[: 
 - `push_heap(Iterator debut, Iterator fin)`
 - `pop_heap(Iterator debut, Iterator fin)`
([[Chapitre-7.pdf#page=180&selection=30,1,92,30&color=yellow|Chapitre-7, p.180]])

## Exemple d'implémentation
```c++
#include <iostream> 
#include <algorithm> 
#include <vector> 
int main() //exemple extrait de www.cplusplus.com 
{ 
    using namespace std;
    
    //vector de 5 entiers
    vector<int> v { 10, 20, 30, 5, 15 };
    
    //repositionne les éléments de v en un tas_max
    make_heap(v.begin(), v.end());
    
    //affiche 1er élément de v  
    cout << "initial max heap : " << v.front() << endl;
    
    //swap 1er et dernier de v et 
    //reconstruit tas sans le dernier élem
    pop_heap(v.begin(), v.end());  v.pop_back();
    
    //enlève ce dernier élément
    cout << "max heap after pop : " << v.front() << endl; //suite prochaine diapo :: 182 Département d’informatique et de génie logiciel Exemples // suite de int main() //exemple extrait de www.cplusplus.com v.push_back(99); //insère 99 à la fin de v qui contient un élément de plus push_heap(v.begin(), v.end()); //reconstruit le tas avec ce dernier élément ajouté cout << "max heap after push: " << v.front() << endl; sort_heap(v.begin(), v.end()); //tri le tas (il faut que v soit d’abord un tas) cout << "final sorted range :"; for (unsigned int i = 0; i < v.size(); i++) { cout << ' ' << v[i]; cout << endl; } return 0 }
```
([[Chapitre-7.pdf#page=182&color=red|Chapitre-7, p.182]])