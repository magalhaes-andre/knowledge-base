# AEM Best Practices

## Resource Mapping

Technique used to define redirects, vanity URLs and virtual hosts for AEM. You are able to use resource mapping to prefix all requests with "/content", this way you prevent the users to understand your code structure by breaking down your url paths.

You are also able to redirect all of the requests that are directed to your gateway page into another site, if needed.

## AEM Design Patterns

Because AEM is coded following OSGi, many of the design patterns intended for OSGi are valid. If to list some of them:

- Singleton (Service)
- Adapter Service
- Resource Adapter Service
- Whiteboeard

Also, because of AEM's modularity, you should be able to use any design pattern in your app.

## Multi-Site Manager

The MSM enables you to manage multiple web sites that share common content with ease. You can define relations between them so that content changes in one site are replicated automatically in other sites.

For example, web sites are provided in multiple languages if you aim for international audiences. When the number of sites in the same language is low (3-5) a manual process of synchronization is possible. But with growth and an international audience, the need for an automatized process is essential.

## Debug Mode

To start AEM in debug mode you need the following addition to your command line on starting AEM instance:

``` nofork -agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=10123 ```