---
layout: post
title: 'Tutorial Gitlab Omnibus completo instalação, baukup e restauração '
---
## //install gitlab

```
sudo apt-get update
```

```
sudo apt-get install ca-certificates curl openssh-server postfix
```

```
cd /tmp
```

```
curl -LO https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh
```

```
sudo bash /tmp/script.deb.sh
```

```
sudo apt-get install gitlab-ce
```

## //configurar firewall

```
sudo ufw status
```

```
sudo ufw allow http
```

```
sudo ufw allow https
```

```
sudo ufw allow OpenSSH
```

## //desabilitar firewall

```
sudo ufw desable
```

## //arquivo de configuraçao do gitlab

```
sudo nano /etc/gitlab/gitlab.rb
```

## //gerar backup do gitlab menos builds,artifacts,lfss

```
sudo gitlab-rake gitlab:backup:create SKIP=builds,artifacts,lfs
```

## //restaurar backup

```
sudo cp 11493107454_2018_04_25_10.6.4-ce_gitlab_backup.tar /var/opt/gitlab/backups/
```

```
sudo chown git.git /var/opt/gitlab/backups/11493107454_2018_04_25_10.6.4-ce_gitlab_backup.tar
```

## //pausar servicos que podem atrapalhar a restauracao

```
sudo gitlab-ctl stop unicorn
```

```
sudo gitlab-ctl stop sidekiq
```

## //confirmar servicos estao pausados

```
sudo gitlab-ctl status
```

## //restaura todo o backup

```
sudo gitlab-rake gitlab:backup:restore BACKUP=1493107454_2018_04_25_10.6.4-ce
```

## //reinicia o servicos do gitlab e checa

```
sudo gitlab-ctl restart
```

```
sudo gitlab-rake gitlab:check SANITIZE=true
```
