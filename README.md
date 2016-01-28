Why
===

Because some people could not run mapbox-studio because of their too old version of glibc (e.g. if you're on wheezy) and need a full graphical linux environment. If you don't need, prefer docker solution


Install
=======

```bash
git clone https://github.com/kurthalex/vagrant-mapbox-studio.git
cd vagrant-mapbox-studio
vagrant up
```

Launch
======

Open Virtualbox and launch mapbox virtual machine
login 'vagrant' with password 'vagrant'

Open a terminal (Icon bottom-left/System Tools/LXTerminal)

For azerty keyboard
```bash
setxkbmap fr
```

Then

```bash
cd mapbox-studio-linux-x64-v0.3.3/mapbox-studio-linux-x64-v0.3.3
./atom
```
