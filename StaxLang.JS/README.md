# Stax Javascript

## Building
In order to build the javascript bundle for stax have [Node.js](https://nodejs.org/en/) installed. Version 10.16.3 LTS +. 

Clone a copy of the repo:

    git clone git@github.com:tomtheisen/stax.git

Change directories into this directory

    cd stax/StaxLang.JS

Install the packages via npm

    npm install

Build the project

    npm run build

## Building Project without Minification (dev build)

Build the project with the following command:

    npm run build-dev

## Testing

In order to run the tests ensure that your node packages are installed (`npm install`).

Run the following command:

    npm run test

## Running

After running the build, your output will be located in the `/dist` folder.

Open `index.html` with the browser of your choice and enjoy. 