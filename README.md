# proxify-vercel

As long as Vercel (formerly Now) CLI does not support being run behind a proxy (see https://github.com/zeit/now/issues/255) you can do so with this small wrapper.

## Usage

Uninstall vercel!

```
npm r -g vercel
```

Install proxify-vercel:

```
npm i -g proxify-vercel
```

Set your http_proxy, https_proxy and no_proxy environment variables.

Start using Vercel (formerly Now) CLI with support for http_proxy, https_proxy and no_proxy:

```
vercel <any Vercel (formerly Now) CLI commands>
```

## How does it work?

proxify-vercel runs Vercel (formerly Now) CLI with ```global-agent``` preloaded. ```global-agent``` adds proxy support to any http agent running in the process.

## Credits

This is a fork of the [wrapper for Now that respects proxy environment variables](https://github.com/Horsed/proxify-now)  by Martin Knopf.
