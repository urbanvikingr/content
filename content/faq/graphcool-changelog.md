---
alias: chiooo0ahn
path: /docs/faq/graphcool-changelog
layout: FAQ
title: Changelog
description: Keep track of the latest features and improvements to the Graphcool platform.
tags:
  - platform
related:
  further:
  more:
    - ul6ue9gait
    - oobai3shoh
---

# Changelog

## Week 30/31 (July 24 - August 8)

* [API](!alias-heshoov3ai)

  * Setting required fields with a default value to `null` in a create or update mutation does not result in an internal server error anymore. Instead, the default value is used.

* [Schema Extensions](!alias-xohbu7uf2e)

  Thanks to all the beta tester for [the great feedback](https://www.graph.cool/forum/t/feedback-schema-extensions-beta/405/3?u=nilan) for Schema Extensions! These issues could be fixed:

  * Scalar lists can now be returned from a schema extension function.
  * Badly shaped return values are now handled gracefully and a helpful error message is returned.
  * URL validation for [webhook functions](!alias-hohl0iy1ji) is improved and helpful errors messages are returned.

* [Subscriptions](!alias-aip7oojeiv)

  You can now also use the connection parameter `authorization` (lower case) in your subscription client to authenticate subscription requests.

* Resources and Community Contributions

  * We released [Chromeless](https://github.com/graphcool/chromeless/), a tool for Chrome automation, on GitHub and were featured on [Product Hunt](https://www.producthunt.com/posts/chromeless) and the [Hacker News Frontpage](https://news.ycombinator.com/item?id=14859084) 🎉 Thanks a lot for the great reception and feedback!
  * Two chapters were added to How to GraphQL: [Subscriptions with Relay](https://www.howtographql.com/react-relay/7-subscriptions/) and [Pagination with Relay](https://www.howtographql.com/react-relay/8-pagination/).
  * Thanks a lot to [@picosam](https://github.com/picosam), [@kbrandwijk](https://github.com/kbrandwijk), [@heymartinadams](https://github.com/heymartinadams), [@mwickett](https://github.com/mwickett), [@aurnik](https://github.com/aurnik) for contributing examples for
    * [Stripe Connect](https://github.com/graphcool-examples/functions/pull/36)
    * [Stripe one time charge](https://github.com/graphcool-examples/functions/pull/44)
    * [address lookup for Dutch addresses](https://github.com/graphcool-examples/functions/pull/37)
    * [reset password workflow](https://github.com/graphcool-examples/functions/pull/41)
    * [AccountKit](https://github.com/graphcool-examples/functions/pull/45)
    * [Open Weather Map API wrapper](https://github.com/graphcool-examples/functions/pull/51)
    * [Everypixel file proxy](https://github.com/graphcool-examples/functions/pull/53)

## Week 29 (July 17 - July 23)

* [Subscriptions](!alias-aip7oojeiv)

  We identified and fixed a bug causing intermittent connection problems with Subscription WebSockets. 🎉

* Resources and Community Contributions

  A bunch of amazing contributions by this week's **Graphcool Heroes** 💪

  * A GraphQL version for the popular admin-on-rest to by the [marmelab team](https://github.com/marmelab) to build an admin interface has finally been released. Check it out: [aor-graphql-client](https://github.com/marmelab/aor-graphql).
  * [@georgelovegrove](https://github.com/georgelovegrove/) prepared an [Authentication Boilerplate Example](https://www.graph.cool/forum/t/latest-react-native-react-and-expo-packages-used-with-graphcool-auth0-and-react-navigation/372/1) with Expo, react-navigation, Auth0 and Graphcool.
  * More examples to the [Graphcool Functions Collection](https://github.com/graphcool-examples/functions) have been added!
    * A [Tic Tac Toe Server Example](https://github.com/graphcool-examples/functions/pull/23) that covers many different components like [Permissions](!alias-iegoo0heez), [Server-Side Subscriptions](!alias-ahlohd8ohn) and [Request Pipeline Functions](!alias-pa6guruhaf) by [@kbrandwijk](https://github.com/kbrandwijk). Have fun playing! 🕹
    * Another great contribution for the schema extension beta! [@katopz](https://github.com/katopz) has put together [an authentication example using Github](https://github.com/graphcool-examples/functions/pull/25).
    * The existing SendGrid example has received an upgrade by [@heymartinadams](https://github.com/heymartinadams) and [@kbrandwijk](https://github.com/kbrandwijk) to cover [adding contacts to a SendGrid email list](https://github.com/graphcool-examples/functions/pull/26).
  * [@export-mike](https://github.com/export-mike) shared a [delete script](https://github.com/graphcool-examples/scripts/pull/1) to delete all nodes of a certain type.

## Week 28 (July 10 - July 16)

* [CLI](!alias-kie1quohli)

  The **Graphcool CLI version 1.2.0** is now released with improvements to regions, better error messages and the status command. See the [full release notes](https://github.com/graphcool/graphcool-cli/releases/tag/v1.2.0).

* [Migrations](!alias-paesahku9t)

  **Schema migrations have been improved** around adding optional and required [relations](!alias-goh5uthoc1), using the [migrationValue](!alias-aeph6oyeez#migrating-the-value-of-a-scalar-field) directive and renaming relations. In general, **schema migrations handle bad input more robust and user friendly** than before.

* [API](!alias-heshoov3ai)

  **Invalid JSON data is now handled gracefully** for queries and mutations. See the fix for JSON data in RP functions below, too.

* [Functions](!alias-boo6uteemo)

  **Event data parsing and validation for [functions in  the Request Pipeline](!alias-pa6guruhaf) has been improved**. [JSON fields](!alias-teizeit5se#json) are now correctly validated and passing empty lists is working as expected.

* Resources and Community Contributions

  * The Fullstack GraphQL Tutorial [How to GraphQL](https://www.howtographql.com) has been [launched](https://www.graph.cool/blog/2017-07-11-howtographql-xaixed1aa9/) with big success 🎉 Thanks to all the initial contributors, but also all the great contributions from the community on GitHub!
  * The closed beta for **Schema Extensions** is quickly progressing thanks to the help of the community 🏇. Many new examples are now available, with more to come soon:
    * [@petrvlcek](https://github.com/petrvlcek) contributed an [amazing example for authentication with Auth0](https://github.com/graphcool-examples/functions/pull/18) and `RS256` tokens. It comes in a AWS Lambda and Auth0 Webtask variant.
    * Another wonderful example for [Email/Password authentication](https://github.com/graphcool-examples/functions/pull/19) has been contributed by [@stevewpatterson](https://github.com/stevewpatterson). It includes flows for **signup, login, updating email and password**.
    * We added an example for [authentication using Google](https://github.com/graphcool-examples/functions/pull/17).

    Reach out in Slack if you're interested to participate in the beta program.

  * Thanks to [@mwickett](https://github.com/mwickett) for improving the [generate slug example](https://github.com/graphcool-examples/functions/pull/20) with a better approach for slug generation.

## Week 27 (July 3 - July 9)

* [Console](!alias-uh8shohxie)
  * Fixed a problem with updating [Server-Side Subscription functions](!alias-ahlohd8ohn).
* [Migrations](!alias-paesahku9t)
  * Fixed removing two related types at once.
  * Fixed a problem that allowed the addition of a required relation to types that already contain data.
  * The [`@isUnique` directive](!alias-aeph6oyeez) is now correctly applied and enums are supported when initializing a new project with the [Graphcool CLI](!alias-kie1quohli).
* [Functions](!alias-boo6uteemo)
  * Fixed passing `DateTime` values in Request Pipeline functions.
* [Schema](!alias-ahwoh2fohj)
  * Fixed regression with size limit of `String` fields.
* [Auth](!alias-wejileech9)
  * The closed beta for custom authentication is being kicked off with [an example for authentication with Facebook Login](https://github.com/graphcool-examples/functions/pull/16).
* Resources and Community Contributions
  * A big shoutout to this week's Graphcool Heroes for their awesome contributions 🎉
    * [@dkh215](https://github.com/dkh215) added an example to fetch and store repository information with the [Github API using Graphcool Function](https://github.com/graphcool-examples/functions/pull/15) ⚡️
    * In his new article, [@j4amesjung](https://medium.com/@j4mesjung) explains how [Optimistic UI works with Apollo and Graphcool](https://medium.com/@j4mesjung/apollo-graphcool-optimistic-ui-for-delete-mutations-abc23f8aab18).
  * [GraphQL Talks](https://graph.cool/blog/2017-07-06-graphql-talks-eevevoo1ae/) was launched together with the release of the first badge videos from [GraphQL-Europe 2017](https://www.youtube.com/playlist?list=PLn2e1F9Rfr6n_WFm9fPE-_wYPrYvSTySt).
  * Thanks to [@wesbos](https://twitter.com/wesbos) and [@stolinski](https://twitter.com/stolinski) for the shoutout on their new [Syntax. podcast](https://syntax.fm/show/001/react-tools).


## Week 26 (June 26 - July 2)

* [API](!alias-heshoov3ai)
  * The pagination information for connections in [the Relay API](!alias-aizoong9ah) has been fixed.
  * When the input argument of a [nested mutation](!alias-yoo8vaifoa) is null or otherwise invalid, an error message is now returned and the outer mutation is cancelled.
* [Migrations](!alias-paesahku9t)
  * The behaviour when [changing the type of a scalar field](!alias-ahv6rohnge#changing-the-type-of-an-existing-field) has been unified.
  * Fixed a problem when migrating a String field to an enum.
  * Fixed several edge cases with migration and default values for enums.
* Resources and Community Contributions
  * A [new episode of GraphQL Radio is available](https://www.youtube.com/watch?v=Gxag5PXGXN8), this time with Jordan Husney and Matthew Krick from Parabol. Discussed topics include adopting GraphQL, GraphQL Subscriptions and RethinkDB for real time support.
  * Another week, another batch of Graphcool heroes! 💪
    * Several [plugins to the File API using Graphcool Functions](https://github.com/graphcool-examples/functions/pull/11) have been collected and provided by community member [@kbrandwijk](https://github.com/kbrandwijk), and reviewed by [@yusinto](https://github.com/yusinto). Thanks for your fantastic contributions! 💯
    * [@derBingle](https://github.com/derBingle/) shared his cool [Graphcool Electron App](https://www.graph.cool/forum/t/nativefied-graphcool-console/277/1).
    * [@notrab](https://github.com/notrab) is putting out a lot of useful GraphQL resources lately in his [YouTube channel](https://www.youtube.com/channel/UCcSj41xzQJCT2V0GNwlob_w)! He also recently [reviewed Graphcool](https://www.youtube.com/watch?v=5S4xaUVc9Dg), thanks for the valuable feedback! 🙋

## Week 25 (June 19 - June 25)

* Graphcool [now runs in multiple regions](!alias-she7yaab6l) and performance improvements reduced response times by 80ms on average! 🏇
* We fixed a problem with [the File API](!alias-eer4wiang0) when renaming files.
* We added a [description of all available filter options](!alias-aephaimu5n#explore-available-filter-criteria) to the GraphQL schema of the GraphQL APIs.

## Week 24 (June 12 - June 18)

* The [Subscription API](!alias-aip7oojeiv) has been upgraded to the protocol specified in [the latest version `0.7` of `subscription-transport-ws`](https://github.com/apollographql/subscriptions-transport-ws/releases). Thanks to the Apollo team for the great work! 💪
* The [Image API](!alias-atiede8ata) is now production ready. 🤳
* The [Graphcool CLI](https://github.com/graphcool/graphcool-cli/) shows more information for invalid commands and received multiple bug fixes. [Full Release Notes](https://github.com/graphcool/graphcool-cli/releases/tag/v1.1.0). Additionally, the CLI now provides a browserless sign in. You can obtain the necessary token in your [project settings](!alias-aechi6iequ).
* A lot of useful resources have been added this week by our great community! 🎉
  * The [functions repository](https://github.com/graphcool-examples/functions) now contains example Graphcool Functions for sending an email with SendGrid, image transformations with Cloudinary, using the Google Geocode API to address information and a small Stripe integration that is setup with Webpack and Babel to allow ES6 and async/await capabilities. Special thanks to the contributing members of the community [@heymartinadams](https://github.com/heymartinadams), [@kuldarkalvik](https://github.com/kuldarkalvik) and [@yusinto](https://github.com/yusinto). ⚡️
  * In this week's [Graphcool Webinar](https://www.youtube.com/watch?v=MT2czo5U7x4), Hackages present an app that they are preparing for a workshop.
  * The [latest tutorial on Relay Modern](!alias-ujaesaen0s) gives insights into the @connection directive that's now needed when querying lists with Relay.

## Week 23 (June 5 - June 11)

- The [data export](!alias-aechi6iequ) feature now supports UTF8 encoding
- Fixed a problem with Algolia Index queries that were not containing the node `id`
- Based on the community feedback [Graphcool Functions](!alias-boo6uteemo) could be improved in many aspects:
  - Functions now support scalar lists, DateTime and Json fields
  - Functions now work correctly when triggered by a nested mutation
  - `PRE_WRITE` functions in the [request pipeline](!alias-pa6guruhaf) now receive the transformed output if a `TRANSFORM_ARGUMENT` function exists
- The `Select User` feature in the [Graphcool Playground](!alias-oe1ier4iej) now works with [GraphQL Subscriptions](!alias-aip7oojeiv) as expected.
- The [Getting Started with Relay](!alias-woodito7ug) tutorial and video guide have been released!
- The project settings, Algolia integration, different popups and more in the [Graphcool Console](https://console.graph.cool) received a lot of UI and UX improvements for Chrome, Safari and Firefox.

## Week 22 (May 29 - June 4)

- We released new guides for [functions along the request pipeline](!alias-zeez7aiph3) and [server-side subscriptions](!alias-dee0aethoo).
- With [graphql-request](https://github.com/graphcool/graphql-request) we published a minimal GraphQL client supporting Node and browsers for scripts or simple apps.
- We restructured our [examples repository](https://github.com/graphcool-examples) to help you find exactly the example that you need and also updated the onboarding accordingly.
- For better support of Relay Modern, we added more choices to the schema export feature. You can now export the full schema needed for Relay Modern and other tools right in your Console!

## Week 21 (May 22 - May 28)

- Our homepage received layout fixes, a new [community section in the docs](https://graph.cool/docs) and a faster signup flow
- In the Console, we released a brandnew onboarding that is even more interactive than before, introduced a mobile landing page, improved the UI for entering values in the field popup and introduced a new fullscreen mode for testing functions
- Queries that involve Permission queries now have up to 10x better performance
- The [fifth chapter of the Freecom tutorial series](!alias-wohfoa8ahz) is finally here and showcases how you can employ business logic with serverless functions.

## Week 20 (May 15 - May 21)

- We **launched officially** and were featured on [Product Hunt](https://www.producthunt.com/posts/graphcool-2) and reached first spot on the [Hacker News](https://news.ycombinator.com/item?id=14350129) frontpage 🎉 We published an article [about the Serverless GraphQL Backend Architecture](!alias-ahde7paig2/) and rolled out the [CLI and Functions](!alias-teko4ab8za).
- As part of the launch, the homepage and documentation received a lot of love and should feel way smoother now.
- We fixed issues with the [Algolia Integration](!alias-emaig4uiki) regarding nested nodes, made a lot of smaller improvements to the UX of the Console and fixed a bug that would apply too restrictive permissions for some mutations.
- On May 21th, we're hosting [GraphQL Europe](https://graphql-europe.org), the first GraphQL conference in Europe.

## Week 19 (May 8 - May 14)

- We incorporated the feedback we received regarding the UX of the Anonymous Authentication in the Console.
- The new [CLI](!alias-kie1quohli) and the [Functions](!alias-boo6uteemo) feature are being tested in a closed beta program.

## Week 18 (May 1 - May 7)

- Enums are now managed on a project-level instead a type-level. This means you can define the possible values for one enum and create fields that use this enum in different types now.
- We added a new authentication provider that allows authentication based on a unique secret: **Anonymous Authentication**. Check [the latest Freecom chapter](!alias-pei9aid6ei) to learn how to use it!

## Week 17 (April 24 - April 30)

- We [released permission queries](![alias](https://www.graph.cool/blog/2017-04-25-graphql-permission-queries)-oolooch8oh/)! This is a novel approach for customizable authorization rules and we're very excited about the launch. Thanks to the **over 100 developers** in our beta program for throroughly testing this feature!
- We improved working with scalar lists in the databrowser.
- To make debugging subscriptions in the Playground easier, API errors are now directly printed.

## Week 16 (April 17 - April 23)

- [GraphQL Radio](https://graphqlradio.com) has been launched in cooperation with [Abhi Aiyer](https://twitter.com/AbhiAiyer).
- Many bugs have been fixed:
  - A subtle bug that prevented the deletion of nodes in self-relations with only a single field
  - Input data when creating or updating JSON fields is now properly validated and a GraphQL error is returned for invalid JSON.
  - The initial synchronization for the Algolia integration could be improved when using `DateTime` or `Json` fields.
- Improvements to relation filters, the File API and String fields:
  - It's now possible to filter nodes that are related to `null` in a to-one relation.
  - The size limit of uploading files to the [File API](!alias-eer4wiang0) has been increased to 200MB to support even big video files. File names now also support UTF-8 encoded characters.
  - [String fields](!alias-teizeit5se) can now hold up to 256 KB data, compared to 64KB before.

## Week 15 (April 10 - April 16)

- [Part 2 of the Freecom tutorial](!alias-oe8ahyo2ei) takes a deep dive into running GraphQL mutations and queries with Apollo Client.
- We improved the UI and workflow of connecting nodes in a relation using the Data Browser. This should feel much smoother now.

## Week 14 (April 3 - April 9)

- With the release of [Freecom](https://www.graph.cool/freecom/), we are kicking off a big full-stack tutorial series to build your own customer chat.
- Performance and usability for the [Subscriptions API](!alias-aip7oojeiv) has been dramatically increased based on the feedback we received from the community.
- Using default values and migrations for Enum and JSON fields have been improved.
- General improvements to migrations when changing a field in the Console.

## Week 13 (March 27 - April 2)

- You can now upload files using the Data Browser as per feature request [#66](https://github.com/graphcool/feature-requests/issues/66). Simply drag and drop a file into your console to upload it and create the corresponding file node.
- The [Homepage](https://graph.cool) including the [Documentation](https://graph.cool/docs) is now way more performant because we added code splitting and improved the Webpack configuration in general.
- The video about [building a booking system with GraphQl](https://www.youtube.com/watch?v=O8vwXEbnbFk) is the first episode of the Graphcool Webinar series.

## Week 12 (March 20 - March 26)

- For some people in the *Permissions Popup* it was not clear what we mean by "Apply to whole Model". A tooltip now explains what it's about. (closes [#536](https://github.com/graphcool/console/issues/536))
- Even when you didn't have changes, the databrowser asked if you really want to leave. This is fixed and now only real changes trigger this popup. (closes [#509](https://github.com/graphcool/console/issues/509))
- Fixed the links in the Onboarding for Learn Apollo & Learn Relay (closes [#756](https://github.com/graphcool/console/issues/756))
- The playground had the problem, that the docs didn't fully expand. Many of you have reported this, which we're really thankful for. It's now fixed and even on a small screen you can expand the docs much wider. (closes [#758](https://github.com/graphcool/console/issues/758), [#695](https://github.com/graphcool/console/issues/695))

## Week 11 (March 13 - March 19)

- We introduce [graphql-up](https://www.graph.cool/graphql-up/) that generates a ready-to-use GraphQL API based on a schema file in [SDL (schema definition language) syntax](!alias-kr84dktnp0).
- Launch of the new Schema View. You now have a better overview over your schema through [Schema Editor](!alias-zezoo7uaph) and an awesome tool called [GraphQL Voyager](https://github.com/APIs-guru/graphql-voyager/), which we've now included in the Graphcool Console for you.

## Week 10 (March 6 - March 12)

- In this week there was a lot of progress regarding the Schema View, which will be released next week.
- The Console now uses [Service Workers](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers) which cache all assets so the whole Console loads faster.
- Minor Bugs like the behavior of the String Cell in the Databrowser have been fixed. (closes
[#703](https://github.com/graphcool/console/issues/703),
[#715](https://github.com/graphcool/console/issues/715),
[#734](https://github.com/graphcool/console/issues/734),
[#741](https://github.com/graphcool/console/issues/741),
[#744](https://github.com/graphcool/console/issues/744))

## Week 9 (February 27 - March 5)

- Launch of our new subscriptions. Not only have we iterated over the subscription API to make it as powerful and easy to use as possible, but also created a unique debugging experience for your GraphQL Subscriptions in the new playground. Give it a try!
