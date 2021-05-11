# Puppeteer

TypeScript based framework to run functional tests for BBLog

### Tech
This framework uses the below tech/libraries to write our automated tests.
* [Puppeteer](https://pptr.dev/) - end-to-end test library/api a chromium based tool
* [Puppeteer with typsescript] - Typescript provides code auto completion and helpful hints with a text editor like Microsoft's Visual Studio Code or another text editor with Typescript support.
* [puppeteer cucumber]- Cucumber implementation for javascript for writing our scenarios using gherkin syntax
* [Chai](http://chaijs.com/api/bdd/) - Assertion library for verifying the results of our tests.


### Installation only once locally
Make sure you have Node and NPM installed in your machine. After cloning the project, install all dependencies by running the below via the terminal:

```cmd
 cd UI_Automation
 npm install
```
Make sure you have puppeteer installed by running the following in the terminal:

```sh
npm install -g puppeteer
```
For windows user, ensure you have java installed (https://www.java.com/en/)

Make sure you have typescript installed by running the following in the terminal:

```sh
npm install -g typescript
```

Make sure you have a few from the list installed (The top 3 are important) via Market place extentions within your VS Code:
1. Cucumber (Gherkin) Full Support
2. SQL Server (mssql)
3. npm commands for VS Code
4. GitLens -- Git Supercharged
5. Git History
6. VSCode-icons

This is relevant for binding the feature file to the step definition.

### Running tests
There are two ways you can run the tests:
1. Use the below script to run the all the specs on your local (remember you have root directory):
    This has been configured inside the package.json file as a script.
  
  Run the localSetup.bat from termial then run the below command

```sh
  npm run test(Please make sure you have the script defined for this in package.json)
``` 
  OR
  
  Look at the scripts created within package.json and run the environment of your choice or you can add the environment of you choice to the script and also update params.json with the required parameters (can be found in Configuration/params.json)
  
### Adding new tests
1. When adding new code / test, turn on the typscript complier via the terminal so it can transcribe it to javascript, if you don't do changes will not be picked up:
    `tsc -w`
2. You can add unique tags to your newly added scenario, remember to also add specify only this tag under the `param.json` file as well, for only your scenario to run on the environment defined.


### Feature file tagging
This is to enure that tests can be run in suits, feature files should be tagged as follows:

#### General Tags:
Regression Scenarios: @regression
Smoke Test Scenarios: @smoke
Regression Test on test environment: @testEnv

#### Scenario Specific Tags:
Articles: `@Articles`
Settings: `@Settings`

#### Run All Features:
Test: `@Test`




