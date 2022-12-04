# Simple interface for Local Storage

Local Storage provides a was to store data persistently in browser. This package provides a way to organize and scope data stored in the Local Storage. Have in mind that scoping is "virtual" and that any JavaScript running on the domain will have access to all data in Local Storage. Main purpose of the package is to provide interface for easier development and more organized code.

## Getting started

Install the package: `npm i --save @banez/browser-storage`. After installation process is completed, you can use `createStorage` function to create an instance of storage interface.

```ts
const storage = createStorage({
  prfx: 'test',
});

storage.set('key', 'value');
console.log(storage.get('key')); // Output will be "value"
storage.set('key2', 'value2');
console.log(storage.getAll());  // Output will be an object:
                                // {
                                //   key: 'value',
                                //   key2: 'value2'
                                // }
storage.clear(); // Delete all data from Local Storage in scope "test"
```
