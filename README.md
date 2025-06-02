## Creating LUKS Encrypted Volumes in Linux

An Alternative to TrueCrypt and VeraCrypt 


### Setup
```
sudo apt update 
sudo apt upgrade -y
apt-get install cryptsetup
```

### Create Encrypted Volume
```
mkdir mytmp
cr-disk test.img 24 M ./mytmp
```
Then follow the prompts.
NB: Remember to type YES (and not yes)

### Mount Encrypted Volume
```
cr-m test.img test ./mytmp
```
Check `mytmp` is mounted with `df -H` then copy some files.

### Unmount Encrypted Volume
```
cr-d test
```