- [ ] update version of MW & SMW in [./ansible/roles/02_mw/defaults/main.yml](./ansible/roles/02_mw/defaults/main.yml) MW stays w LTS `REL1_35` SMW changes to 4.2.0
- [ ] variables in [./hosts-box.yml](./hosts-box.yml)
- [ ] remove uncessary extension
- [ ] change logos and details
- [ ] closed wiki
- [ ] wsiwyg editor
- [ ] 


wikimedia/composer-merge-plugin

composer config --no-plugins allow-plugins.wikimedia/composer-merge-plugin true

COMPOSER=composer.local.json composer require --no-update "mediawiki/semantic-media-wiki "~4.0""

COMPOSER=composer.local.json composer config --no-plugins allow-plugins.wikimedia/composer-merge-plugin true 