# fxos-proposal_history-ui
##### "The past affects the future" - a different app history viewer concept exemplified

_Proposed behaviour exemplified:_

**(FxOS state:) Site open/active:**

```
x ->
{ Site 1 } ->
  [#] ->
    { Site 2 } ->
      [# User using site 3 #] () =>
        { Site 3 } -> y
```

**(FxOS state:) History mode active:**  

Sidenote: Currently exclusively reachable by pressing the physical homes screen key.

```
x ->
{{ Site 1 }} ->
  [#] ->
    {{ Site 2 }} ->
      [# User viewing entry of site 3 #] ->
        {{ Site 3 }} -> y

x ->
{{ Site 1 }} ->
  [# User viewing entry of site 2 #] ->
    {{ Site 2 }} ->
      [#] ->
        {{ Site 3 }} -> y

x ->
{{ Site 1 }} ->
  [# User viewing site 2 #] () =>
    {{ Site 2 }} ->
      [#] ->
        {{ Site 3 }} -> y
```

User goes to the home screen (let's call it the `hub`) and then activates any other app from there (let's say `Site 4`).

```
{{ Site 1 }} ->
  [#] ->
    {{ Site 2 }} ->
      [# User viewing site 4 #] () =>
        {{ Site 4 }} ->
          [#] ->
            {{ Site 3 }} -> y
```

Let's call `{ Site 3 }` our most recent "`future entry`".

**Related question:**  
Can the constraint be dropped, that the home screen has to be reached, in order to create a new
future entry? Maybe we should create a fitting JavaScript API?
