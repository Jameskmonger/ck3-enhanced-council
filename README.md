# Enhanced Council

## Set up

- Clone to `Documents/Paradox Interactive/Crusader Kings III/mod`

(e.g. this file becomes `Documents/Paradox Interactive/Crusader Kings III/mod/enhanced-council/README.md`)

- Copy the `descriptor.mod` from this folder into the `/mod/` folder
- Rename it to `enhanced-council.mod`
- Add the following line:
```
path="/mod/enhanced-council"
```

## Mod Structure

There are a number of "Decisions" in `/common/decisions/`. Decisions are the single-use actions on the right-hand side of the game.

Decisions are used to start "Activities" which are the long-running events that a council member can take part in. An example of the Activities are listed below.

- Defend Liege (Spymaster)

You will notice that these Activities generally have a one-to-one relationship with a Decision.

The Activity code are defined in `/common/activities/`, and the "behaviour" of an Activity can be found in `/common/on_action/`.

An Activity is made up of a series of "Events". Events are the things that pop up while you're playing and give you options/notifications (this is a simplification). You can see the event definitions in `/events/activities/` - you'll notice that the behaviours defined in `/common/on_action/` call events described in `/events/activities/`. An Activity is made up of a series of Events.