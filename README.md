Starter-NEAT-D6
===============

ABOUT THEME
-----------

Thème RWD pour les sites de l'Association développés sous Drupal 6.
Thème développé avec Sass - Compass - Bourbon Neat

REGLAGES A FAIRE
----------------

dans template.php :
remplacer le nom du theme dans les fonctions necessaires.

Changer le nom du fichier .info

Changer le favicon
Changer le screenshot
Changer le logo

dans fichiers tpl
remplacer le nom du theme dans les appels d'includes
<pre>
 <?php
$theme_path = drupal_get_path('theme', 'starterd6_pf_rwd'); //Nom du thème idem nom du fichier .info
include ($theme_path.'/chemin/vers/fichier.php');
?>
</pre>

Vérifier les réglages dans le fichier config.rb
Pour le thème en production, inutile d'envoyer sur le serveur les dossiers sass, fichier config.rb

Dans images
-----------

Mettre a jour les images du theme

Compilation des fichiers scss
-----------------------------
dans le terminal :
user@vm-server1:~$ compass watch /PATH/TO/THEMENAMEFOLDER/

Usage des mixins de Bourbon NEAT
------------------------

<pre>
<body>
 <section class="blog">
  <aside></aside>
  <article></article>
 </section>
</body>
</pre>

<pre>
section.blog {
  @include outer-container;
  
  aside {
    @include span-columns(4);
  }
  
  article {
    @include span-columns(8);
  }
}
</pre>


Ordre et hierarchie des blocs du layout
-------------------------
<pre>
#general
    #header
        #header-inner
            .headHaut
                .logoHead
                .menuImg
            .headBas
                .site-slogan
                .headSearch
                .menuHead
    #content-global
        #left-content
        #content-inner
            .content-top
            .content-header
            .middle-content
            .content-bottom
        #right-content
    #footer
    #bloc_stats
</pre>

 Breakpoints pour Bourbon Neat
----------------------------------
<pre>
 @include breakpoint ($mobile){}
 @include breakpoint ($desktop){}
 @include breakpoint ($tablet){}
</pre>