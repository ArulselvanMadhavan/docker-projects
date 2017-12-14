# AWS CLI Container Challenge

Put your Dockerfile and Linux skills to the test and build a portable AWS CLI that can be used anywhere.

## Requirements

1 - Create a Dockerfile that:

- Uses the smallest possible Python distribution.
- Updates and upgrades system packages.
- Installs the AWS CLI package via the `pip` Python package manager - `pip install pip awscli --upgrade`
- The working directory should be `/usr/src/app`
- The default command should be `bash`.
- As we *desire no state* to be stored, running this container should be done with the `--rm` flag.

2 - Create a `Makefile` that has commands for building and running.

## Bonus Challenge

Added the following two lines to the `/root/.bashrc` to make using the AWS CLI nicer.

    complete -C '/usr/local/bin/aws_completer # Tab completion for API calls
    aws configure # Not much point having an CLI without configuring it for us
