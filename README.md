# **META WORLD Module – v1.0.3**

**by dionednd**

Commissioned by **Zelda In A Blankey / Doug Walker**

A  recreation of **Umineko: Golden Fantasia’s Meta World** mechanic for IKEMEN GO.
---

## **Features**

### **Meta World Declaration / Reversal System**

Accurate debate flow:

* **Declare Metaworld** (costs 1000 meter by default)
* **Meta Reversal** (costs 2000 meter by default)
* **Meta Re-expansion** (costs 2000 meter by default)
* **Meta Re-objection** (costs 2000 meter by default)
* **Forced Meta Expansion** (costs 2000 meter by default)

### **Attack & Defense Buffs**

* **2.0× Attack**
* **0.5× Damage Taken**

### **Speed Buff**

* Speeds up attack-state animation timing during Meta World.
* Can be disabled if it conflicts with character scripts.

### **Meta Super Support**

* Optional mechanic that allows Meta Supers.
* Can be enabled by defining these constants in your character's .cns file.

* MetaSuperState = Stateno (disables meta super if not defined)
* MetaSuperStateType = 0/1/2 (0 by default)
*	0 = AIR AND GROUND
*	1 = GROUND ONLY
*	2 = AIR ONLY

### **Custom Visual Effects & Glow Effect**

Includes handmade FX to emulate Golden Fantasia’s visuals.
Glow Effect code from xcheatdeath's edit of toukachan's Glow Effect Module.
Effects automatically disable on invisible characters.

### **Interactive Stage Support**

* detect if a Meta World is active using: `player(1), map(MetaWorld_Active)`

---

## **Installation**

1. Open your **config.ini** and look for **[Common]**
2. Under **States**, add:

   ```
   , data/meta_world/meta_world.zss
   ```
3. Under **cmd**, add:

   ```
   , data/meta_world/meta_world_command.cns
   ```
4. Under **commonfx**, add:

   ```
   , data/meta_world/meta_world.def
   ```

5. Run IKEMEN GO.

---

## **Constants Overview**

In your character's .cns file, you can use these constant names to customize your character's animations and such.

| Constant                                                   | Description                        |
| ---------------------------------------------------------- | ---------------------------------- |
| `MetaWorldAnimDeclare`                                     | Animation for declaration          |
| `MetaWorldAnimReversal`                                    | Animation for reversal             |
| `MetaWorldVoiceEnabled`                                    | Enable/disable voice lines         |
| `MetaWorldVoiceGroupDeclare` , `MetaWorldVoiceIdDeclare`   | Declaration voice                  |
| `MetaWorldVoiceGroupReversal` , `MetaWorldVoiceIdReversal` | Reversal voice                     |
| `MetaSuperState`                                           | Optional Meta Super                |
| `MetaSuperStateType`                                       | Optional Meta Super State Type     |

---
