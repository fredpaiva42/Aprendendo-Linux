# Comandos Linux

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
- Retornar para o diretório anterior: `cd ..`
- Criar um novo diretório: `mkdir {nome do diretório}`
- Apagar um diretório vazio: `rmdir {nome do diretório}`
- Apagar diretório: `rm -r {nome do diretório}`
- Apagar um arquivo: `rm {nome do arquivo}`
- Ler arquivos baseados nos caracteres que eles possuem:
    - Para ler um arquivo que tem **um** caracter qualquer depois do seu nome, basta usarmos `?`, exemplo: `cat arquivo?.txt` então se no nosso diretório tiver qualquer arquivo que tenha um caracter ao seu lado vai ser lido.
    - Para ler um arquivo que tem **qualquer** número de caracteres seguidos do nome base, basta usarmos `*`, por exemplo `cat arquivo1.txt` seria lido pelo `?`, mas o arquivo `cat arquivo10.txt` só é lido pelo `cat arquivo*.txt` 

