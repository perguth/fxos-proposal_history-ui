# fxos-proposal_history-ui
##### "The past affects the future" - a different app history viewer concept exemplified

I want to illustrate my proposal with this short user experience story:

Depict a FxOS user. The following graph shows him having 3 items in his history:

```
{ Site 1 }
  -> { Site 2 }
      -> { Site 3 } --- User using `Site 3`
```

The User opens the `history viewer` and activates `Site 2`.

```
{ Site 1 }
  -> { Site 2 } --- User using Site 2
      -> { Site 3 }
```

The User goes to the `home screen` and from there activates any other app (let's say `Site 4`).

```
  { Site 1 }
      -> { Site 2 }
          -> { Site 4 } ---- User using `Site 4`
              -> { Site 3 }
```

Now let's call `{ Site 3 }` our most recent "`future entry`". But when the user opens the history viewer he will not see `{ Site 3 }` anymore, it cuts off after `{ Site 4 }`. I propose FxOS should display "future entries" to the user.

**Related question:**  
Can the constraint be dropped, that the home screen has to be reached, in order to create a new
future entry? Maybe we should create a fitting JavaScript API?

***

* [Discussion Issue](https://github.com/pguth/fxos-proposal_history-ui/issues/1)
