# plugin_reg_error

Demonstration of a common plugin registration error silently handled by Flutter

## Getting Started

Running this project will throw the following error:

```
Unhandled Exception: MissingPluginException(
  No implementation found for method getAll on channel plugins.flutter.io/shared_preferences
)
```

This occurs because Flutter has silently stopped processing plugins, after
experiencing some kind of error setting up the flutter_facebook_auth plugin.

While this error's cause is driven by user error, the fact that Flutter
silently handles it and produces a spurious error with absolutely no
connection to the reason for the issue, this seems to clearly be a something
that the Flutter developers are responsible for, not the plugin developers
(although in this case, the plugin causing the error is one supported by the
Flutter team, too).
