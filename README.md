# Algorithme d'encodage de Huffman : 
Ce code permet de compresser un fichier texte de longueur raisonnable. 
Pour l'utiliser, il vous suffit d'entrer l'adresse de ce fichier à la ligne 28 dans l'algorithme, là où il est écrit "src/text_to_encode.txt".

Le fichier compressé alors créée se trouvera dans le dossier où se situe votre fichier Huffman.java et se nommera : huffman_encoded.txt.

### Langage utilisé : 
Java

## Méthodes utilisées pour la compression : 

### calculateFrequences(nodesQueue);
1. On remplit le tableau ASCII en analysant le texte à encoder.
2. On crée les Node feuilles avec un caractère et un code vide.
3. On affiche les caractères et leur nombre d’occurrence.

### buildTree(nodesQueue); 
On construit l’ensemble de l’arbre grâce à l’algorithme de Huffman : on prends les 2 Node ayant les nombres d’occurrences les plus petits et on crée un nouveau Node à partir de ces deux premiers.
Ainsi de suite jusqu’à ce qu’il ne reste qu’un unique Node, la racine de l’arbre.

### generateCodes(nodesQueue.peek(), "");
Parcours l’arbre et génère le code de chaque Node en fonction de sa position 	dans celui-ci.

### printCodes(); 
Affiche les pairs <caractère, code>.

### generateBin();
Concatène dans l’ordre du texte, les codes binaires des caractères.

### normalizeBin();
Ajoute des zéros à la fin du code binaire jusqu’à ce que le taille de celui-ci soit multiple de 8.

### normalizeBin_To_newString();
1. Découpe la String binaire en octet.
2. Transforme les octets leur caractères associés.
3. Concatène ces caractères dans la String encodedStr qui est le résultat de l’algorithme.

### createFile(encodedStr);
Crée un fichier txt dans lequel est stocké la String encodedStr.

## Contact
Thomas Cormier,
Etudiant en Informatique Données Usages à Polytech Annecy Chambéry.

Code inspiré de celui de ahmedengu que vous pouvez retrouver ici : 
https://gist.github.com/ahmedengu/aa8d85b12fccf0d08e895807edee7603/
