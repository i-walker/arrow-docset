## [Λrrow](https://next.arrow-kt.io/docs/)-docset
<img height="70" src="https://avatars2.githubusercontent.com/u/29458023?v=4&amp;s=200" width="70">

### Why should you use it?
- *Λrrow-docset* is **faster** and **more intuitiv** than surfing through the internet
- *Λrrow-docset* gives you an **Single Point of Reference** for everything related to the Λrrow Documentation, **including the whole API Doc's**, which you previously had to manuelly search through with IntelliJ

![The workflow](https://gph.is/g/aRzvVwa)

#### Prerequsite:
- [Dash for macOS or iOS ](https://kapeli.com/dash) or any other .docset Browser, e.g. [Zeal for linux](https://zealdocs.org)

- (Very much recommended - still optional) [Dash Alfredo Workflow](https://github.com/Kapeli/Dash-Alfred-Workflow) with [Alfredo](https://www.alfredapp.com)

- Powerusers should add the [IntellijDash Plugin](https://github.com/gdelmas/IntelliJDashPlugin) for an even smoother workflow 

### Install Λrrow-Docset

- Download the [current docset](https://github.com/i-walker/Arrow-Docset/releases)
- Open [Dash](https://kapeli.com/dash) -> click the plus icon -> click Download Docsets -> click Main Docsets 

- Under the Thread: Docsets -> click the plus icon in the left-hand corner -> click Add Local Docs -> specify the arrow-kt.docset file

### Dash a powerful time saver
- Enjoy Λrrow Offline 
![minimal](Screenshot%202019-04-22%20at%2008.23.14.png)

- Quick-search through the whole library without breaking a sweat - thanks to [Alfredo](https://github.com/Kapeli/Dash-Alfred-Workflow) and auto-rendering 

![Arrow example](Screenshot%202019-04-21%20at%2021.51.02.png)

- Search with tags and filters

![Haskell example](Screenshot%202019-04-21%20at%2021.34.08.png)

### Features

- [X] Enable arrow-playground
- [X] Searchable type classes and classes
- [X] Searchable functions
- [X] Searchable packages
- [X] Searchable guides
- [X] Searchable types 
- [ ] Available through the dash contribution platform 


## Contributions

This beautiful library deserves a dash-docset. 
Help me to create a more discoverable version. 

To enable more features we will use [dashing](https://github.com/technosophos/dashing)
It is pretty straight-forward, we map [Dash Datatypes](https://kapeli.com/docsets#supportedentrytypes)
to Arrow. 

PR's are very welcomed ! 
Visit the [dashing website](https://github.com/technosophos/dashing) to get started.

Your development environment is the [next.arrow-kt.io file](https://github.com/i-walker/Arrow-Docset/tree/master/next.arrow-kt.io). 
Add the appropriate mappings to dashing.json under selector and check-out the issues.

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
## Available Docset Datatypes

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
"css selector": "Docset Datatype"

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
This is a pretty good [example](https://www.awesome-testing.com/2017/05/how-to-find-test-cssselector-using.html) how to specify the css selectors with this [tester](https://www.w3schools.com/cssref/trysel.asp) and an [cheat-cheet](https://www.w3schools.com/cssref/css_selectors.asp)
- Debugging and building the docset

```bash
$ dashing build
```

## Acknowledgement
Many Thanks to the Λrrow Community who set up the API Doc's and Guides. Special thanks to [@nomisRev](https://github.com/nomisRev) and [@raulraja](https://github.com/raulraja) !