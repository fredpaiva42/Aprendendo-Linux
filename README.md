# Comandos Linux

## Trabalhando com arquivos e diretórios
- Verificar diretõrio atual: `pwd`
- Listar arquivos e diretótios: `ls`
- Mostrar informações sobre os arquivos e pastas do diretório: `ls  -l`
- Mostrar todos os arquivos, incluindo os escondidos: `ls -la`
- Limpar o terminal: `clear` ou `Ctrl + L`
- Imprimir mensagem no terminal: `echo "mensagem"`
- Armazenar mensagem dentro de um arquivo: `echo "mensagem" > arquivo.txt`
- Armazenar mensagem sem apagar mensagem anterior: `echo "mensagem" >> arquivo.txt`
- Ler conteúdo de um arquivo: `cat arquivo.txt`
- Abrir o manual: `man`
- Ver um comando específico no manual: `man {comando que quero entender}`
- Para ter uma ajuda mais resumida: `help date` ou `date --help`
- O comando `help` mostra as instruções do bash
- Retornar para o diretório anterior: `cd ..`
- Criar um novo diretório: `mkdir {nome do diretório}`
- Apagar um diretório vazio: `rmdir {nome do diretório}`
- Apagar diretório: `rm -r {nome do diretório}`
- Apagar um arquivo: `rm {nome do arquivo}`
## Caracteres coringa no bash
- Ler arquivos baseados nos caracteres que eles possuem:
    - Para ler um arquivo que tem **um** caracter qualquer depois do seu nome, basta usarmos `?`, exemplo: `cat arquivo?.txt` então se no nosso diretório tiver qualquer arquivo que tenha um caracter ao seu lado vai ser lido.
    - Para ler um arquivo que tem **qualquer** número de caracteres seguidos do nome base, basta usarmos `*`, por exemplo `cat arquivo1.txt` seria lido pelo `?`, mas o arquivo `cat arquivo10.txt` só é lido pelo `cat arquivo*.txt` 

## Manipulando, compactando e descompactando arquivos
### Copiando, movendo e renomeando
- Copiar o conteúdo de um arquivo para outro: `cp {arquivo origem} {arquivo destino}`
- Para renomear um arquivo ou move-lo para um outro diretório: `mv {arquivo original} {novo nome do arquivo}` ou para mover: `mv {arquivo original} {direitório destino}/`
- Para copiar um diretório precisamos usar o recursivo: `cp -r {diretório origem} {diretório destino}`

### Criando e abrindo ZIP
- Compactar um diretório: `zip -r {nome do arquivo zip}.zip {diretório que desejo compactar}/`, exemplo: `zip -r linux.zip linux/`
- Saber o que tem dentro do arquivo.zip: `unzip -l work.zip`
- Descompactar: `unzip work.zip`
- Caso queira descompactar, mas sem poluir o terminal podemos usar o **quiet**: `unzip -q work.zip`
- Já no caso da compactação precisa ser **-rq**: `zip -rq work.zip workspace`

## Mais sobre Compactação e Descompactação e comandos do terminal
### Compactação e descompactação usando o tar (menor tamanho)
- Compactar (create and zip -cz): `tar -cz workspace > work.tar.gz`
- Compactar sem redirecionamento: `tar -czf work.tar.gz workspace`
- Descompactar (xtract zip): `tar -xz < work.tar.gz`
- Descompactar sem redirecionamento: `tar -xzf work.tar.gz`
- `<`: entrada de fluxo para leitura do arquivo.
- `>`: saída de fluxo para mandar para um arquivo.
- Para ter informações sobre a compactação e descompactação podemos usar o `v` de verbose antes do `-xzf` ou do `-czf`
### Data
- Sinalizar uma modificação ou atualizar a data da última modificação: `touch arquivo.txt`
- Para ver a data do meu sistema: `date` or `date "+%d/%m/%Y`
