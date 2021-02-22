# Action append Github PR description

This action append the provided deployment URL to Github's pull request description if not already present.

## Inputs

### `auth`

**Required** The github auth token.

### `repo`

**Required** The github repo name.

### `owner`

**Required** The github repo owner.

### `pr`

**Required** The pr number.

### `url`

**Required** The output deployed url.

## Example usage

```
uses: actions/action-append-pr-description
with:
  auth: 'AUTH_TOKEN'
  repo: 'Hello-World'
  owner: 'octocat'
  pr: 3
  url: 'http://www.test.url'
```

## How to test

You can test the action locally by copying the code to your own repo (that use a github workflow).
When updating the code, don't forget to run `yarn package` and commit the `dist/index.js` file since this is the one used by the action.
