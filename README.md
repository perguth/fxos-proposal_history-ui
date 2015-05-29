# fxos-proposal_history-ui
##### "The past affects the future" - a different `history` viewer concept exemplified

_Proposed behaviour exemplified:_

## fxos state: site open/active:

```
x ->
{ Site 1 }
  [#] ->
    { Site 2 } ->
      [# User using site 3 #] =>
        { Site 3 } -> y
```

## fxos state: history mode active (currently reachable by pressing the physical homes screen key):

```
x ->
{{ Site 1 }}
  [#] ->
    {{ Site 2 }} ->
      [# User viewing entry of site 3 #] ->
        {{ Site 3 }} -> y

x ->
{{ Site 1 }}
  [# User viewing entry of site 2 #] ->
    {{ Site 2 }} ->
      [#] ->
        {{ Site 3 }} -> y

x ->
{{ Site 1 }} ->
  [# User activating/then viewing site 2 #] =>
    {{ Site 2 }} ->
      [#] ->
        {{ Site 3 }} -> y


User goes to the home screen (let's call it `hub`) and then activates any other app from there (let's say "Site 4").

{{ Site 1 }} ->
  [#] ->
    {{ Site 2 }} ->
      [# User viewing entry of site 4 #] ->
        {{ Site 4 }} ->
          [#] ->
            {{ Site 3 }} -> |

Let's call `{ Site 3 }` now our most recent "future entry".

**Related question:**\
Can the requirement be dropped that the home screen has to be reached in order to create a new
future entry? Maybe create a fitting API to create furure entries from a websites JS code?
