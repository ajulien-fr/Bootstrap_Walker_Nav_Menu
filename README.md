# Bootstrap_Walker_Nav_Menu
A Bootstrap 4 Navbar for WordPress

```php
require_once('bootstrap-walker-nav-menu.php');
```

```php
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="<?= {{ home_url('/') }} ?>">Navbar</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbar-content" aria-controls="navbar-content" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
  </button>
  <?php
  if (has_nav_menu('primary_navigation')) :
  wp_nav_menu([
    'theme_location'  => 'primary_navigation',
    'container_id'    => 'navbar-content',
    'container_class' => 'collapse navbar-collapse',
    'menu_class'      => 'navbar-nav',
    'walker'          => new Bootstrap_Walker_Nav_Menu()
  ]);
  endif;
  ?>
</nav>
```
If you want an icon as a text like fa-github in FontAwesome use "fa fa-github" in attr_title (Title Attribute).
