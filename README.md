# webstresstool

The easiest way to prepare an input file based on apache2 log file:
```
@web01:/var/log/apache2# cat other_vhosts_access.log | gawk '{ print $7}' > webstresstool.input
```

To cleanup input file from static files, images ang others:
```
@web01:/var/log/apache2# cat webstresstool.input | grep -v 'api' | grep -v 'images' | grep -v 'template' | grep -v 'static' > webstresstool.input.clean
```