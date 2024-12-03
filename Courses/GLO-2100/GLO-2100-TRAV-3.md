---
name: Tp2
type: Evaluation
course: GLO-2100
date: 2024-12-10T14:00
ponderation: 10
note:
status: En cours
---
#school/GLO-2100 
***

### Mandat
---
Votre mandat est de représenter l’information nécessaire à la gestion d’un bottin téléphonique. Cette information décrit un ensemble de membres du personnel dans une organisation, et pour chacun d’eux, un numéro de téléphone, un numéro de cellulaire, et une adresse courriel. Toutefois, afin de rechercher efficacement l’information pertinente à une personne, il vous faudra bâtir un index représenté par une table de dispersion dont les collisions devront être gérées par adressage ouvert. Il s'agit précisément d'implanter un type abstrait Bottin. Ce type est constitué de plusieurs associations. Une association relie une clé primaire, par exemple une chaîne de caractère représentant un numéro de téléphone, à un nom et un prénom associés à ce numéro de téléphone, donc un couple <clé, nomprénom>. Les clés d'un dictionnaire sont toutes uniques; les noms ne le sont pas (i.e. il peut y avoir des clés différentes qui ont un même nom associé, cependant, toute paire nom/prénom est unique et peut être considérée comme une seconde clé pour la recherche). Nous désirons un accès le plus rapide possible pour trouver une association, soit par la clé numéro de téléphone, soit par la clé nom/prénom. Vous devez implanter les associations comme étant des encapsulations qui sont insérées dans deux tables de dispersion : l'une pour indexer les numéro de téléphone, l'autre, pour indexer les noms/prénoms. Ainsi, l'implantation ressemblera au graphique ici-bas. Une seule information, i.e., un entier, caractérise une association. Celui-ci désigne l'endroit dans un tableau des entrées où les informations complètes sur l'association en question peuvent être retrouvées
([[Tp3-Enoncer.pdf#page=2&selection=23,0,87,0&color=yellow|Tp3-Enoncer, p.2]])

### Structures
---
![[Tp3-Enoncer.pdf#page=3&rect=11,343,587,747&color=yellow|Tp3-Enoncer, p.3]]

### À faire
---
##### critère
- [ ] Les tables de dispersion doivent avoir une taille adéquate. ([[Tp3-Enoncer.pdf#page=3&selection=54,0,56,1&color=yellow|Tp3-Enoncer, p.3]])
- [ ] La fonction de hachage et de redispersions doit être celle fournie (HString1). ([[Tp3-Enoncer.pdf#page=3&selection=60,0,71,1&color=yellow|Tp3-Enoncer, p.3]])
- [ ] Vous devez gérer les exceptions dans toutes les méthodes de la classe Bottin ([[Tp3-Enoncer.pdf#page=3&selection=74,1,75,76&color=yellow|Tp3-Enoncer, p.3]])

##### fonctionnalité

> [!note] Format des entré dans le fichier text
> Nom, Prenom (666) 666-6666 (999) 999-9999 courriel
> - (666) 666-6666: Numéro de téléphone fixe
> - (999) 999-9999: Cellulaire
> > [!attention] 
> > Dans le fichier que nous vous fournissons, les champs sont séparés par des tabulations ( '\t' ). Notez que les espaces ne constituent pas une délimitation de champ, mais que les noms et prénoms sont séparés par , + espace.
> > ([[Tp3-Enoncer.pdf#page=4&selection=96,0,108,1&color=yellow|Tp3-Enoncer, p.4]])

- [ ] Bottin.cpp
    - [ ] Constructeur ([[Tp3-Enoncer.pdf#page=4&selection=26,0,28,60&color=yellow|Tp3-Enoncer, p.4]])
        - [ ] Précondition: le fichier est conforme au format attendu([[Tp3-Enoncer.pdf#page=4&selection=40,0,40,41&color=yellow|Tp3-Enoncer, p.4]])
        - [ ] Paramètres d'entré: `std::ifstream & p_fichierEntree`
        - [ ] Paramètres d'entré: `size_t p_table_size = 100`
    - [ ] void Bottin::ajouter ([[Tp3-Enoncer.pdf#page=5&selection=10,0,10,20&color=yellow|Tp3-Enoncer, p.5]])
        - [ ] ``const std::string & p_nom`` Nom ([[Tp3-Enoncer.pdf#page=5&selection=10,22,10,47&color=yellow|Tp3-Enoncer, p.5]])

### FAQ
---

>[!question] **Puis-je ajouter des attributs à la classe Bottin?**
>OUI!  Pour cette classe, vous décidez du modèle d'implantation.  Vous pouvez donc ajouter des attributs non-constants afin de résoudre le problème demandé.  Vous pouvez aussi évidemment ajouter des constantes et des méthodes privées.

>[!question]  **Puis-je ajouter des attributs à la classe TableDeHachage?**
>NON! Vous pouvez seulement ajouter des constantes et des méthodes privées, mais aucun attribut non-constant.  Vous devez utiliser cette classe telle qu'elle vous est fournie.

>[!question] **La classe Entree est privée à la classe Bottin.  Comment faire des tests?  Que faire?**
>Au fond, il existe deux workarounds pour faire vos tests.  Le premier est de simplement comparer les attributs voulus:
>```c++
>EXPECT_EQ(test_bottin.trouverAvecTelephone("(510) 642-6417").m_prenom, 
>    "Irma");
>```
>Le second est d'utiliser le mot-clé auto pour récupérer la valeur à tester:
>```c++
>auto entree = test_bottin.trouverAvecTelephone("(510) 642-6417") ; 
>EXPECT_EQ(entree.m_prenom, "Irma");
>```

>[!question] **Je veux utiliser un ou des fichiers de données pour faire mes tests, où dois-je le mettre et que dois-je régler?**
>On vous demande, afin de simplifier le travail des correcteurs de bien vouloir déposer tous les fichiers utilisés pour conduire des tests dans votre répertoire tests.  Si vous voulez utiliser le fichier de données fourni avec le TP veuillez le copier dans votre répertoire tests.
>Vu qu'on ne peut pas éditer la configuration All CTest car elle utilise son répertoire de travail pour trouver les tests, il vous faudra hard coder le chemin des fichiers utilisés par vos tests.  Sur la VM ça va problement donner ceci:
>`std::ifstream("../../tests/mesdonnees.txt") ;`