# tomkd

Tool scritto in bash per convertire immagini `jpg` o documenti `pdf` in markdown; viene sfruttato il servizio CLI di [MathPix](https://mathpix.com/) (non open, con un piano gratuito). 

Questo tool è stato utilizzato per generare la maggior parte delle pagine di [questo sito](https://unict-dmi.github.io/DFA-compiti/) powered by [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). Leggi qui il [caso d'uso](https://unict-dmi.github.io/DFA-compiti/note/#voglio-caricare-un-nuovo-compito_1).

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

### Mandatory options

`-i` for the input file. It can be `.jpg` or `.pdf`

```bash
tomkd -i compito.jpg
```

### Optional

`-o` for the output (it must be `.md`)

```bash
tomkd -i compito.pdf -o YYYY-MM-DD.md
```

`-t` for the tag

```bash
tomkd -i compito.pdf -o YYYY-MM-DD.md -t "Questo è il mio tag"
```

### Output

The output consists of:
- markdown file
- input file moved to a specific folder based on the extension of the file (e.g. `pdf/input.pdf` or `images/input.jpg`)
- images included in the input file organized in an `images/` directory.

## Build

If you want to build the tool from the repo, downloat this repo and then run

```bash
sudo ./build
```

This is the same of [setup](#set-up) but in this way you can use your own modified 

## Credit
Dennis Angemi