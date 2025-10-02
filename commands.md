### Linux commands

#### General
- Start an app and see logs
````bash
    dbeaver-ce &
````

- Show application using a port
````bash
    netstat -tulpn | grep :<port>
    netstat -tulpn | grep :9000
````

- Show env var
````bash
    printenv | grep <env var>
    printenv | grep AWS
````

- Unset env var
````bash
    unset <env var>
    unset AWS_SECRET_ACCESS_KEY
    unset AWS_ACCESS_KEY_ID
````

#### Using apt
- Update package list
````bash
    sudo apt-get update
````

- Upgrade all packages
````bash
    sudo apt-get upgrade
````

- Upgrade a single package
````bash
    sudo apt-get install --only-upgrade <pkg>
    sudo apt-get install --only-upgrade snapd
````

- Searching
````bash
    sudo apt-cache search <pkg>
    sudo apt-cache search mysql
````

- Install
````bash
    sudo apt-get install <pkg>
    sudo apt-get install mysql-workbench
````

- Uninstall
````bash
    sudo apt-get autoremove <pkg>
    sudo apt-get autoremove mysql-workbench
````

#### Using grep
- Procurando string exato num arquivo
````bash
    grep "trecho a procurar" arquivo.txt
````

- Procurando em todos os arquivos do diretório
````bash
    grep "trecho a procurar" *
````

- Procurando string sem se importar com letras maiúsculas e minúsculas
````bash
    grep -i "trecho a procurar" arquivo.txt
````

- Procurando em todos os arquivos do diretório e subdiretórios
````bash
    grep -R "trecho a procurar" /var/www/
````

- Procurando em todos os arquivos do diretório e subdiretórios
````bash
    grep -Ri "trecho a procurar" /var/www/
````

- Procurando os trechos onde a string não aparece
````bash
    grep -v "trecho a procurar" arquivo.txt
````

- Imprimindo o resultado em um arquivo txt
````bash
    grep "trecho" arquivo.txt > aquivodesaida.txt
````

- Combinando o grep com o ls para retornar arquivos que contenham uma determinada string
````bash
    ls | grep *string*
````

#### Using ps
- Verificar se o processo está rodando
````bash
    ps -e | grep <PID>
    ps -e | grep 1221482

    ps -e | grep '<PKG>'
    ps -e | grep 'vlc'
````

- Verificar se o processo está rodando
````bash
    kill -9 <PID>
    kill -9 1221482
````

#### Using find
- Procurando arquivos pelo nome
````bash
    find . -name '*.so'
````

#### Returning Ubuntu informations
````bash
    lsb_release -a
````

#### Using MySQL
- Connecting
````bash
    mysql -u root -p -h 187.33.4.241 (conexao remota de banco de dados)
````

- Reiniciando o Apache e Mysql
````bash
    sudo /etc/init.d/apache2 restart
    sudo /etc/init.d/mysql restart
````

#### Using chmod
- Permissão total para o arquivo
````bash
    chmod -R 777 nome_pasta_ou_arquivo (permissao total do arquivo)
````

#### Using gzip
- Extrair arquivo
````bash
    gzip -d file.json.gz
````

#### Using tar
- Extrair arquivo
````bash
    tar zxvf file.tar.gz
````

#### Using ssh and scp
- Acessando pelo terminal
````bash
    ssh root@192.168...
````

- Acessando pelo terminal com senha
````bash
    ssh -p 22022 andre@mediaboxtech.com
````

- Upload para um servidor
````bash
    scp <source file> <username>@<destination server>:<destiny>
    scp cacuria.exe andre@telemidia.puc-rio.br:public_html/
````

- Download de um servidor
````bash
    scp <username>@<destination server>:<source file> <destiny>
````

- Download de uma pasta
````bash
    scp -rp <username>@<destination server>:<folder path> <destiny>
    scp -rp andre@139.82.71.211:"/home/jvitorlocal/MPRJ_similaridade/novo_dataset/pdf/" /media/infra/LES-PUC-RIO/Similiaridade/pdf/
````

- Download de uma pasta passando o password de acesso
````bash
    sshpass -p <password> scp -rp <username>@<destination server>:<folder path> <destiny>
    sshpass -p "password" scp -rp andre@139.82.24.96:"/media/infra/extracted_text" /home/andre/Similiaridade
````

#### Using df para listar informações do sistema de arquivos
- Listar o tamanho em escala de 1024
````bash
   df -h
````

- Listar o tamanho em escala de 1000
````bash
   df -H
````

#### Using du para retornar o tamanho de arquivo ou diretório em bytes (Kb/Mb)
- Listar o tamanho de todos os arquivos dentro do diretório
````bash
   du -ha (nome do arquivo)
````

- Ver o tamanho de um arquivo ou diretório sem listar
````bash
   du -hs (nome do arquivo)

- Retorna o tamanho em bytes
````bash
   du -hsb (nome do arquivo)
````

- Retorna o tamanho em KB
````bash
   du -hsk (nome do arquivo)
````

- Retorna o tamanho sempre em MB
````bash
   du -hsm (nome do arquivo)
````

#### Compilando e executando arquivos
- Para c
````bash
    gcc -Wall Mochila.cpp -o Mochila
````

- Para c++
````bash
    g++ -Wall Mochila.cpp -o Mochila
````

- Executando Arquivo
````bash
	./Mochila
	./Mochila <entrada.txt>saida.txt
````

#### Using ldd
- Retorna todas as dependências que o executável está utilizando
````bash
    ldd <executável>
````

#### Using ffmpeg
- Converting videos
````bash
    ffmpeg -i Video_10.mp4 -acodec aac -ac 2 -ab 96k -ar 44100 -b 345k -s 1280x720 Video_16.mp4
    ffmpeg -i Midia_16.mp4 -acodec libvorbis -ac 2 -ab 96k -ar 44100 -b 345k -s 1280x720 Midia_16.webm
    ffmpeg -i Audio.ogg -vn -ar 44100 -ac 2 -ab 192k -f mp3 Audio.mp3
````

- Concatena
````bash
    ffmpeg -f concat -safe 0 -i concat.txt -c copy output.mp4
````

#### Manual de um comando
````bash
    man <commnad_name>
````

#### Using pkg
- Provides a unified interface for querying installed libraries for the purpose of compiling software from its source code
````bash
    pkg-config --libs gstreamer-1.0 //
````

- Return all pkgs and versions
````bash
    dpkg -l | grep gstreamer
````

- Shows where is the pkg
````bash
    which gst-inspect-1.0
````

#### Solving GUI Problems
- Reinstall ubuntu-desktop
````bash
    sudo apt-get install --reinstall ubuntu-desktop
````

- Restart only GUI Session
````bash
    sudo service lightdm restart
````

#### Open Documents, Folders etc.
````bash
    xdg-open
    gnome-open
````

#### Print the number of lines of a file
````bash
    wc -l DCP_PERSONAGEMPROCESSO_2013-2017.csv
````

#### Print the first 20 lines of a file
````bash
    head -20 file.csv
````

#### Java
- Escolhendo a maquina virtual instalada
````bash
	sudo update-alternatives --config java
````
- Abrindo programa com Java
````bash
	java -jar ~/ProgramasRFB/IRPF2020/irpf.jar
````

#### Snap
- Search an app
````bash
    snap find dbeaver
````

- Install an app
````bash
    sudo snap install dbeaver-ce
````

- Get app info
````bash
    snap info <snap1>
    snap info dbeaver-ce
````

- List app versions
````bash
    snap list <snap1> --all
    snap list dbeaver-ce --all
````

- Upgrade app
````bash
    sudo snap refresh <snap1>
    sudo snap refresh dbeaver-ce
````

- Downgrade app
````bash
    sudo snap revert <snap1>
    sudo snap revert dbeaver-ce
````

- Supress updates
````bash
    snap refresh --hold=<duration> <snap1> <snap2>
    snap refresh --hold=forever dbeaver-ce
````

- Remove an app
````bash
    sudo snap remove <snap1>
    sudo snap remove dbeaver-ce
````

- Remove all disabled snaps
````bash
    snap list --all | awk '/disabled/{print $1, $3}' | while read snapname revision; do sudo snap remove "$snapname" --revision="$revision"; done
````

