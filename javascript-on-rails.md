# about package managers

There are many package managers out there:
* Bower (front-end only)
* JamJS
* Ender
* Volo
* ... there Gems for ruby of course

But node comes with a built-in package manager, NPM

https://npmjs.org

    $ npm -v
    # 2.10.2

---

# how to use NPM

`npm` is pretty simple, it's similar to `gem`, except it
will install locally by default in `node_modules`. And `npm`
is much cooler than `gem`.

    $ mkdir npm-101 && cd npm-101
    $ npm install lodash # npm i === npm install

    $ ls
    # node_modules/

    $ ls node_modules
    # lodash/

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

---

# let's see about spliting our app in tiny pieces

take some time to look at the javascripts in the app
you just cloned, it is not too poorly written, but dumping
everything in one file kind of sucks.

let's see how we would go about splitting on file into many
taking advantage of modules.

also, if you take a look at the app it breaks :(
jQuery is missing! let's fix that first

---

# moving towards a more client-heavy app

ok, now it works again. let's see how the backend works so
we have an idea of what type of API are we targeting.

`songs_controller.rb` has your typical actions, `#index`,
`#show`, `#create`... they render a partial, but that is not
how we want to do it, it works but it's not very javascript-ish.

let's change it return a json we can manipulate with our
javascripts.

---

# adapting our frontend to handle the new API

demo

---

# what now?

we've redone the app for `#index`, let's move it everything else
to the frontend.

first you will have to create JSON endpoints for the rest of the
actions, it should be pretty similar to the `#index` action.

there might be some actions you don't really need anymore on the
rails side, but I'll let your figure out which ones.

> hint: if you are stuck you might want to checkout the json-api
>       branch for the rails application
