# Setup Validator

## Install Geth

## Install Prysm

### Install Prysm


mkdir prysm && cd prysm

./prysm.sh beacon-chain --http-web3provider=http://localhost:8545 --pyrmont

## Get Goerli

## Generate Keys

```
curl -LO https://github.com/ethereum/eth2.0-deposit-cli/releases/download/v1.1.0/eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz
tar -xzf eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz 
rm -f eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz 
eth2deposit-cli-ed5a6d3-linux-amd64/
./deposit new-mnemonic --num_validators 1 --mnemonic_language=english --chain pyrmont
```
```shell
mkdir -p goethereum
mkdir -p grafana
mkdir -p prometheus
mkdir -p prysm/beaconchain
mkdir -p prysm/validator/passwords
echo <YOUR_WALLET_PASSWORD> >> prysm/validator/password/wallet-password
mkdir -p prysm/validator/wallets
mkdir -p keys
cp -r <YOUR_KEYS_PATH/validator_keys> keys/
```

docker-compose -f docker-compose.create-account.yml run validator-import-launchpad
docker-compose -f docker-compose.create-account.yml run validator-list-accounts
docker-compose up -d












    1  sudo apt-get update
    2  sudo apt-get upgrade
    3  sudo apt-get install nodejs
    4  nodejs -v
    5  exit
    6  cat /etc/ssh/ssh_config 
    7  exit
    8  pwd
    9  exit
   10  ls
   11  ls -lh
   12  pwd
   13  ls -la
   14  exit
   15  ls
   16  dmesg
   17  dmsg
   18  dmesg
   19  docker ps
   20  docker
   21  exit
   22  sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.factory-defaults 
   23  sudo vi /etc/ssh/sshd_config
   24  l
   25  ls -la
   26  pwd
   27  mkdir ~/.ssh
   28  chmode 700 ~/.ssh/
   29  chmod 700 ~/.ssh/
   30  l
   31  ls -la
   32  vi .ssh/authorized_keys
   33  chmod 600 ~/.ssh/authorized_keys
   34  logout
   35  ufw -l
   36  ufw
   37  sudo ufw
   38  netstat -an
   39  vi /etc/ssh/sshd_config
   40  sudo vi /etc/ssh/sshd_config
   41  sudo cat /etc/ssh/sshd_config
   42  service sshd status
   43  service sshd restart
   44  sudo service sshd restart
   45  service sshd status
   46  exit
   47  logout
   48  exit
   49  sudo apt update
   50  sudo apt upgrade
   51  sudo apt gist-upgrade
   52  sudo apt dist-upgrade
   53  sudo apt install ufw
   54  ufw
   55  ufw list
   56  ufw status
   57  sudo ufw status
   58  sudo ufw allow 22/tcp
   59  sudo ufw status
   60  sudo ufw allow 9022/tcp
   61  sudo ufw enable
   62  sudo ufw status numbered
   63  ufw app list
   64  sudo ufw app list
   65  sudo ufw app info OpenSSH
   66  sudo ufw allow OpenSSH
   67  sudo grep '^### tuple' /lib/ufw/user*.rules
   68  whereis ufw
   69  cat /lib/ufw/ufw-init
   70  cat /lib/ufw/ufw-init-functions 
   71  sudo ufw enable
   72  sudo ufw status
   73  sudo vi /etc/ssh/sshd_config
   74  sudo ufw status
   75  sudo service sshd restart
   76  sudo service sshd status
   77  sudo vi /etc/ssh/sshd_config
   78  sudo service sshd restart
   79  sudo service sshd status
   80  sudo ufw allow 30303
   81  ufw status numbered
   82  sudo ufw status numbered
   83  sudo add-apt-repository -y ppa:ethereum/ethereum
   84  sudo add-repository -y ppa:ethereum/ethereum
   85  sudo apt-get install software-properties-common
   86  sudo apt update
   87  sudo add-apt-repository -y ppa:ethereum/ethereum
   88  sudo apt update
   89  sudo apt install geth
   90  sudo useradd --no-create-home --shell /bin/false goeth
   91  sudo mkdir -p /var/lib/goethereum
   92  sudo chown goeth-goeth -R /var/lib/goethereum/
   93  sudo chown -R goeth:goeth /var/lib/goethereum/
   94  sudo vi /etc/systemd/system/geth.service
   95  sudo systemctl start geth
   96  sudo systemctl daemon-reload
   97  sudo systemctl start geth
   98  sudo vi /etc/systemd/system/geth.service
   99  sudo systemctl daemon-reload
  100  sudo systemctl start geth
  101  dmesg
  102  sudo journalctl -f -u geth.service
  103  whereis geth
  104  sudo vi /etc/systemd/system/geth.service
  105  whereis geth
  106  sudo systemctl daemon-reload
  107  sudo systemctl start geth
  108  sudo journalctl -f -u geth.service
  109  dmesg
  110  sudo journalctl -f -u geth.service
  111  sudo vi /etc/systemd/system/geth.service
  112  sudo apt-get install docker
  113  apt-get install     apt-transport-https     ca-certificates     curl     gnupg-agent     software-properties-common
  114  sudo apt-get install     apt-transport-https     ca-certificates     curl     gnupg-agent     software-properties-common
  115  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  116  sudo apt-key fingerprint 0EBFCD88
  117  sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
  118     $(lsb_release -cs) \
  119     stable"
  120  sudo apt-get update
  121  sudo apt-get install docker-ce docker-ce-cli containerd.io
  122  docker
  123  docker run hello-world
  124  sudo docker run hello-world
  125  docker ps
  126  sudo docker ps
  127  sudo docker images
  128  sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  129  docker-compose version
  130  sudo docker-compose version
  131  sudo docker-compose --version
  132  sudo /usr/local/bin/docker-compose --version
  133  sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
  134  docker-compose
  135  sudo docker-compose
  136  sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-Linux-x86_64" -o /usr/local/bin/docker-compose
  137  sudo docker-compose
  138  sudo /usr/local/bin/docker-compose 
  139  sudo chmod +x /usr/local/bin/docker-compose
  140  docker-compose
  141  docker-compose --version
  142  docker ps
  143  ip addr show | grep "inet " | grep -v 127.0.0.1
  144  cd ethereum2/
  145  cd prysm/
  146  l
  147  ls dist/
  148  ls -la
  149  ls dis
  150  ls dist
  151  cd dist
  152  ls -la
  153  ls -lah
  154  ..
  155  cd ..
  156  ./prysm.sh -h
  157  ./prysm.sh beacon-chain -h
  158  ..
  159  cd ..
  160  git clone https://github.com/ethereum/eth2.0-deposit-cli.git
  161  cd eth2.0-deposit-cli/
  162  l
  163  ls -la
  164  ./deposit.sh -h
  165  ./deposit.sh help
  166  ./deposit new-mnemonic --num_validators 1 --mnemonic_language=english --chain pyrmont 
  167  ..
  168  cd ..
  169  rm -rf eth2.0-deposit-cli/
  170  curl -LO https://github.com/ethereum/eth2.0-deposit-cli/releases/download/v1.1.0/eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz
  171  tar -xzf eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz 
  172  ls -la
  173  rm -f eth2deposit-cli-ed5a6d3-linux-amd64.tar.gz 
  174  ls -la
  175  ./eth2deposit-cli-ed5a6d3-linux-amd64/deposit new-mnemonic --num_validators 1 --mnemonic_language=english --chain pyrmont 
  176  cd eth2deposit-cli-ed5a6d3-linux-amd64/
  177  cd ..
  178  ls
  179  ls -la
  180  cd eth2deposit-cli-ed5a6d3-linux-amd64/
  181  ls -la
  182  ./deposit new-mnemonic --num_validators 1 --mnemonic_language=english --chain pyrmont 
  183  l
  184  ls -la
  185  sudo docker stats
  186  docker ps
  187  sudo docker ps
  188  history


      1  sudo apt-get update
    2  sudo apt-get upgrade
    3  sudo apt-get install nodejs
    4  nodejs -v
    5  exit
    6  cat /etc/ssh/ssh_config 
    7  exit
    8  pwd
    9  exit
   10  ls
   11  ls -lh
   12  pwd
   13  ls -la
   14  exit
   15  ls
   16  dmesg
   17  dmsg
   18  dmesg
   19  docker ps
   20  docker
   21  exit
   22  sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.factory-defaults 
   23  sudo vi /etc/ssh/sshd_config
   24  l
   25  ls -la
   26  pwd
   27  mkdir ~/.ssh
   28  chmode 700 ~/.ssh/
   29  chmod 700 ~/.ssh/
   30  l
   31  ls -la
   32  vi .ssh/authorized_keys
   33  chmod 600 ~/.ssh/authorized_keys
   34  logout
   35  ufw -l
   36  ufw
   37  sudo ufw
   38  netstat -an
   39  vi /etc/ssh/sshd_config
   40  sudo vi /etc/ssh/sshd_config
   41  sudo cat /etc/ssh/sshd_config
   42  service sshd status
   43  service sshd restart
   44  sudo service sshd restart
   45  service sshd status
   46  exit
   47  logout
   48  exit
   49  sudo apt update
   50  sudo apt upgrade
   51  sudo apt gist-upgrade
   52  sudo apt dist-upgrade
   53  sudo apt install ufw
   54  ufw
   55  ufw list
   56  ufw status
   57  sudo ufw status
   58  sudo ufw allow 22/tcp
   59  sudo ufw status
   60  sudo ufw allow 9022/tcp
   61  sudo ufw enable
   62  sudo ufw status numbered
   63  ufw app list
   64  sudo ufw app list
   65  sudo ufw app info OpenSSH
   66  sudo ufw allow OpenSSH
   67  sudo grep '^### tuple' /lib/ufw/user*.rules
   68  whereis ufw
   69  cat /lib/ufw/ufw-init
   70  cat /lib/ufw/ufw-init-functions 
   71  sudo ufw enable
   72  sudo ufw status
   73  sudo vi /etc/ssh/sshd_config
   74  sudo ufw status
   75  sudo service sshd restart
   76  sudo service sshd status
   77  sudo vi /etc/ssh/sshd_config
   78  sudo service sshd restart
   79  sudo service sshd status
   80  sudo ufw allow 30303
   81  ufw status numbered
   82  sudo ufw status numbered
   83  sudo add-apt-repository -y ppa:ethereum/ethereum
   84  sudo add-repository -y ppa:ethereum/ethereum
   85  sudo apt-get install software-properties-common
   86  sudo apt update
   87  sudo add-apt-repository -y ppa:ethereum/ethereum
   88  sudo apt update
   89  sudo apt install geth
   90  sudo useradd --no-create-home --shell /bin/false goeth
   91  sudo mkdir -p /var/lib/goethereum
   92  sudo chown goeth-goeth -R /var/lib/goethereum/
   93  sudo chown -R goeth:goeth /var/lib/goethereum/
   94  sudo vi /etc/systemd/system/geth.service
   95  sudo systemctl start geth
   96  sudo systemctl daemon-reload
   97  sudo systemctl start geth
   98  sudo vi /etc/systemd/system/geth.service
   99  sudo systemctl daemon-reload
  100  sudo systemctl start geth
  101  dmesg
  102  sudo journalctl -f -u geth.service
  103  whereis geth
  104  sudo vi /etc/systemd/system/geth.service
  105  whereis geth
  106  sudo systemctl daemon-reload
  107  sudo systemctl start geth
  108  sudo journalctl -f -u geth.service
  109  dmesg
  110  sudo journalctl -f -u geth.service
  111  sudo vi /etc/systemd/system/geth.service
  112  sudo apt-get install docker
  113  apt-get install     apt-transport-https     ca-certificates     curl     gnupg-agent     software-properties-common
  114  sudo apt-get install     apt-transport-https     ca-certificates     curl     gnupg-agent     software-properties-common
  115  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  116  sudo apt-key fingerprint 0EBFCD88
  117  sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
  118     $(lsb_release -cs) \
  119     stable"
  120  sudo apt-get update
  121  sudo apt-get install docker-ce docker-ce-cli containerd.io
  122  docker
  123  docker run hello-world
  124  sudo docker run hello-world
  125  docker ps
  126  sudo docker ps
  127  sudo docker images
  128  sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  129  docker-compose version
  130  sudo docker-compose version
  131  sudo docker-compose --version
  132  sudo /usr/local/bin/docker-compose --version
  133  sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
  134  docker-compose
  135  sudo docker-compose
  136  sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-Linux-x86_64" -o /usr/local/bin/docker-compose
  137  sudo docker-compose
  138  sudo /usr/local/bin/docker-compose 
  139  sudo chmod +x /usr/local/bin/docker-compose
  140  docker-compose
  141  docker-compose --version
  142  docker ps
  143  ip addr show | grep "inet " | grep -v 127.0.0.1
  144  history
  145  sudo journalctl -f -u geth.service
  146  sudo service geth status
  147  sudo service geth stop
  148  sudo service geth status
  149  sudo service geth start
  150  sudo service geth status
  151  sudo journalctl -f -u geth.service
  152  sudo du /var/lib/goethereum/ -h -d 1
  153  sudo journalctl -f -u geth.service
  154  sudo geth attach --datadir /var/lib/goethereum/
  155  sudo service geth status
  156  pwd
  157  history | grep systemctl
  158  git clone https://github.com/ethereum/eth2.0-deposit-cli.git
  159  l
  160  rm -r eth2.0-deposit-cli/
  161  rm -rf eth2.0-deposit-cli/
  162  pwd
  163  mkdir ethereum2
  164  cd ethereum2/
  165  mkdir prysm && cd prysm
  166  curl https://raw.githubusercontent.com/prysmaticlabs/prysm/master/prysm.sh --output prysm.sh && chmod +x prysm.sh
  167  l
  168  ls -la
  169  history | grep tulpn
  170  history | grep tulpen
  171  service geth status
  172  sudo netstat -tulpen | grep -v '127.0.0.1'  | grep -v '::1:' 
  173  netstat
  174  sudo netstat -tulpen
  175  ./prysm.sh beacon-chain --http-web3provider=http://localhost:8545
  176  ./prysm.sh beacon-chain --http-web3provider=http://localhost:8545 --pyrmont
  177  ./prsym.sh -h
  178  ./prysm.sh help
  179  ./prysm.sh beacon-chain -h
  180  echo $PATH
  181  cat /etc/systemd/system/geth.service 
  182  ..
  183  cd ..
  184  mkdir deployment
  185  ls
  186  mv deployment/ deployment-pyrmont
  187  l
  188  cd deployment-pyrmont/
  189  l
  190  ls
  191  ls -la
  192  ls
  193  du -d 1 -h /var/lib/goethereum/
  194  sudo du -d 1 -h /var/lib/goethereum/
  195  sudo docker-compose up
  196  sudo service geth status
  197  sudo service geth stop
  198  sudo docker-compose up
  199  sudo docker-compose up -d
  200  sudo du -d 1 -h /var/lib/goethereum/
  201  cat /etc/systemd/system/geth.service 
  202  sudo du -d 1 -h /var/lib/goethereum/goerli/
  203  sudo docker-compose stop
  204  sudo mv -r /var/lib/goethereum/ /var/lib/goerli/
  205  sudo mv -R /var/lib/goethereum/ /var/lib/goerli/
  206  sudo mv /var/lib/goethereum/ /var/lib/goerli/
  207  sduo ls /var/lib/goerli/
  208  sudosduo ls /var/lib/goerli/
  209  sudo ls /var/lib/goerli/
  210  mkdir /var/lib/goethereum
  211  sudo mkdir /var/lib/goethereum
  212  ls -la /var/lib/
  213  sudo mv /var/lib/goerli/ /var/lib/goethereum/
  214  ls -la /var/lib/
  215  sudo ls -la /var/lib/goethereum/goerli/
  216  sudo du -d 1 -h /var/lib/goethereum/goerli/
  217  sudo rm -rf /var/lib/goethereum/goerli/goerli/
  218  sudo du -d 1 -h /var/lib/goethereum/goerli/
  219  sudo docker-compose up -d
  220  sudo docker logs -f deployment-pyrmont_geth_1
  221  sudo du -d 1 -h /var/lib/goethereum/goerli/
  222  sudo docker-compose down
  223  sudo docker-compose up
  224  sudo docker-compose up -d
  225  docker ps
  226  sudo docker ps
  227  sudo docker exec -it deployment-pyrmont_geth_1
  228  sudo docker exec -it deployment-pyrmont_geth_1 /bin/bash
  229  sudo docker exec -it deployment-pyrmont_geth_1 shell
  230  sudo docker exec -it deployment-pyrmont_geth_1 sh
  231  sudo docker logs -f deployment-pyrmont_geth_1
  232  curl
  233  curl -s v4.ident.me
  234  sudo mkdir /var/lib/prysm/beaconchain
  235  sudo mkdir -p /var/lib/prysm/beaconchain
  236  ../prysm/prysm.sh beacon-chain -h
  237  docker-compose down
  238  sudo docker-compose down
  239  cat docker-compose.yml 
  240  sudo ufw allow 13000/tcp
  241  sudo ufw allow 12000/udp
  242  sudo ufw status
  243  docker-compose up
  244  sudo docker-compose up
  245  cat docker-compose.yml 
  246  sudo docker-compose up
  247  sudo docker-compose down
  248  sudo docker-compose up
  249  sudo docker-compose down
  250  vi docker-compose.yml 
  251  sudo docker-compose up
  252  sudo docker-compose down
  253  sudo docker-compose up
  254  sudo docker-compose up -d
  255  docker stats
  256  sudo docker stats
  257  sudo docker-compose down
  258  sudo docker ps
  259  sudo docker-compose up -d
  260  sudo docker ps
  261  free -m
  262  free -c
  263  free -m
  264  sudo docker-compose stop
  265  history
