#ABOUT VERSION 0.37.0
With version 0.37.0 SafetyNet for Android API is added into PoGo. This (now) prevents any XPosed modules from working. This also prevents PoGo from working on rooted device. Since my device is rooted, I cannot play PoGo, let alone do and test any hacks.

Because I cannot play PoGo I have no interest in working on this anymore. May be in a day, may be in a week, or in a year, workaround will be found. Then I will see. You will see status update here, if I do.

It was really nice to tag along with other developers, work with users and learn new stuff.

If ever anyone from Niantic is reading this - it was best cat-and-mouse game, from day one. Your team is pros, and make great things. Bad that you ended it in kick-in-balls fashion. Breaking our little hacks is one thing, preventing us playing it is entirely different.

#Pokemon GO (c) direct Man-in-the-Middle
![pokemon](https://img.shields.io/badge/Pokemon%20GO-0.35.0-blue.svg?style=flat-square")
![license](https://img.shields.io/github/license/ELynx/pokemon-go-xposed-mitm.svg)

Consider module field-tested with 0.35.0.
##Pre-build version
You can download prebuilt version from [XPosed repository](http://repo.xposed.info/module/com.elynx.pogoxmitm).

<b>Make sure that both module and PoGo have Storage Permissions</b>. App uses them to store settings, PoGo - to read them. If you experience crashes of UI, or PoGo app at start, first check permissions. If it still crashes, please provide feedback via Issues.

<b>IV output format</b> is "Grade Perfection% Attack Defense Stamina Level". Grade is A for 100 to 91 perfection, B for 90 to 81 and so on. With grade, you can sort pokemons A-Z to have best first, then good, then worse etc.

All hacks implemented now don't modify data sent to Niantic servers, only examine it. They modify data going back, to add gist to it.
This hack don't do additional request, so it does not overload Niantic servser. No 'data scraping'.

I had not heard/read about bans for this or similar modules. If I ever know of such, I will inform users wherever I can and pause distribution.

##Brief
Uses XPosed framework to intercept web communications of app and process out- and inbound packages.

Internally use [POGOProtos](https://github.com/AeonLucid/POGOProtos). See root build.gradle for instructions and build tasks.

##What it can do now
Intercept packages going from client to server; all without breaking actual communications.

Intercept packages going from server to client, too.

###Branch right-now, as released on XPosed repo
Simple hack to put IVs into pokemon nickname.

Simple hack to put remaining lure time into pokestop description.

Export pokemon data including IV's and attacks to tsv file located in external storage at `Pokemon/PokemonData.tsv`.
It is done each time the application starts. You can see toast message with confirmation during loading screen.
The data can be later used for calculations. For example, like in the [Pokemon Evolution Calculator](https://docs.google.com/spreadsheets/d/1vlEsToajcid9KTkLzgqZCpji8bDVEpMM6GQ8SqNL4-k/edit?usp=sharing)

UI for turning hacks on and off.

##What is planned
Grandeur plan - use JRuby to allow different data modifications without recompilation.

##Current state
Master branch is undergoing changes related to adding Ruby script execution. Unstable development is in branch jruby.

Code for XPosed repo release is in branch right-now.

##Resources and projects used
* [POGOProtos](https://github.com/AeonLucid/POGOProtos) by [Mike](https://github.com/AeonLucid)
* [Launcher icon generator](https://romannurik.github.io/AndroidAssetStudio/index.html) by [Roman Nurik](https://github.com/romannurik)
* [Pokeball icon set](http://tamarinfrog.deviantart.com/art/All-Poke-Balls-Free-Icons-368996730) by [TamarinFrog](http://tamarinfrog.deviantart.com/)
* [Xposed module for Jodel](https://github.com/krokofant/JodelXposed) by [krokofant](https://github.com/krokofant/JodelXposed)
