#### Installation:

```
sudo apt-get update
sudo apt-get -y upgrade
```

```
sudo curl -O https://storage.googleapis.com/golang/go1.9.linux-amd64.tar.gz
sudo tar -xvf go1.9.linux-amd64.tar.gz
sudo mv go /usr/local
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.profile
source ~/.profile
```

#### Run:

`go run hello.go`

