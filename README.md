# action-append-pr-description

The `chabroA/action-append-pr-description` action is a JavaScript action that appends a provided deployment URL to a GitHub pull request description if not already present.

## Usage

```yaml
steps:
  - name: Add deploy URL to PR description
    uses: chabroA/action-append-pr-description@master
    with:
      auth: ${{ secrets.GITHUB_TOKEN }}
      repo: ${{ github.event.repository.name }}
      owner: ${{ github.repository_owner }}
      pr: ${{ github.event.number }}
      url: "https://my-url.test"
      message: "My url :" 
```

## Inputs

- `auth` - (required) A [GitHub Secret Token](https://docs.github.com/en/actions/reference/authentication-in-a-workflow) with access to the repository you want to update.

- `repo` - (required) The GitHub repository name containing the PR to update.

- `owner` - (required) The GitHub repository owner.

- `pr` - (required) The pull request number.

- `url` - (required) The url to append to the specified pull request description.

- `message` - (optional) The message to append before the url.

## Outputs

This action does not configure any outputs.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

You can test the action locally by copying the code to your own repo (that uses a github workflow).

When updating the code, don't forget to run `yarn package` and commit the `dist/index.js` file since this is the one used by the action.

cf. [GitHub Docs about JavaScript action](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action)

## License

[MIT](./LICENSE.md)
