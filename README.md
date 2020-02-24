# Installation for firebase function


1.Create a Firebase Project
In the firebase console, click Add project, then select or enter a Project name.If you have an existing Google Cloud Platform (GCP) project, you can select the project from the dropdown menu to add Firebase resources to that project.

(Optional) If you are creating a new project, you can edit the Project ID.

"npm install -g firebase-tools"

When you initialize Firebase SDK for Cloud Functions, you create an empty project containing dependencies and some minimal sample code, and you choose either TypeScript or JavaScript for composing functions.

To initialize your project:

1. Run firebase login to log in via the browser and authenticate the firebase tool.

2. Go to your Firebase project directory.

3. Run firebase init functions. The tool gives you an option to install dependencies with npm. It is safe to decline if you want to manage dependencies in another way.

4. The tool gives you two options for language support:

· JavaScript

· TypeScript

For this tutorial, select JavaScript.

After these commands complete successfully, your project structure looks like this:

myproject

+- .firebaserc # Hidden file that helps you quickly switch between
| # projects with `firebase use`
|
+- firebase.json # Describes properties for your project
|
+- functions/ # Directory containing all your functions code
|
+- .eslintrc.json # Optional file containing rules for JavaScript linting.
|
+- package.json # npm package file describing your Cloud Functions code
|
+- index.js # main source file for your Cloud Functions code
|
+- node_modules/ # directory where your dependencies (declared in package.json are installed)

2.Deploy and execute function

Run this command to deploy your functions:

"firebase deploy"

(or)

"firebase deploy - -only functions"

(or)

"firebase deploy --only functions:function1,functions:sample(two or more cloud function)"

