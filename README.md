# Bootstrap_Walker_Nav_Menu
A Bootstrap 4 Navbar for WordPress

```php
require_once('bootstrap-walker-nav-menu.php');
```

```php
<nav class="navbar navbar-full navbar-light bg-faded">
  <a class="navbar-brand" title="Accueil" href="<?= esc_url( home_url( '/' ) ); ?>"><?= get_bloginfo( 'name' ); ?></a>
  <button class="navbar-toggler hidden-lg-up" type="button" data-toggle="collapse" data-target="#navbar-content" 
          aria-controls="navbar-content" aria-expanded="false" aria-label="Toggle navigation"></button>
  <?php
  if (has_nav_menu('primary_navigation')) :
  wp_nav_menu([
    'theme_location'  => 'primary_navigation',
    'container_id'    => 'navbar-content',
    'container_class' => 'collapse navbar-toggleable-md',
    'menu_class'      => 'nav navbar-nav',
    'walker'          => new Bootstrap_Walker_Nav_Menu()
  ]);
  endif;
  ?>
</nav>
```
If you want an icon as a text like fa-github in FontAwesome use "fa fa-github" in attr_title (Title Attribute).
