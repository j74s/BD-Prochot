# BD-Prochot

This was the way I found to deal with my laptop CPU not working properly.
 
 ```bash
sudo dnf install msr-tools
```

```bash
sudo modprobe msr
```

```bash
sudo wrmsr 0x1FC 14004d
```

copy `bdprochot.sh` to /usr/bin and make executable

```bash
sudo cp -v bdprochot.sh /usr/bin
```

```bash
sudo chmod +x /usr/bin/bdprochot.sh
```

copy bdprochot.service and bdpres.service to /etc/systemd/system

```bash
sudo cp -v bdprochot.service /etc/systemd/system
```

```bash
sudo cp -v bdpres.service /etc/systemd/system
```

```bash
sudo systemctl enable bdprochot.service 
```

```bash
sudo systemctl enable bdpres.service
```
