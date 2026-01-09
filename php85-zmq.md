1. Remove corrupted ZMQ module (WARNING):

```
sudo dpkg -r --force-depends php8.5-zmq
```

```
sudo rm /usr/lib/php/20250925/zmq.so
sudo phpdismod zmq
```

2. Check if there is any installed ZMQ module:

```
php -m | grep zmq
php --ri zmq
```

3. Manual assembly of PHP v8.5:

```
sudo apt update 
sudo apt install libsqlite3-dev libxml2-dev libssl-dev libcurl4-openssl-dev libzmq3-dev pkg-config build-essential autoconf bison re2c libonig-dev php8.5-dev
```

```
cd /usr
sudo wget https://www.php.net/distributions/php-8.5.0.tar.gz
sudo tar -xzf php-8.5.0.tar.gz
cd php-8.5.0
```

```
sudo ./configure --prefix=/opt/php8.5 --enable-cli --enable-fpm --with-curl --with-openssl --enable-mbstring --with-zmq
sudo make -j$(nproc)
sudo make install
cd ..
sudo rm -r php-8.5.0
```
4.  Manual assembly of ZMQ module (fixed):

```
cd /usr
sudo wget https://github.com/zeromq/php-zmq/archive/94920ac64398901175dc4372a429781712.tar.gz
sudo tar -xzf 94920ac64398901175dc4372a429781712.tar.gz
cd php-zmq-94920ac64398901175dc4372a429781712
```

```
sudo /opt/php8.5/bin/phpize
sudo ./configure --with-php-config=/opt/php8.5/bin/php-config
sudo make -j$(nproc)
sudo make install
cd ..
sudo rm -r php-zmq-94920ac64398901175dc4372a429781712
```
5. Add line: `extension=zmq.so` to this file:

```
sudo nano /opt/php8.5/lib/php.ini
```

6. Copy output of this command:

```
find /opt/php8.5 -name zmq.so
```

7. Check where is configuration directory for INI (may be /etc/php/8.5/fpm/conf.d): `http://localhost/info.php`

8. Add line from step 6: `extension=/opt/php8.5/lib/php/extensions/no-debug-non-zts-20250925/zmq.so`

```
sudo nano /etc/php/8.5/fpm/conf.d/20-zmq.ini
```

```
sudo nano /etc/php/8.5/mods-available/zmq.ini
```

9. Enable ZMQ module:

```
sudo phpenmod zmq
sudo systemctl restart apache2
```
