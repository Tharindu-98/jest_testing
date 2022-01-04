
## My First Testing With Jest + eslint-plugin-jest

**eslint setup**

 1. `npm install eslint --save-dev`
 2. .`/node_modules/.bin/eslint --init`
			 - To check syntax + find problems  | ~~style guide~~
			 - json or js
			  
 3. `npm install eslint-plugin-jest --save-dev`
 4. add "jest" support for `.eslintrc` configuration file.
		 i. For all files.
		 ii. Only for *.test.js files / overrides.   (this repo used this method)
		 
	[Overrides way-stackoverflow](https://stackoverflow.com/a/69755865/13237885)
	[npm eslint-plugin-jest](https://www.npmjs.com/package/eslint-plugin-jest)

**Jest setup**

 5. `npm install jest --save-dev`
 6. Inside package.json
		 

        "scripts": {
	        "test": "jest"
	     }
	    
7. create a `sum.js`  file.
 
 	   function sum(a, b) {
	      return a + b;
	    }
	    module.exports = sum;
8. Then, create a file named `sum.test.js`
	

	    const sum = require('./sum');
	    
	    test('adds 1 + 2 to equal 3', () => {
	      expect(sum(1, 2)).toBe(3);
	    });
9. `npm run test`

   [https://jestjs.io/docs/getting-started](https://jestjs.io/docs/getting-started)


*Extra :- You can use [Jest runner extension](https://marketplace.visualstudio.com/items?itemName=Orta.vscode-jest&ssr=false#review-details)*

