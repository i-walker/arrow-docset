## [Λrrow](https://next.arrow-kt.io/docs/)-docset
<img height="70" src="https://avatars2.githubusercontent.com/u/29458023?v=4&amp;s=200" width="70">

This beautiful library deserves a dash-docset. 
Help me to create a more discoverable version of this minimal example. 

To enable all features we will use [dashing](https://github.com/technosophos/dashing)
It is pretty straight-forward, we map [Dash Datatypes](https://kapeli.com/docsets#supportedentrytypes)
to Arrow. 

PR's are very welcomed ! 
Visit the [dashing website](https://github.com/technosophos/dashing) to get started.


#### Prerequsite:
- [Dash for macOS or iOS ](https://kapeli.com/dash) or any other .docset Browser, e.g. [Zeal for linux](https://zealdocs.org)

- (Very much recommended - still optional) [Dash Alfredo Workflow](https://github.com/Kapeli/Dash-Alfred-Workflow) with [Alfredo](https://www.alfredapp.com)

- Powerusers should add the [IntellijDash Plugin](https://github.com/gdelmas/IntelliJDashPlugin) for an even smoother workflow 

### Install Λrrow-Docset

- Download the [current docset](https://github.com/i-walker/Arrow-Docset/releases)
- Open [Dash](https://kapeli.com/dash) -> Click the plus icon -> Go to Download Docsets 
-> Main Docsets 

- Under the Thread: Docsets -> in the left corner there is a plus and go to -> Add Local Docs -> specify the arrow-kt.docset file

### Dash a powerful time saver
- You will have Λrrow Offline 
![minimal](Screenshot%202019-04-21%20at%2021.49.08.png)

- Combined with [Alfredo](https://github.com/Kapeli/Dash-Alfred-Workflow) and its auto-rendering - You can quick-search through the whole library without breaking a sweat

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
This is a pretty good [example](https://www.awesome-testing.com/2017/05/how-to-find-test-cssselector-using.html) how to specify the css selectors with this [tester](https://www.w3schools.com/cssref/trysel.asp)

- Debugging and building the docset

```bash
$ dashing build
```