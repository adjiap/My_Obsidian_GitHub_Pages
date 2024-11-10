---
created on: 2024-11-01
last modified on: 2024-11-01
aliases:
  - GDD
tags:
  - gamedevelopment
  - softwaredevelopment
  - requirementsengineering
  - featuredrivendevelopment
---

---
# Definition
It is a highly living descriptive software design document for a video game[^1] That's the result of endless [[A Prototype is a stripped down version of a product used for feasibility test as well as validation of customer interest|prototyping]] together between the [[Game Designers|game designers]], game developers, and game artists, that becomes the guiding document of what the game should become. It can be used to keep track of the core themes, styles, features, mechanics and ideas of your game project.[^3]

## Questions to ask for GDD [^2]
- What is the **Hook** of your game? What makes players **WANT** to play or even buy your game?
	- There're three types of Hooks[^4]:
		- Story - Hunting "Mechanical" Dinosaurs in what looks to be post-apocalyptic earth (Horizon Zero Dawn)
		- Mechanical - Repeating the day over and over again to kill certain people (Death Loop)
		- Visual - Amazing nature in old Japan (Ghost of Tsushima)
- What is the **Loop** of your game? What would the players be doing over and over and over and over again to get to the goal that was mentioned in the Hook?[^4]
- What should the game type be?
	- Would it be 2D? Casual 2D/3D? Hardcore 3D?
	- What kind of "render pipeline" do you want to use? Do you want Unity/Unreal/Godot/etc.?[^4]
- What should be the gaming platform? -> Console? PC? Mobile? -> **For newbies, just do a Steam launch :)**
- What's the genre? -> Simulation? Adventure? RPG? Puzzle? -> As a rule of thumb, if you have a small budget, don't make RPGs or simulations as they need a huge amount of detail to work out and implement. If you aim to have a Rouge-Lite, then you need many player builds, if you want to have Metroidvania, then you need multiple interconnected levels[^3]
- What's the intended gameplay? 1st person? 3rd person?
- What's the "big" game mechanics? 
	- Leveling up? Crafting? Base Building? Do player choices matter?
- Who are the characters? Or should there be no characters?
	- How would the world change if the character succeed? Or if they fail?
- If it's not a casual game, what's the plot?
	- What's the overarching narration?
	- Is there a [[Macguffin]]?

## Typical Template of GDDs
- Core concept
- [[Game Design Pillars]]
- Main features & mechanics
- Target platform & target audience
- Interface & controls
- Basic story
- Visual style
- Music & sound
- Similar games & genres
- Development timeline & major milestones

![[GDD_Template_IronSand.png|700]]

![[GDD_Template_MassFlux.png|700]]

### Example Template
%% https://docs.google.com/document/d/1CHK2TPrArOCNuqC2sl8xVacfNoLS-v5zKCPTHmPn25w/edit?tab=t.0 %%
#### Game Jam Design Document

Add the details to this template. Focus on the really important features. The point is to communicate a game idea with your team or think through it yourself so you can dive into prototyping with a plan. 
###### Game Outline/Reference: 

| Game Title:                                                                                                                                                                      |     |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| Game Summary: <br><br>Give an explanation of what the game is about. Shorter is generally better.                                                                                |     |
| Core Mechanics: <br><br>List the core features of your game as bullet points. For example, “time only moves when the player moves.”                                              |     |
| Gameplay:<br><br>Give an example of a gameplay scenario and how it would play out. You should imagine the gameplay and get inspired.                                             |     |
| Music: <br><br>Write how music and sound will be used in the game, and what feeling you want to get from the player. If it’s helpful, name a couple of songs in a similar style. |     |
| Art Style:<br><br>Describe the art style you’ll be using, put reference images below and write the game names in case someone wants to research them.                            |     |
| Winning Condition: <br><br>Write how players would win the game.                                                                                                                 |     |

##### Scope Check 

Doing a scope check can seem tedious, but it’s the foundation of good design. Knowing the core experience for your game allows you to know what to build first; you won’t get lost in building unnecessary features or assets. You’ll also end up with a game that feels intentional because every element will contribute to the whole. 

##### Visualization 

To get a good grasp of what your game will hopefully look like by the end of the jam, brainstorm some ideas and concepts. To help get you started, here are some things to consider:

- What’s the goal of the game? 
- What perspective will your game be? Choose from first-person, second-person, third person, or top down (also known as isometric). 
- Think about what your UI will display? It would be best to create instructional, intuitive UI before, during and after game-play. Consider timers, health bars and backgrounds. 
- What will move or change in your game? Keep in mind what type of visual and sound effects you’d like to have and where they’ll be implemented. For example, a ‘thump’ sound when placing an object. 
- What will each player be doing and what happens in response? For example, if a character is charging up a jump, how would your game show players that this is happening? 
##### Implementation 

For each of the features and ideas you have, think about how you would achieve this in your game. Which ideas are feasible and which take too much time? Imagine how you would write code for each of the things on your list; for example, things that move and player interactions. 

To save time during the jam, have a look for free pre-written code online or previous project code which you can copy and adapt. Alternatively, look for tutorials or asset packs that could take care of some of the functionality for you. If you have any other questions, consider checking out [answers.unity3d.com](https://answers.unity.com/index.html). 

##### Scale 

Take a moment to consider your game from a broader perspective. 

1.  Create a list of all the parts of the game that can be numbered and grouped. For example, you could have 3 levels and 8 enemies. Here are some things you may want to add to your game:  
- Levels
- Power-ups
- Enemy types 
- Puzzles 
- Enemies 
- Obstacles 

2.  Once you’ve made your list, cut everything to one. In other words, you’ll have one of each feature. 
Ask yourself if your game still works. This exercise will help you focus on the key mechanics and basic game play for each level. If your game works with one of every feature, you should find that you’ll be able to scale it up easier. You can use the table below to help you:

| Feature/Part | How does it work? (Mechanics) | How does the user interact with this feature? |
| ------------ | ----------------------------- | --------------------------------------------- |
|              |                               |                                               |
|              |                               |                                               |
|              |                               |                                               |
|              |                               |                                               |
|              |                               |                                               |
|              |                               |                                               |

---
# References
[^1]: https://en.wikipedia.org/wiki/Game_design_document
[^2]: [6 Key Stages of Game Development](https://kevurugames.com/blog/6-key-stages-of-game-development-from-concept-to-standing-ovation/)
[^3]: https://gamedevbeginner.com/how-to-write-a-game-design-document-with-examples/
[^4]: [How I would Start Game Development (If I Started Over)](https://www.youtube.com/watch?v=5yWvB79On10)