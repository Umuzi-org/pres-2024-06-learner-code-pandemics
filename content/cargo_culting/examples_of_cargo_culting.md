## Examples of cargo culting

Assignee submits the following code for review:
```javascript
function simpleFetchData() {
    return fetch('https://api.example.com/data');
}
simpleFetchData().then(response => response.json()).then(data => console.log(data));
```
Reviewer asks the learner to use async/await without any valid reason:
```javascript
async function fetchData() {
    return await fetch('https://api.example.com/data');
}
fetchData().then(response => response.json()).then(data => console.log(data));
```