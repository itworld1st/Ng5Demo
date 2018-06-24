## Update for Angular 6

>***Angular 6** now depends on **TypeScript 2.7**, **RxJS 6.0.0** or **higher**.*

Changes [systemjs.config.js](https://github.com/itworld1st/Ng5Demo/blob/master/Ng5Demo/systemjs.config.js) file by adding code as follows:

```javascript
packages: {
      rxjs: {
        main: 'index.js',
        defaultExtension: 'js'
      },
      'rxjs/operators': {
        main: 'index.js',
        defaultExtension: 'js'
      }
    }
```

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
