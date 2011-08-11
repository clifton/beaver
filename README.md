# Beaver - log tailing over tcp

## What does beaver do?

Beaver chucks logfiles anywhere we want via TCP. It's kinda like tailing a log
and piping the output to netcat, except without tail or netcat.

## Why would a beaver do that?

Syslog-shipper was constantly losing connection to loggly and I had no
intention of writing monitoring scripts for it.

## Installation

- Install nodejs available at nodejs.org
- Install NPM via `curl http://npmjs.org/install.sh | sh`
- `npm install -g beaver`
- `beaver logs/my-huge.log yourtargetdomain.com:1337`

## Daemoning

- `npm install -g forever`
- `forever beaver logs/very-important-log.log importantplace.com:1337`
