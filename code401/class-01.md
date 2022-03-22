# Read 01 - Node Ecosystem, TDD, CI/CD

1. ***Describe (in plain English) what `Array.map()` does.*** `Array.map` creates a new array from an existing array. The new array is populated with new computed values, each based on the corresponding value in the original.
2. ***Describe (in plain English) what `Array.reduce()` does.*** `Array.reduce` calculates one single value by performing an operation on each element in an array and storing that result between repetitions.
3. ***Provide code snippets showing how to use `superagent()` to fetch data from a URL and log the result.*** Answered with the help of the [SuperAgent docs](https://visionmedia.github.io/superagent/#get-requests)
    - ***With normal Promise `.then()` syntax.***

    ```js
    superagent
      .get('citySearch')
      .query({ searchTerms : 'seattle' })
      .then(res => {
        // do stuff with the response
      })
      .catch(console.error);
    ```

    - ***Again with `async` / `await` syntax.***

    ```js
    async function mySeattleSearch () {
      try {
        response = await superagent.get('citySearch').query({ searchTerms : 'seattle' })

        // Then do stuff with the response

      } catch(err) {
        console.error(err);
      }
    }
    ```

4. ***Explain promises as though you were mentoring a Code 301 level student.*** Promises are a way of 
5. ***Are all callback functions considered to be Asynchronous? Why or Why Not?***
