# CloudClip

Your own clipboard in the cloud, copy and paste text with gist. Inspired by pbcopy/pbpaste from Mac OS X.

## Tutorial

Copy text on a local system to the cloud:

    echo "Hello, Cloud Clipboard" | cloudcopy

Paste on a remote system from the cloud:

    cloudpaste

And you will see the text coppied from another system:

    Hello, Cloud Clipboard

Same access token and gist id must be setup before copy/paste, see below


## Installation

Clone the repository from github:

```bash
git clone https://github.com/skywind3000/CloudClip.git
```

Add repository path to your `$PATH`:

For linux, add these line at the bottom of your `.bashrc`:

    export PATH="/path-to-cloud-clip:$PATH"

For Windows:

Manully setup the PATH in your control panel. 

## Documentation

usage: python cloudclip.py <operation> [...]
operations:

```
-i token [id]  Initialize token and id, create a new gist if id is empty
-c [name]      Takes the standard input and places it in the cloud
-p [name]      Read content from cloud and output to standard output
-l             List information of the gist
-e             Clean the clipboard
```

A github access token is needed before everything, you can generate a new one from: https://github.com/settings/tokens

Create a new gist with "-i token" on your own PC, remember the gist id. then use "-i token id" on a remote one which you may exchange data with.

## Requirement

* Python 2
* [requests](http://www.python-requests.org/en/master/)

Install requests with pip:

    pip install requests

## Credit

TODO
