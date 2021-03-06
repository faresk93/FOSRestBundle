Upgrading From 2.7 To 2.8
=========================

 * The `ExceptionValueMap` class is marked as `final`. Extending it will not be supported as of 3.0.
   Its `resolveThrowable()` method is marked as internal and will be removed in 3.0.

 * The `isFormatTemplating()`, `renderTemplate()`, and `prepareTemplateParameters()` methods of the
   `ViewHandler` class and the `ViewHandlerInterface` have been deprecated.

 * The constructor of the `ViewHandler` class has been deprecated. Use the static `create()` factory
   method instead.

 * The `setTemplateVar()`, `setPopulateDefaultVars()`, `getTemplateVar()`, and `isPopulateDefaultVars()`
   methods of the `Controller\Annotations\View` class have been deprecated.

 * The `setEngine()`, `setTemplate()`, `setTemplateData()`, `setTemplateVar()`, `getEngine()`,
   `getTemplate()`, `getTemplateData()`, and `getTemplateVar()` methods of the `View\View` class
   have been deprecated.

 * The `fos_rest.templating` alias has been deprecated.

 * The `fos_rest.view.templating_formats` option has been deprecated.

 * Not setting the `fos_rest.service.templating` and `fos_rest.view.default_engine` options to
   `null` has been deprecated.

 * Not setting the `fos_rest.view.force_redirects` option to the empty array has been deprecated.

 * Not configuring the `fos_rest.exception.exception_controller` option is deprecated. Its default
   value will be changed to `fos_rest.exception.controller::showAction` in 3.0.

 * The `TemplatingExceptionController` and the `TwigExceptionController` classes have been deprecated.

 * The `fos_rest.exception.twig_controller` service has been deprecated.

 * Not passing a `RestControllerReader` instance as the third argument to the constructor of the
   `RestRouteLoader` class is deprecated. Support for passing a `ControllerNameParser` instance
   will be removed in 3.0.

   Set the `fos_rest.routing_loader.parse_controller_name` option to `false` to opt-out:

   ```yaml
   fos_rest:
       routing_loader:
           parse_controller_name: false
   ```

   The default value for this option is `true`. Not setting it to `false` is deprecated and will
   result in an exception in 3.0.
