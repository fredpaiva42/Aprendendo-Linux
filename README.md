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

### Leitura de arquivos

- Ler um arquivo: `cat google.txt`
- Ler apenas as primeiras dez linhas do arquivo: `head google.txt`
- Especificar quantas linhas do começo do arquivo: `head -n 3 google.txt`, dessa maneira o terminal só retorna as 3 primeiras linhas do arquivo, que foi o que eu pedi.
- Para ler as dez últimas linhas: `tail google.txt`
- Especificar quantas linhas do final do arquivo eu desejo ler: `tail -n 3 google.txt`
- Para abrirmos um arquivo e navegar pelo seu texto podemos usar o comando: `less google.txt`

## Edição de arquivos com o VI: inclusão, alteração, exclusão, repetição

### Edição de arquivos com o vi

- Para abrir o VI: `vi arquivo.txt`
- Podemos navegar pelo texto utilizando as setas do teclado
- Para entrar no modo de inclusão, basta apertarmos a tecla `i` onde queremos inserir texto.
- Para retornar ao modo navegação basta apertarmos a tecla: `ESC`
- Para salvar as alterações: `:w`
- Para sair do VI: `:q`
- Para inserir na posição seguinte onde se encontra o cursor: `a`
- Para excluir caracteres: `x`, se digitarmos o número de caracteres que queremos apagar antes do `x`, será apagada aquela quantidade de caracteres: `11 x` 11 carateres serão apagados
- Para excluir uma linha inteira: `dd`, digitar uma quantidade antes do `dd` funciona da mesma maneira que com o x.
- Se quisermos salvar e sair ao mesmo tempo: `:wq`
- Sair sem salvar: `:q!`
- Adiciona texto ao final da linha: `Shift + a`
- Ir para última linha do texto: `Shift + g`
- Se quisermos ir para linha n, devemos apertar o número e logo em seguida `Shift + g`
- Para ir para o final da linha atual: `$` ou `Shift + 4`
- Para ir ao inicio da linha digitamos 0.
- Para procurarmos uma palavra no texto: `/Palavra que quero encontrar`, isso vai para a primeira ocorrência da palavra, se apertarmos `n`, ele ira para a próxima ocorrência e se apertarmos `Shift + n`, voltamos para a anterior.
- Para copiarmos uma linha basta apertar `yy`, podemos dizer a quantidade de linhas que queremos copiar também.
- Para colar o que foi copiado: `p`, para colar mais de uma vez, basta informarmos a quantida antes do `p`.

## Processos

- Saber quais processos estão sendo executados: `ps`
- Todos os processos do sistema: `ps -e`
- Para obter informações sobre os processos em execução: `ps -ef`
- Para encontrar um processo específico (isso também funciona nos arquivos): `ps -ef | grep firefox`, ele vai mostrar só os processos que tem o firefox.
- Encerrar um processo: `kill ID do processo`, exemplo `kill 164274`
- Encerrar um processo que não está se encerrando: `kill -9 id do processo`
