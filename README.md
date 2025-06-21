## Summary

- [Requirements](https://github.com/jotavemonte/lazydocker#requirements)
- [Usage](https://github.com/jotavemonte/lazydocker#usage)
- [Keybindings](/docs/keybindings)
- [Cool Features](https://github.com/jotavemonte/lazydocker#cool-features)
- [Config Docs](/docs/Config.md)
- [FAQ](https://github.com/jotavemonte/lazydocker#faq)

### Manual

You'll need to [install Go](https://golang.org/doc/install)

```
go install
```

You can also use `go run main.go` to compile and run.

## Usage

Call `lazydocker` in your terminal. If you run it a folder with a docker-compose.yml expect to have the services listed.

## Cool features

everything is one keypress away (or one click away! Mouse support FTW):

- viewing the state of your docker or docker-compose container environment at a glance
- viewing logs for a container/service
- viewing ascii graphs of your containers' metrics so that you can not only feel but also look like a developer
- customising those graphs to measure nearly any metric you want
- attaching to a container/service
- restarting/removing/rebuilding containers/services
- viewing the ancestor layers of a given image
- pruning containers, images, or volumes that are hogging up disk space

## FAQ

### How do I edit my config?

By opening lazydocker, clicking on the 'project' panel in the top left, and pressing 'o' (or 'e' if your editor is vim). See [Config Docs](/docs/Config.md)

### How do I get text to wrap in my main panel?

In the future I want to make this the default, but for now there are some CPU issues that arise with wrapping. If you want to enable wrapping, use `gui.wrapMainPanel: true`

### How do you select text?

Because we support mouse events, you will need to hold option while dragging the mouse to indicate you're trying to select text rather than click on something. Alternatively you can disable mouse events via the `gui.ignoreMouseEvents` config value.

Mac Users: See [Issue #190](https://github.com/jesseduffield/lazydocker/issues/190) for other options.

### Why can't I see my container's logs?

By default we only show logs from the last hour, so that we're not putting too much strain on the machine. This may be why you can't see logs when you first start lazydocker. This can be overwritten in the config's `commandTemplates`
