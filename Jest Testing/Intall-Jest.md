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
