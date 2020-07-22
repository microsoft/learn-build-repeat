# Escape the Code
Welcome to the repo for the 202 Hackathon project `Escape the Code`!

## Team
| Avatar | Name | 
|--------|------|
| <img src="https://avatars2.githubusercontent.com/u/1314285?s=460&u=46fd83b38323c7de99dace65d061c236105394d6&v=" width="50" height="50"> | Sarah Guthals | 
|  | Jenn Jinhong |
| <img src="https://raw.githubusercontent.com/cassieview/bio/master/cassieb.png" width="50" height="50"> | Cassie Breviu |
|  | Morgan Mitchell |
|  | Jayme Singleton |

## Three Sub-Teams
### The Video
- Narrative
- What assets we need in the video
- What we want to convey

### The "Pretty" Prototype
- Using Framer
- Clickabale, but not functional
- Used mostly for the video

### The "Functional" Prototype
- Unity
- Something people can actually play
- Not super pretty
- Kind of functional (can be magical)

## Project Outline
### Ultimate Goal (likely out of scope for hackathon, but important for the narrative)
The goal here is to create an end to end experience that starts and ends in Learn. You could imagine that you aren't allowed to sign up for an event unless you have completed 
certain Learn modules or done enough practice or something (with scaffolding and easy-entry ones of course)
- A Learn landing page with Learning Paths that support these "games"
- A webpage where learners can practice "fast" coding (just practice writing, learning, getting feedback)
- The game will be a 3D escape room that will be walkable with MR
  - Players will just be on their computer at home on a browser
  - Players will choose a coding language they want to write in
  - Players will be given challenges based on the room
  - Players will write code and will be insetivised to "push" their code live even when it isn't complete to get feedback from the host
  - When Players feel they have the code complete they can test the code to encourage testing
  - At the timer, all Players code are run one final time all at once and we see if they collectively escaped
  - While Players are writing code, the Host will "walk" around the world and will be able to see the code that the Players are writing (if they pushed it) 
  - The Host will give feedback and will also provide commentary
  - An even further stretch is that there are two teams in two rooms that are similar to see who can get out first. Instead of a timer they have to all decide they are "ready"
- After the game there can be interviews and a debrief with the Players (optional)
- After the game there is a live stream where the Host will walk through the different solutions that the Players did and other ones that are similar

### Lowest Scope for Hackathon
We could do something *very* simple to show this off for Hackathon.
- Players connect to a webpage where they are issued coding challenges
- Players submit their code
- A 2D image of the "room" gets shown and if their code worked then the "Room updates" (a new image is shown)
- We only do one programming language
- The rest is narrative in our video
- Tips

### Future Features
 - Other themes
 - Start with coding basics, could also have:
   - Data Science (use machine learning to solve problems)
   - Networking

## Similar Games to Serve as Inspiration

- [Battlesnake](https://play.battlesnake.com/)
  - [Battlesnake GitHub Repos](https://github.com/battlesnakeofficial)
  - [Battlesnake Docs](https://docs.battlesnake.com/)
- [Azure Mystery Mansion](https://dev.to/azure/unraveling-the-azure-maya-mystery-and-building-a-world-4pp2)

## Game Themes and Coding Challenges 
We thought about some themes, we were thinking maybe instead of "escape" we could *also* do "find all of the tacos".

The challenges could be something like "Go through the entire room and find all of the keys, unlock all locks, and if there is a taco, collect it."
The code would be something like (this is not real code in any particular language, no judging....):
```
# Find Keys and Locks
lockLocations = [];
for(int x = 0; x < room.width; x++) {
  for(int y = 0; y < room.height; y++) {
    if(room[x][y].hasKey()) {
      pocket.add(room[x][y].key())
    }
    else if(room[x][y].hasLock()) {
      lockLocations.add((x,y));
    }
  }  
}

for(int x = 0; x < lockLocations.length; x++) {
  for(int y = 0; y < pockets.length; y++) {
    if(pockets[y].isKey()){
      if(room[lockLocations[x].getX][lockLocations[x].getY].unlockWith(pockets[y]).unlocks) {
        if(room[lockLocations[x].getX][lockLocations[x].getY].hasTaco) {
          pockets.add(room[lockLocations[x].getX][lockLocations[x].getY]);
          pockets.remove(y);
        }
      }
    }
  }
}

tacoCount = 0;

for(int x = 0; x < pockets.length; x++) {
  if(pockets[x].isTaco()) {
    tacoCount++;
  }
}

Host.message(tacoCount);
```

We would obviously want to be more creative and not just having them write code for no reason. We could have some APIs to make it easier to navigate the room and we could even have them do some actual calls to Azure (maybe they find a photo album and have to find how many images have dogs in them). 

## Project Tech
- Unity
- BabylonJS
- Playfab
- [Framer](https://www.framer.com/)

## Brainstorming Notes
During our early July meeting we started discussing the desire to create an experience for more novice developers to learn new skills through a fun, collaborative experience. 

Cassie mentioned that one challenge for customers coming to Learn looking to learn something brand new is that they are often met with a wall of text. She found CodeFights to be an engaging way to learn to code (at least in the past it was). For CodeFights:
- You chose the language you wanted to code in
- The goal was to figure out how you could have solved coding challenges better than you did the first time
- You also were given the opportunity to see how other people solved the same or similar problems. 

Jenn mentioned "Escape the Code" which was like an escape room, but with code. 

We thought we would double down on these ideas and basically build an Escape the Code game that would encompass Learn modules prior (as a practice or prep - Read the Manual type activity), then maybe a practice area (maybe using sometimes like .NET Interactive where you're given a simple challenge and asked to write the code to solve it and given feedvack), then you participate in a game with other people, and then maybe we have a video afterwards that comments on the code and other solutions (most efficient, fastest to write, etc) to show different ways of solving the same problem. 

This fits really nicely into research Sarah has done in the past on effective learning practices (e.g. [From competition to metacognition: designing diverse, sustainable educational games](https://dl.acm.org/doi/abs/10.1145/2470654.2470669)). 

We also discussed being able to have no-code solutions for learners who want to explore other aspects. 

We also discussed the importance of a metaphor (like an escape room). This is also based in research (e.g. [CodeSpells: embodying the metaphor of wizardry for programming](https://dl.acm.org/doi/abs/10.1145/2462476.2465593), and that it is important to choose something inclusive. Let's **NOT** choose "hacking" or something like that. 

Finally, we discussed how this would create somewhat of a "glass-box" experience where folks could try out bits of code that is part of a larger solution without having to dive into all of it (also based in research: [Of black and glass boxes: scaffolding for doing and learning](https://dl.acm.org/doi/abs/10.5555/1161135.1161153).


# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
