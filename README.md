# Basic Backend Interview Question

### INTERVIEWER NOTES
- Confirm that correct status codes were returned

### Task

Build a backend API server in TypeScript that managers a registry of books. 

### Requirements
- Use the framework or method you are most familiar with. <a href="https://www.npmjs.com/package/express">Express.js</a> is set up here for convenience.
- Implement `GET`, `POST`, `PUT`, and `DELETE` methods for invidual books.
- Use the following interface:
```
interface Book {
  id: string;
  title: string;
  author: string;
  year: number;
}
```
- Use an array to track books. We won't worry about databases for this question.
```
const books: Book[] = [];
```
- Handle improper requests, requests for missing books, etc.
- Add general error handling via middleware or other methods.

### Bonus
- For `POST` and `PUT` requests, make a request to <a href="https://openlibrary.org/dev/docs/api/search">OpenLibrary</a> to validate if the book exists in the real world.

### Additional Questions
- How might you handle rate limiting?
- How might you authenticate users?
- What database might you use? How would you interact with that database from TypeScript?

### Bonus 2
- Write a background worker that periodically validates if each book current in the array exists in the real world. Delete the book if it doesn't.
