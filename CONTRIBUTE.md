

# Contribute:

To install all dependencies run:

```
npm i
```

It will install:

- `dependencies` and `devDependencies` from ./package.json
- `peerDependencies` from ./package.json thanks to `install-peers-cli`
- `dependencies` and `devDependencies` from ./example/package.json (example `create react app` for testing)

## Developing your library:

To start developing your library, run `npm run dev`. It will build your library and run example `create-react-app` where you can test your components. Each time you make changes to your library or example app, app will be reloaded to reflect your changes.

## Styled-components:

Developing library with components built with styled-components is challenging because you have to keep only one instance of styled-components. If you would just symlink your library (`file:../` or `npm link`) to example app that is also using styled-components you'll get a console warning about multiple instances of styled-components (even though styled-components are peer dependency) and your styles will be possibly broken. To be able to conveniently develop styled components I am injecting bundled files directly into example app's /src folder and importing it in App.tsx along with type declaration.

## Typescript

This boilerplate lets you develop your libraries in Typescript and you can simultaneously test it in Typescript example create-react-app.


Thanks to:
* https://github.com/volcanioo/Human-Body-Rendering-HTML