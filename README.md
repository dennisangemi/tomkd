# tomkd

Questo tool funziona per convertire jpg o pdf to latex. Viene sfruttato il servizio di MathPix (non open, con un piano gratuito)

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
    sudo chmod +x /usr/local/bin/tomkd
    ```


## Getting started

Requirements
- imagemagick
- mpx (MathPix CLI)
- pandoc

Login to your MathPix account
```shell
mpx login
```


## Usage

You can run

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

ma anche
```bash
tomkd -i compito.jpg/pdf -o YYYY-MM-DD.md -t "Nome Cognome"
```

## Build

Download this repo and simply run

```bash
sudo ./build
```

## Future developements
- check if latex contains images and manage that 
