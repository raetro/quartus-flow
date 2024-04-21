# Quartus Flow V1

This action use the `quartus_sh` executable with the `--flow` option to perform a complete compilation flow with a single command.

# What's new

Please refer to the [release page](https://github.com/raetro/quartus-flow/releases/latest) for the latest release notes.

# Usage

```yaml
name: Quartus Workflow
on: [ push ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v4

      - name: Runs Quartus analysis & synthesis, fitter, timing analysis, and programming file generation
        uses: raetro/quartus-flow@v1
        with:
          # Quartus Project File. For example, blinking_led
          # [Required]
          project: ''

          # Project Revision Name. For example, blinking_led_rgb
          # Default: Empty
          revision: ''

          # Quartus Version/Alias. For example, 17.1 or pocket
          # Default: 17.1
          version: ''

          # Project Folder containing the qpf file. For example, projects/sockit
          # Default: projects
          project_folder: ''
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
