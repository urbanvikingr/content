# Function Types

There are many different contexts that you can use a Graphcool Function in.

* The [Request Pipeline](!alias-pa6guruhaf) offers different hooks along the HTTP requests of your operations. Typical use cases for functions in the request pipeline are defining **custom validations**, **sending calls to external APIs** and more. Functions as part of the Request Pipeline are executed **synchronously**.
* [Server-side subscriptions](!alias-ahlohd8ohn) (formerly called mutation callbacks) allow you to get notified of special events **asynchronously**. This can be used to build custom integrations with external services like **sending emails when a User signs up**.
* [Schema Extensions]() are used to **extend the GraphQL API** with custom queries and mutations. This can be used for **custom authentication**, **wrapping external REST APIs** and more.

More use cases for functions are planned, for example **cron jobs**. Please submit [a new feature request on  GitHub](https://github.com/graphcool/feature-requests/issues?q=is%3Aissue+is%3Aopen+label%3Aarea%2Ffunctions) if you have suggestions.
