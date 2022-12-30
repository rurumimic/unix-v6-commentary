# Build SimH

- simh/simh: [Building and running a simulator](https://github.com/simh/simh#building-and-running-a-simulator)

Windows: [Win32-Development-Binaries](https://github.com/simh/Win32-Development-Binaries)

```bash
git clone https://github.com/simh/simh.git
cd simh
```

## Build

### Dependencies

#### Ubuntu

```bash
sudo apt-get install gcc libpcap-dev libvdeplug-dev libpcre3-dev libedit-dev libsdl2-dev libpng-dev libsdl2-ttf-dev
```

### Simulator

#### PDP-11

```bash
make pdp11
```

##### Binary

```bash
tree -F simh/BIN

simh/BIN/
├── buildtools/
└── pdp11*
```

#### Build all simulators

```bash
make all
```

## Move the binary file

in project directory:

```bash
mkdir -p labs
cp simh/BIN/pdp11 labs/pdp11
```

```bash
tree -F -L 1 .

./
├── README.md
├── docs/
├── images/
├── labs/
│   └── pdp11*
├── simh/
└── src/
```

Run [Unix v6 on PDP-11](run.unix.v6.md)
