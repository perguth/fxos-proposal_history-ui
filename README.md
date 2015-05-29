# fxos-proposal_history-ui
##### "The past affects the future" - a different app history viewer concept exemplified

_Proposed behaviour exemplified:_

**(FxOS state:) History mode active:**  

Exclusively reachable by pressing the physical homes screen key.

The user sees the history browser. He/she has already opened a few apps so he/she see a couple of them in hir history. The following graph depicts a user that has 3 items in hir history.

```
{ Site 1 }
  -> { Site 2 }
      -> { Site 3 } --- [ User `viewing` entry of site 3 ]
```

The User goes to the home screen (let's call it the `hub`) and then activates any other app (let's say `Site 4`).

```
  { Site 1 }
      -> { Site 2 } ---- [ User *viewing* site 4 ]
          -> { Site 4 }
              -> { Site 3 }
```

Let's call `{ Site 3 }` our most recent "`future entry`". In the current version of FxOS we would no longer be able to swipe to `Site 3` by now (or even graphically see it).

**Related question:**  
Can the constraint be dropped, that the home screen has to be reached, in order to create a new
future entry? Maybe we should create a fitting JavaScript API?

***

* [Discussion Issue](https://github.com/pguth/fxos-proposal_history-ui/issues/1)
