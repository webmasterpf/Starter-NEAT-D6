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

Vérifier les réglages dans le fichier config.rb
Pour le thème en production, inutile d'envoyer sur le serveur les dossiers sass, fichier config.rb

Dans images
-----------

Mettre a jour les images du theme

Compilation des fichiers scss
-----------------------------
dans le terminal :
webmaster@vm-server1:~$ compass watch /PATH/TO/THEMENAMEFOLDER/

Usage des mixins de Bourbon NEAT
------------------------
<body>
 <section class="blog">
  <aside></aside>
  <article></article>
 </section>
</body>



section.blog {
  @include outer-container;
  
  aside {
    @include span-columns(4);
  }
  
  article {
    @include span-columns(8);
  }
}


Ordre et hierarchie des blocs du layout
-------------------------

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
