<!--- vim: set fdm=marker: -->
% title: Webdev Workflow
% subtitle: Hook up your development environment
% author: Zach Fogg
% author: @zfogg
% thankyou: Thanks &#58;&#41;
% thankyou_details:
% contact: <div id="roboto-wrapper"><img src="http://terrapinhackers.com/img/roboto_icon.png" width="80" height="80" alt="Roboto"></div>
% favicon: http://terrapinhackers.com/img/favicon.ico

<!--Intro{{{-->
---
title: Workflow
build_lists: true

- Good developers spend time on them
- A good workflow equals better output
- The best workflow could be better

<!--{{{-->
---
title: Pretend like you're blackout-drunk
subtitle: Relevant XKCD
class: img-top-center

<img src="http://girlingumboots.files.wordpress.com/2012/06/ballmer_peak-1-2.jpg" alt="Ballmer Peak">

<footer class="source">http://xkcd.com/323/</footer>

<!--}}}-->

<!--{{{-->
---
title: Know your tools
subtitle: like the back of your hand

<q>
I think we’re seeing the emphasis shift from valuing trivia to valuing tools.
</q>

<footer class="source">
    <a href="http://rmurphey.com/blog/2012/04/12/a-baseline-for-front-end-developers/">
        Rebecca Murphey - Adventures in JavaScript Development
    </a>
</footer>

<!--}}}-->

<!--{{{-->
---
title: Know your tools
subtitle: like the back of your hand
build_lists: true

<q>
As an engineer, there is a short list of tools that you must be rabid about. Rabid. Foaming at the mouth crazy.
</q>

<br>

- Text editor  

- Terminal

<footer class="source">
    <a href="http://randsinrepose.com/archives/the-foamy-rules-for-rabid-tools/">
        Michael Lopp - randsinrepose.com
    </a>
</footer>

<!--}}}-->

<!--Intro}}}-->


<!--Text editor{{{-->
---
title: Text editor
class: segue dark nobackground

<!--{{{-->
---
title: Text editor
class: centered-content

<br> <br> <br> <br> <br> <br>

This is where you will spend most of time.

You should know your text editor best of all.

<!--}}}-->

<!--{{{-->
---
title: Text editor
build_lists: true

Your text editor should be
<br> <br>

- customizable  

- extendable  

- informative  

- a ' magic wand '

<!--}}}-->

<!--{{{-->
---
title: Text editor
build_lists: true

### **How I rank them**
on a scale of `ed` to `vi`
<br>

- Notepad.exe  
A stick

- Notepad++  
_Harry Potter_'s broken wand

- Sublime Text 2  
Your standard magic wand

- Emacs  
_Merlin_'s wand

- Vim  
_Gandalf the White_'s staff, fully automatic and turbocharged

<!--}}}-->

<!--{{{-->
---
title: Text editor
subtitle: Hands on the home row
build_lists: true

- Mice are good for many things
- but not code
<!--}}}-->

<!--{{{-->
---
title: Text editor
subtitle: Hands on the home row
build_lists: true

Keyboard shortcuts are a GoodThing™

- Learn them
- Make your own

<!--}}}-->

<!--Text editor}}}-->


<!--The command line{{{-->
---
title: The command line
subtitle: because it looks like you're 'hacking'
class: segue dark nobackground

<!--{{{-->
---
title: SSH is sweet
subtitle: and super simple
build_lists: true

- ~/.ssh/config
- Passwords are stupid
- <a href="https://github.com/zfogg/zfogg/blob/master/.ssh/config">/home/zfogg/.ssh/config</a>

- <pre class="prettyprint">
Host gh
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa
</pre>

- <pre class="prettyprint" data-lang="zsh">
$ git clone gh:zfogg/zfogg
Cloning into 'zfogg'...
</pre>

<!--}}}-->

<!--{{{-->
---
title: tmux is terrific
subtitle: and your terminal is terrible

- <a href="http://tmux.sourceforge.net/">tmux</a>
- <a href="http://www.github.com/zfogg/zfogg">/home/zfogg/.tmux.conf</a>

<!--}}}-->

<!--{{{-->
---
title: tmux is terrific
subtitle: and your terminal is terrible
build_lists: true

- Tabs and splits
- Sessions and SSH
- <a href="https://github.com/Lokaltog/powerline">Powerline</a> - the ultimate statusline/prompt utility

<!--}}}-->

<!--{{{-->
---
title: Aliases are amazing

<pre class="prettyprint" data-lang="zsh">
<b>$ alias please="sudo"</b>
$ touch /newfile
touch: cannot touch ‘/newfile’: Permission denied
<b>$ please touch /newfile</b>
$ 

$ alias ls="ls --color=auto"
# You can't avoid typos
$ alias sl="ls"

# Upgrade your `cat`! Syntax highlighting for any language
$ alias cat="pygmentize -O style=monokai -f console256 -g"

# Grab the IP addresses of a domain
$ alias ipaddr="dig +short myip.opendns.com @resolver1.opendns.com"

# Instant HTTP server in the current directory
$ alias server="python -m SimpleHTTPServer"
</pre>

<!--}}}-->

<!--{{{-->
---
title: Zsh is . . . zee best
subtitle: and Bash bites

- <a href="http://www.zsh.org/">Zsh</a>
- My own <a href="http://www.github.com/zfogg/zfogg">~/.zshrc</a>
- <a href="https://github.com/robbyrussell/oh-my-zsh">oh-my-zsh</a>  ~ Zsh themes and plugins

<!--}}}-->

<!--{{{-->
---
title: Zsh is . . . zee best
subtitle: and Bash bites
build_lists: true

- Navigation
- Spelling
- Command history
- Argument completion
- Prompts
- Syntax highlighting

<!--}}}-->

<!--{{{-->
---
title: The shell
subtitle: is full of secrets and wonders
build_lists: true

- `$ sudo !!`  

- `$ z somewhere`  

- `$ sudo pacman -S typo-package`  
`$ ^typo^correct^`  
or  
`$ !!:s/typo/correct`  

- `$ wget -O - http://placekitten.com/$[500 + RANDOM % 500]`  

<!--}}}-->

<!--The command line}}}-->


<!--Actual Web Development{{{-->
---
title: Actual web development
class: segue dark nobackground

<!--Actual Web Development}}}-->


<!--CSS Sucks{{{-->
---
title: CSS sucks
class: segue dark nobackground

<!--{{{-->
---
title: CSS sucks
subtitle: The defaults are ridiculous
class: centered-content img-top-center

<pre class="prettify" data-lang="css">* { box-sizing: border-box }</pre>
<br>
<img src="http://www.binvisions.com/wp-content/uploads/2011/09/css-box-model-border-content_590x328.jpg" alt="">

<!--}}}-->

<!--{{{-->
---
title: CSS sucks
subtitle: Too verbose for drunk Ballmer

<pre class="prettify" data-lang="css">
#header-bottom-left .tabmenu li a { direction: rtl; unicode-bidi: bidi-override; font-family: "Webdings";}
#header-bottom-left .tabmenu li {  height: 28px;  border: 0px; margin: 0px 5px; display: inline-block; }
#header-bottom-left .tabmenu li a {width:70px;color:#98C4F0;background:none;padding: 5px 2px!important;} 
#header-bottom-left .tabmenu li a:hover {color:#002B4D;} 
#header-bottom-left .tabmenu li.selected a {color:#002B4D;border:none!important;} 
#header-bottom-left .tabmenu li.selected a:before {content:"XD"} 
#header-bottom-left .tabmenu ul { width: 425px !important; height: 36px !important; z-index: -1 }
#header-bottom-left .tabmenu li { list-style-type: none; display: inline-block !important; margin: 0px; padding: 0px }
#header-bottom-left .tabmenu li a { color: #5F4444 !important; font: normal 14px/34px "Lucida Grande", "Lucida Sans Unicode", Arial, Helvetica, sans-serif;  }
</pre>

<!--}}}-->

<!--{{{-->
---
title: CSS sucks
subtitle: The simplest concepts are unnecessarily difficult

<pre class="prettify" data-lang="css">
.center-horizontal {
    margin: 0 auto;
    // :)
}

.center-vertical {
    margin: auto 0;
    // :(
}
</pre>

<!--}}}-->

<!--{{{-->
---
title: CSS sucks
subtitle: <br>
class: centered-content

#:/

<!--}}}-->

<!--CSS Sucks}}}-->


<!--Less and SASS{{{-->
---
title: LESS and SASS
subtitle: Leaner CSS and Syntactically Awesome Stylesheets
class: segue dark nobackground

<!--{{{-->
---
title: LESS and SASS
build_lists: true

- Variables
- Math
- Mixins
- Nested rules
- Libraries ~ Compass and Bootstrap

<!--}}}-->

<!--Less and SASS}}}-->


<!--JavaScript sucks{{{-->
---
title: JavaScript sucks
class: segue dark nobackground

<!--{{{-->
---
title: JavaScript sucks
subtitle: wtf

<pre class="prettyprint" data-lang="javascript">
!(new Boolean(false)) === !(new Boolean(true)); // true

1 == false; // true

(function () {
    return
        { haha: "ha!" };
}
)(); // undefined

var a = {};
a.b === undefined; // true
undefined = 42;
a.b === undefined; // false
</pre>

<!--}}}-->

<!--{{{-->
---
title: JavaScript sucks
subtitle: I'm done
class: centered-content

(╯°□°)╯︵ ┻━┻

<!--}}}-->

<!--{{{-->
---
title: JavaScript sucks
subtitle: <br>
build_lists: true

- `var` is stupid
- `==` is broken
- OOP is awkward
- implicit globals are dangerous
- semicolons and braces are unnecessary
- strings and lists are difficult

<!--}}}-->

<!--JavaScript sucks}}}-->


<!--CoffeeScript{{{-->
---
title: CoffeeScript
subtitle: A little language that compiles into JavaScript
class: segue dark nobackground

<!--{{{-->
---
title: CoffeeScript

<pre class="prettyprint" data-lang="coffeescript">
1 == true   # false

foo?.bar?() # `foo` and `bar` may not exist

[k,v] for k,v of { x:1, y:2, z:3 } # [["x", 1], ["y", 2], ["z", 3]]

times_two = (xs) -> 2*x for x in xs
doubles   = times_two [1..5] # [2, 4, 6, 8, 10]
1 < doubles[0] < 3           # true

[x, y] = [1, 2] # x = 1; y = 2
{pow}  = Math   # pow = Math.pow

good_enough = "#{ 22 / 7 } is a decent approximation of π" # string interpolation

StuffHandler = (stuff) ->
    @stuff = stuff # //this.stuff = stuff;
    $("#stuff").click (event) => @stuff.doSomething event
</pre>

<!--}}}-->

<!--{{{-->
---
title: CoffeeScript

<pre class="prettyprint" data-lang="coffeescript">
Array::head = -> @[0]
Array::tail = -> @[1..]

map = (f, xs) ->
    f x for x in xs

zip = (xs, ys) ->
    [xs[i], ys[i]] for i in [0...Math.min xs.length, ys.length]

fold1 = (f, xs) ->
    fold f, xs.tail(), xs.head()

fold = (f, xs, acc) ->
    if xs.length > 0
        fold f, xs.tail(), (f xs.head(), acc)
    else acc
</pre>

<!--}}}-->

<!--{{{-->
---
title: CoffeeScript

<pre class="prettyprint" data-lang="coffeescript">
class Mascot
    constructor: (@icon) ->
        @icon or= "img/default.png"
    draw: (x=0, y=0) ->
        drawPNG @icon, x, y

class Roboto extends Mascot
    constructor: ->
        super "img/roboto.jpg"
    draw: (x=0, y=0) ->
        drawJPG @icon, x, y
</pre>

<!--}}}-->

<!--{{{-->
---
title: CoffeeScript

<pre class="prettyprint" data-lang="coffeescript">
partial = (f, args1...) -> (args2...) ->
    f.apply @, args1.concat args2
partial$ = (f, args) ->
    partial.apply @, [f].concat args

sum     = do -> partial fold1, ((x,y) -> x+y)
product = do -> partial fold1, ((x,y) -> x*y)

factorial = (n) -> product [1..n]
</pre>

<footer class="source"><a href="https://gist.github.com/zfogg/9d69011f501437217c6e">source @ gist.github.com</a></footer>

<!--}}}-->

<!--{{{-->
---
title: CoffeeScript

<pre class="prettyprint" data-lang="coffeescript">
curry = (n, f, args...) ->
    curry$ (n - args.length), (partial$ f, args)
curry$ = (n, f, args...) ->
    if n > args.length
        partial curry$, (n - args.length), (partial$ f, args)
    else f.apply @, args

<b>Function::curry = (args...) ->
    curry.apply @, [@length, @].concat args</b>

Math.pow.curry()(2)(5)                       # 32
Math.pow.curry()(2, 5)                       # 32
Math.pow.curry(2, 5) == Math.pow.curry(2)(5) # 32

multiply  = (x, y) -> x*y
times_two = (xs)   -> xs.map multiply.curry(2)
</pre>

<footer class="source"><a href="https://gist.github.com/zfogg/9d69011f501437217c6e">source @ gist.github.com</a></footer>

<!--}}}-->

<!--{{{-->
---
title: CoffeeScript
build_lists: true

is not your only option

[AltJS - list of languages that compile to JS](http://altjs.org)

Don't like CS? Need more language features?

Choose another altjs language!

- [ClojureScript](https://github.com/clojure/clojurescript) by the Clojure team. Clojure (a JVM lisp) to JS compiler.
- [Dart]() by Google. Class based and object oriented with a C or Java-like syntax.
- [TypeScript](http://www.typescriptlang.org/) by Microsoft. Superset of JS with compile-time type support.

<!--}}}-->

<!--CoffeeScript}}}-->


<!--Git{{{-->
---
title: Git
subtitle: distributed version control
class: segue dark nobackground

<!--{{{-->
---
title: Git
subtitle: yourself a better workflow
build_lists: true
class: img-top-center

<img width="531" height="454" src="http://erickryski.com/assets/img/git_branch_diagram.jpg" alt="Git branch diagram">

<!--}}}-->

<!--{{{-->
---
title: Git
subtitle: yourself a better workflow
build_lists: true

You should know how to:

- `$ git add -p`  

- `$ git stash`  

- `$ git rebase -i`

- `$ git merge`

<!--}}}-->

<!--{{{-->
---
title: Git
subtitle: yourself a better workflow
build_lists: true

oh-my-zsh plugins `git` and `git-extras`
<br> <br>

- Automatic aliases - `$ alias | grep 'git'`  
<br>  
- Additional awesomeness:
- `$ git whatchanged -p --abbrev-commit --pretty=medium`
- `$ git delete-submodule` # Doing it yourself is messy.
- `$ git delete-branch`    # Local and remote
- `$ git undo`             # Undo last commit.

<!--}}}-->

<!--Git}}}-->


<!--Yeoman{{{-->
---
title: Yeoman
subtitle: modern workflow for modern apps
class: segue dark nobackground

<!--{{{-->
---
title: Yeoman
subtitle: yo

Scaffolding for new projects.

<!--}}}-->

<!--{{{-->
---
title: Yeoman
subtitle: Grunt
build_lists: true

Build from source; the equivilant of a `Makefile`.

[Grunt](http://gruntjs.com/)

- compile
- uglify
- livereload
- some sort of shell command
- TJ hates them :(

<footer class="source"><a href="http://www.youtube.com/watch?v=f7AU2Ozu8eo#watch-discussion">+Tj Holowaychuk</a></footer>

<!--}}}-->

<!--{{{-->
---
title: Yeoman
subtitle: Bower

Frontend dependency manager.

<!--}}}-->

<!--{{{-->
---
title: The browser
subtitle: Dev tools
build_lists: true

Chrome and Firefox:  
Almost better at debugging than your fancy IDE

- Change stuff
- Console
- All sorts of good stuff
- Firefox has improved

<!--}}}-->

<!--Yeoman}}}-->

