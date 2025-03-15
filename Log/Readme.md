# 18-03-2025 The real construction is getting closer now...
Team plantcontainer is going to the Action to buy paint, brushes, ...
Team water is looking into calibrating the ion sensors.

# 15-03-2025 Waiting on orders and preparing/testing (open-door day)
With most of our components on the way, and mr. Coppens working on the full closet, we are mostly testing sensors, ESP's and yaml code. We're also searching for other materials we'll need soon; white paint, paintbrushes, coconutfiber, ...

# 11-03-2025 PCB's ordered!
The PCB's have been ordered from PCBWay. 

# 06-03-2025: We sowed our first seeds, to be used as a reference or maybe even to repot them in our working VF soon!
We sowed:
  - Basil
  - Coriander
  - Mint
  - Oregano
  - Leaf lettuce
We also broke down the old construction.

# 25-02-2025: Our first order!
We ordered several components that we'll need for our construction. The sites used were Mouser, TinyTronics, AliExpress, PCBWay, Mouser, RS, ...

# First month of semester 2: Preparation for the real deal has begun
Each group, team plantcontainer, team light and team water, have started researching and thinking about how to really implement their parts of the construction. We farmed as much components as possible from the old construction, that we're hoping to reuse.

# 17-12-2024: Presentation and feedback
We presented our progress and collected the feedback in the ClickUp notes.

# 19-11-2024: Planning 
While waiting for our PCBs to arrive, we are creating a schedule to start working on our vertical farm. We aim to divide the assignment into smaller subtasks and assign them to all team members.

# 22-10-2024: Working on the old system
We gathered to work on the previous system. The plan was to get it running again and examine the causes of failure a bit more.

## What we did
### Powering up the system
Using the instructions on https://verticalfarmib3.github.io/inhoud/operation/ we turned on all of the systems (after trying some times).
The esphome server runs on 192.168.0.40:8123 on the CM3 network. By setting up an automation we can automatically make the lights turn on and of at the correct time of day. We verified that the lights, pumps, fans and mixer work.
The Grafana interface was accessible through port 3000.

### Moving the setup to a new place
First we removed the wood enclosure and put it aside.
Next we disassembled the top and front part that holds the glass. By doing this we could access the electronics and plants. The old plants were cleaned up and we cleaned the insides a bit.
Then we moved the wooden frame to the new location. We put the aluminium frame around it.

### A new seed
We carefully planted new seeds in the working planters.
The timing of the lights was changed to be active from 8:00 to 20:00. We let the timing of the fans stay the same (active for 5 minutes, every 30 minutes).
The plants are a mixture of basil, dill, chives, oregano, parsley and African marigolds.

## The problems we found
- The mixer only works for a few seconds at a time. This isn't enough to mix all the nutrients in the big container.
- The drainage tubes (that return excess water) get clogged by the rockwool.
- Instead of using silicone to glue the tubes to the system, hot glue was used. This is not water proof.
- Because of the high start up current of the most right lights, the relay gets melted closed sometimes. This is because the current exceeds the relay's specifications.
- The pumps will pump new water to the plants whenever the soil moisture sensor drops below 50%. This means that when the sensors broke down, the system just kept on pumping water. This problem in combination with the clogged drainage tubes meant that there were water leaks.

# 16-10-2024: Brainstorming

## Starting up the old system
- drainage tubes have to be fixed
- relays have to be changed for better ones
- the substrate (rock wool) should be changed for new substrate (we might have to try a different type of substrate)
- fix the water replacement issue (easier access)

## Our ideas for the new system, modularity
We will make something to put in your home (kitchen) instead of an Industrial scale farm. Not every home is the same, that's why our system should be modular.
Our system is based on hydroponics.
- a system with drawers inside drawers
![image](./figure1.jpg)
![image](./figure2.jpg)
![image](./figure3.jpg)
- connecting the sensors via I2C bus, having single common rail for all modules
- Plug & Play system for every module

## Plans for our next session
- getting the system running




