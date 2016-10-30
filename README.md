# TabbedView
A Quark for the SuperCollider porgramming Language

deprecated. Please use TabbedView2 instead.
an array of CompositeViews (or ScrollViews) with tabs for switching



## <a class="anchor" name="description">Description</a>

There are extensive explanations in the [Examples](#Examples) section on how to use TabbedView with its many configuration options .

### <a class="anchor" name="Author">Author</a>

by Jost Muxfeldt, OCT 09, 2012 version 1.29\. [Change History](#Change History) at bottom.

<div class="warning"><span class="warninglabel">WARNING:</span> TabbedView is maintained only for backward compatabiity!. Please use [TabbedView2](./../Classes/TabbedView2.html) for new code. (you may have to activate the TabbedView2 Quark).</div>

## <a class="anchor" name="classmethods">Class Methods</a>

### <span class="methprefix">*</span>[new](./../Overviews/Methods.html#new) (<span class="argstr">parent</span>, <span class="argstr">bounds</span>, <span class="argstr">labels</span>, <span class="argstr">colors</span>, <span class="argstr">name: " "</span>, <span class="argstr">scroll: false</span>)

<div class="method">

create a Tabbed View

#### Arguments:

| parent | 

a parent view. if nil, then a new window is created

 |
| bounds | 

Rect . if nil then the parent Rect is used

 |
| labels | 

an array of strings. determines how many tabs there are. default ["tab1", "tab2", "tab3"]

 |
| colors | 

an array of colors. if the array is smaller than the amount of labels, the color series repeats. For convenience, a color scheme is automatically created using these colors. You cannot use gradients here, because the tabs are drawn with Pen. Gradients only work with background_; Custom color schemes and shapes can be controlled with instance variables or with the *new variations below.

 |
| name | 

a name for the window if a new window is created (view==nil) -- default " "

 |
| scroll | 

boolean defaults to false. It substitutes the CompositeView with a ScrollView.

 |

#### Returns:

<div class="returnvalue">

returns a TabbedView

</div>

</div>

### <span class="methprefix">*</span>[newPacked](./../Overviews/Methods.html#newPacked) (<span class="argstr">parent</span>, <span class="argstr">bounds</span>, <span class="argstr">labels</span>, <span class="argstr">colors</span>, <span class="argstr">name: " "</span>, <span class="argstr">scroll: false</span>)

<div class="method">

create a very space efficient TabbedView

</div>

### <span class="methprefix">*</span>[newFlat](./../Overviews/Methods.html#newFlat) (<span class="argstr">parent</span>, <span class="argstr">bounds</span>, <span class="argstr">labels</span>, <span class="argstr">colors</span>, <span class="argstr">name: " "</span>, <span class="argstr">scroll: false</span>)

<div class="method">

create a flat TabbedView

</div>

### <span class="methprefix">*</span>[newTall](./../Overviews/Methods.html#newTall) (<span class="argstr">parent</span>, <span class="argstr">bounds</span>, <span class="argstr">labels</span>, <span class="argstr">colors</span>, <span class="argstr">name: " "</span>, <span class="argstr">scroll: false</span>)

<div class="method">

create a tall TabbedView

</div>

### <span class="methprefix">*</span>[newColor](./../Overviews/Methods.html#newColor) (<span class="argstr">parent</span>, <span class="argstr">bounds</span>, <span class="argstr">labels</span>, <span class="argstr">colors</span>, <span class="argstr">name: " "</span>, <span class="argstr">scroll: false</span>)

<div class="method">

create a Tabbed View with rgb tabs

</div>

### <span class="methprefix">*</span>[newColorLabels](./../Overviews/Methods.html#newColorLabels) (<span class="argstr">parent</span>, <span class="argstr">bounds</span>, <span class="argstr">labels</span>, <span class="argstr">colors</span>, <span class="argstr">name: " "</span>, <span class="argstr">scroll: false</span>)

<div class="method">

create a Tabbed View with rgb labels

</div>

### <span class="methprefix">*</span>[newBasic](./../Overviews/Methods.html#newBasic) (<span class="argstr">parent</span>, <span class="argstr">bounds</span>, <span class="argstr">labels</span>, <span class="argstr">colors</span>, <span class="argstr">name: " "</span>, <span class="argstr">scroll: false</span>)

<div class="method">

create a very basic TabbedView

</div>

### <span class="methprefix">*</span>[newTransparent](./../Overviews/Methods.html#newTransparent) (<span class="argstr">parent</span>, <span class="argstr">bounds</span>, <span class="argstr">labels</span>, <span class="argstr">colors</span>, <span class="argstr">name: " "</span>, <span class="argstr">scroll: false</span>)

<div class="method">

create a transparent TabbedView

</div>

### <span class="methprefix">*</span>[newRGB](./../Overviews/Methods.html#newRGB): METHOD NOT FOUND!

<div class="method">

deprecated, use newColor

</div>

### <span class="methprefix">*</span>[newRGBLabels](./../Overviews/Methods.html#newRGBLabels): METHOD NOT FOUND!

<div class="method">

deprecated, use newColorLabels

</div>

### <a class="anchor" name="Inherited class methods">Inherited class methods</a>

### <a class="anchor" name="Undocumented class methods">Undocumented class methods</a>

### <span class="methprefix">*</span>[newIDEdefault](./../Overviews/Methods.html#newIDEdefault) (<span class="argstr">w</span>, <span class="argstr">bounds</span>)

<div class="extmethod">From extension in [/Users/fuo/Documents/SC3_IDE/QT_only/SystemOverwrites//Overrides.sc](file:///Users/fuo/Documents/SC3_IDE/QT_only/SystemOverwrites//Overrides.sc)</div>

## <a class="anchor" name="instancemethods">Instance Methods</a>

### <span class="methprefix">-</span>[view](./../Overviews/Methods.html#view)

<div class="method">

#### Returns:

<div class="returnvalue">

the container for all the views

</div>

</div>

### <span class="methprefix">-</span>[views](./../Overviews/Methods.html#views)

<div class="method">

#### Returns:

<div class="returnvalue">

an array of Composite/Scroll Views

</div>

</div>

### <span class="methprefix">-</span>[add](./../Overviews/Methods.html#add) (<span class="argstr">label</span>, <span class="argstr">index</span>)

<div class="method">

adds a tab with label

#### Arguments:

| label | 

string, the label

 |
| index | 

int, (optional) the index at which the tab is inserted (if nil, add to the end)

 |

#### Returns:

<div class="returnvalue">

the tab container that was added

</div>

</div>

### <span class="methprefix">-</span>[insert](./../Overviews/Methods.html#insert) (<span class="argstr">index</span>, <span class="argstr">label</span>)

<div class="method">

inserts a tab at index with label string

#### Arguments:

| index | 

the index at which the tab is inserted

 |
| label | 

(describe argument here)

 |

#### Returns:

<div class="returnvalue">

the tab container that was added

</div>

</div>

### <span class="methprefix">-</span>[removeAt](./../Overviews/Methods.html#removeAt) (<span class="argstr">index</span>)

<div class="method">

remove tab at Index

#### Arguments:

| index | 

the index of the tab to be removed

 |

</div>

### <span class="methprefix">-</span>[focus](./../Overviews/Methods.html#focus) (<span class="argstr">index</span>)

<div class="method">

selects one of the tabs

#### Arguments:

| index | 

int, the index to focus

 |

</div>

### <span class="methprefix">-</span>[activeTab](./../Overviews/Methods.html#activeTab)

<div class="method">

#### Returns:

<div class="returnvalue">

returns the index of the focused tab

</div>

</div>

### <span class="methprefix">-</span>[focusActions](./../Overviews/Methods.html#focusActions)

### <span class="methprefix">-</span>[focusActions](./../Overviews/Methods.html#focusActions) = value

<div class="method">

#### Arguments:

| (value) | 

an Array of user onFocus functions.

 |

#### Returns:

<div class="returnvalue">

an Array of user onFocus functions.

</div>

</div>

### <span class="methprefix">-</span>[unfocusActions](./../Overviews/Methods.html#unfocusActions)

### <span class="methprefix">-</span>[unfocusActions](./../Overviews/Methods.html#unfocusActions) = value

<div class="method">

#### Arguments:

| (value) | 

an Array of user onUnfocus functions.

 |

#### Returns:

<div class="returnvalue">

an Array of user onUnfocus functions.

</div>

</div>

### <span class="methprefix">-</span>[tabPosition](./../Overviews/Methods.html#tabPosition)

### <span class="methprefix">-</span>[tabPosition](./../Overviews/Methods.html#tabPosition) = <span class="argstr">symbol</span>

<div class="method">

#### Arguments:

| symbol | 

\left, \top, \right, or \bottom.

 |

</div>

### <span class="methprefix">-</span>[followEdges](./../Overviews/Methods.html#followEdges)

### <span class="methprefix">-</span>[followEdges](./../Overviews/Methods.html#followEdges) = <span class="argstr">bool</span>

<div class="method">

Set tabs parallel or perpendicular to container edges.

#### Arguments:

| bool | 

default true. (Set tabs parallel)

 |

</div>

### <span class="methprefix">-</span>[resize](./../Overviews/Methods.html#resize)

### <span class="methprefix">-</span>[resize](./../Overviews/Methods.html#resize) = <span class="argstr">int</span>

<div class="method">

sets the resize flag (1-9 ). see [Resize behaviour](./../Reference/Resize.html)

#### Arguments:

| int | 

default 1

 |

</div>

### <span class="methprefix">-</span>[labelColors](./../Overviews/Methods.html#labelColors)

### <span class="methprefix">-</span>[labelColors](./../Overviews/Methods.html#labelColors) = <span class="argstr">colorArray</span>

<div class="method">

set the label colors

#### Arguments:

| colorArray | 

Array of Colors for the tabs.

 |

</div>

### <span class="methprefix">-</span>[unfocusedColors](./../Overviews/Methods.html#unfocusedColors)

### <span class="methprefix">-</span>[unfocusedColors](./../Overviews/Methods.html#unfocusedColors) = <span class="argstr">colorArray</span>

<div class="method">

set the unfocusedColors colors

#### Arguments:

| colorArray | 

Array of Colors for the unfocused tabs

 |

</div>

### <span class="methprefix">-</span>[focusFrameColor](./../Overviews/Methods.html#focusFrameColor)

### <span class="methprefix">-</span>[focusFrameColor](./../Overviews/Methods.html#focusFrameColor) = <span class="argstr">color</span>

<div class="method">

set the focusFrameColor

#### Arguments:

| color | 

Array of Colors for the unfocused tabs Color of the focus frame of the tabs. Cocoa only

 |

</div>

### <span class="methprefix">-</span>[unfocusTabs](./../Overviews/Methods.html#unfocusTabs)

### <span class="methprefix">-</span>[unfocusTabs](./../Overviews/Methods.html#unfocusTabs) = value

<div class="method">

Unfocuses the UserView which draws the tabs after a tab is clicked. Defaut on Cocoa or QT is false, otherwise true. (because Swing can't hide focus frames);

</div>

### <span class="methprefix">-</span>[backgrounds](./../Overviews/Methods.html#backgrounds)

### <span class="methprefix">-</span>[backgrounds](./../Overviews/Methods.html#backgrounds) = <span class="argstr">colorArray</span>

<div class="method">

#### Arguments:

| colorArray | 

Array of Colors for the CompositeViews

 |

</div>

### <span class="methprefix">-</span>[stringColor](./../Overviews/Methods.html#stringColor)

### <span class="methprefix">-</span>[stringColor](./../Overviews/Methods.html#stringColor) = <span class="argstr">color</span>

<div class="method">

#### Arguments:

| color | 

a Color

 |

</div>

### <span class="methprefix">-</span>[stringFocusedColor](./../Overviews/Methods.html#stringFocusedColor)

### <span class="methprefix">-</span>[stringFocusedColor](./../Overviews/Methods.html#stringFocusedColor) = <span class="argstr">color</span>

<div class="method">

#### Arguments:

| color | 

a Color

 |

</div>

### <span class="methprefix">-</span>[labelPadding](./../Overviews/Methods.html#labelPadding)

### <span class="methprefix">-</span>[labelPadding](./../Overviews/Methods.html#labelPadding) = <span class="argstr">int</span>

<div class="method">

#### Arguments:

| int | 

if autosizing is on, then this determines left and right padding from th label text

 |

</div>

### <span class="methprefix">-</span>[tabWidth](./../Overviews/Methods.html#tabWidth)

### <span class="methprefix">-</span>[tabWidth](./../Overviews/Methods.html#tabWidth) = <span class="argstr">int</span>

<div class="method">

#### Arguments:

| int | 

int or \auto ; a fixed tab width, or "auto" for automatic tab width (default "auto", unless using themes)

 |

</div>

### <span class="methprefix">-</span>[tabHeight](./../Overviews/Methods.html#tabHeight)

### <span class="methprefix">-</span>[tabHeight](./../Overviews/Methods.html#tabHeight) = <span class="argstr">val</span>

<div class="method">

#### Arguments:

| int | 

int or \auto ; a fixed tab height, or "auto" for automatic tab height (default "auto", unless using themes)

 |

</div>

### <span class="methprefix">-</span>[tabCurve](./../Overviews/Methods.html#tabCurve)

### <span class="methprefix">-</span>[tabCurve](./../Overviews/Methods.html#tabCurve) = <span class="argstr">int</span>

<div class="method">

#### Arguments:

| int | 

the radius in pixels of the rounded tab corners

 |

</div>

### <span class="methprefix">-</span>[swingFactor](./../Overviews/Methods.html#swingFactor)

### <span class="methprefix">-</span>[swingFactor](./../Overviews/Methods.html#swingFactor) = value

<div class="method">

#### Arguments:

| (point) | 

Point ; a multiplication factor for a string/tab width for GUI.swing only. default Point(0.52146,1.25)

 |

</div>

### <span class="methprefix">-</span>[font](./../Overviews/Methods.html#font)

### <span class="methprefix">-</span>[font](./../Overviews/Methods.html#font) = <span class="argstr">fnt</span>

<div class="method">

(describe method here)

#### Arguments:

| fnt | 

(describe argument here)

 |

#### Returns:

<div class="returnvalue">

(describe returnvalue here)

</div>

</div>

### <span class="methprefix">-</span>[doActions](./../Overviews/Methods.html#doActions)

<div class="method">

do the actions of the current tab

</div>

### <a class="anchor" name="Inherited instance methods">Inherited instance methods</a>

## <a class="anchor" name="examples">Examples</a>

**Usage:**

**use CompositeView style GUI**

<pre class="code prettyprint lang-sc">(
t=TabbedView(name:"** this is a mock preferences pane **");

ActionButton(t.views[0],"go to next tab ",{t.focus(1)}).bounds_(Rect(50,50,200,100));
)</pre>

**use FlowView style GUI**

<pre class="code prettyprint lang-sc">(
t=TabbedView(); // use Flow Style

    t.views[0].flow({|w| 
        GUI.button.new(w,Rect(50,50,250,50))
        .states_([["control the tab with method 'focus' -->"]]).action_({t.focus(1)})
    });

    t.views[1].flow({|w| 
        GUI.button.new(w,Rect(50,50,200,100))
        .states_([["go to last tab"]]).action_({t.focus(2)})
    });

)</pre>

**quick styling with variations on *new:**(There are some color differences for swing)

<pre class="code prettyprint lang-sc">TabbedView.newBasic

TabbedView.newColor

TabbedView.newColorLabels

TabbedView.newFlat

TabbedView.newTall

TabbedView.newTransparent

TabbedView.newPacked(nil,nil,Array.fill(20,{|i| i.asString})); //very good for tons of tabs :</pre>

**set tabPosition and followEdges:**live switching adjusts positions of contents if you use .flow .

<pre class="code prettyprint lang-sc">(
v=TabbedView.newColorLabels(nil,nil,Array.fill(5,{arg i; var q="aa"; i.do{q=q++"a"}; q })); //default
v.views[0].flow({arg w;
    ActionButton(w,"tabs top",{v.tabPosition_(\top)},300,50);
    w.startRow;
    ActionButton(w,"tabs left",{v.tabPosition_(\left)},148,50);
    ActionButton(w,"tabs right",{v.tabPosition_(\right)},148,50);
    w.startRow;
    ActionButton(w,"tabs bottom",{v.tabPosition_(\bottom)},300,50);

    GUI.button.new(w,300@50)
        .states_([["set followEdges=false",Color.black,Color.red.alpha_(0.2)],
            ["set followEdges=true",Color.black,Color.green.alpha_(0.2)]])
        .action_({arg b;(b.value==1).if{v.followEdges_(false)}{v.followEdges_(true)};});
});

)

TabbedView.newColorLabels(nil,nil,Array.fill(25,{|i| "tab"++i.asString})).tabPosition_(\right).followEdges_(false);

TabbedView.newTall(nil,nil,Array.fill(5,{|i| "tab"++i.asString})).tabPosition_(\left);

TabbedView.newTall(nil,Rect(100,500,400,100),Array.fill(5,{|i| "tab"++i.asString})).tabPosition_(\bottom);</pre>

**Drag objects from one tab to another (under cocoa and qt only at the moment):**

<pre class="code prettyprint lang-sc">(
v=TabbedView.newColorLabels;
n = GUI.dragSource.new(v.views[0], Rect(50, 50, 140, 24));
            n.object = "Drag me to Tab2";
 GUI.textView.new (v.views[1], Rect(50, 50, 140, 80));
)</pre>

**add, removeAt, insert tabs**

defaults on *new, but other thems use fixedwidths:

<pre class="code prettyprint lang-sc">v=TabbedView.newColor

v.add("I am last")

v.insert(2,"squeeze me in")

v.removeAt(2)

resize_()

( 
w=GUI.window.new.front;
v=TabbedView.newColorLabels(w,Rect(40,40,280,280),Array.fill(12,{|i| "tab"++i.asString})).tabPosition_(\right).followEdges_(false);
v.resize_(5);
GUI.slider.new(v.views[0],Rect(10,80,200,30)).resize_(2);
)</pre>

**nest TabbedViews & use scrolling**

uses scroll:true in the inner tab

<pre class="code prettyprint lang-sc">(
v=TabbedView.newPacked(nil,Rect(200,200,600,400).insetBy(20,20),["1","2","3"])
        .tabHeight_(40).tabPosition_(\right).followEdges_(false);

q=TabbedView.newColorLabels(v.views[0],nil,["tab1.1","tab1.2","tab1.3"], scroll: true)
        .tabPosition_(\right).resize_(5).followEdges_(false);

q.views[0].flow({ arg w;
    78.do({ arg i;
        b = Button(w, Rect(rrand(20,300),rrand(20,300), 75, 24));
        b.states = [["Start "++i, Color.black, Color.rand],
        ["Stop "++i, Color.white, Color.red]];
    });
});
GUI.slider.new(q.views[1],q.views[1].bounds.insetBy(50,50));
)</pre>

**user functions: focus and unfocus**

turn on/off scopes , e.g.

<pre class="code prettyprint lang-sc">( 
v=TabbedView.new();
v.focusActions[1]={"tab2 is focused".postln};
v.unfocusActions[1]={"tab2 just unfocused".postln};
)</pre>

**focusFrameColor_(color) and unfocusTabs_(bool)**The tabs are drawn with user view which have a clear focus frame on Cocoa. On Swing, the frame cannot be made clear, so by default the tabs are unfocused after clicking. You can change this if it interferes with your tabbing scheme.

<pre class="code prettyprint lang-sc">( 
v=TabbedView.new();

v.unfocusTabs_(false);  // default is false on Cocoa, true otherwise;
v.focusFrameColor_(Color.red); //cocoa only

)</pre>

**default autosizing tabs**

defaults to auto on *new, but other themes use fixedwidths:

<pre class="code prettyprint lang-sc">(
TabbedView.new(nil,Rect(150,100,400,500),["1","two","threeeeeeeeeeee","four","5"]); 
)

(
v=TabbedView.newFlat(nil,Rect(150,100,400,300),["1","two","threeeeeeeeeee","four","5"]); 
v.tabWidth_(\auto);
)</pre>

**fixed tab sizes**

<pre class="code prettyprint lang-sc">(
TabbedView(nil,nil,["1","two","three","four","5"]).tabWidth_(70);  
)</pre>

**set font**

Swing fonts only work within certain limits for now. use swingFactor_ to adjust the conversion.

<pre class="code prettyprint lang-sc">(
v=TabbedView.newBasic.font_(GUI.font.new("Monaco",9)).tabHeight_(18);

)
(
v=TabbedView.newBasic.font_(GUI.font.new("Monaco",36));

)

(
v=TabbedView.newBasic.font_(GUI.font.new("Helvetica",14)).tabHeight_(\auto);

)

(
v=TabbedView.newTall.font_(GUI.font.new("Helvetica",18)).tabPosition_(\left);

)
(
v=TabbedView.newTall.font_(GUI.font.new("Helvetica",36)).tabHeight_(\auto).tabWidth_(\auto);

)</pre>

**Set colors with an argument to .new**Colors can wrap around if there are less than there are labels. Unfocused colors are calculated automatically.

<pre class="code prettyprint lang-sc">(
v=TabbedView(nil,nil,Array.fill(8,{|i| i.asString}),
    [Color.rand,Color.rand,Color.rand]);
    //Colors can wrap around 
)</pre>

**Set colors very specifically to your own taste using set methods**

<pre class="code prettyprint lang-sc">(
v=TabbedView.new(nil,nil,["one","two","three"]); 
    //Colors can wrap around 
v.labelColors_([Color.rand,Color.rand,Color.rand]);
)

(
v=TabbedView.new(nil,nil,["one","two","three"]); 
v.labelColors_([Color.red,Color.blue,Color.yellow]);
v.unfocusedColors_([Color.red.alpha_(0.1),Color.blue.alpha_(0.1),Color.yellow.alpha_(0.1)]);
v.backgrounds_([Color.red.alpha_(0.1),Color.blue.alpha_(0.1),Color.yellow.alpha_(0.1)]);
)</pre>

**adjust padding and curves for small autowidth**

labelPadding only has an effect on autowidth

<pre class="code prettyprint lang-sc">(
v=TabbedView(nil,nil,Array.fill(20,{|i| i.asString}));
v.labelPadding_(8);      //tighter padding
v.tabCurve_(3);           //sharper curves
v.stringColor_(Color.black);
v.backgrounds_([Color.white.alpha_(0.3)]);
)

// or simply use *newPacked:

(
v=TabbedView.newPacked(nil,nil,Array.fill(20,{|i| i.asString}));
)</pre>

**adjust tab height and curves**

<pre class="code prettyprint lang-sc">// super flat and elegant

(
v=TabbedView(nil,nil,["1","two","three","four","5"]).tabWidth_(70).tabHeight_(13).tabCurve_(3); 
)

// super tall and clear

(
TabbedView(nil,nil,["1","two","three","four","5"]).tabWidth_(70).tabHeight_(30).tabCurve_(3); 
)</pre>

## <a class="anchor" name="Change History">Change History</a>

*   Aug 27, 2007 : code optimized; instanceVar tabPosition. Version 1.0;
*   Aug 24, 2007 : small code optimizations Version 1.01;
*   Aug 23, 2007 : fixed small bug when bounds=nil Version 1.02;
*   Aug 30, 2007 : added scroll option. Convenience new methods can now take arguments of form arg:value Version 1.03;
*   Sep 2, 2007 : FlowView contents will now reposition in real time if tab position is changed. tabPosition getter. Version 1.04; Tabs can switch during drags(cocoa only);
*   Feb 12, 2008 : relativeOrigin variable added to adjust to new SCCompositeView behavior. Swing compatibility. Version 1.10;
*   Feb 16, 2008 : Version 1.11; Swing themes adjusted to use no transparency. deprecated: newRGB and newRGBLabels ; use new methods: newColor and newColorLabels instead. swingFactor defaults to 7 (integers work better than floats,
*   Feb 19, 2008 : Version 1.12; focus_() deprecated; use focus(index) instead. focused added.
*   Feb 19, 2008 : Version 1.13; focused removed and changed to activeTab. All variables that had a double s in "focussed", changed to singel s;
*   Feb 20, 2008 : Version 1.14; Fixed returned tab on add and insert methods
*   Feb 20, 2008 : Version 1.15; added font variable. other bug fixes
*   Feb 26, 2008 : Version 1.20; added followEdges option.
*   July 09, 2008 : Version 1.21; updates for SC3.21
*   Dec 15, 2008 : Version 1.22; changed swing font calculation
*   Dec 19, 2008 : Version 1.23; changed swing font calculation
*   Jan 28, 2008 : Version 1.24; fixed loop bug (thanks Fredrik Olofsson) . relativeOrigin deprecated (always use r/o)
*   Jun 11, 2009 : Version 1.25; removed all calls to relativeOrigin. focusFrameColor_(color) and unfocusTabs_(bool). arg w changed to parent
*   July 15, 2009: Version 1.26; GUI context change bug fixed (thanks to sciss). Font calculations put in an AppClock.
*   July 26, 2009: Version 1.27; removed AppClock and returned to factored font calculation for swing. AppClock causes flow layout problems
*   Aug 01, 2009: Version 1.28; small fix to Help file
*   Oct 09, 2012: Version 1.29; Removed deprecated methods. QT support. SCDoc Support.

<div class="doclink">source: [/Users/fuo/Library/Application Support/SuperCollider/downloaded-quarks/TabbedView/HelpSource/Classes/TabbedView.schelp](file:///Users/fuo/Library/Application Support/SuperCollider/downloaded-quarks/TabbedView/HelpSource/Classes/TabbedView.schelp)
link::Classes/TabbedView::
sc version: 3.7.2</div>

</div>