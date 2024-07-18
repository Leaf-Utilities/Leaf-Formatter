# Leaf Formatter

The base formatting system in Leaf Essentials. Does not include any variables/functions by default, you need to code them yourself :3

Example usage:
```js
let formatter = new LeafFormatter();
formatter.addVariable("example", (sessionData)=>{
  return sessionData.customText ?? "Example variable!"
})
formatter.addVariable("example", (data)=>{
  return data.text ?? "Example text!"
})

// To format
formatter.format(`<example>`, {}) // => Example variable!

// Or use session data
formatter.format(`<example>`, { customText: "Hello, world!" }) // => Hello, world!

// Use functions
formatter.format(`Example 1: =example()`) // => Example text!
formatter.format(`Example 2: =example(text="hi :3")`) // => hi :3
```
