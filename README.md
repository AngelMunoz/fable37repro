# Perla + Feliz Template

Reproduction steps

```
dotnet perla serve
```

it doesn't finish compiling ever (this might be how we invoke the fable executable), one has to invoke the manual compilation

```
dotnet fable src
dotnet perla serve
```

visit `localhost:7331`

in the browser console you will get a message like

```
Router.fs.js:4
    Uncaught SyntaxError: The requested module '../Feliz.1.57.0/React.fs.js' does not provide an export named 'React_useCallbackRef_7C4B0DD6'
```

although F# sources do have React.useCallbackRef

To _un-reproduce_ just switch to fable 3.6
