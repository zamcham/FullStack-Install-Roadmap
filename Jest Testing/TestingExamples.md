Here are four examples of testing functions with Jest, increasing in complexity:

---

1. Testing a pure function:
```JavaScript
// Simple function that adds two numbers together
function add(a, b) {
  return a + b;
}

// Test case for add function
test('add function returns correct result', () => {
  expect(add(2, 3)).toBe(5);
});
```

2. Testing a function that interacts with the DOM:
```JavaScript
// Function that sets the text of an HTML element
function setText(id, text) {
  const element = document.getElementById(id);
  element.textContent = text;
}

// Test case for setText function
test('setText function sets text of HTML element correctly', () => {
  // Set up the HTML element
  document.body.innerHTML = '<div id="test">Initial text</div>';
  
  // Call the setText function
  setText('test', 'New text');
  
  // Check that the text was updated
  expect(document.getElementById('test').textContent).toBe('New text');
});
```

3. Testing a function that makes an HTTP request:
```
// Function that retrieves data from a REST API
async function fetchData() {
  const response = await fetch('https://jsonplaceholder.typicode.com/todos/1');
  const data = await response.json();
  return data;
}

// Test case for fetchData function
test('fetchData function retrieves data from API correctly', async () => {
  const data = await fetchData();
  expect(data.userId).toBe(1);
  expect(data.id).toBe(1);
  expect(data.title).toBe('delectus aut autem');
  expect(data.completed).toBe(false);
});
```

4. Testing a function that uses callbacks and mocks:
```JavaScript
// Function that calls a callback function after a delay
function delayCallback(callback) {
  setTimeout(() => {
    callback('done');
  }, 1000);
}

// Test case for delayCallback function using Jest mocks
test('delayCallback function calls callback after 1 second', () => {
  const mockCallback = jest.fn();
  delayCallback(mockCallback);
  expect(mockCallback).not.toBeCalled();
  jest.advanceTimersByTime(1000);
  expect(mockCallback).toBeCalledWith('done');
});
```
