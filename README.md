# pinger [![CircleCI](https://circleci.com/gh/nezorflame/pinger/tree/main.svg?style=svg)](https://circleci.com/gh/nezorflame/pinger/tree/main) [![Go Report Card](https://goreportcard.com/badge/github.com/nezorflame/pinger)](https://goreportcard.com/report/github.com/nezorflame/pinger) [![GolangCI](https://golangci.com/badges/github.com/nezorflame/pinger.svg)](https://golangci.com/r/github.com/nezorflame/pinger) [![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fnezorflame%2Fpinger.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fnezorflame%2Fpinger?ref=badge_shield)

Example bot template for Telegram.

## Description

With this type of setup all you need to do is:

- create a project from the template and `git clone` it
- replace the module and bot name to your own
- add required code
- change the config file to your needs
- modify `.service` file for systemd to manage your bot
- deploy your bot to the server of choice, using modified config and service files

## Dependencies

This bot uses:

- [tgbotapi](https://pkg.go.dev/github.com/go-telegram-bot-api/telegram-bot-api/v5) package to work with Telegram API
- [bbolt](https://pkg.go.dev/go.etcd.io/bbolt) for local database
- [viper](https://pkg.go.dev/github.com/spf13/viper) for configuration
- [slog](https://pkg.go.dev/log/slog) for logging

## Structure

This project mostly adheres to the [Project Layout](https://github.com/golang-standards/project-layout) structure, excluding `pkg` folders.

`internal` package holds the private libraries:

- `config` for configuration
- `bolt` for database (using BoltDB)
- `file` for file and network helpers
- `telegram` package with bot implementation

## Customization

To add another custom command handler, you can:

- add a command to `config.toml` (and also a corresponding message, if required)
- edit `internal` packages

## License

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fnezorflame%2Fpinger.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fnezorflame%2Fpinger?ref=badge_large)
