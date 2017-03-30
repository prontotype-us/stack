# The Prontotype Stack

Prontotype's technology stack was designed to build complex web apps and services with minimal overhead.

## Web apps

Every web site is of course made with HTML, CSS and Javascript. We use a set of languages that compile into each of these, which follow a common "Pythonic" style (bracketless and indentation-based).

We use [Metaserve](https://github.com/prontotype-us/metaserve) to automatically compile these languages during development and to deploy (by "bouncing" a compiled version of the file).

### CoffeeScript (Javascript)

CoffeeScript is a bracketless version of Javascript with a few syntactic niceties including arrow functions (`timesFive = (a) -> a * 5`) , object destructuring (`{name, age} = person`) and spreads (`person = {name, age}`)

#### React and JSX

With [coffee-reactify](https://github.com/jsdf/coffee-reactify) the JSX syntax can be used within CoffeeScript:

```coffee
ItemSummary = ({item}) ->
    <div className='item'>
        {item.name}
    </div>
```

### Styl / Sass / Rework (CSS)

[Styl](https://github.com/tj/styl), based on [Rework](https://github.com/reworkcss/rework), is a bracketless CSS variant (alone known as Sass) with plugins (supported by Rework). The Rework framework allows for plugins which support [variables](https://github.com/bloglovin/node-rework-variant), [calculations](https://github.com/reworkcss/rework-calc), [color modifications](https://github.com/ianstormtaylor/rework-color-function), and [custom functions](https://github.com/reworkcss/rework-plugin-function), and more.

```sass
.item
    color: color($colors.blue shade(10%))
    font-size: $fonts.small
```

### Jade (HTML)

Jade is an indentation based HTML templating language with support for variables, loops, and conditionals.

```jade
body
    h1 Hello
    for item in list
        li.item Item: #{item}
```

## Web APIs

*TODO* Describe super-api and AWS API Gateway

## Mobile apps

*TODO* Describe React Native

## Backend services

*TODO* Describe Somata
