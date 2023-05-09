## spacetraders-api@2.0.0

A [SpaceTraders](https://spacetraders.io/) SDK utilising [axios](https://github.com/axios/axios), auto-generated using the [OpenAPI definition](https://docs.spacetraders.io/api-guide/open-api-spec). The generated Node module can be used in the following environments:

Environment
* Node.js
* Webpack
* Browserify

Language level
* ES5 - you must have a Promises/A+ library installed
* ES6

Module system
* CommonJS
* ES6 module system

It can be used in both TypeScript and JavaScript. In TypeScript, the definition should be automatically resolved via `package.json`. ([Reference](http://www.typescriptlang.org/docs/handbook/typings-for-npm-packages.html))

### Installation

Navigate to the folder of your consuming project and run the following command:

```
npm install spacetraders-api axios@0.27.2 --save
```

### Usage

Here's an example using the SDK:
```ts
import axios from 'axios';
import {
  Configuration,
  SystemsApi
} from 'spacetraders-api';

const configuration = new Configuration({
  basePath: process.env.BASE_PATH,
  accessToken: process.env.ACCESS_TOKEN,
});

const instance = axios.create({});

const system = new SystemsApi(configuration, undefined, instance);

const systems = await system.getSystems();
console.log(systems.data);
```

### Building

To build and compile the typescript sources to javascript use:
```
npm install
npm run build
```
