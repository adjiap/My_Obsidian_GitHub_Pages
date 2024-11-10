---
created on: 2024-10-29
last modified on: 2024-10-29
aliases:
  - Insights on Solo Game Development
tags:
  - softwaredevelopment
  - developmentlifecycle
  - gamedevelopment
  - productdevelopment
---

---
# Quick Start for Solo Game Dev 
First things, first. Game development is hard. It's figuratively really not for the weak. You'll have long days and long nights to create the game, and you also likely do not get as quick of a feedback that you want or need. Which is why, it's best as well as a (solo) game dev, you should have an accountability partner to bounce ideas, to validate concepts, or to keep you motivated[^3]
## Step 1 - Make a Game Design Document
> [!note]
> Ideally, this only happens in the first two months (e.g. January and February)

Then, firstly, you need to make a so-called [[Game Design Document]] which will serve as your north star, on what you're going to do. Ask yourself the following questions:
![[Game Design Document#Questions to ask for GDD[ 2]|GDD]]

> [!tip] Tip for solo game developers
> You're likely be *really* good at one aspect of game dev, like design, or programming or story telling. Try to focus on one thing, and don't sweat about the rest. As an example, if you're good at art design, don't make complicated game mechanics, and just use a light story.

## Step 1.5 - If you're already experienced, you can skim through Step 1[^3]
Instead, you can focus more on designing for:
- Proper UI
- Better SFX
- Good Music
- Compelling Narrative
- Localization
- Prepare for multiple platforms
- Handling playtest, demo feedback
## Step 2 - Prototype the game
> [!note]
> Ideally, this only happens in the first two months (e.g. January and February)

When prototyping, this is where you want to [[verify]] that the core mechanics and concepts that you want to have can be done, make sense to work with each other, and would also **FUN** to play with. You can however build some codebase/common library to use.

> [!danger] 
> DO NOT build anything with complicated **art** and **details**.
> DO NOT build with **scale** in mind

> [!hint]
> DO build "building blocks" for later usage. [^4]
> Scope creep could happen if you don't know what would happen next. Try to make things as simple as possible

It's best to **not think** about the scale, nor **the art** or **the details**, or to even think about **reusing assets or code**. It's likely better if you just **throw everything** out of the window afterwards. [^2]
## Step 3 - Develop and test the game
> [!note]
> This happens after pre-production is settled, and this ideally happens for the next 7 months (March till September). 

Based on the building blocks that you have made during [[prototyping]], you now build things to create "valuable" features and adding content. The switch between Step 2 and Step 3 for Solo developer will be REALLY hard.
## Step 4 - Market the game[^7]

> [!note] 
> Ideally, some marketing will already be done in the 4th month (April) for gathering people for playtests, and then a more comprehensive marketing in the 7th month (July)

We will need to put up good screenshots, a video of the gameplay, or do a trailer of the game. Maybe write some articles, get some feedback on people and even do some advertisement.
April: Ideally we make first screenshots or some movements of gifs of the game that can then be put on the Steam page to generate interest (but NOT) that we want to get wishlisted
July: By this point, we should have already a good-enough demo and the marketing goal is for it to be wishlisted as much as possible, as that will help during the release, and also get Steam's algorithm to get us be recommended as well.
## Step 5 - Publish the game

> [!note]
> Ideally this will happen in the 10th month, October

And this is where we finally release the game into the public, basically putting it on Steam, and have people buy and download it for them to play.
## Step 6 - Maintain the game

> [!note]
> Ideally, from November till December, is where you will do the bug fixings

Now that the game is out, there will now come a lot of feedback from the general public. The next 2 months after the release is then will be doing bugfixing. After awhile, it's then time for you to just let go of the game, and begin the cycle anew :) 

# General Tips / Summary for Solo Dev  [^3] [^4]
## At the beginning
- Just like any software projects, **requirement is key**, which means that we need to be sure what kind of mechanics we need to have in the game, before we even start coding anything.
	- A tip for this, is to do some kind of "game jam" to have your core game concepts first
- A rule of thumb on making a game make something that‘s within your interest, choose a specific scope you want to have and reign in adding too many stuff/feature (scope creep). Then make a timeframe, and finally choose the worst case scenario with the timing
- If this is your first game, with a dev time of 2 months, you can forget about architecture and just create something. It's okay to just make a "shitty game", if you're just aiming for it for learning.
- Set right expectations, do a prototype and programming for 2 weeks to familiarise yourself with the toolset. Try to not use asset packs, and the first goal is to learn.
- Do a prototype game to see how it's supposed to work, to see if things actually work as it should. -> Fail fast, and then make a more scalable approach
- Getting started, it's helpful to have a class diagram. But it **doesn't** have to be that way. Only make the [[Types of UML Diagram can be divided into two, Structural Diagrams and Behavioral Diagrams|UML]] [[Types of UML Diagram can be divided into two, Structural Diagrams and Behavioral Diagrams#Class Diagram|Class Diagram]]  when: 
	- You don't understand what's going on during coding or game structure, OR 
	- You work in a medium to large team (8 to15 People), OR 
	- You constantly need to onboard new people
- The 3 best game types to start with if you have no experience in game devs would be[^6]:
	1. Platformer (like Super Mario)
	2. Puzzle games (like Portal)
	3. Metroidvania (like Hollow Knight)
## Once you have some hours in
- You could have already "wasted" hours in because you didn't know, so here is where it's best to better plan for both Prototyping and Production
- If your game has to be very polished from the very start, then unfortunately that's the focus of the game. Something like Undertale, which notoriously has a 1000 LOC of if statements, still works, because gamers would just need to pass it once, and technically it's already scalable just like that.
- Remember the pareto principle to figure out what‘s most important. In General, this is what‘s going to focus your attention and work. Don‘t be afraid to outsource some stuff so you can focus on what‘s important to save time and frustration
- Don't depend on internal motivation. Best to have a schedule, just like building any habits, or having an accountability partner
- Code Refactoring might just not happen at all if the entire code is unfortunately bad. This is where code rewriting unfortunately happens. This often happens especially if you're new to the language or the framework.
- Think about the scale of the game
- Visuals do matter. It doesn't have to be as polished as Horizon Zero Dawn, but the least you need is **consistent art direction**
	- Use custom shaders that can make that "polished" look faster.
## At the end
- You also (unfortunately) need to do some marketing. If people don't know that your game exists, how can you be sure that it is even good?
## Game Architecture tips
- Once you create the modules, you also have to figure out whether or not they can or will talk to each other. -> likely we need to have Interfaces if that's what you need. [[Interface Segregation Principle]]
- Fundamental rules in the game that belong in architecture should be specific "enough", but should also be open to addition ([[Open-Closed Principle]])
- Split the games into modules, where you have a folder that is used for Taverns, so anything that's involved with the mechanics of the tavern would be put in the tavern folder, and have a `Tavern` prefix. This would then hold the `TavernManager` class, and anything under it should be under the same folder. ([[Single Responsibility Principle]])
- Learn to organize your code, by reading the book, Game Programming Patterns by Robert Nystrom

> [!quote] Game Programming Patterns p. 14 -  Robert Nystrom
> It’s less about writing code than it is about organizing it. Every program has some organization, even if it’s just *“jam the whole thing into `main()` and see what happens”*, so I think it’s more interesting to talk about what makes for good organization. How do we tell a good architecture from a bad one?

## Choosing a game engine [^2]
The best way to choose, is to actually try the game engines, and see which one do you like the most. But if you have no idea, then there are 5 things for you to decide, before you can more confidently choose a game engine. 
1. The features that they give
   Unity has the most resources, followed by Unreal, then Godot
2. The pricing structure (**Look here if you're building in a team!**)
3. The programming language
   Unity is with C#, Unreal is C++ (although Visual Scripting with Blueprint is supported), Godot has GDScript (similar to Python) 
4. The community
5. The type of game you want to make.  
   ![[images/Game_Engines_Based_on_Games_you_Make.png|700]]

> [!tip] Tips for Unity
> - Apply Fast Script Reload asset to make opening projects and compiling faster
> - Choose the [[graphics pipeline]] WISELY, it will be difficult for you to switch afterwards. (Choices are: universal render pipeline, high definition render pipeline, built-in)

### Diagrams of game engines with their export options
![[images/Diagrams_of_game_engines_and_their_export_options.png]]
## Planning Tips to avoid being stuck in Prototyping and Production [^5]

> [!note]
> This is pretty much a problem that most **Solo** developer will face, so these tips would hopefully help avoid it.

> [!warning] Symptoms of being stuck in Prototyping
> - This would mean that you perhaps had overplanned
> - Also means that you might be getting no feedback
> - This can also feel like you're prototyping forever

> [!warning] Symptoms of being stuck in Production
> - There are no deadlines for things
> - You basically just polish infinitely
> - You feel like there's no plan on what to do next

When you **DON'T** have a clear line between the two, you'd then be stuck in the two phases. This is why you need to have the following to focus on each phases:
### Prototyping
#### ✅ Focus on
- Building working systems
- Building working core game mechanics
#### 📝You scope for prototyping by
Actually doing the work, and just having "fun" ([[divergence thinking]]). This is where you explore the ideas, where you try out the mechanics that you thought about, tweak it if it doesn't work, etc.
#### 🤔What to do with feedback from prototyping?
You either change the systems, or change the mechanics. Either removing or adding more to it. Have only 5-10 people from your target audience to give feedback, and that's where you can gauge the feedback better.
### Production
#### ✅ Focus on
- Building more content
- Scaling up the levels/enemies/inventories
### 📝You scope for production by
Planning, and sticking to it. You do this more like you're doing work ([[convergence thinking]])
#### 🤔What to do with feedback from production?
Feedback here, most of the time will be coming from QA Testers regarding the bugs. But from real audiences, ideally ~100 or so, you'll only get it from alpha and beta testers. You don't aim to overhaul the mechanics. Here you aim to get Quality of Life issues ironed out, polishing the game because of animation and finding bugs to fix even more.
  ![[forteBuildingSecondBrain2022#Illustration of divergence and convergence thinking in creative process, with CODE]]
  
### Difference of effort between Prototyping and Production
![[images/Prototyping_Effort_vs_Production_Effort.png]]
### Ideal Protoyping and Production effort
![[images/Ideal_prototyping_and_production_effort.png]]
## FAQ for Prototyping vs Production[^5]
### 1. What if your content needs lots of content to prototype?
e.g. Stardew Valley?
Well it really **depends on the genre of the game**. Something like a platformer, you'd have a shorter prototyping phase, and then a long production one for you to scale up the different levels, but the core mechanics are the same. Others, you'd need to have a super long prototyping phase, but relatively short production, because everything is not really scaled up.
### 2. What about stuff like RPG maker?
Something like RPG maker would help you with prototyping the technical mechanics of the game, sure. But you'd still want to prototype the story
### 3. How do I know when to switch to production?
Not an easy answer, but the short answer is, when you found the game has all the core mechanics you want, and it is engaging to users
### 4. What about market research?
It is most important when you want to sell your game, sure. This should be done most during Pre-production/Prototyping phase, as you want to check what trends do people want for this.
### 5. When you switch to production, do you rewrite your systems?
When you switch to production, you should be focusing more on content. So that means you shouldn't want to be doing any systems or mechanics in the code. In an earlier tip, I  say that we should throwaway the code, while in another, i said that we should be building building blocks. This is where only experience kicks in, and you'd know better to either refactor or rewrite the code.


---
# See also
[[My Insights on Team-based Game Development]]

[^1]: [6 Key Stages of Game Development](https://kevurugames.com/blog/6-key-stages-of-game-development-from-concept-to-standing-ovation/)
[^2]: [choosing a game engine is easy, actually](https://www.youtube.com/watch?v=aMgB018o71U)
[^3]: [7 Tips from a Solo Dev](https://youtu.be/X_76ITqA22s?si=pZr7BdPVk1_3vCmn)
[^4]: [The Basics of Game Architecture](https://youtu.be/Hp7BSg3v5q8?si=XMNpmCELGmRHP1XA)
[^5]: [How to PLAN your Game as a Solo Developer](https://www.youtube.com/watch?v=NsMHicoZTzQ)
[^6]: [Ultimate Indie Gamedev Genre Tierlist](https://www.youtube.com/watch?v=Yg8wig1LTtE)
[^7]: [Roadmap to becoming a GameDev](https://youtu.be/6cU3ru8NSWQ)