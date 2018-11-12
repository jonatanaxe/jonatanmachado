---
layout: post
title: 'Tutorial Gitlab Omnibus completo instalação, baukup e restauração '
tags: gitlab
---
## //Install gitlab

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

## //Configurar firewall

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

## //Desabilitar firewall _(essa opção não deve ser utilizado em produção)_

```
sudo ufw desable
```

## //Arquivo de configuração do gitlab

```
sudo nano /etc/gitlab/gitlab.rb
```

## //Gerar backup do gitlab menos builds, artifacts, lfss

```
sudo gitlab-rake gitlab:backup:create SKIP=builds,artifacts,lfs
```

## //Restaurar backup

```
sudo cp 11493107454_2018_04_25_10.6.4-ce_gitlab_backup.tar /var/opt/gitlab/backups/
```

```
sudo chown git.git /var/opt/gitlab/backups/11493107454_2018_04_25_10.6.4-ce_gitlab_backup.tar
```

## //Pausar serviços que podem atrapalhar a restauração

```
sudo gitlab-ctl stop unicorn
```

```
sudo gitlab-ctl stop sidekiq
```

## //Confirmar serviços estão pausados

```
sudo gitlab-ctl status
```

## //Restaura todo o backup

```
sudo gitlab-rake gitlab:backup:restore BACKUP=1493107454_2018_04_25_10.6.4-ce
```

## //Reinicia o serviços do gitlab e checa

```
sudo gitlab-ctl restart
```

```
sudo gitlab-rake gitlab:check SANITIZE=true
```
