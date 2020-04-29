# self_taught_good_flutter_practices



remember dont just blindly pass context..
for eg here u passed model.of method directly to MyHomePage widget who is a child of material app so in that context inhertied widget doesnt exits/...its below tht.class

Use const to build your widgets
Without const, selective rebuilding of the sub-tree does not happen. Flutter creates a new instance of each widget in the sub-tree and calls build() wasting precious cycles especially if your build methods are heavy.


keep inherited widgests small : use different inherited widgerst for diff purposes...users students etc...


!!!!!!Page-scoped widgets cannot cross route boundary!!!!!!!!!!1 remember this everytime u r creating routes.!!!!!


keeping inhgerited widgest at the top can cost security...be carefull


in providers use proxyprovider for already initisialezd models...


while using scoped models:
--> remember to use abstract classes to make multiple models eg
```
class Counter Extends Model{
int count=0;
abstract class CountAdd extends Counter{
//void incrementfunc()..
}}
 &&finally add 
class BundledClass extends Model with Counter,CountAdd{};
refer this in SCOPEDpacakge use





```

use slivers for beautiful designs

also wrap scaffold body or scaffold in safeArea
