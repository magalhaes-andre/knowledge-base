# OSGi

## Basic SCR Annotations

@Component -> Class of a component
@Service -> Service interface provided by the component
@Reference -> Dependency injection of a service into the component
@Property -> Defines a property that can be used in the class

## Resource Resolving

By using ResourceResolver class that provides the getResourceResolver method and then resolve().

## Resource Adapting

By using adaptTo() method, which accepts class type you want to adapt, ex: 

```Page page = resource.adaptTo(Page.class);```

## OSGi Bundle vs Normal Jar File

- OSGi bundles are jar files with metadata inside. This metadata when read by an OSGi runtime container, is what powers the bundle.

- With OSGi, a class being public does not mean you can access it. All bundles include an export list of package names, and if a package is not in the list it does not exist to the outer world. This allows developers to build an extensive hierarchy in the internal classes and minimize the surface of the bundle's API without abuse of private modifier. One common practice include putting interfaces in one package and implementations in another while only exporting the interface.

- All OSGi bundles have a version number, therefore an application can access simultaneously different versions of the same bundle. Since each bundle has a proprietary classloader, both bundle classes can coexist in the same JVM.

- OSGi bundles include their dependncies.

- OSGi bundles have an Activator.java class which is an optional listener to be notified of bundle start and stop events.