# Пакетный менеджер XBPS

Состоит из набора отдельных утилит для выполнений конкретных операций.

## xbps-install - установка и обновление пакетов

Для установки пакета 
```
# xbps-install -S <package>
```
Для установки обновлений
```
# xbps-install -Su
```


## xbps-remove - удаление пакетов

## xbps-query - получении информации о пакетах

## xbps-src - установка пакетов отсутствующих в официальном репозитории

Для установки пакета необходимо перейти в директорию где развернут репозиторий пакетов.
```
$ cd void-packages
$ ./xbps-src pkg <pkgname>
```

После этого можно выполнить локальную установку пакета.
```
xi <pkgname>
```
После того как пакет и его зависимости собран, можно воспользоваться обычными утилитами для управления пакетами с указанием пути до локального репозитория.

```
$ xbps-install --repository=hostdir/binpkgs ...
$ xbps-query --repository=hostdir/binpkgs ...
```
