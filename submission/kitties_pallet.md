# Kitties Pallet Design

This is a design document submitted for substrate developer academy assignment 2 (Kitties Pallet)

## Storage (decl_storage!)

    * kitties: map Vec<u128> => T::AccountId

## Events (decl_event!)

    * Kitty_Created(Vec<u128>, AccountId)

## Errors (decl_error!)

    * NoOwnerOfKitty 
  <!-- tbh I don't think we'd ever encounter this error, but I guess for the hygiene, and in case any 2 random dna match (astronomical chances tho) -->

## Calls (decl_module!)

    * fn creatKitty() -> Kitty_Created(dna, owner)
