# eslint-plugin-flowtype-errors bug

1. `yarn`

2. `yarn run eslint`

   ```
   yarn run v0.21.3
   $ eslint . 
   Done in 0.75s.
   ```

3. `yarn run flow`

```
yarn run v0.21.3
$ flow check 
index.js:6
 6: ReactDOM.render(<Hello/>, document.getElementById("app"));
                    ^^^^^^^^ React element `Hello`
 2: export default function Hello({name = "World"}: {name: string}) {
                                                    ^^^^^^^^^^^^^^ property `name`. Property not found in. See: Hello.js:2
 6: ReactDOM.render(<Hello/>, document.getElementById("app"));
                    ^^^^^^^^ props of React element `Hello`


Found 1 error
error Command failed with exit code 2.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```
