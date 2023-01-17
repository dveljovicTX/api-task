# Goldbach API task

## Start development
- ```npm i```
- ```npm run start```

## Task description

Create api endpoint that returns and filters the list of of publicly available apis and satisfies the following requirements:

* the endpoint accepts `num_elements` (number of items in response) and `start_element` parameters that are used for pagination
    * 0 < `num_elements` <= 100, defaults to 100
    * `start_element` > 0, defaults to 0
    * in case parameters are bad, return descriptive error
* user needs to be authorized in order to access the endpoint
    * use tokens generated from the `/auth/login` route
    * users of role `User` can see apis that don't have auth set
    * users of role `Admin` can see all of the apis
    * list of all available apis can be found in the `ApiContoller`
* response needs to contain the following properties:
    * `count`
    * `num_elements`
    * `start_element`
    * `items`

Approach the task as you would approach real life project, code base changes and refactors are allowed.