## Configure IIS route rules

In [App_Start/RouteConfig.cs](https://github.com/itworld1st/Ng5Demo/blob/master/Ng5Demo/App_Start/RouteConfig.cs) file, change url as follows:

```c#
routes.MapRoute(
                name: "Default",
                url: "{*.}",
                defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
            );
```

For using the Angular Router, In [Views/Shared/_Layout.cshtml](https://github.com/itworld1st/Ng5Demo/blob/master/Ng5Demo/Views/Shared/_Layout.cshtml) file, add a `<base>` element as the first child in the `<head>` tag.

```html
<head>
    <base href="/">
</head>
```
