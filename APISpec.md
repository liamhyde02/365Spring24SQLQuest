# API Specification for SQL Quest

## 1.  Character creation flow

The API calls are made in this sequence when creating a character:
1. `Create base character`
2. `Rename character`
3. `Choose starter inventory`
4. `Finilize creation`

### 1.1 Create Base Character - `/character/` (POST)

Creates a base character that is new for the player.

**Response**:

```json
[
    {
        "id": "string", /* Matching regex ^[a-zA-Z0-9_]{1,20}$ */
        "name": "string",
        "player_name": "string", /* Unique to each player */
        "inventory_id": "integer", /* refrence to an inventory */
    }
]
```

### 1.2 Rename Character - `/character/{char_id}/rename` (POST)

Renames a character.

**Response**:

```json
{
    "success": "boolean"
}
```

### 1.3 Choose Starter Inventory - `/character/{char_id}/inventory` (POST)

With a shop allow starter items to be asigned to a character.

**Response**:

```json
{
    "success": "boolean"
}
```

### 1.4 Finilize Creation - `/character/{char_id}/create` (POST)

Locks the characters starter items and name in place so they can start on their quests.

**Response**:

```json
{
    "success": "boolean"
}
```



## 2.  

The API calls are made in this sequence when equipping an item on a character:

### 1.1 Get Inventory - `/inventory/{char_id}` (GET)

Using the character ID, open the inventory and returns a list of all items in the inventory
Note: Items are still subject to change
**Response**:

```json
[
    {
        "item_id": "string", /* Matching regex ^[a-zA-Z0-9_]{1,20}$ */
        "item_name": "string", /* Unique to each item */
        "quantity": "integer", /* Non-negative */
        "stats": [a, b, c] /*a - strength, b - magic, c - health */
    }
]
```




## 3.  

The API calls are made in this sequence when creating a character:
1. ``




