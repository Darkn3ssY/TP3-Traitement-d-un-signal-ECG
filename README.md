# TP3-Traitement-d-un-signal-ECG


![image](https://user-images.githubusercontent.com/90354895/215298957-4a491bb2-6c66-4af3-a98b-7d368b7fdd92.png)


# Objectifs:
Dans ce troisième Tp on cherche a Supprimer du bruit autour du signal produit par un électrocardiographefaire et faire la représentation temporelle et fréquentielle en utilisant la transformée de fourrier discrète sous le logiciel Matlab.


# troduction :

Un électrocardiogramme (ECG) est un test qui mesure l'activité électrique du cœur. Il est utilisé pour détecter des anomalies cardiaques telles que les troubles du rythme cardiaque, les infarctus du myocarde et les maladies cardiaques congénitales.

![image](https://user-images.githubusercontent.com/90354895/215298871-44eca1d4-db08-4d76-8d36-928ddaf74239.png)
L’onde P représente la première étape du cycle où les oreillettes (ou atriums) se contractent permettant le passage du sang, à travers les valves auriculoventriculaires, vers les ventricules. Ensuite, le complexe QRS symbolise à la fois la contraction ventriculaire (permettant l’éjection du sang vers les artères) notamment par le pic en R, dans le même temps,le relâchement des oreillettes entraîne le remplissage de celles-ci en attente d’un nouveau cycle).

L’onde T représente le relâchement des ventricules suite à leur contraction.L’enchaînement de ces complexes permet par ailleurs de déterminer la fréquence cardiaque, c’est-à-dire le nombre de cycle cardiaque par unité de temps. Une fréquence cardiaque normale est comprise entre 60 et 100 battements par minute, en dessous de cette valeur, le patient est en « bradycardie », au-dessus de cette valeur,le patient est en « tachycardie ».

Les signaux ECG sont contaminés avec différentes sources de bruits. Les bruits de hautes fréquences sont provoqués par l’activité musculaire extracardiaque et les interférences dues aux appareils électriques, et des bruits de basses fréquences provoqués par les mouvements du corps liés à la respiration, les changements physicochimiques induits par l’électrode posée sur la peau et les micro variations du flux sanguin. Le filtrage de ces bruits est une étape très importante pour faire un diagnostic réussi.

1 - Suppression du bruit provoqué par les mouvements du corps:

![image](https://user-images.githubusercontent.com/90354895/215298874-15f5c4e7-ad68-41e2-8bfe-2cae7f29376f.png)

Son spectre d'amplitude :

![image](https://user-images.githubusercontent.com/90354895/215298876-8a0b1f34-3527-4c3e-92dd-21e7f7116190.png)

Ensuite on procède a supprimer le bruit des mouvements du corps en utilisant un filtrage idéal passe haut et on trace la différence par rapport au signal d'origine

![image](https://user-images.githubusercontent.com/90354895/215298879-80f462e7-890c-4b28-a59e-5e957f3a3d29.png)

2 - Suppression des interférences des lignes électriques 50Hz:
![image](https://user-images.githubusercontent.com/90354895/215298882-e3465a76-08ab-43ce-8d8c-f851a910ebcc.png)

On remarque qu'il y a un bruit qu'on doit éliminer avec un filtrage notch
3 - Suppression des interférences des lignes électriques 50Hz :
![image](https://user-images.githubusercontent.com/90354895/215298884-68305bfa-00bd-41df-9225-3c6917c70d2f.png)

On remarque que ce signal est encore bruité quand on le compare avec le signal ECG qu'on doit avoir. Pour eliminer ce bruit on applique un filtrage pass bas pour eliminer les bruits de basses fréquences.

ECG 2 apres le filtrage notch avec ses spectres et le bruit qui doit etre eliminer

![image](https://user-images.githubusercontent.com/90354895/215298887-78a03f61-e666-47b3-9cb0-faed9dd9b40a.png)
4 - Amélioration du rapport signal sur bruit :
![image](https://user-images.githubusercontent.com/90354895/215298899-682a3bcd-b486-4758-846c-40696ea5b0b1.png)

5 - Identification de la fréquence cardiaque avec la fonction d'autocorrélation :
La fréquence cardiaque peut être identifiée à partir de la fonction d'autocorrélation du signal ECG. Cela se fait en cherchant le premier maximum local après le maximum global (à tau = 0) de cette fonction.
On utilise la fonction xcorr pour le signal ecg3

![image](https://user-images.githubusercontent.com/90354895/215298906-d32d4b67-ce91-4e38-938a-a529ecd952a6.png)

On detecte une correlation dans un maximum a taux = 2

# ENCADRE PAR : Pr.Alae Ammour


