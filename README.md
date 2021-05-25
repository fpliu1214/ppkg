# zpkg
a lightweight, portable package manager for UNIX.

## Install via package manager

|OS|PackageManager|Installation Instructions|
|-|-|-|
|`macOS`|[HomeBrew](http://blog.fpliu.com/it/os/macOS/software/HomeBrew)|`brew tap leleliu008/fpliu`<br>`brew install zpkg`|
|`GNU/Linux`|[LinuxBrew](http://blog.fpliu.com/it/software/LinuxBrew)|`brew tap leleliu008/fpliu`<br>`brew install zpkg`|
|`ArchLinux`<br>`ArcoLinux`<br>`Manjaro Linux`<br>`Windows/msys2`|[pacman](http://blog.fpliu.com/it/software/pacman)|`curl -LO https://github.com/leleliu008/zpkg/releases/download/v0.1.0/zpkg-0.1.0-1-any.pkg.tar.gz`<br>`pacman -Syyu --noconfirm`<br>`pacman -U zpkg-0.1.0-1-any.pkg.tar.gz`|
|`Windows/WSL`|[LinuxBrew](http://blog.fpliu.com/it/software/LinuxBrew)|`brew tap leleliu008/fpliu`<br>`brew install zpkg`|

## Install using shell script
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/leleliu008/zpkg/master/install.sh)"
```

## zsh-completion for zpkg
I have provide a zsh-completion script for `zpkg`. when you've typed `zpkg` then type `TAB` key, it will auto complete the rest for you.

**Note**: to apply this feature, you may need to run the command `autoload -U compinit && compinit`


## Give a Star!
𝙄𝙛 𝙮𝙤𝙪 ❤𝙩𝙝𝙞𝙨 𝙥𝙧𝙤𝙟𝙚𝙘𝙩, 𝙥𝙡𝙚𝙖𝙨𝙚 𝙜𝙞𝙫𝙚 𝙞𝙩 𝙖 𝙨𝙩𝙖𝙧 <span style='color:red;font-size:1.2em'>★</span> . 𝙏𝙝𝙖𝙣𝙠𝙨!


## zpkg command usage
*   print the help infomation of `zpkg` command
        
        zpkg -h
        zpkg --help
        
*   print the version of `zpkg`
        
        zpkg -V
        zpkg --version
        
*   update the [zpkg-formula-repository](https://github.com/leleliu008/zpkg-formula-repository)
        
        zpkg update
        
*   search packages can be installed
        
        zpkg search curl
        zpkg search lib
        
*   print the basic infomation of packages
        
        zpkg info curl
        zpkg info curl openssl
        
*   install packages
        
        zpkg install curl
        zpkg install curl bzip2  -v
        zpkg install curl bzip2  -v -x
        zpkg install curl bzip2  -v -x --dry-run
        zpkg install curl bzip2  -v -x --keep-working-dir
        
*   reinstall packages
        
        zpkg reinstall curl
        zpkg reinstall curl bzip2  -v
        
*   uninstall packages
        
        zpkg uninstall curl
        zpkg uninstall curl bzip2
        
*   upgrade the outdated packages
        
        zpkg upgrade curl
        zpkg upgrade curl bzip2  -v
        
*   view the formula of a package
        
        zpkg formula view curl
        
*   edit the formula of a package
        
        zpkg formula edit curl
        
*   create a formula
        
        zpkg formula create curl
        
*   delete a formula
        
        zpkg formula delete curl
        
*   rename a formula to new name
        
        zpkg formula rename curl curl7
        
*   list the available packages
        
        zpkg list available
        zpkg list available -q
        
*   list the installed packages
        
        zpkg list installed
        
*   list the outdated packages
        
        zpkg list outdated
        
*   is the specified package available ?
        
        zpkg is available curl
        
*   is the specified package installed ?
        
        zpkg is installed curl
        
*   is the specified package outdated ?
        
        zpkg is outdated curl
        
*   list contents of a installed package directory in a tree-like format.
        
        zpkg tree curl
        zpkg tree curl -L 3
        
*   download formula resources of a package to the cache
        
        zpkg fetch curl
        
*   print the logs of a installed package
        
        zpkg logs curl
        
*   pack a installed package
        
        zpkg pack curl
        
*   visit the homepage of a formula or the `zpkg` project
        
        zpkg homepage
        zpkg homepage curl
        
*   show the installation direcotory of a formula or the zpkg home
        
        zpkg prefix
        zpkg prefix curl
        
*   show the depended packages by a package
        
        zpkg depends curl
        
*   cleanup the unused cache
        
        zpkg cleanup
        
