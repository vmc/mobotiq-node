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
6. Install essentials  ``apt-get install build-essential git``
7. Clone VMC-Cosmos Blockchain ``git clone https://github.com/inspiraluna/vmc-token.git; cd vmc-token``
8. Type ``make``
9. Run VMC-cosmos blockchain ``nscd init; nscd start`` to start a new blockchain
10. Import genesis.json to connect to vmc network
11. Add seed nodes.
