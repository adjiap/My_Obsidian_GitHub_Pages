---
created on: 2024-10-30
last modified on: 2024-10-30
aliases:
  - Insights on Team Game Development
tags:
  - softwaredevelopment
  - developmentlifecycle
  - gamedevelopment
  - productdevelopment
---

---
# Realistic Game Dev Phases and Planning when you work in a Team [^1]
There are realistically 6 game development stages in order for you to make a game. If you're to do this **solo**, **and** doing this as a side-project, then realistically, you could release a small game in 12 months time. [^2] The phases shown below is more for a team of game devs, but for timeline visualization reasons, I will still write down the months, as if they're working in the same time scale.
## 1. Pre-Production

> [!note]
> Ideally, this only happens in the first two months (e.g. January and February)

This is where [[Game Designers]]:
- Start making their game ideas and overarching narration
- They talk about the general concept of the game
- They talk about the idea, vision, plot, characters
- They talk about dialogues, victory and defeat conditions and gameplay elements as well as how it reacts to player actions
- And finally make a [[Game Design Document]].

Once the GDD is done, Game Developers can start making the [[A Prototype is a stripped down version of a product used for feasibility test as well as validation of customer interest|prototype]]. It's best to **not think** about the scale, nor **the art** or **the details**, or to even think about **reusing assets or code**. It's likely better if you just **throw everything** out of the window afterwards. [^2] It is likely that the developers would collaborate a lot with the Game Designers to talk about the feasibility of the mechanics, especially with the projected time frame.

> [!Warning] General Rules for Gameplay mechanics
> There should be around 3-5 "big" mechanics that the game revolves around. 

Game Producers will also work here with the Project Manager on the budgeting, planning, milestone and required resources. Here would be the basic questions you need to ask (some should reference to the game designer):
- What is the game budget? -> How long do you plan to make the game?
- What's the genre? -> Simulation? Adventure? RPG? Puzzle? -> As a rule of thumb, if you have a small budget, don't make RPGs or simulations as they need a huge amout of detail to work out and implement
- Who's the target audience? -> Casual games? Highly specialized in genre?
- How do you want to monetize this?
## 2. Production

> [!note]
> Ideally, this happens after pre-production is settled, and this happens for the next 7 months (March till September). 

Once the Pre-Production stuff is done, and the mechanics are settled, this is where the real work begins. 

There are mainly 3 different type of work that happens in Production Phase:
- Graphics and design
	- 2D/3D artists involved in creating characters, assets, visual effects, environments and interface elements
	- Level designers should work regarding the structure of the levels and the main obstacles that the player will face
	- Writers create the stories and work with storyboard artists to create concept arts
	- UX Designers will do the interfaces (menu pages) for players to use while playing the game
 - Programming 
	 - Game developers will take what they learned in pre-production, and will first work to make a playable game, worthy for a [[playtest]], and then a demo for [[beta testing]], before continuing to further develop and polish the game
	 - Developers work together with QA Testers fixing the bugs and adding new features from feedback
 - Sound design
	 - Sound engineers or sound designers to create game's sound design which includes sound effects, voice acting and music

During this stage, the Project Manager will likely already make a Roadmap an creating Milestones for each work type to achieve. Those milestones could be:
- Completing certain levels
- Implementing core mechanics
- Alpha and Beta testing stages
- Final Concept Art
- Final Character Design, etc.

In a more granular view:[^2]
1. March and April - is for the developers to create something that's usable for a [[playtest]]. 
2. April - This is where the a "Screenshot" of the game should be taken, and put up on the Steam Page for the "pre-prelaunch". The target is not for it to be marketed, but for people to be sent for playtests
3. May till July - Is for developers to finish creating the demo. This is where you would create a short 15 min - 1 hour game where you would showcase all of your mechanics and design to users to play as a demo.
4. July till September - Is for developers to expand on the content, and expand on the experience
## 3. Testing

> [!note]
> Ideally, this happens concurrently with Production stage, and this should be a [[Amplifying Feedback Loop is about creating, shortening and strengthening the Feedback loop between organizations in the entire value chain|Continuous Feedback loop]], to improve the game itself. So it occurs for the next 7 months (March till September)

Game testing is unfortunately often skipped due to deadlines, and then after releases to the public, you can't take things back anymore (e.g. Cyberpunk 2077's release). The QA tester's responsibility here is to check the accessibility of all areas of the game, correct display of elements from different sides, check for game exploits, optimizations.

Ideally this phase will be done concurrently with the production phase, as it will give a much faster feedback loop to the developers, for them to catch bugs early.

 There are 3 types of game testers:
	 - **Stress Testers** do their best to check whether the game will work in all possible functionality
	 - **Walkthrough tester** implement 100% playthrough with all the achievements and prizes to make sure things work
	 - **Engagement testers** test the game just for fun
## 4. Pre-Launch

> [!note]
> Ideally, this should start on the 4th month (April), and then a more comprehensive pre-launch activities somewhere in the 7th month (July)

In a more granular view:
1. April - Create screenshots and find people for PlayTest, to get early feedback and to find the content to expand
2. June till September - This is where the Marketing work would be done the most. They're like:
	- Commercials
	- Articles
	- Screenshots and videos of the game
	- Sending Steam Page for getting wishlisted and so forth.
	- Trailers
	- Pre-Sale with certain game bonuses
	- Exclusive previews of the game

> [!warning] Marketing costs
> Be aware, the cost of marketing could be **ENORMOUS** and the same size of the entire development project

## 5. Launch

> [!note]
> Ideally, this happens after QA Testing has gone through, and the release in a digital store (i.e. Steam), this should happen in the 10th month, October

This is the release of the games to the public. Ideally the last month is where the final polishing for quality of textures, or animation improvement will be done, and finally you can publish it
## 6. Post-Production

> [!note]
> Ideally, this happens after launch, on the 11th and 12th month, before we "close" the game dev phase

Now that the game is out, the Game Developer and QA Tester's work continues. Some help from the Level Designers would also be there to either *buff* or *nerf* stuff depending on the feedback you've gotten. Ideally of course, there only some small bugfixes. But there could be some kind of game breaking bugs, that you'd need to create patches as soon as possible, so the players would be satisfied. 

The best thing for the players however, is that you'd then make a (ideally paid) Downloadable Content, and this is where the Level Designers, Writers, Game Developers and QA Testers  work again to expand the base game. This is technically a whole new game development, but a much smaller version, though it does build up on things that had been built from before.
# Key Roles in Game Dev as a Team [^1]

## Project Managers
Responsible for:
- Being the central role to oversee the whole development process
- Coordinating the team
- Managing resources
- Setting deadlines
- Ensuring the project stays on track
## Game Developers/Programmers
Responsible for:
- Bringing the design and mechanics to life through programming languages and dev tools
- Polishing the games through feedback from QA Tester and Users
- Game Devs are responsible to ensure the main character and the game world are inseparable
- Rapid Prototyping and [[Playtesting]] for proof of game design
- Optimizing the game so it's runnable in the chosen platform(s)[^3]
## Game Artists
Responsible for:
- Creating visual elements to captivate players imaginations
- Crafting characters
- Crafting stunning environments
- Creating eye-catching animations
## Game Designers
%% Role can be joined or collaborate most with [[My Insights on Starting a Solo Game Development#Level Designers|Level Designers]] and [[My Insights on Starting a Solo Game Development#Writers/Narrative Designers|Writers/Narrative Designers]] %%
![[Game Designers#Responsibility[ 1]]

> [!note]
> They have deep understanding of player psychology and engagement, to create challenges rewards and interactive elements
## Sound Designers
%% Role can be joined or collaborate most with [[My Insights on Starting a Solo Game Development#Game Designers|Game Designers]] %%
Responsible for:
- Create captivating soundscapes
- Create music and SFX for atmosphere
- Creating soundbites
## QA Testers
%% Role collaborate most with [[My Insights on Starting a Solo Game Development#Game Developers/Programmers|Game Developers/Programmers]] %%
Responsible for:
- Finding bugs, glitches and issues within the game
- Giving feedback to make sure the game is polished and free of technical hiccups
## Writers/Narrative Designers
%% Role can be joined or collaborate most with [[My Insights on Starting a Solo Game Development#Game Designers|Game Designers]] and [[My Insights on Starting a Solo Game Development#Level Designers|Level Designers]] %%
Responsible for:
- Writing captivating stories and compelling characters into the game's fabric
- Creating immersive dialogues, rich lore and engaging narratives
- Detailing the main idea, vision, plot and characters
## Game Producers
%% Role can (probably) be joined with [[My Insights on Starting a Solo Game Development#Project Managers|Project Managers]] %%
Responsible for:
- Overseeing entire process from a business perspective
- Managing budgets, schedules and resources
- Ensuring project is financially viable and commercially successful
## Level Designers
%% Role can be joined or collaborate most with [[My Insights on Starting a Solo Game Development#Game Designers|Game Designers]] and [[My Insights on Starting a Solo Game Development#Writers/Narrative Designers|Writers/Narrative Designers]] %%
![[Level Designers#Responsibility[ 1]]

## UX Designers
Responsible for:
- Creating intuitive and user-friendly gaming experience
- Designing interfaces, menus and controls that is easy to navigate and understand to enhance player satisfaction.


---
# References
[^1]: [6 Key Stages of Game Development](https://kevurugames.com/blog/6-key-stages-of-game-development-from-concept-to-standing-ovation/)
[^2]: [Roadmap to becoming a GameDev](https://youtu.be/6cU3ru8NSWQ)
[^3]: [7 Days of Indie Game Dev - Walk in My Shoes](https://youtu.be/ZQqxwp0CO-w?si=CLnbqP6bgId8QtrO)
# See also
[[My Insights on Starting a Solo Game Development]]
