<h1 align="center">github-endpoints</h1>

<h4 align="center">Find endpoints on GitHub.</h4>

<p align="center">
    <img src="https://img.shields.io/badge/go-v1.13-blue" alt="go badge">
    <img src="https://img.shields.io/badge/license-MIT-green" alt="MIT license badge">
    <a href="https://twitter.com/intent/tweet?text=https%3a%2f%2fgithub.com%2fgwen001%2fgithub-endpoints%2f" target="_blank"><img src="https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Fgithub.com%2Fgwen001%2Fgithub-endpoints" alt="twitter badge"></a>
</p>

<!-- <p align="center">
    <img src="https://img.shields.io/github/stars/gwen001/github-endpoints?style=social" alt="github stars badge">
    <img src="https://img.shields.io/github/watchers/gwen001/github-endpoints?style=social" alt="github watchers badge">
    <img src="https://img.shields.io/github/forks/gwen001/github-endpoints?style=social" alt="github forks badge">
</p> -->

---

## Install

```
go install github.com/gwen001/github-endpoints@latest
```

or

```
git clone https://github.com/gwen001/github-endpoints
cd github-endpoints
go install
```

## Usage

```
$ github-endpoints -h

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
    	github token (required), can be:
    	  • a single token
    	  • a list of tokens separated by comma
    	  • a file (.tokens) containing 1 token per line
    	if the options is not provided, the environment variable GITHUB_TOKEN is readed, it can be:
    	  • a single token
    	  • a list of tokens separated by comma
```

If you want to use multiple tokens, you better create a `.tokens` file in the executable directory with 1 token per line  
```
token1
token2
...
```
or use an environment variable with tokens separated by comma:  
```
export GITHUB_TOKEN=token1,token2...
```

Tokens are disabled when GitHub raises a rate limit alert, however they are re-enable 1mn later.
You can disable that feature by using the option `-k`.

<img src="https://github.com/gwen001/github-endpoints/raw/master/preview.png">

## Todo

- change the order of the extra searches ?
- ?

## Changelog

**20/09/2022**
- fix regexp for subdomains

**25/09/2020**
- quick mode added
- tokens can be read from any file

**23/09/2020**
- fixed an issue in the api call (params name)
- added binary

**10/08/2020**
- creation

---

Feel free to [open an issue](/../../issues/) if you have any problem with the script.  

