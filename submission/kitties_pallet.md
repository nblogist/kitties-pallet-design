<!-- For my own reference: https://discordapp.com/channels/772968587060445244/772968587060445251/813166983364739095 -->
# Kitties Pallet Design

This is a design document submitted for substrate developer academy assignment 2 (Kitties Pallet)

## Storage (decl_storage!)

    * kitties: double_map (kitty_dna: u128, owner: AccountId )  => kitty_id:u32

## Events (decl_event!)

    * Kitty_Created(u128, AccountId, u32) 

## Errors (decl_error!)

    * NoOwnerOfKitty 
  <!-- tbh I don't think we'd ever encounter this error, but I guess for the hygiene, and in case any 2 random dna match (astronomical chances tho) -->

## Calls (decl_module!)

    * fn creatKitty() -> Kitty_Created(dna, owner, kitty_id)
