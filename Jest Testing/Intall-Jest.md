Here are the steps to install Jest and the Jest local storage mock:

---

1. **Install Jest**: as a dev dependency by running the following command in your project directory:
```
npm install --save-dev jest
```

2. Create a __tests__ folder in your project root directory.
3. Inside the __tests__ folder, create a test file (e.g., mytest.test.js) that will contain your test code.
4. In your test file, import the Jest local storage mock by adding the following code at the top of the file:
```
import 'jest-localstorage-mock';
```
5. Now you can use the local storage mock in your test code. For example, you can set a value in local storage using the localStorage.setItem() method and then retrieve it using the localStorage.getItem() method:
```
test('testing local storage', () => {
  localStorage.setItem('myKey', 'myValue');
  expect(localStorage.getItem('myKey')).toBe('myValue');
});
```
