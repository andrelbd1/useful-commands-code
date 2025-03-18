### Install Ubuntu (Dual Boot)
- Dual boot: https://lcomlinux.wordpress.com/2018/08/20/instalacao-ubuntu-18-04-e-windows-10-dual-boot-uefi/
- Disable RST: https://askubuntu.com/questions/1233623/workaround-to-install-ubuntu-20-04-with-intel-rst-systems
- Handle bitlocker: https://itsfoss.com/dual-boot-ubuntu-windows-bitlocker/

### Install general packages:
- Essentials apps
````bash
    sudo apt install vim terminator aptitude ubuntu-restricted-extras ffmpeg vlc p7zip p7zip-full p7zip-rar unrar pdfarranger kazam kdenlive git gh gitk meld gimp build-essential mesa-common-dev screenruler python3 python3-dev python3-gpg retext htop exfat-fuse exfat-utils -y
````

- Latex apps
````bash
    sudo apt install kile texmaker texlive-lang-portuguese -y 
````

- Misc.
````bash
    sudo apt install filezilla mysql-server apache2 phpmyadmin mysql-workbench -y 
````

- Other multimedia packages
````bash
    sudo apt install faac faad ffmpeg2theora flac flashplugin-installer icedax id3v2 lame libjpeg-progs mencoder mjpegtools mpeg2dec mpeg3-utils mpegdemux mpg123 mpg321 regionset sox uudeview vorbis-tools x264 arj unace-nonfree -y
````

- Install general packages using snap:
````bash
    sudo snap install spotify dbeaver-ce discord
    sudo snap install slack --classic
    sudo snap install code --classic
````

### Install Gnome extensions
- Install Gnome packages
````bash
    sudo apt install gnome-shell-extensions gnome-shell-ubuntu-extensions gnome-shell gnome-shell-common gnome-shell-extension-appindicator gnome-shell-extension-alphabetical-grid gnome-shell-extension-prefs gnome-shell-extension-manager -y
````

- View extensions installed
   - https://extensions.gnome.org/local/

- Essential extensions
   - [Alphabetical App Grid](https://extensions.gnome.org/extension/4269/alphabetical-app-grid/)
   - [Caffeine](https://extensions.gnome.org/extension/517/caffeine/)
   - [Hide Activities Button](https://extensions.gnome.org/extension/744/hide-activities-button/)
   - [OpenWeather Refined](https://extensions.gnome.org/extension/6655/openweather/)
   - [Panel World Clock (Lite)](https://extensions.gnome.org/extension/946/panel-world-clock-lite/)
   - [Places Status Indicator](https://extensions.gnome.org/extension/8/places-status-indicator/)
   - [Screenshot Window Sizer](https://extensions.gnome.org/extension/881/screenshot-window-sizer/)
   - [Status Area Horizontal Spacing](https://extensions.gnome.org/extension/355/status-area-horizontal-spacing/)
   - [System Monitor](https://extensions.gnome.org/extension/6807/system-monitor/)
   - [Ubuntu AppIndicators](https://extensions.gnome.org/extension/1301/ubuntu-appindicators/)
   - [Ubuntu Dock](https://extensions.gnome.org/extension/1300/ubuntu-dock/)
   - [User Themes](https://extensions.gnome.org/extension/19/user-themes/)

### Install PyEnv
- Install dependencies
````bash
    sudo apt install libbz2-dev libncurses-dev libffi-dev libssl-dev libsqlite3-dev tk-dev libreadline-dev liblzma-dev
````

- Download pyenv
````bash
    curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
````

- Set .bashrc
````bash
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
    echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
    echo 'eval "$(pyenv init -)"' >> ~/.bashrc
    source ~/.bashrc
````

### Install Spark
````bash
    sudo apt-get update
    sudo apt install curl mlocate default-jdk -y
    
    # download spark 3.4 or higher version on https://spark.apache.org/downloads.html
    wget https://dlcdn.apache.org/spark/spark-3.4.0/spark-3.4.0-bin-hadoop3.tgz 
    tar xvf spark-3.4.0-bin-hadoop3.tgz
    sudo mv spark-3.4.0-bin-hadoop3/ /opt/spark
    
    # add these lines in ~/.bashrc:
    export SPARK_HOME=/opt/spark
    export PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin
    
    # after run .bashrc:
    source ~/.bashrc
````

### Set github
````bash
    git config --global user.name "André Brandão"
    git config --global user.email "andrelbd1@gmail.com"
````

### Set MySql
````bash
    sudo mysql_secure_installation
    sudo mysql
    
    mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'very_strong_password';
    mysql> FLUSH PRIVILEGES;
````

### Set phpmyadmin
````bash
    cp -r /usr/share/phpmyadmin/ /var/www/phpmyadmin vim
````
- In case of localhost/phpmyadmin not working
````bash
    # Access apache2.conf
    sudo nano /etc/apache2/apache2.conf

    # Include this line
    /etc/phpmyadmin/apache.conf

    # Restart apache
    sudo service apache2 restart
````

### SonarQube using Docker: 
- Source: https://docs.sonarsource.com/sonarqube/10.5/setup-and-upgrade/install-the-server/installing-sonarqube-from-docker/

- Create volume
````bash
    docker volume create --name sonarqube_data
    docker volume create --name sonarqube_logs
    docker volume create --name sonarqube_extensions
````

- Starting
````bash
   docker run -d --name sonarqube \
    -p 9000:9000 \
    -v sonarqube_data:/opt/sonarqube/data \
    -v sonarqube_extensions:/opt/sonarqube/extensions \
    -v sonarqube_logs:/opt/sonarqube/logs \
    sonarqube
````
- PS: Default credentials: admin admin

## SonarScanner
- Source: https://joorgelm.medium.com/sonarscanner-instala%C3%A7%C3%A3o-e-configura%C3%A7%C3%A3o-para-o-sonarqube-825d0b208c32
- Download: https://docs.sonarqube.org/latest/analysis/scan/sonarscanner/
- Save and extract file at /home
- Set file /home/<your-user>/sonar-scanner/conf/sonar-scanner.properties
````bash
    # Set here general information about the environment, such as SonarQube server connection details for example
    # No information about specific project should appear here
    # — — — Default SonarQube server
    sonar.host.url=http://localhost:9000
    # — — — Default source code encoding
    #sonar.sourceEncoding=UTF-8
````
- Set .bashrc adding
````bash
    export PATH=$PATH:/home/<seu-usuario>/sonar-scanner/bin
````
- Run .bashrc:
````bash
    source .bashrc
````
- Run "sonar-scanner -v" and check output is:
````bash
    INFO: Scanner configuration file: /home/<seu-usuario>/sonar-scanner/conf/sonar-scanner.properties
    INFO: Project root configuration file: NONE
    INFO: SonarQube Scanner 4.2.0.1873
    INFO: Java 11.0.3 AdoptOpenJDK (64-bit)
    INFO: Linux 4.15.0–88-generic amd64
````
