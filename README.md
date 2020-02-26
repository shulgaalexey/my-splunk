# Learning Splunk
Learning Splunk solutions


This is a simple project to learn Splunk

Splunk login:
ashulga
shulgaalexey+splunk@gmail.com
pw: XXX

# Container run
```
docker run -it -p 88:8000 ubuntu /bin/bash

apt update
apt upgrade
apt install -y net-tools wget git-all curl vim
```

# VIM install
```
git clone https://github.com/scrooloose/nerdtree.git ~/.vim/pack/vendor/start/nerdtree
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/nerdtree/doc" -c q
vim ~/.vimrc
syntax on
set noswapfile
set number
set hlsearch
```

apt install firefox
wget https://github.com/browsh-org/browsh/releases/download/v1.6.4/browsh_1.6.4_linux_amd64.deb
apt install ./browsh_1.6.4_linux_amd64.deb
rm ./browsh_1.6.4_linux_amd64.deb
browsh

# Download Splunk via command line
```
wget -O splunk-8.0.2-a7f645ddaf91-linux-2.6-amd64.deb 'https://www.splunk.com/bin/splunk/DownloadActivityServlet?architecture=x86_64&platform=linux&version=8.0.2&product=splunk&filename=splunk-8.0.2-a7f645ddaf91-linux-2.6-amd64.deb&wget=true'

apt install ./splunk-8.0.2-a7f645ddaf91-linux-2.6-amd64.deb

/opt/splunk/bin/splunk start --accept-license
admin
adminadmin

vim /opt/splunk/etc/splunk-launch.conf
OPTIMISTIC_ABOUT_FILE_LOCKING = 1

In browser:
0.0.0.0:88
or
localhost:88
or
127.0.0.1:88
```

# Run another docker console
```
docker ps -a
docker exec -it 1c0cc4922bee bash
```

# Start a container
```
docker start 1c0cc4922bee
```


================================================================================


# Install Java 11
```
apt-get install openjdk-11-jre openjdk-11-jdk
```

# Install git and curl
```
apt-get install git-all
apt-get install curl
```

# VIM install
```
apt-get install vim
git clone https://github.com/scrooloose/nerdtree.git ~/.vim/pack/vendor/start/nerdtree
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/nerdtree/doc" -c q
mkdir -p ~/.vim/syntax && cd ~/.vim/syntax
curl -LSso "antlr4.vim" "https://raw.githubusercontent.com/dylon/vim-antlr/master/syntax/antlr4.vim"
vim ~/.vimrc
syntax on
set noswapfile
set number
set hlsearch
au BufRead,BufNewFile *.g4 set filetype=antlr4
```

# ANTLR install
```
cd /usr/local/lib
curl -O https://www.antlr.org/download/antlr-4.8-complete.jar
```

# Setup bash
```
vim .bash_profile
alias ll='ls -lGa'
export CLASSPATH=".:/usr/local/lib/antlr-4.8-complete.jar:$CLASSPATH"
alias antlr4='java -jar /usr/local/lib/antlr-4.8-complete.jar'
alias grun='java org.antlr.v4.runtime.misc.TestRig'
```

# Test ANTLR installed correctly
```
java -jar /usr/local/lib/antlr-4.8-complete.jar
or
java org.antlr.v4.Tool
or
antlr4
```

# Run another docker console
```
docker ps -a
docker exec -it 1c0cc4922bee bash
```

# Start a container
```
docker start 1c0cc4922bee
```

# Commit snf push a new image to the repository using the CLI
```
//docker tag local-image:tagname new-repo:tagname
docker tag 6d0557fcfc07 shulgaalexey/myantlr:myantlr03
docker login -u "shulgaalexey" -p "qwer1357" docker.io && docker push shulgaalexey/myantlr:myantlr03
docker login -u "shulgaalexey" -p "qwer1357" docker.io && docker pull shulgaalexey/myantlr:myantlr03
`
