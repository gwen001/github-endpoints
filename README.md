# github-endpoints

Find endpoints on GitHub.


# Warning

This repository is not public yet.
If you get access it means that you're part of the GitHub sponsors program.
For now, you're not allowed to release it, publish it or give access to anyone else.

Please remember that this program is still under development, bugs and changes may occur.


# Install

```
go get -u github.com/gwen001/github-endpoints
```

or

```
git clone https://github.com/gwen001/github-endpoints
cd github-endpoints
go install
```


# Usage

```
github-endpoints -h

Usage of github-endpoints:
  -all
    	displays urls of all other domains, default=false
  -d string
    	domain you are looking for (required)
  -e	extended mode, also look for <dummy>example.com
  -k	exit the program when all tokens have been disabled
  -o string
    	output file, default: <domain>.txt
  -r	display relative urls, default=false
  -raw
    	raw output
  -t string
    	github token (required)
```

If you want to use multiple tokens, you should create a `.tokens` file in the executable directory with 1 token per line  
```
token1
token2
...
```
or use an environment variable with tokens separated by comma:  
```
export GITHUB_TOKEN=token1,token2...
```

<img src="https://github.com/gwen001/github-endpoints/raw/master/preview.png">


# Todo

- change the order of the extra searches ?
- ?


# Changelog

**23/09/2020**
- fixed an issue in the api call (params name)
- added binary

**10/08/2020**
- creation


---

Feel free to ping me on Twitter if you have any problem to use the script.  
https://twitter.com/gwendallecoguic
