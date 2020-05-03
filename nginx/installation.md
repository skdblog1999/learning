# Installing Nginx

## For Debian or Ubuntu

## Method 1

Does not install latest version

```
sudo apt-get install nginx
nginx -v
```

### Method 2

Installs latest versions

```
sudo vim /etc/sources.list.d/nginx.list

deb http://nginx.org/packages/mainline/ubuntu/ bionic nginx                                                            
deb-src http://nginx.org/packages/mainline/ubuntu/ bionic nginx
```

```
sudo wget http://nginx.org/keys/nginx_signing.key
sudo apt-key add nginx_signing.key
sudo apt-get update
sudo apt-get install -y nginx
sudo /etc/init.d/nginx start
nginx -v
```

## For Redhat & Centos

```
sudo vim /etc/yum.repos.d/nginx.repo 
[nginx]                                                                           name=nginx repo                               baseurl=http://nginx.org/packages/mainline/rhel/8/$basearch/                        gpgcheck=0
enabled=1
```

```
sudo yum -y install nginx
sudo systemctl enable nginx
sudo systemctl start nginx
```



## Verify Installation

```
nginx -v
ps -ef | grep nginx
```

