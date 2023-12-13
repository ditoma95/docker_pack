1. D'abord créer une image

```bash
sudo docker build -t laravel_php .
```

2. Créer un container et lié avec l'image

```bash
sudo docker run -itd --name applicatin laravel_php

```

1. Autres options
2. Pour rentrer dans le container
3. Installer composer pour verification
4. Manipulation du projet

   1. [ ]  execution du projet

```
sudo docker compose up [-d]
```

2. [ ]  Arrèter la stact et supprimer tout ce qui a été construit

```bash
sudo docker compose down
```

3. Voir les erreurs

```bash
sudo docker compose logs
```

### TRAVAUX D'AUJOUR D'HUI

Créer un container a partir d'une image et associer le nom du domaine a une addresse ip au container

```bash
sudo docker run -itd --name conteneur_web --add-host app:192.168.60.152 web
```

Explication ❤️

```text
On a mis l'ip parce que app est une variable. Quand on lancé 
```

Demarrage du service sur le host:

```bash
php artisan serve --host=192.168.60.152
ou
php artisan serve --host=0.0.0.0 --port 9000 (pour dire tout addresse ip)

```

Rebuilder l'image après modification dans les fichiers de configurations

```sudo
udo docker build -t web --no-cache .

```

Voir les erreurs dans le container

```bash
sudo docker logs conteneur_web
```

Configuratin du point .env

```php
DB_CONNECTION=pgsql
DB_HOST=db
DB_PORT=5432
DB_DATABASE=laravel
DB_USERNAME=admin
DB_PASSWORD=admin
```

Pour verifier la configuration

```bash
sudo docker compose config
```
