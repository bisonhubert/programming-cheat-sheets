```javascript
// get element by XPath
const header = '//android.widget.text[1]'
driver.elementByXPath(header).then(element => {
  // do stuff
})
```

```javascript
// add value to text field
const email = 'bison@pillowhomes.com'
const emailField = '//android.widget.TextEdit[1]'
driver.elementByXPath(emailField).then(element => {
  element.setImmediateValue(email)
})
```
