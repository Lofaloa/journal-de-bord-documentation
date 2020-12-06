---
description: This page covers some development related topic
---

# Development

## Unit testing

When working on the project using Visual Studio Code, it is really worth it to install the Jest extension. The unit tests are run in the background and error messages show up while writing the tests.

{% embed url="https://create-react-app.dev/docs/running-tests/" %}

{% embed url="https://jestjs.io/docs/en/snapshot-testing" %}

{% embed url="https://enzymejs.github.io/enzyme/" %}

### Resources

{% embed url="https://stackoverflow.com/questions/38815439/how-to-properly-unit-test-a-react-component" %}

{% embed url="https://stackoverflow.com/questions/42796835/react-application-unit-testing" %}

Node.js is required to run the application unit tests.

## Private routes

Some of the routes should be public, others should be protected \(available to authenticated users only\).

[Solution using react-router-dom](https://stackoverflow.com/questions/43164554/how-to-implement-authenticated-routes-in-react-router-4) \(the same dude has written an [article](https://ui.dev/react-router-v4-protected-routes-authentication/)\).

The was created using creact-react-app and is using the typescript template following this [tutorial](https://create-react-app.dev/docs/getting-started).

The app is hosted on Netlify.

## Dependencies

I start using enzyme so that I can find elements easily in the unit tests.

### React router

**Note:** lors du déploiement d’une SPA sur Netlify il faut activer le routage du coté client comme suit : [https://create-react-app.dev/docs/deployment/\#netlify](https://create-react-app.dev/docs/deployment/#netlify)

* [https://www.npmjs.com/package/react-circular-progressbar](https://www.npmjs.com/package/react-circular-progressbar) is used to render a custom progress bar in the home page.

