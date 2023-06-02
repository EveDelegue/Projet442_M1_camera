# Projet442_M1_camera
Projet de M1 EEA. L'objectif est de faire fonctionner une caméra et de lire les données d'intensité lumineuses sur les pixels d'une ligne.

Ce programme fonctionne sur la caméra ov9655, sur une carte stm32f746G.

On utilise un DMA entre la caméra et l'afficheur LCD, afin d'observer l'image.

On recupere les données d'un pixel en définissant un pointeur sur un pixel de l'image. On utilise cette technique pour remplis un tableau des valeurs sur une ligne. On compare ensuite cette valeur à des seuils (blanc et noir) pour observer les changement d'intnsité lumineuse (entre les barres d'un code barre par exemple).

En cas d'appui sur l'écran, le dma se bloque, jusqu'à un nouvel appui.

A la fin du scan, on dispose de deux tableaux : l'un contiens les intensités lumineuses, l'autre si les pixels peuvent etre considérés noirs, blancs ou autre.
On affiche par exemple les intensités lumineuses sur 3 pixels.
