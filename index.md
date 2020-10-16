## Lesson 0 - Pilot on Kaizen

Welcome to the Lovelace Academy!

We want to begin by demonstrating building a sample smart contract in Marlowe.

Copy and paste this into the Marlowe Playground

```haskell
When
    [Case
        (Deposit
            (Role "party1")
            (Role "party1")
            (Token "" "")
            (Constant 500)
        )
        (When
            [Case
                (Deposit
                    (Role "party2")
                    (Role "party2")
                    (Token "" "")
                    (Constant 300)
                )
                (Pay
                    (Role "party1")
                    (Party (Role "party2"))
                    (Token "" "")
                    (Constant 500)
                    (Pay
                        (Role "party2")
                        (Party (Role "party1"))
                        (Token "" "")
                        (Constant 300)
                        Close 
                    )
                )]
            20 Close 
        )]
    15 Close 
```
