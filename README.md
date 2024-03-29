# VMC blockchain over Cosmos-SDK

## Installation on fresh Debian-Linux

### Install go
1. Download go ``wget https://dl.google.com/go/go1.12.6.linux-amd64.tar.gz`` (see: https://golang.org/doc/install)
2. Install go ``tar -C /usr/local -xzf go1.12.6.linux-amd64.tar.gz``
3. Add this to your path variable in .profile ``export PATH=$PATH:/usr/local/go/bin;source .profile``
4. Execute:
```
mkdir -p $HOME/go/bin
echo "export GOPATH=$HOME/go" >> ~/.bash_profile
source ~/.bash_profile
echo "export GOBIN=$GOPATH/bin" >> ~/.bash_profile
source ~/.bash_profile
echo "export PATH=$PATH:$GOBIN" >> ~/.bash_profile
source ~/.bash_profile
```
5. Make make sure go lang works ``go version``
6. Install essentials  ``apt-get install build-essential git jq``
7. Clone Mobotiq-Cosmos Blockchain ``git clone https://github.com/vmc/mobotiq-node.git; cd mobotiq-node``
8. Type ``make``
9. Import genesis.json to connect to Mobotiq network ``cp genesis.json ~/.nsd/config``
10. Add seed to ~/.nsd/config/config.toml in 
```
seeds = "aa07d07b42f692436f6e1540a50d8432d363aa9c@34.66.28.194:26656"
```
10. Run Mobotiq-cosmos blockchain ``nsd start`` to start a new Mobotiq cosmos node!