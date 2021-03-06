# Collider for CloudFoundry
A websocket-based signaling server in Go based on appartc project

# Building

1. Install the Go tools and workspaces as documented at [http://golang.org/doc/install](http://golang.org/doc/install) and [http://golang.org/doc/code.html](http://golang.org/doc/code.html) 

2. Checkout this repository
```
go get github.com/tkausch/collidermain
```

3. Now you should be able to run ```mycollider``` locally
```
UM00339:collidermain tzhkath4$ go run mycollider.go 
2017/03/07 16:32:13 Starting collider: tls = false, port = 8090, room-server=https://appr.tc/
```

# Deploy on Cloud Foundry

1. Install the ```glide``` package manager 
```
brew install glide
```  

2. Update dependencies 
```
glide up
```

3. Login into Cloud Foundry and push the go app:
```
cf push mycollider
```

# Configure Collider Environment

To define your room server you can set the following environment variable 
```
ROOM_SRV = https://appr.tc
```
 
