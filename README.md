# Nginx config for Drupal

[Nginx](https://nginx.org/) configuration files for [Drupal](https://www.drupal.org/).


## Branches

- main: my own version, mix from the following
- basic: very basic, must work in almost every case
- nginx-recipe: adapted version of [Nginx recipe for Drupal](https://www.nginx.com/resources/wiki/start/topics/recipes/drupal/)
- aegir-light: stripped-down version from [Aegir project](https://www.aegirproject.org/): no cache, less module specific stuff, ...


## How to use

- clone the repo next to your Drupal folder into /usr/local/etc/nginx-config

    sudo git clone https://github.com/argopecten/drupal-nginx-conf /usr/local/etc/nginx-config

  - drupal.conf is the main config file for Nginx, it includes all files from below
  - sited.d/ folder has the site specific settings: server name, document root, ...
  - common.d/ folder has the heavy stuff
- check out the branch you want:

    sudo ln -s /usr/local/etc/nginx-config/drupal.conf /etc/nginx/conf.d/.

- link drupal.conf to /etc/nginx/config folder
- rename sites.d/d10.local as appropriate
- review and update variables in files of sites.d/
- adjust your DNS or /etc/hosts settings ans restart nginx


## Drupal versions

- usually tested with recent Drupal versions (v10.x)
