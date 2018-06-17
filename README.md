# RN-eslint-prettier-flow-jest

  ##### This is the sample React native application with following library integration
  
  * ESlint 
  * Prettier
  * Flow
  * Jest
  
  ### ESlint
  This is the link to [ESlint](https://eslint.org/docs/rules/) documentation
  
  Following are the dev dependencies need to add for ESLint to work
  
  * eslint 
  * babel-eslint 
  * eslint-config-airbnb 
  * eslint-plugin-flowtype 
  * eslint-plugin-import 
  * eslint-plugin-jsx-a11y 
  * eslint-plugin-react
  
  you can also run following command in your terminal
  
  **Step 1** 

     yarn add --dev eslint babel-eslint eslint-config-airbnb eslint-plugin-flowtype eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react
     
  **Step 2** 

   also add following code in the package.json under script tag
   
        "scripts": {
          // ...
          "lint": "eslint app"
        }
        
  ### Prettier
  
  This is the link to [Prettier](https://github.com/prettier/prettier) github repository 
  
  **Step 1** 

  Run following command in your terminal
  
        yarn add --dev prettier husky lint-staged
  
  **Step 2** 
     
  Add following code in the package.json
  
        "scripts": {
          // ...
          "pretty": "prettier --semi false --print-width 100 --single-quote --trailing-comma all --write \"app/**/*.js\"",
          "precommit": "lint-staged && yarn test"
        },
        "lint-staged": {
          "*.js": [
            "yarn pretty",
            "git add"
          ]
        }

  
   ### Flow
   
  This is the link to [Flow](https://flow.org/en/) documentation

  **Step 1** 

    yarn add --dev flow-bin@0.61.0 babel-preset-flow
  
  **Step 2** 

  Add following line of code in .bablerc file
  
    {
      "presets": ["react-native", "flow"]
    }
    
    
  **Step 3** 

  Add following code in the package.json
  
        "scripts": {
          // ...
          "flow": "flow",
          "flow-stop": "flow stop"
        }

   ### Jest
   
   This is the link to [Jest](https://facebook.github.io/jest/docs/en/getting-started.html) documentation. Also refer 

   Here are the [enzyme](https://github.com/airbnb/enzyme) dependencies for jest. Add following plugins
   
  **Step 1** 
   
    yarn add --dev enzyme enzyme-adapter-react-16 enzyme-to-json react-dom

  **Step 2** 
   
  Add following line of code under jest in package.json. Also make sure that your 'jest' folder in the root of the project
  
    "testMatch": [
        "**/?(*.)test.js?(x)"
      ],
      "snapshotSerializers": [
        "enzyme-to-json/serializer"
      ],
      "setupFiles": [
        "<rootDir>/jest/setup.js"
      ]
      
      
  **Step 4** 
  Also add following under script tag,
  
        "scripts": {
          "test:unit": "jest",
          "test": "yarn lint && yarn flow && jest"
        }
        
  **Step 5**      
  Create setup.js file under 'jest folder' and add following setup code
  
        import { configure } from 'enzyme'
        import Adapter from 'enzyme-adapter-react-16'
        configure({ adapter: new Adapter() })
        
        
# For any queries 

  Please connect me at below email, request to add **RN-eslint-prettier-flow-jest** in your email subject 

    askap.yourquery@gmail.com
