# Blog Theme

[Orchard Core](https://github.com/OrchardCMS/OrchardCore) Theme for simple blog website.

## Status

[![Build Status](https://secure.travis-ci.org/moov2/Moov2.OrchardCore.BlogTheme.png?branch=master)](http://travis-ci.org/moov2/Moov2.OrchardCore.BlogTheme) [![NuGet](https://img.shields.io/nuget/v/Moov2.OrchardCore.BlogTheme.svg)](https://www.nuget.org/packages/Moov2.OrchardCore.BlogTheme)

*Currently under development but available as a pre-release on NuGet.*

## Getting Started

This theme is available as a pre-release on [NuGet](https://www.nuget.org/packages/Moov2.OrchardCore.BlogTheme).

### Package Manager Console

```
PM> Install-Package Moov2.OrchardCore.BlogTheme
```

### .NET CLI Console

```
> dotnet add package Moov2.OrchardCore.BlogTheme
```

## Development

Below is all that's needed to know to contribute to the theme.

### Prerequisities

#### [.NET Core](https://docs.microsoft.com/en-us/dotnet/core/)

Orchard Core runs on the .NET Core. Download the latest version from [https://www.microsoft.com/net/download/core](https://www.microsoft.com/net/download/core).

#### [NodeJS](https://nodejs.org/en/)

The theme requires NodeJS to assist with gathering third party front-end dependencies and compiles front-end assets. Compilation of front-end assets is handled by [Webpack](https://webpack.js.org/).

### Commands

#### Compiling Front-end Assets

When developing, it's likely you'll be working with front-end assets (located in `/Assets`) that need to be compiled in to files that are referenced by the theme (in `Views/Layout.cshtml`). The command shown below will compile CSS & JavaScript assets via Webpack and keep watch of files that will trigger compilation.

    npm run develop

*Hint: Running `npm start` will run the command above after running `npm install`.*

When the theme is deployed to a production environment we need to serve compressed assets for optimial delivery to improve page load times. The command below will compile assets ready for optimal delivery.

    npm run bundle

#### Packaging

When the theme is compiled (using `dotnet build`) it's configured to generate a `.nupkg` file (this can be found in `\bin\Debug\`).