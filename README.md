# tomkd

Questo tool funziona per convertire jpg o pdf to latex. Viene sfruttato il servizio di MathPix (non open, con un piano gratuito). Questo tool è stato utilizzato per generare la maggior parte delle pagine di questo sito in Material for MkDocs https://unict-dmi.github.io/DFA-compiti/

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

Signup to MathPix and then login to your MathPix account running
```shell
mpx login
```


## Usage

### Essential options

`-i` for the input file. It can be `.jpg` of `.pdf`

```bash
tomkd -i compito.jpg
```

### Optional flags

`-o` for the output (it must be `.md`)

```bash
tomkd -i compito.pdf -o YYYY-MM-DD.md
```

`-t` for the tag

```bash
tomkd -i compito.pdf -o YYYY-MM-DD.md -t "Questo è il mio tag"
```

## Build

If u want to build the tool from the repo, downloat this repo and then run

```bash
sudo ./build
```

This is the same of [setup](#set-up) but in this way you can use your own modified 