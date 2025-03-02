# A Git repository to publish @davidthornton/hello-world

This is a list of all the steps taken to publish a package to npm.

## Steps

Following steps from this URL: https://docs.npmjs.com/creating-and-publishing-scoped-public-packages

Firstly, run:

    npm init --scope=@davidthornton

Then, create the `index.js` file, and sign in:

    npm adduser

then, after completing the browser passkey challenge, finally run:

    npm publish --access public

And it is done!

Wow, that is so cool: https://www.npmjs.com/package/@davidthornton/hello-world we are live!


## Using @davidthornton/hello-world

In a separate directory, run:

    npm i @davidthornton/hello-world

Then convert the default `package.json` file into an ES module by specifying

    {
        ...
        "type": "module"
        ...
    }

and create an `index.js` file as follows

    import helloworld from '@davidthornton/hello-world';

    helloworld.printMsg()

then run:

    node index.js

and voilà ! We get back:

    Hello, World!
