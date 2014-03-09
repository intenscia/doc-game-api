# Data Store - Fetch

[GameJolt API](../index.md) > [Data store](index.md) > __Fetch__

## Description

Returns data from the `Data Store`.

## URL Endpoint

```
/data-store/
```

## Parameters

#### game_id
> Type: `string`
>
> Required: Yes
>
> The ID of your game.

#### key
> Type: `string`
>
> Required: Yes
>
> The key of the data item you'd like to fetch.

#### username
> Type: `string`
>
> Required: No
>
> The user's username.

#### user_token
> Type: `string`
>
> Required: No
>
> The user's token.

## Returns

#### success
> Type: `boolean`
>
> Whether the request succeeded or failed.
>
> __Example__: `true`

_These values get returned if the request was not successful:_

#### message
> Type: `string`
>
> If the request was not successful, this contains the error message.
>
> __Example__: `Unknown fatal error occurred.`

_These values get returned if the request was successful:_

#### data
> Type: `string`
>
> If the request was successful, this contains the item's data.
>
> __Example__: `some example data.`

## Remarks

- If you pass in the user information, this item will be fetched for a user. If you leave the user information empty, it will be fetched globally for the game.
- We suggest using the `dump` format for returning data from this call.

## Syntax

```
/data-storage/?game_id=xxxxx&key=myglobalkey
/data-storage/?game_id=xxxxx&key=myuserkey&username=myusername&user_token=mytoken
```

## Version history

Version		 | Description
---			 | ---
1.0			 | First implementation