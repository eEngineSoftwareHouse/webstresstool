# webstresstool

The easiest way to prepare an input file based on apache2 log file:
```
@web01:/var/log/apache2# cat other_vhosts_access.log | gawk '{ print $7}' > webstresstool.input
```
