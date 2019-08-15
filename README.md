# useful-dev-tools

## e2e tests

```sh
Run all tests: $ protractor protractor.conf.js
```
```sh
Run single test: $ protractor protractor.conf.js --specs='e2e/src/features/test-name.feature'
```
```sh
Update webdriver: $ webdriver-manager update --versions.chrome=$(google-chrome --version | cut -d ' ' -f 3)
```
