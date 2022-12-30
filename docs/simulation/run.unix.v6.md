# Run Unix v6 on PDP-11

```bash
tree -Fh labs

[4.0K]  labs/
├── [809K]  pdp11*
├── [2.0M]  rk0
├── [2.0M]  rk1
├── [2.0M]  rk2
└── [6.0M]  unixv6.tap
```

#### Start PDP-11

```bash
./pdp11
```

```bash
PDP-11 simulator V3.12-3
sim>
```

#### Bootloader

```bash
set cpu 11/40
set cpu idle
set tto 7b
set tm0 locked
attach rk0 rk0
attach rk1 rk1
attach rk2 rk2
attach lpt printer.txt
set dci en
set dci lines=8
set dco 7b
att dci 5555
boot rk0
```

![](/images/install/bootloader.png)

#### Boot Unix v6

```bash
unix
```

![](/images/install/boot.unixv6.png)

#### Login

```bash
root
```

![](/images/install/login.png)

#### Unix v6

```bash
who
date
echo "Hello, World!"
ls -al /
```

![](/images/unixv6.png)
