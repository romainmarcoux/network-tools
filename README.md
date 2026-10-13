Various network tools

# subnet_to_regex.sh

Converts a file containing network addresses into regular expressions.

Example:

```
192.168.1.0/28
```
becomes
```
^192\.168\.1\.([0-9]|1[0-5])$
```

The resulting file can then be used in the grep command to extract from a file containing IP addresses those matching the regular expressions:

```
grep -E -f /path/regex_file file_with_IP
```

