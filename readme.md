# Bespoken Voice App Testing: Unit & End-to-end test demo for multi-locale skills
Bespoken tools make it easy to unit and end-to-end test your Alexa skill. Please check this sample to know how to do the testing for a multi locale skill. 

For Unit testing we rely on our Virtual Alexa simulator, which is the element behind the execution of the Unit test scripts. 

For End-to-end testing we use Bespoken Virtual Device as a backend to process the TTS and STT going and coming back from the real Alexa AVS.

Our YAML Test Scripts are meant to make it easy for anyone to write automated tests for Alexa (and Google Assistant, soon).


## Setup

### 1. Install Bespoken Tools
Make sure you have npm installed, [get it here](https://www.npmjs.com/get-npm).

Install Bespoken CLI. Open a command-line and run this command:  

```
npm install -g bespoken-tools
```
### 2. Get your Virtual Device Token to perform End-to-end testing
First, you need to get a token. See [here for instructions](https://github.com/bespoken/virtual-device-sdk/blob/master/docs/setup.md).

### 3. Configure your test scripts:  
Create a folder named `test` under the root of your project, then, inside of `test`, create a folder named `unit` to store the Unit testing scripts and other called `e2e` for the End-to-end.

Create a `testing.json` file inside the `e2e` and `unit` folders. That will store the configuration for each type of test.

Create your test scripts for your tests. 

Please take a look at the files on this repo to help you get started. Also check this docs for further information:
- [End-to-end testing with Bespoken Tools](https://read.bespoken.io/end-to-end/getting-started)
- [Unit testing with Bespoken Tools](https://read.bespoken.io/unit-testing/getting-started)

__Note__: End-to-end configuration file contains a token to execute the scripts. We have included our token in this repo so you can run the example and see our tools in action. You should add
your own token when creating your test scripts. 

**FYI - the included token is so that new users can get started quickly. However, it is a common token and will NOT work as reliably as creating your own.** Please follow the steps above to create your own Virtual Device Token.

 
### 4. Running tests
Once you have created your tests, go to the root of your project and run a particular file by entering:
```
bst test test-directory\my-test-file.yml
```

To run a directory containing many tests, provide the directory path instead:
```
bst test test-directory
```

For example to run all unit tests:
```
bst test test\unit
```

To run all End-to-end tests:
```
bst test test\e2e
```

That's it! Now just wait, and your tests will run.


## Questions/Feedback? 
If you need assistance, reach us on any of these channels:
* [Chat with us](https://apps.bespoken.io/dashboard) (lower right-hand corner of the page)
* [Email](mailto:contact@bespoken.io)
* [Slack](http://www.alexaslack.com/)
* [Twitter](https://twitter.com/bespokenio)
* [Gitter](https://gitter.im/bespoken)  