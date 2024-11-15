# Hugo Boilerplate

![Hugo Boilerplate](https://github.com/fleek-tools/hugo-template/assets/74613246/fe3e3d3d-2fd9-46c9-9438-5654f19a5410)

## 🚀 Project Structure

Inside of your Hugo project, you'll see the following folders and files:

```text
/
├── archetypes/
├── public/
├── resources/
├── themes/
├── config.toml
└── package.json
```

If you want to learn more about `Hugo`, you can checkout the official [Hugo Documentation](https://gohugo.io/documentation/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command       | Action                        |
| :------------ | :---------------------------- |
| `hugo`        | Generate your website         |
| `hugo server` | Start Hugo development server |

## ⚡ How to deploy to Fleek (IPFS)

### 1. Create a `fleek.json` config file

You can configure this site deployment using [Fleek CLI](https://fleek.xyz/docs/cli/) and running:

```bash
 > fleek sites init
   WARN! Fleek CLI is in beta phase, use it under your own responsibility
   ? Choose one of the existing sites or create a new one. ›
   ❯ Create a new site
```

It will prompt you for a `name`, `dist` directory location & `build command`

- `name`: How you want to name the site
- `dist`: The output directory where the site is located, for this template it's `public`
- `build command`: Command to build your site, this will be used to deploy the latest version either by CLI or Github Actions

### 2. Deploy the site

After configuring your `fleek.json` file, you can deploy the site by running

```bash
fleek sites deploy
```

After running it you will get an output like this:

```bash
 WARN! Fleek CLI is in beta, use it at your own discretion
 > Success! Deployed!
 > Site IPFS CID: Qmbv2NT91iPkXaoim5CSwdR8MLEoquRPcsdZncZ5QaxAqn

 > You can visit through the gateway:
 > https://ipfs.io/ipfs/Qmbv2NT91iPkXaoim5CSwdR8MLEoquRPcsdZncZ5QaxAqn
```

### Extra features

- **Continuous Integration (CI):** `fleek sites ci` [Documentation.](https://fleek.xyz/docs/cli/sites/#continuous-integration)
- **Adding custom domains:** `fleek domains create` [Documentation.](https://fleek.xyz/docs/platform/domains/)

### Keep in mind

This template has been configured to produce a static output. This means you can deploy it directly to IPFS without needing a server. Make sure to generate your static site before deploying using `hugo`.

For absolute URLs to work correctly on IPFS, you need to configure the URLs to be the relative. This can be done in the `config.toml` file:

```toml
relativeURLs = true

```

## 👀 Want to learn more?

Feel free to check [Fleek Documentation](https://fleek.xyz/docs/) & [Hugo Documentation](https://gohugo.io/documentation/).
