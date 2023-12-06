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

	4. Installer composer pour verification
3. Manipulation du projet
   1. [ ]  execution du projet

```
sudo docker compose up [-d]
```
2. Supprimer tout ce qui a été construit
```bash
sudo docker compose down
```
3. Voir les erreurs
```bash
sudo docker compose logs
```
