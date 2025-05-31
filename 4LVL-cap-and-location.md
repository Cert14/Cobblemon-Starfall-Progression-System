# LVL Lock and Location

Let me give you a straight piece of advice: if you let players run free on day one, they will break your game by day two.

That is not theory. That is experience.

---

## :pushpin: Why Level Lock?

You need something to **slow down the climb** without turning the game into a chore.

Not everyone plays six hours a day. But if one player reaches breeding-ready IV Pokémon by the end of the first week, you have lost the rest.

That is where **level lock** becomes your best tool. It slows the rush and keeps the hype wave moving at a steady pace.

By setting level limits tied to time, you:

- Give players breathing room
- Prevent rushers from leaving others behind
- Encourage side activities like building bases or experimenting with team setups

Most important, it lets players experience what it means to be a low-level trainer. They get time to test movesets, strategies, and learn the pacing of the world. All without being pushed out by someone who found an ultra ball in a chest and caught a level 40 Tauros on day one.

Without a level cap, that Tauros becomes the new standard, and every starter team becomes useless. Players drop their Pokémon. They stop caring. The magic fades.

With a level cap, players invest in their early team. They plan movesets. They choose between evolving now for a temporary edge or waiting to unlock a future powerhouse. 

The result is balance, excitement, and lasting engagement.

---

## :wrench: How to Add a Level Cap in Cobblemon (Step-by-Step)

### 1. Install Cobblemon Config API

You will need a config-compatible loader like Forge or Fabric, and the proper version of **Cobblemon Config API**. Follow their setup instructions:

- [Cobblemon Config API GitHub]([https://github.com/Cobblemon/Config](https://gitlab.com/cable-mc/cobblemon))

### 2. Locate the `cobblemon.config.json` File

Once your server is up and Cobblemon has loaded once, a config folder will be generated.

```bash
/config/cobblemon/cobblemon.config.json
```

### 3. Modify the Level Cap Setting

Open the `cobblemon.config.json` file and search for the section:

```json
"levelCap": {
  "enabled": false,
  "maxLevel": 100
}
```

Change it to:

```json
"levelCap": {
  "enabled": true,
  "maxLevel": 25
}
```

Replace `25` with the current cap you want. You can raise this over time through updates or scheduled unlocks.

### 4. Schedule Increases

Plan milestone dates or server-wide events to raise the level cap.

Example progression:
- Week 1: Cap 15
- Week 2: Cap 25
- Week 3: Cap 40
- Week 4+: Gradually raise to 100

# Location Lock: The Journey Over the Map

Let me tell you something that most server owners learn too late.

If you let players go anywhere on day one, they will. And they will not come back.

---

## Why Location Lock Matters

The moment you open the whole map, you lose control over the story.

That mountain in the distance? Climbed.
That exotic biome three towns away? Looted.
That hidden cave meant for week three? Cleared.
The chest in the village full of ultra balls? Looted.

Players want to explore. That’s what makes Pokémon magical. But when they rush past everything and hit the ceiling too fast, they burn out. And they leave.

That’s where **location gating** becomes your best ally. And it becomes a guide, a compass.

And a double edge weapon.

Because if you overdo it, players feel caged. They feel like your world is fake, with invisible walls and arbitrary blocks. They stop feeling like trainers and start feeling like hostages.

So what’s the balance?

The answer is **meaning**.

---

## Lock with Purpose

Don’t block an area just because. Block it **with a reason**:

- The bridge is broken. The community must gather materials to repair it.
- A sandstorm makes the desert impassable until a weather device is found.
- A legendary slumbers in the volcano. It wakes only when the server reaches a milestone.

Tie locations to quests, server milestones, or lore. Make the block a chapter in the story, not a wall in the way.

When the gate opens, it should feel earned.

---

## Give Them Something to Miss

Early players shouldn’t see the whole map. They should hear about it. Wonder about it.

> “I heard someone found ruins past the cliffs.”  
> “There’s a biome full of ghost types past the swamp, but it’s sealed.”

These whispers do more than any sign or warning zone. They create hunger.

And while they wait?

**Give them something to do.**
- Side games that test their knowledge or timing.
- Activities like catching contests, scavenger hunts, or time trials.
- Long quests that uncover lore, introduce NPCs, or unlock useful items.
- Lore pieces scattered across the region, telling a story when pieced together.

Give them time to fall in love with what they have before giving them more.

---

## Timing is Everything

Location locks work best when paired with server-wide pacing:

- Week 1: Forests, hills, and beginner towns
- Week 2: Desert and rocky terrain
- Week 3: High-level zones and mid-tier legendaries

Link each unlock to events, server progress, or a collective achievement.

> “We repaired the train line. The mountain is open.”

It turns your map into a living story.

---

# 🌐 How to Use World Border to Lock Locations from Spawn

This native Minecraft feature lets you create an invisible wall around spawn in all directions. It is simple, effective, and immersive for guiding player progression.

---

## ✅ Step-by-Step Setup

### Step 1: Set the Border Center at Spawn
Position the world border at your spawn point:
```bash
/worldborder center <x> <z>
```
Replace `<x>` and `<z>` with the coordinates of your spawn.

### Step 2: Set the Initial Border Size
Define the diameter of the playable area:
```bash
/worldborder set 200
```
This sets a 200x200 block square centered on spawn.

### Step 3: Visual and Physical Limits
Players will see a faint red border as they approach. They cannot pass through it.

### Step 4: Expand the Border Over Time
Grow the world gradually as your server progresses:
```bash
/worldborder set 400 60
```
This command expands the border to 400 blocks over 60 seconds.

### Step 5: Use for Story Progression
- Tie expansions to server-wide goals or quests.
- Announce events: "The border weakens as the town restores power."
- Add lore to make each expansion meaningful.

---

# 🌿 How to Increase Biome Variety Near Spawn

One of the most common world generation mistakes is letting randomness dictate the early game.

If players don't find the biomes they like early, they can feel frustrated. They want a forest, but it's all desert. They look for snow, but it's just jungle. That kills the mood.

The fix: **more biomes, smaller sizes, near spawn**.

This improves exploration and creates a real sense of adventure. If done right, biomes can become larger and more defined the farther you go from spawn.

---

## 🎯 Goal

- A wide variety of small biomes near spawn
- Gradually larger, more defined biomes with distance
- Visual and strategic progression across the map

---

## 🧰 How to Do It

### Option 1: Use Mods Like **TerraForged** or **Terralith**

These mods give full control over biome generation.

#### Step 1: Install the Mod
- Use Forge or Fabric
- Download TerraForged or Terralith

#### Step 2: Adjust Biome Size
In the configuration folder:
```json
"biome": {
  "size": 1
}
```
- Lower numbers mean smaller, more frequent biomes

#### Step 3: Control the Spawn Location
Place your spawn where multiple biomes intersect.
Use `/locatebiome` and `/setworldspawn` for fine tuning.

#### Step 4: Scale Biome Size with Distance
Terralith allows custom rules that increase biome size the farther you get from spawn. This creates a natural progression.

---

### Option 2: Use Advanced Datapacks

While more limited than mods, datapacks can influence biome sources.

#### Step 1: Create a Datapack
Define `worldgen/biome_source` with multiple biomes and custom distribution.

#### Step 2: Set Zone Variety
While you can't dynamically scale with distance in vanilla, you can design high variety zones near spawn.

---

## 📌 Recommendations

- Avoid large, single-biome stretches near spawn
- Include multiple biomes within the first 500 blocks
- Mix forests, lakes, mountains, and rare zones
- Reserve extreme biomes (jungle, snow, volcanic) for mid-to-late game

---

Giving players what they need early doesn’t break immersion. It invites them to stay.

And when they eventually discover something far away, that sense of wonder will be even greater.
