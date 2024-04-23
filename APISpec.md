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

### 1.2 Rename Character - `/character/1/rename` (POST)

Renames a character.

**Response**:

```json
{
    "success": "boolean"
}
```

### 1.3 Choose Starter Inventory - `/character/1/inventory` (POST)

With a shop allow starter items to be asigned to a character.

**Response**:

```json
{
    "success": "boolean"
}
```

### 1.4 Finilize Creation - `/character/1/create` (POST)

Locks the characters starter items and name in place so they can start on their quests.

**Response**:

```json
{
    "success": "boolean"
}
```



## 2.  

The API calls are made in this sequence when creating a character:
1. ``




## 3.  

The API calls are made in this sequence when creating a character:
1. ``




