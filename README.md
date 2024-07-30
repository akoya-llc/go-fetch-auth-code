# Getting an auth code (TESTING)

This golang code sample demonstrates how to programmatically fetch an auth code using the sandbox app credentials obtained from recipient hub. It uses the gin web framework and templates to render a rudimentary HTML page with a button to start the consent flow process.

## key concepts
* Making a GET request for an auth code from the identity provider
* Redirecting to an example test bank "Mikomo" to simulate "consent flow" permissioning of account access
* Redirecting to recipient hub's auth code viewer page to receive the auth code after consenting to access

## overview of project
The main.go module includes a single route "/" which drops the user on a basic HTML page rendered from the content in ./templates/index.tmml. The page includes an anchor link that points to a sandbox identity provider URL. The value of your ClientId variable is used in this URL, so be sure it is properly set to your client id.

The go.mod file includes the application's golang dependencies, and the run.sh file is a shell script that consolidates the dependency fetching and application compilation, and binary execution into a single step for convenience.


## running the sample
### from localhost
1. Initialize the ClientId and Secret variables in main.go with the client id and secret of your sandbox app
2. Open a terminal in the sandbox
3. Run the command "chmod +x run.sh"
4. Run the command "./run.sh"
5. The application will be available at http://localhost:8123
6. Follow the instructions in the browser once the application is opened.

### from code sandbox
1. Open the project in code sandbox
2. Click the "sign in" button with code sandbox
3. Choose "sign in" with github
4. Authenticate using your github credentials and grant codesandbox access to your repos
5. After signing in, click the dropdown next to the "sign in" button in codesandbox and choose "Fork project"
6. When prompted, search for this repository to fork from: https://github.com/fabrizio-akoya/go-fetch-auth-code
7. Click the "fork" button to fork the project
8. The application will start to run in codesandbox, after which you'll be prompted to open preview via a "Preview: 8123" button
9. Click the "Preview: 8123" button to open the application in the browser
10. In the tool bar next to the preview URL bar, note the icons: Hover over the icons and look for the tooltip text "Open in a new tab" and click that
11. The application will start running in a new browser window where you can interact with it
