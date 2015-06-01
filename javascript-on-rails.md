# about package managers

There are many package managers out there:
* Bower (front-end only)
* JamJS
* Ender
* Volo
* ... there Gems for ruby of course

But node comes with a built-in package manager, NPM

https://npmjs.org

`npm -v` should output something greater than (or equal) to 2

---

# how to use NPM

`npm` is pretty simple, it's similar to `gem`, except it
will install locally by default in `node_modules`

```bash
mkdir npm-101 && cd npm-101
npm install lodash # npm i === npm install
ls # node_modules/
ls node_modules # lodash/
```

---

# how to use NPM with Rails then?

the `browserify-rails` gem does the magic for us, so just
add it to your Gemfile and run `bundle`

next run `npm init` in the root of our rails app, accept
the default configuration, ENTER ENTER ENTER ENTER ENTER

open the newly created `package.json` file and let's go
through it, you may configure it later

---

# using browserify

now let's get rid of rails's jQuery and install it via
npm by doing `npm i jquery --save`

now take another look at your `package.json`, what changed?

next go to your `application.js` file and remove the two
lines containing jquery and then we're ready to start coding
with NPM modules.
