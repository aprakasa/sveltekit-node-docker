# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

## Container

Build docker image
```bash
docker build . -t sveltekit:alpine-multistage
```

Run docker image
```bash
docker run -dp 5050:5050 -e PORT=5050 -e ORIGIN=http://localhost:5050 --name sveltekit-app sveltekit:alpine-multistage
```
SvelteKit has [Block cross-site form POSTs by default](https://github.com/sveltejs/kit/pull/6510). So we need to expose the [ORIGIN](https://github.com/sveltejs/kit/tree/master/packages/adapter-node#origin-protocol_header-and-host_header) from the environment variable.

Run the image with docker compose:
```bash
docker compose up -d
```

## Video Explaination

https://youtu.be/kVMG2nWjWk4