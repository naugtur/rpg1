# Zystem

## Basics 

### Character creation

All character traits are values 0-5
Character has only 2 basic traits: `BODY` and `WITS`
When creating one, you have 6 points to distribute between the two.
You can use one of the points to increase wealth to 2 instead.

Other traits get added on, they are skills (but you can bend the rule a little and add more traits as well)

#### Health

Health bar has 3 sections. When creating the character, fill in the "hurting"  and "out" and fill `BODY` of slots in the "OK" section. That's the maximum HP your character has.

Now fill in slots in the silhouette. Head HP is `BODY-1`, chest HP is `BODY+1` and the rest is `BODY`. 
When you put armor on, add big dots under the slots to record that.

Treatment can regain points in "out" section
First Aid and resting can regain points in "hurting" section.
Resting can regain points in "OK" section.

#### Wealth

Instead of counting coins or credits, there's a wealth factor here.
- 0 - you can afford nothing, even food
- 1 - you can afford food and travel and cheap items
- 2 - middle class
- 3 - seriously rich, can buy any common item without making a dent

You start with 1. It changes based on the story, no mechanics for that.

#### Skills

Fill in your `ATTACK` trait. `ATTACK` is one of: 
- average of `BODY` and `weapon power`
- average of `WITS` and weapon's `projectile power`

Choose your speciality.
You start with up to 3 skills. Write them in speciality and other sections depending on what they match. Now fill in 5 triangles of your choice. Each full square is 1 skill  point. Write your skill in the Traits column with their current value filled in.

### Mechanics of dice rolling

#### Skill test

Take `SKILL` of K6. Roll. 

Count how many dice has `value > TEST DIFFICULTY`

1. Barely succeeded, took lots of time
2. Done
3. Good effect
4. Good effect, done quickly
5. Epic results

#### Attack

`A` - attacker
`D` - defender

Take `A:ATTACK` of K6. Roll.

If any of the dice has `value > D:WITS`, the attack successful, otherwise you miss.

Number of dice with `value > D:ARMOR` is damage.
`ARMOR` is taken from the body part you hit, damage goes to that body part and the HP bar

Yes, it's easy to get seriously hurt.

#### Magic / Artifacts / Tech / Implants (depending on setting)

Let's call it Magic and Spells for short, but you shouldn't have trouble changing vocabulary.

- Spell `LEVEL` is taken from your HP when you use magic
- Spells use skill test mechanic, where `TEST DIFFICULTY` is the spell level
- `LEVEL` and what happens if successful is defined in the spell itself.


### Skill development

You add a new skill when you spend the time/effort to learn one. You also need to have the points alocated. You can only fill triangles next to ones already filled.

There are two possible speeds of character development
- rapid (good for oneshots, fun with mechanics) - get a point for each successful skill test
- regular (good for campaigns) - get experience points after a scenario, in varying numbers, depending on GM's whim

#### Super skills: Magic / Artifacts / Tech / Implants (depending on setting)

When you reach a circle with a number, you can gain a super skill on the level of the number.

You design one by spending `LEVEL * 5` points to fill the card:

| | 0 | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|---|
|duration|none, instant|seconds |minutes|hours|days|years/forever|
|time to cast|days|hours|under 1h |minutes|seconds |none, instant|
|distance|0|reach|throw|sight|far...|anywhere|
|area|point | point|arms reach|room|room|horizon|
|creation, morphing, destruction|nothing|tiny|10cm|100cm|1000cm|any size|

||effect|
|---|---|
|damage| points of damage |
|buff| points to add to a trait for given time or points healed|
|illusion|cheats creatures with `WITS` lower or equal to illusion|

### Plugins

#### Sanity

Put a sanity bar above your HP bar. 
```
_ _ _ _ _ | _ _ _ | @
ok        losing it  crazy
```

Fill in the "loosing it" section. Fill the ok section up to `WITS`

- When casting a spell HP is only decreased if the spell failed, but the number of pairs of dice with same value is removed from sanity. 
- When first bit of "loosing control" is removed, permanently decrease `WITS` by 1
- When crazy is reached, you know what to do (depends on setting)

#### Armor decay

Number of pairs of dice with same value is armor damage

#### More difficult aiming

Number of dice with `value > A.WITS` needs to be a half or more to hit where you wanted. Otherwise the hit goes to the least damaged limb.

#### Heroic battle

When fighting multiple anonymous enemies, take a K6 for each. Roll.
- `value > ATTACK` - you got hit
- `value = ATTACK` - enemy killed instantly
- `value < ATTACK` - enemy wounded, needs another hit

#### Heroic armor

Damage decreases the armor first, only when armor is out goes to the body.
