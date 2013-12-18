[![Build Status](https://travis-ci.org/mozilla/webmaker.org.png)](https://travis-ci.org/mozilla/webmaker.org)
[![Dependency Status](https://gemnasium.com/mozilla/webmaker.org.png)](https://gemnasium.com/mozilla/webmaker.org)


# webmaker.org

## Dependencies

The setup portion of this README assumes you have the following installed:

* Node.js & npm
* Bower: `npm install -g bower`
* grunt-cli: `npm install -g grunt-cli`

You should also have these Webmaker stack applications running:

* MakeAPI: [https://github.com/mozilla/MakeAPI]()
* Webmaker Login: [https://github.com/mozilla/login.webmaker.org]()

## Project Setup

1. Clone webmaker.org and enter the directory: `git clone https://github.com/mozilla/webmaker.org && cd webmaker.org`
2. Install webmaker.org's Node and Bower dependencies: `npm install`
3. Copy the configuration template to its expected location: `cp env.dist .env`
4. Open `.env` in your favourite text editor and ensure that your `PORT`, `APP_HOSTNAME`, `MAKE_ENDPOINT`, `LOGIN` and `LOGINAPI` environment variables are set to the correct values. `PORT` can be any available port. `HOSTNAME` is the local address. `MAKE_ENDPOINT`, `LOGIN` and `LOGINAPI` should point to the URL of your running MakeAPI and Webmaker Login service instances.
5. Run `node app.js`, and open up `http://localhost:7777/` in your favourite web browser!

## Grunt Tasks

- `grunt` - Validate LESS, beautify and lint JS, compress images as needed. Run before you push.
- `grunt verify` - Verify LESS and JS are formatted and lint free. Read only. Used by Travis.

## Contributing

Please review our contributing guidelines [here](https://github.com/mozilla/webmaker.org/blob/master/CONTRIBUTING.md).
