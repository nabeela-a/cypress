# Cypress

> An open source, front-end testing tool, built for the modern web.

**End to End Testing**, or UI testing is one the many approaches for testing a web application. An end to end test is supposed to check whether a web application works as expected or not, by testing the user flow. 

Cypress is a Javascript test automation framework for web applications.

### Features
>Cypress comes fully baked, batteries included. Here is a list of things it can do that no other testing framework can:
>
>-   **Time Travel:**  Cypress takes snapshots as your tests run. Hover over commands in the  [Command Log](https://docs.cypress.io/guides/core-concepts/test-runner.html#Command-Log)  to see exactly what happened at each step.
>-   **Debuggability:**  Stop guessing why your tests are failing.  [Debug directly](https://docs.cypress.io/guides/guides/debugging.html)  from familiar tools like Developer Tools. Our readable errors and stack traces make debugging lightning fast.
>-   **Automatic Waiting:**  Never add waits or sleeps to your tests. Cypress  [automatically waits](https://docs.cypress.io/guides/core-concepts/introduction-to-cypress.html#Cypress-is-Not-Like-jQuery)  for commands and assertions before moving on. No more async hell.
>-   **Spies, Stubs, and Clocks:**  Verify and  [control the behavior](https://docs.cypress.io/guides/guides/stubs-spies-and-clocks.html)  of functions, server responses, or timers. The same functionality you love from unit testing is right at your fingertips.
>-   **Network Traffic Control:**  Easily  [control, stub, and test edge cases](https://docs.cypress.io/guides/guides/network-requests.html)  without involving your server. You can stub network traffic however you like.
>-   **Consistent Results:**  Our architecture doesn’t use Selenium or WebDriver. Say hello to fast, consistent and reliable tests that are flake-free.
>-   **Screenshots and Videos:**  View screenshots taken automatically on failure, or videos of your entire test suite when run from the CLI.
>
> Reference- 

## Installing Cypress
Cypress is a desktop application and can be installed directly on your computer. 

If using `npm` to install, [Node.js 8](https://nodejs.org/en/) or above is required. (recommended)

### Installation

Install Cypress via `npm`:  
- Open your command prompt or terminal.
- Run `npm cypress install`
- This will install Cypress locally as a dev dependency for your project.

> Make sure that you have already run  [`npm init`](https://docs.npmjs.com/cli/init)  or have a  `node_modules`  folder or  `package.json`  file in the root of your project to ensure cypress is installed in the correct directory.

If you’re not using Node or `npm` in your project or you want to try Cypress out quickly, you can always [download Cypress directly from the CDN](https://download.cypress.io/desktop).

### Opening Cypress
- Go inside your project root from the command prompt or terminal.
- Run `npx cypress open` ([npx](https://www.npmjs.com/package/npx) is included with `npm > v5.2` or can be installed separately)
- The Cypress Test Runner will launch.

### Adding a Test File
1.  Create a `test.spec.js`  file.
2.  Launch the Cypress Test Runner.
3. Click on the `test.spec.js` on the Test Runner
4. Cypress opens the test in a browser (note: it'll be blanck since we haven't written any tests yet)

### First Test

Let's write our first test for the AT&T Buyflow in `test.spec.js`
```
describe('AT&T Buyflow', function() {
  it('visits the ATT App', function() {
    cy.visit('https://shopatt.centerfieldqa.com/v1/?cookiereset=1')
   })
});
```
The Test Runner should refresh itself and the test in the browser displays the AT&T Buyflow site
![First test](https://imgur.com/a/0nvbnxp)
>**What are describe and it?**
>
>All of these functions come from  [Bundled Tools](https://docs.cypress.io/guides/references/bundled-tools.html)  that Cypress bakes in.
>
>-   `describe`  and  `it`  come from  [Mocha](https://mochajs.org/)
>
>Cypress builds on these popular tools and frameworks that you  _hopefully_  already have some familiarity and knowledge of. If not, that’s okay too.
>
>Reference - [[https://docs.cypress.io/guides/getting-started/writing-your-first-test.html#Write-your-first-test](https://docs.cypress.io/guides/getting-started/writing-your-first-test.html#Write-your-first-test)]

### Cypress Resources
- [Testing The Way It Should Be (aka Intro Into Cypress)](https://www.youtube.com/watch?v=pJ349YntoIs)
- [Tutorials](https://docs.cypress.io/examples/examples/tutorials.html#Best-Practices)
- [Fixtures - `cy.fixture()`](https://docs.cypress.io/api/commands/fixture.html#Syntax)
