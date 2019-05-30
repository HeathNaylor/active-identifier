# Active Identifier - `active`
The objective of this application is to take in a list of projects/stories that you are working on and have one active at a time. You can add, remove, and activate any identifier. There must always be one active identifier at all times. The philosophy behind `active` is to be a global store for the story number, project name, or whatever string you like for quick access and insertion into other command line tools.

## API
`active` - Get the active identifier to stdout as a string.

`active <string>` - Set the active identifier, if one does not exist for the given string, create it.

`active ls` - List all of the identifiers, denote which one is active.

`active rm <string>` - Removes the identifier from the active list

## Recommended Alias
It is recommended that you alias `a` for the `active` binary, allowing very quick access.

## Usage Example
One use of `active` could be to pipe the active story you are working on into a time tracking app such as [Watson](https://tailordev.github.io/Watson/).
```
watson add $(active)
```
or
```
watson add myproject +$(active)
```
