DDNS Agent
==========

This repository contains the code for the DDNS (Dynamic DNS) agent. It is a Node.js application built using the Moleculer framework and other related libraries.

Installation
------------

To install the dependencies, run the following command:

bashCopy code

`npm install`

Usage
-----

To start the DDNS agent, use the following command:

bashCopy code

`npm start`

Configuration
-------------

The agent can be configured using the `config.js` file. It uses the `config-mixin` library to load the configuration. The available configuration options are as follows:

-   `ddns.logging`: Enable or disable logging (default: `true`)

Actions
-------

The DDNS agent provides the following actions:

### createRecord

Creates a new DNS record.

-   Parameters:
    -   `fqdn`: Fully Qualified Domain Name (string, required)
    -   `type`: Type of the DNS record (enum: A, AAAA, CNAME, SOA, MX, NS, TXT, CAA, SRV; required)
    -   `data`: Data for the DNS record (string, required)
    -   `replace`: Replacement string (string, optional)
    -   `ttl`: Time to Live value (number, default: 99, optional)
    -   `priority`: Priority value (number or string, default: 5, optional)
    -   `flag`: Flag value (number, default: 0, optional)
    -   `tag`: Tag value (string, optional)
    -   `admin`: Admin value (string, optional)
    -   `serial`: Serial value (number, optional)
    -   `refresh`: Refresh value (number, optional)
    -   `retry`: Retry value (number, optional)
    -   `expiration`: Expiration value (number, optional)
    -   `minimum`: Minimum value (number, optional)
    -   `nullified`: Nullified flag (boolean, default: false, optional)

### removeRecord

Removes a DNS record.

-   Parameters:
    -   `id`: ID of the record (string, required)
    -   `fqdn`: Fully Qualified Domain Name (string, required)
    -   `network`: Network value (string, optional)
    -   `type`: Type of the DNS record (enum: A, AAAA, CNAME, SOA, MX, NS, TXT, CAA, SRV; required)

### sync

Synchronizes the DNS records with the server.

### maps

Retrieves the DNS record maps.

### stats

Retrieves the statistics of the DNS agent.

### bind

Binds the DNS record to an address.

-   Parameters:
    -   `address`: Address to bind (string, required)
    -   `proxy`: Proxy flag (boolean, default: false, optional)

License
-------

This project is licensed under the MIT License.
