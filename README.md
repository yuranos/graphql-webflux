# GraphQL and Spring Webflux

This is a sample GraphQL application written in kotlin that
uses [graphQL-java](https://github.com/graphql-java/graphql-java) and spring webflux (with spring-boot 2).

When browsing the application on `localhost:8080`, you will see the [graphiQL](https://github.com/graphql/graphiql) explorer.

## Why

There is a [graphql-spring-boot-starter](https://github.com/graphql-java/graphql-spring-boot)
already available but it uses a Servlet which forces us to use spring MVC.

Creating a handler for webflux using graphql-java is fairly trivial but there is actually
a [spec to follow](https://graphql.org/learn/serving-over-http/) when serving graphql
over HTTP.

This is my implementation of the spec, it is fully tested and ready to be used in your
application.

I hope it can serve as a base implementation if graphql-java's authors wish to support
Webflux in the future.   

## Tests

Tests are written using the reactive WebClient and junit 5.

They require gradle 4.6 to work, so be sure to use the wrapper.

## Your feedback is welcome

I'm not a reactor specialist and I don't have a clear understanding of graphql-java async's internals yet.
In particular, I'm curious about [this issue](https://github.com/geowarin/graphql-webflux/issues/2).

If you have more insights, please give your opinion.

I did my best to implement the graphql spec but there might be bugs or things I overlooked.

If you find anything odd, contributing with an issue or a failing test would be wonderful. ❤️

Thanks! 
