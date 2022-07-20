# Googlers Magisk Repo

This is an personal repository. It's directly props from the `modules.json` instead of url requests.

## How it works

Inside every folder is an `app.prop` that includes all required properties like `name`, `package`, and more. There is also the `repo.conf` configuration, that loads some properties directly from the repository, like `description`, `download` and `readme`.

## Requesting `README` from another repo

You can it make like old school with `https://raw.githubusercontent.com/Fox2Code/FoxMagiskModuleManager/master/README.md`, but.. if you use `{Mirror=Fox2Code/FoxMagiskModuleManager:Branch=master:File=README.md}`, than will you get the same result.

## Configuration

### `app.prop`

| `name`        | required | Used get the name                                                                                |
| ------------- | -------- | ------------------------------------------------------------------------------------------------ |
| `package`     | required | Used the share it as url / link                                                                  |
| `description` | optional | Describe your app :)                                                                             |
| `versionName` | required | Displays the current versions name                                                               |
| `versionCode` | required | Displays the current versions code                                                               |
| `icon`        | optional | To set the icon of the app. Use `{localURL}/path/to/icon.png` to get an icon from current folder |
| `download`    | required | Used to download the app or redirect to another download                                         |

### `repo.conf`

| `repo`   | optional | Uses the ability to take parameters from the given repository. Overrides `description` and `download` |
| -------- | -------- | ----------------------------------------------------------------------------------------------------- |
| `readme` | optional | Overrides the notes url                                                                               |
