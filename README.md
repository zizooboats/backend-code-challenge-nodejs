# Zizoo GraphQL Code Challenge

## Goal

Create a simple GraphQL API satisfying the given requirements.


## Tasks

- Create the following queries:
  - getBoats(input: GetBoatsInput): [Boat!]!
  - getBoat(boatId: String!): Boat

- Create the following mutations:
  - updateBoat(boatId: String!, input: UpdateBoatInput!): Boat
  - deleteBoat(boatId: String!): Boat

## Schema
```
type Boat {
  id: ID!
  name: String
  type: BoatTypeEnum
  year: Int
  marina: String
  skipper: SkipperTypeEnum
  active: Boolean
  cabins: Int
  length: Int
  price: Float
}

enum BoatTypeEnum {
  CATAMARAN
  GULET
  MOTOR_BOAT
  MOTOR_CATAMARAN
  RIB
  SAILBOAT
  SPEEDBOAT
}

enum SkipperTypeEnum {
  OPTIONAL
  MANDATORY
  BAREBOAT
}

input GetBoatsInput {
  active: Boolean
}

input UpdateBoatInput {
  name: String
  type: BoatTypeEnum
  year: Int
  marina: String
  skipper: SkipperTypeEnum
  active: Boolean
  cabins: Int
  length: Int
  price: Float
}
```
> You can extend the schema if needed

## Bonus (no required but a plus)

- Dockerize the API

## Test submission process and evaluation

- Please provide a link to a GitHub or other public repository containing the solution’s source code
- Ensure the repository has a valid README.md containing precise instructions on how to build and run the API (GraphQL Playground)
- The solution will be evaluated for completeness and the coding style

## Estimated solution Time

2-5 hours