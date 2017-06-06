# MoneyGo

## Installation

First, install npm and libofx in your distribution:

	$ sudo pacman -S npm libofx

Install browserify globally using npm:

	$ sudo npm install -g browserify

You'll then want to build everything (the Golang and Javascript portions) using
something like:

	$ export GOPATH=`pwd`
	$ go get -v github.com/aclindsa/moneygo
	$ go generate -v github.com/aclindsa/moneygo
	$ go install -v github.com/aclindsa/moneygo

## Running

Assuming you're in the same directory you ran the above installation comands
from, running MoneyGo is then as easy as:

	$ ./bin/moneygo \
	  -port 8080 \
	  -base src/github.com/aclindsa/moneygo/