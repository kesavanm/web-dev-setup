# Device Setup

## _IDE & Editors_
- [ ] PHPStorm
- [ ] VSCode - VS Code Insiders - Codium
- [ ] ATOM - Stable/Nightly
- [ ] VIM & gVIM
    - Oni, NeoVIM
- [ ] Sublime
- [ ] Notepad++
- [ ] CudaText
- [ ] Brackets

## _WSL_
- [ ] Apache
- [ ] PHP
- [ ] MySQL
- [ ] MemCached



### Installing Apache/MySQL/PHP (Latest)


The following commands will install latest versions of Apache/MySQL/PHP along with `git` , `memcached` , `composer` and other `php` libraries.

```bash
sudo apt install mysql-server mysql-client mysql-common
sudo apt install apache git memcached composer php php-bcmath php-cli php-curl php-gd php-gmp php-intl php-ldap php-mbstring php-memcached php-mysql php-odbc php-pear php-redis php-soap php-xdebug php-zip
sudo a2enmod headers rewrite ssl
sudo service apache2 restart
```
##### Installing specific versions (Optional)

Replace specific version number (like 8.2) in below commands with the prefered choice

```bash
sudo apt install apache2
sudo apt install php7.4 php7.4-bcmath php7.4-cli php7.4-curl php7.4-gd php7.4-gmp php7.4-intl php7.4-ldap php7.4-mbstring  php7.4-memcached php7.4-mysql php7.4-odbc php7.4-pear php7.4-redis php7.4-soap php7.4-xdebug php7.4-zip
```

##### Switching from X.X to Y.Y (Ex: 7.4 to 8.2)

```bash
sudo a2dismod php7.4              # Disable module for Apache2
sudo a2enmod  php8.2              # Enable module for Apache2
sudo apache2ctl configtest        # Test the config
sudo service  apache2 restart     # Restart services
```
##### Start services

Replace `start` with `restart` in the below commands if required.

```bash
sudo service mysql     start
sudo service apache2   start
sudo service memcached start
sudo mysql -e "SET @@GLOBAL.sql_mode=''"
sudo service ssh       start
```


##### MySQL password config
```sql
 CREATE USER 'kesavan'@'%' IDENTIFIED BY 'password';  -- Query OK, 0 rows affected (0.01 sec)
 GRANT ALL PRIVILEGES ON *.* TO 'kesavan'@'%';        -- Query OK, 0 rows affected (0.01 sec)
 FLUSH PRIVILEGES;                                    -- Query OK, 0 rows affected (0.00 sec)
 SELECT VERSION();                                    -- 8.0.19-0ubuntu5
 ALTER USER 'kesavan'@'%' IDENTIFIED WITH mysql_native_password BY 'password';    -- Query OK, 0 rows affected (0.01 sec)
```

**Losing connectivity Solution**

Losing net connection on WSL2 when connected with VPN? It's an known issue : DNS server coming from vpn network is not reflected in WSL · Issue #1350 · microsoft/WSL . Fix - https://superuser.com/a/1666368/677650


```bash
# fix for error: chmod on /mnt/c/Users/***/.git/config.lock failed: Operation not permitted
sudo umount /mnt/c
sudo mount -t drvfs C: /mnt/c -o metadata

```

## _Browsers & Internet_
- [ ] Mozilla
    - Firefox - Stable, Dev, Nightly
    - Firefox ESR
- [ ] Mozilla based - TOR
- [ ] Google
  - Chrome - Stable, Dev & Beta
  - Chrome Canary https://www.google.com/chrome/canary/
- [ ] Chromium - https://github.com/Hibbiki/chromium-win64
- [ ] Thorium - https://github.com/Alex313031/Thorium-Win
- [ ] Thunderbird, NextCloud

## _SQL clients_

- [ ] NaviCat
- [ ] HeidiSQL


## _Tools_
- [ ] PuTTY
- [ ] Tabby
- [ ] WebServiceStudio
- [ ] SoapUI
- [ ] 7z
- [ ] PdfSam
- [ ] PostMan
- [ ] GitBash
- [ ] RipGrep
- [ ] FZF

## Fonts & UI
- [ ] [solarized_dark.reg](https://github.com/altercation/solarized/blob/master/putty-colors-solarized/solarized_dark.reg) for PuTTY - May this help without Admin right: `reg import solarized_dark.reg`
- [ ] [DejaVu Sans Mono Nerd Font Complete](https://raw.githubusercontent.com/ryanoasis/nerd-fonts/master/patched-fonts/DejaVuSansMono/Regular/complete/DejaVu%20Sans%20Mono%20Nerd%20Font%20Complete.ttf)
- [ ] [DejaVu Sans Mono Nerd Font Complete Mono](https://raw.githubusercontent.com/ryanoasis/nerd-fonts/master/patched-fonts/DejaVuSansMono/Regular/complete/DejaVu%20Sans%20Mono%20Nerd%20Font%20Complete%20Mono.ttf)
- [ ] [DejaVu Sans Mono for Powerline](https://raw.githubusercontent.com/powerline/fonts/master/DejaVuSansMono/DejaVu%20Sans%20Mono%20for%20Powerline.ttf)

## _Media_
- [ ] VLC
- [ ] KODI
