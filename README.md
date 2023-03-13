# poke-api-testing
## What is this repository for?
Practicing api testing using Postman and Newman against Pokemon API https://pokeapi.co.

This repo contains Postman collection with three GET requests containing tests for three different pokemons: Charmander, Bulbasaur and Squirtle.

Following fields are asserted in tests: 

- Weight
- Ability/Abilities
- Name
- Type/Types

## How to run tests?

Using Postman import collection and environment and using runner execute the tests.
Using Newman: 
`npm install -g newman`
`newman run PokeApi.postman_collection.json -e PokeApi.postman_environment.json`

```javascript

PokeApi

→ Charmander Weight, Ability, Name, Type
  GET https://pokeapi.co/api/v2/pokemon/4 [200 OK, 255.55kB, 635ms]
  √  Status code is 200
  √  Charmander weight is correct
  √  Charmander name is true
  √  Charmander has two abilities
  √  Charmander abilities are correct
  √  Charmander has one type
  √  Charmander types are correct

→ Bulbasaur Weight, Ability, Name, Type
  GET https://pokeapi.co/api/v2/pokemon/1 [200 OK, 220.98kB, 43ms]
  √  Status code is 200
  √  Bulbasaur weight is correct
  √  Bulbasaur name is true
  √  Bulbasaur has two abilities
  √  Bulbasaur abilities are correct
  √  Bulbasaur has two types
  √  Bulbasaur types are correct

→ Squirtle Weight, Ability, Name, Type
  GET https://pokeapi.co/api/v2/pokemon/7/ [200 OK, 246.75kB, 49ms]
  √  Status code is 200
  √  Squirtle weight is correct
  √  Squirtle name is true
  √  Squirtle has two abilities
  √  Squirtle abilities are correct
  √  Squirtle has one type
  √  Squirtle type is correct

┌─────────────────────────┬────────────────────┬────────────────────┐
│                         │           executed │             failed │
├─────────────────────────┼────────────────────┼────────────────────┤
│              iterations │                  1 │                  0 │
├─────────────────────────┼────────────────────┼────────────────────┤
│                requests │                  3 │                  0 │
├─────────────────────────┼────────────────────┼────────────────────┤
│            test-scripts │                  3 │                  0 │
├─────────────────────────┼────────────────────┼────────────────────┤
│      prerequest-scripts │                  0 │                  0 │
├─────────────────────────┼────────────────────┼────────────────────┤
│              assertions │                 21 │                  0 │
├─────────────────────────┴────────────────────┴────────────────────┤
│ total run duration: 1133ms                                        │
├───────────────────────────────────────────────────────────────────┤
│ total data received: 719.66kB (approx)                            │
├───────────────────────────────────────────────────────────────────┤
│ average response time: 242ms [min: 43ms, max: 635ms, s.d.: 277ms] │
└───────────────────────────────────────────────────────────────────┘

```
