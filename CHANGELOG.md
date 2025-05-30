# Changelog

## 0.3.0

Updates to dependencies and adding `times` option to `expect`:

- Replace fifth argument in `expect` from `pid` to options.
  In the scenarios where you've used `expect/5`, wrap the value in `times: old_value`.
- Allow `times` option in `expect/5` to limit the amount of times a mock may be used.

## 0.2.1

This version has mostly been about internal improvements, reliability where we'll see more helpful
error messages and easier usage.

- Treat non-binary response bodies as JSON
- Add type specs to all public functions
- Improve consistency in error messages
- Raise when callback functions doesn't return a `Moxinet.Response`
- Clean up signatures after test process shuts down

## 0.2.0

A few minor upgrades to make `expect` both more powerful, but also easier to use.

- Add `%Moxinet.Response{}` struct to formalize responses from `expect` callbacks
- Allow both 1- and 2-arity functions for `expect` callbacks to allow headers to be verified
- Always pass request body to `expect` callbacks (empty bodies will be `nil`)
