# fxos-proposal_history-ui
##### "The past affects the future" - a different app history viewer concept exemplified

I want to illustrate my proposal with this short user experience story: Depict a FxOS user. He has already opened 3 apps by now. The following graph depicts, in an abstract form, what the user sees when he opens the FirefoxOS `app history viewer`:

```
{ App 1 }
  -> { App 2 }
      -> { App 3 }
```

The User opens the `app history viewer` and activates `App 2`:

```
{ App 1 }
  -> { App 2 } --- User using App 2
      -> { App 3 }
```

The User goes to the `home screen` and from there activates any other app (let's say `App 4`). He then opens the `app history viewer`:

```
  { App 1 }
      -> { App 2 }
          -> { App 4 }
```

Note that FirefoxOS has cut something off here. I propose to change that so the user would rather see this:

```
  { App 1 }
      -> { App 2 }
          -> { App 4 } --- in focus since most recently used
              -> { App 3 }
```


Let's call `{ App 3 }` our most recent "`future entry`" and allow for endlessly deep nesting.

**Related question:**  
Can the constraint be dropped, that the home screen has to be activated, in order to create a new
future entry? Maybe we should create a fitting JavaScript API to do that programmatically?

***

* [Discussion Issue](https://github.com/pguth/fxos-proposal_history-ui/issues/1)
