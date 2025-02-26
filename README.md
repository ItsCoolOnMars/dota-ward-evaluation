# Algorithm/Model to Evaluate Wards (that been placed or hypothetical)

**Purpose:**  
Useful analysis of the very important aspect of dota 2 - warding. Could be used to assist and guide regular players as well as high/pro level players (tailored analysis of pro teams).

**Obvious thing to keep in mind:**  
To find a ward both vision and true-sight should be overlapped at the same time. To find best wards, two main philosophies can be applied, retroactive or proactive. The combination of both i believe will yield the best results.

---

## Approaches that could be taken (combination of both is what im looking for actually)

### Retroactive Approach
- Based on analysis of players past behaviour (replay analysis).

### Proactive Approach
- Based on the game data alone.

---

## Vision Wards

- **Ward survived a long time** – good  
  is it though? or the amount of information it gathered should be a major factor. i.e. ward survived whole 6min but showed nothing of value then its actually anet negative (because wards are limited resource?)
- **Ward observes important locations** – good

### What are important locations/events?
A teamfight is a top priority one or is farming spot of an enemy carry is one? I guess its quite unclear to make any solid decisions here (lots of implications, i.e. bara who needs constant vision on creeps for escape/farm), so we need to break it down further:

#### Properties of a Ward That Could Be Derived for Future Use:
- **Units that are visible due to this ward** (meaning no other means of vision were involved) can be just an unbounded score or normalised (due to complications like having many heroes/units visible at the same time the score would be more feasible)
- **Type of these units** (hero ordered by its networth – top 1 priority, then couriers/illusions/creep-heroes/creeps; other stuff is not so clear how to score)
- **How long they been visible**
- **New item information that team got due to ward** (newly bought bkb, blink etc. detected first on ward)
- **Meaningful actions done on these units** (check inventory, bara charge, sunstrike, smoke gang etc.) – very tricky to implement
- **Dewarded/survived/denied** – very straightforward but not too useful actually I think
- **Actions that been done on the ward** (smoke used – huge, manta used – big, an enemy support placed a ward, tp used to or from etc..)
- **The areas that the ward shows** should also be ranked (active rune spot, ancient camp, outposts)
- **The time and state of the game during this ward lifetime** – very important topic that needs its own breakdown

#### Additional Consideration:
- What if this ward sees nothing but that still useful (a neutral camp that never been visited by an enemy carry gives a hint that the enemy is somewhere else)

#### Hero Considerations:
- **Hero that placed the ward wasn't visible while placing the ward** – good
- **Hero wasn't visible with the placed ward in their inventory at all or recent to placing the ward** – diminishingly better
- **The ward is hard to place** (deep ward or requires preparations like a tree cut) – bad in isolation but I bet it correlates well with other good values of a ward

- The wards can be ranked on the scale from full stealth ones to fully apparent.

---

**Side note:**  
This will not only be an interesting data point, but also will help with detection of suspicious players (if a player consistently detecting full stealth wards with sentries, especially if they are in non-trivial places). Basically it could be a part of cheater detection tool:  
[Reddit Link](https://www.reddit.com/r/DotA2/comments/88k9j9/how_we_made_cheat_detector_gosuai_against_cheaters/#:~:text=anti%2Dcheat%20works-,To%20detect%20cheating%20we%20extracted%20mouse%20movements%20and%20all%20the,player's%20real%20action%20was%20registered).

---

## Interesting Ward Properties That Would Be of Interest for Players (but not for the algorithm)

- **Stealth/apparent** (was this ward placement detectable by other team)

To be thought about...

---

## Detection of "Wasted Wards" from Replays

- To be thought about...
---

## Sentry Wards

- To be thought about...

---

## Final Metrics

- The final metrics from 0 to 1 (worst - best ward) can be given through algorithm but further away AI can come to play (Deep RL or unsupervised learning).
- The metric can be different depending on the benchmark, (what is a user looking for, what weights the user has chosen).
