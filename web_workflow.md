## Bring new site down to local machine

1. Clone repository into new directory from GitHub (~/Sites/sitename)
2. "Composer install" in root site directory
3. Composer drupal-scaffold
3. Create empty database "sitename_local"
4. Navigate to localhost site in browser and install drupal, using "Standard" installation and no country and UTC time zone
5. Sync the database: $ ../vendor/bin/drush sql-sync @saginaw.dev @saginaw.local
6. Sync files: $ ../vendor/bin/drush rsync @saginaw.dev:%files @saginaw.local:%files/
7. Navigate to the Drupal theme folder and run compass to generate the stylesheet(s)
