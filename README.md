# Flutter Notes

## Where To?

Q: Where to call super.initState()?
A: Always first, before any custom initialization logic.
[Implementations of this method should start with a call to the inherited method, as in super.initState().](https://api.flutter.dev/flutter/widgets/State/initState.html)

Q: Where to call super.dispose()?
A: Always last, after releasing resources and cancelling subscriptions.
[Implementations of this method should end with a call to the inherited method, as in super.dispose().](https://api.flutter.dev/flutter/widgets/State/dispose.html)

Q: Where to call super.didChangeDependencies()?
A: Not specified by docs. Doesn’t matter. You can call it first by convention, for consistency.

Q: Where to call super.didUpdateWidget(oldWidget)?
A: Always first.
[Implementations of this method should start with a call to the inherited method, as in super.didUpdateWidget(oldWidget).](https://api.flutter.dev/flutter/widgets/State/didUpdateWidget.html)

Q: Where to call super.activate()?
A: Always first.
[Implementations of this method should start with a call to the inherited method, as in super.activate().](https://api.flutter.dev/flutter/widgets/State/activate.html)

Q: Where to call super.deactivate()?
A: Always last.
[Implementations of this method should end with a call to the inherited method, as in super.deactivate().](https://api.flutter.dev/flutter/widgets/State/deactivate.html)

## Should I?

Q: Should I use const constructors in Flutter?
A: Yes.
[Use const constructors on widgets as much as possible, since they allow Flutter to short-circuit most of the rebuild work.](https://docs.flutter.dev/perf/best-practices)
