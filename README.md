# cohod
Cosmic Horizon

# Install Golang (go)

# Install required software packages
```sudo apt-get install git curl build-essential make jq -y```

# Setup Go
```curl https://dl.google.com/go/go1.17.6.linux-amd64.tar.gz | sudo tar -C/usr/local -zxvf -```

```
cat <<'EOF' >>$HOME/.profile
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GO111MODULE=on
export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
EOF
```
<code>source $HOME/.profile</code>

<code>go version </code>

#Install Starport
<code>curl https://get.starport.network/starport | bash</code>
<code>sudo mv starport /usr/local/bin/</code>

#Install CoHo

<code>git clone https://github.com/cosmic-horizon/coho.git</code>
<code>cd ~/coho</code>
<code>starport chain build</code>


#Initiate CoHo Instance

Create
<code>cohod keys add <your_validator_key_name></code>

Import
<code>cohod keys add <your_validator_key_name> --recover</code>
  
  #Download the genesis file
  <code>curl -s https://raw.githubusercontent.com/cosmic-horizon/testnets/main/darkmatter-1/genesis.json > $HOME/.coho/config/genesis.json</code>
