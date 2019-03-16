# Atdgen Workshop Starter Project

Clone this repo to help you start the [atdgen workshop](https://github.com/feihong/atdgen-workshop/).

## Prerequisites

Install BuckleScript

```bash
npm init

# Install bs-platform
npm add bs-platform --dev

# Add runtime to be used by generated code
npm add @ahrefs/bs-atdgen-codec-runtime
```

We have compiled atdgen for you into a JavaScript file, you can view its documentation by running `node bin/atdgen.js --help`.

### Optional

If you want to use native OCaml version of atdgen, you can use [Esy](https://esy.sh) to install it.

```bash
# Create esy config file:
echo '{
  "dependencies": {
    "@opam/atd": "*",
    "@opam/atdgen": "*"
  },
  "resolutions": {
    "@opam/atd": "github:mjambon/atd:atd.opam#8089d9e",
    "@opam/atdgen": "github:mjambon/atd:atdgen.opam#8089d9e"
  },
  "devDependencies": {
    "ocaml": "~4.7.1"
  }
}' > esy.json
# Download and build dependencies:
esy install && esy build
# Verify it's working:
esy x atdgen --help
```

## Suggested approach

1. Download api key and store it in `api-key.txt`
1. Write a function to download ...
1. Modify `server.js` to return your response at `/api/` endpoint
1. Start the server by running `yarn server.js`
