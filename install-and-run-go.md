#### Installation:
```
sudo apt install golang
```
or
```
sudo apt-get update
sudo apt-get -y upgrade

sudo curl -O https://dl.google.com/go/go1.12.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.12.linux-amd64.tar.gz

echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.profile
echo 'export PATH=$PATH:$HOME/go/bin' >> ~/.profile
source ~/.profile
```

#### Run:

`go run hello.go`

