[![Storj Bridge](https://nodei.co/npm/dgp-hub.png?downloads=true)](http://storj.github.io/hub)
=======================================================================================================

[![Build Status](https://img.shields.io/travis/dgpdev/dgp-hub.svg?style=flat-square)](https://travis-ci.org/dgpdev/dgp-hub)
[![Coverage Status](https://img.shields.io/coveralls/dgpdev/dgp-hub.svg?style=flat-square)](https://coveralls.io/r/dgpdev/dgp-hub)
[![NPM](https://img.shields.io/npm/v/dgp-hub.svg?style=flat-square)](https://www.npmjs.com/package/dgp-hub)
[![GitHub license](https://img.shields.io/badge/license-AGPLv3-blue.svg?style=flat-square)](https://raw.githubusercontent.com/Storj/data-api/master/LICENSE)

Access the [Storj](http://storj.io) network via simple REST API.

Running Your Own Bridge
-----------------------

If you're planning to run your own hub in production, mainnet, there are several issues that need to be addressed before this use case will be better supported. The largest of the issues is that there are several manual processes that will need to be run including running monthly payouts to farmers as well as communicating with farmers to add a new "trusted key" for the hub. Decentralized hubs is described in the [Storj whitepaper](https://storj.io/storj.pdf) *(a.k.a Federated Bridges)* and is an area of ongoing research. There are also several [Storj Improvement Proposals](https://github.com/storj/sips) to streamline these processes using Ethereum smart contracts.

Aside from those issues, running a hub within a private network is currently an option as those will not be issues in that environment. Please see https://github.com/storj/storj-sdk and https://github.com/storj/integration for quick setup of an entire Storj network.

Quick Start
-----------

Install MongoDB, Git and Wget:

```
apt-get install mongodb redis-server git wget
```

Install NVM, Node.js and NPM:

```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.30.1/install.sh | bash
source ~/.profile
nvm install --lts
```

Clone the repository, install dependencies:

```
git clone https://github.com/dgpdev/dgp-hub.git && cd hub
npm install && npm link
```

Start the server (set the `NODE_ENV` environment variable to specify the config):

```
NODE_ENV=develop dgp-hub
```

> **Note:** Storj Bridge cannot communicate with the network on it's own, but 
> instead must communicate with a running 
> [Storj Complex](https://github.com/Storj/complex) instance.

This will use the configuration file located at `~/.dgp-hub/config/develop.json`.

Windows
-------

Install utilizing automated script

```
https://github.com/Storj/storj-automation/archive/master.zip
```

The default configuration can be modified as needed.  It is located at

```
%USERPROFILE%\.dgp-hub\config
```

Edit `production` in notepad/wordpad. For more information, see [the documentation](http://storj.github.io/hub).

License
-------

Storj Bridge - Access The Storj Network via REST Interface  
Copyright (C) 2017 Storj Labs, Inc

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see http://www.gnu.org/licenses/.

Terms
-----

This software is released for testing purposes only. We make no guarantees with
respect to its function. By using this software you agree that Storj is not
liable for any damage to your system. You also agree not to upload illegal
content, content that infringes on other's IP, or information that would be
protected by HIPAA, FERPA, or any similar standard. Generally speaking, you
agree to test the software responsibly. We'd love to hear feedback too.
