# findNclean

findNclean created to automate filesystem cleaning and/or file searching.

You can use it as 'find' superstructure to run/schedule multiple heavy
and optimized commands at the same time with logging of all found files.

You can set find and/or move options in specific config and then run single
simple command or create multiple cron jobs for all configurations you need.
Find action heavily rely on 'find', so it's fast enough.
Bash builtins extensively used, so dependencies list is short enough.
It designed to support ancient environments (like CentOS 5.5) but to use
features of modern envs (like Ubuntu 16.04) if possible.

For more info just run it without arguments.
For even more info see the code ;)!

## To try
- Clone this repo to your *nix host
```
cd ~/path/to
git clone https://github.com/vmspike/findNclean.git
cd findNclean
```
Or just download executable and optionally config example
```
mkdir findNclean
cd findNclean
wget https://github.com/vmspike/findNclean/raw/master/findNclean
chmod +x findNclean
wget https://github.com/vmspike/findNclean/raw/master/findNclean.conf.example
```
- Quickly review the docs and example of synthetic verbose output
```bash
./findNclean
./findNclean help -c
./findNclean tricks
less example.out
```
- Review/edit `./findNclean.conf.example`
- Run `./findNclean find -c ./findNclean.conf.example`
- Check result lists, remove the lines with the items you want to keep.
- Add `.approved` suffix to the result lists filenames
- Run `./findNclean mv -c ./findNclean.conf.example`
