## [Arrow](https://next.arrow-kt.io/docs/) Docs

This beautiful library deserves a dash-docset. 
Help me to create a more discoverable version of this minimal example. 

To enable all features we will use [dashing](https://github.com/technosophos/dashing)
It is pretty straight-forward, we map [Dash Datatypes](https://kapeli.com/docsets#supportedentrytypes)
to Arrow. 

PR's are very welcomed ! 
Visit the [dashing website](https://github.com/technosophos/dashing) to get started.

### How to use it

- Download the [current docset](https://github.com/i-walker/Arrow-Docset/releases)
- Open Dash and Go to Download Docsets 
-> Main Docsets 

- Under the Thread Docsets in the left corner there is a plus and go to -> Add Local Docs

- Currently it is a bit verbose because every link is specified as a class named Arrow, but that won't stay that long

### Dash a powerful time saver
- You will have Arrow Offline 
![minimal](Screenshot%202019-04-18%20at%2010.24.45.png)

- Combined with Alfredo - You can quick-search through the whole library without breaking a sweat

Here is an Haskell example:
![Haskell example](Screenshot%202019-04-18%20at%2010.30.01.png)

- Search with tags and filters

![Haskell example](Screenshot%202019-04-18%20at%2010.39.19.png)

### Features

- [X] Enable arrow-playground
- [ ] Searchable type classes
- [ ] Searchable effects
- [ ] Searchable data-types
- [ ] Searchable optics
- [ ] Searchable AQL 
- [ ] Searchable Generics
- [ ] Searchable Integrations
- [ ] Searchable Free
- [ ] Searchable Recursion Schemes

## Contributions
Your development environment is the [next.arrow-kt.io file](https://github.com/i-walker/Arrow-Docset/tree/master/next.arrow-kt.io). 
Add the appropriate mappings to dashing.json under selector. Check-out the issues.

Dowload dashing:
```
$ brew install dashing
```
or 
```
$ go get -u github.com/technosophos/dashing
```
Here are the [sources](https://github.com/technosophos/dashing/releases)

```
## Docset Datatypes

Annotation  Attribute   Binding     Builtin     Callback    Category
    
Class   Command     Component   Constant    Constructor   Define   
 
Delegate   Diagram     Directive       Element     Entry       Enum 

Environment     Error       Event       Exception       Extension  

Field       File        Filter      Framework       Function     

Global      Guide       Hook        Instance        Instruction     

Interface       Keyword     Library     Literal     Macro       Method

Mixin       Modifier        Module      Namespace       Notation 

Object      Operator        Option      Package     Parameter       Plugin

Procedure       Property        Protocol        Provider     Provisioner

Query       Record      Resource        Sample      Section     Service  
   
Setting     Shortcut        Statement       Struct      Style         Subroutine 

Tag     Test        Trait       Type        Union       Value       Variable        Word

```

You then specify the exact place in the HTML where Dash can find the Datatype, e.g.:
"html xpath": "Docset Datatype"

```
dashing.json
{
  //...
  "selectors": {
          "title": "Interface"
      },
      //...
}
```
This is a pretty good [example](https://www.awesome-testing.com/2017/05/how-to-find-test-cssselector-using.html) how to specify the css selectors with this [tester](https://www.w3schools.com/cssref/trysel.asp)

- Debugging 

```bash
$ dashing build
```