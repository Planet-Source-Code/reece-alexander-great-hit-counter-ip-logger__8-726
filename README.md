<div align="center">

## Great Hit Counter/IP Logger


</div>

### Description

A Great Counter
 
### More Info
 
Use: <?php include("counter.php"); ?> where u want it to show up


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Reece Alexander](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/reece-alexander.md)
**Level**          |Beginner
**User Rating**    |4.3 (52 globes from 12 users)
**Compatibility**  |PHP 4\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__8-1.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/reece-alexander-great-hit-counter-ip-logger__8-726/archive/master.zip)





### Source Code

```
<?php
  $countfile = "data/counter.txt";
  $logfile = "data/WebLog.txt";
  if (!file_exists("$countfile")) {
    $fp = fopen("$countfile", "a");
    fputs($fp, "0");
    fclose($fp);
  }
  $count = join('', file($countfile));
  trim($count);
  $count++;
  echo $count;
  $fp = fopen($countfile, "w");
  fputs($fp, $count);
  fclose($fp);
  $fp = fopen($logfile, "a");
  $date = date("d M, Y");
  $time = date("g:i a");
  fputs($fp, "IP: ".$_SERVER['REMOTE_ADDR']." Date: ".$date." Time: ".$time);
  fputs($fp, "\n");
  fclose($fp);
?>
```

