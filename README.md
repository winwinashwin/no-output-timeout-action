# no-output-timeout for GitHub Actions

A functional composite action to kill commands/scripts that hasn't produced any output for x seconds. Inspired by CircleCI's `no_output_timeout` feature.

> [!IMPORTANT]  
> This action is highly platform specific as it requires access to process tables and related commands. It is developed and tested on debian based images, you might want to edit the [action.yml](./action.yml) file for other platforms. **Contributions are welcome!**

## Input Variables

See [action.yml](./action.yml) for detailed information.

|      Input      | Description                                                         |  Default Value   |
| :-------------: | ------------------------------------------------------------------- | :--------------: |
|     timeout     | Elapsed time the command can run without output (in seconds)        | 600 (10 minutes) |
| fail_on_timeout | Whether or not to exit with non-zero code when command is timed out |      False       |
| redirect_stderr | stderr to stdout redirection                                        |      False       |
|     script      | Commands to be executed                                             |                  |
