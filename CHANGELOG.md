CHANGELOG
=========

4.0
---

 * allowed using multiple @Security annotations (class and method)
 * removed support for the Templating component (only plain Twig is supported)
 * removed unneeded phpdocs, converted protected to private properties
 * bumped Symfony minimum version to 3.0
 * bumped PHP minimum version to 5.5.9
 * removed class parameters in container definitions

3.0
---

 * fixed the Doctrine param converter that sent 500 when an entity was not found under some circumstances
 * ParamConverterInterface now uses ParamConverter as a type hint instead of ConfigurationInterface
 * added support for @Security
 * added support for HTTP validation cache in @Cache (ETag and LastModified)

2.2
---

 * added the possibility to configure the repository method to use for the
   Doctrine converter via the repository_method option.
 * [BC break] When defining multiple @Cache, @Method or @Template annotations on
   a controller class or method, the latter now overrules the former

2.1
---

 * added the possibility to configure the id name for the Doctrine converter via the id option
 * [BC break] The ParamConverterInterface::apply() method now must return a
   Boolean value indicating if a conversion was done.
