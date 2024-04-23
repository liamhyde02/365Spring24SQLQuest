Example Flows #1:
**Player wants to equip an item and begin a quest**

Rain, the adventurer, comes into town seeking to begin a quest.
First, he must equip his trusty sword. He requests to see his inventory by calling GET /inventory/45 where 45 is his character ID
Rain sees his health potions, armor, and most importantly he sees his trusty sword. 
That sword has an id of 8, so he calls POST /equip/45/8, which marks that sword in his inventory as equipped.

Now ready to undertake the newest quest, he requests to see the quest board by calling GET /quests
Rain checks the list of quests being offered. A goblin eradication quest for 70 gold, a merchant escort request for a new helmet.
Rain wants that new helmet, so he calls POST /quests/45/86, where 86 is the quest_id number for that merchant escort request.
Now off Rain goes with his trusty sword equipped to help that merchant and earn himself a shiny new helmet.



Example Flows #2:
**Player completes a quest and wants to buy a potion from a shop**

Example Flows #3:
**Player creates a character, but immediately regrets the name they gave their character and seeks to change it**
