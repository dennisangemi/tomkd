# tomkd

Questo tool funziona per converti jpg o pdf to latex se il file di input non ha immagini!
Bisogna aggiornare il tool per le immagini

Read requirements

## Set up

1. Download the bash script
```shell
wget "https://raw.githubusercontent.com/dennisangemi/tomkd/main/tomkd"
```
1. Move it to `/usr/local/bin`
```shell
sudo mv ./tomkd /usr/local/bin
```
1. Make it executable
```shell
sudo chmod +x /usr/local/bin/frictionless2md
```


## Getting started

## Usage

```bash
tomkd -i compito.jpg -o YYYY-MM-DD.md
```

oppure

```bash
tomkd -i compito.pdf -o YYYY-MM-DD.md 
```

oppure
```
tomkd -i compito.pdf
```

## Build
simply run

```bash
sudo ./build
```

## Future developements
- add button for download pdf or jpg file (different icon) to md file
- check if latex contains images and manage that 