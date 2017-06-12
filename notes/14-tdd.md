[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Test-Driven Development

1. (Re)Write a Test
2. Check if the Test fails
3. Write Production Code
4. Run all Tests
5. Clean-up Code
6. Repeat

**Test-Driven Development** involves setting goals (in the form of tests) such that writing code will eventually pass those tests.

- Tests in TDD should be _unit_ tests
- That is, they should not access code outside the module
- But in any system, by definition, modules wil need to access other modules..

## Fakes and Mocks

- Define an interface
- Implement it twice — one for the real code, and the other as "dummy" code, which "fakes" or mocks the real code in terms of output
- Fakes are dummy code that does nothing but return plausbible data
- Mocks are dummy code that does input validation
- Theory: this will result in more loosely-coupled, more cohesive code