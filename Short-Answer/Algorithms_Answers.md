#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) 0(n)
I'm sure my read on this is pretty simplistic, but it strikes me as linear. It seems that
no matter what value is put in for 'n', the time to run it it will be proportionate to that.

b) 0(n^3)
Hmmm...sort of up in the air on this one.  When I see for loops I think of 0(n), and here we have
four of them.  Could it be 0(n^4)?  The last for loop though (e.g., for 'l') seems linear because
it has k+1 and 10+k.  Whatever is plugged into 'k' wil keep this consistent.  If so, I think it makes
that loop 0(1). My gut is telling me it's probably 0(n^3).  Or maybe I'm just feeling nauseous.

c) 0(n)
I will go with 0(n) on this one.  The complexity will be proportionate to whatever is plugged into bunnies,
and I don't mean Eveready bunnies.

## Exercise II

Let's assume I took an elevator up to the middle floor of a building.  This is where I would start dropping
eggs.  Now if I were to drop an egg and it broke, I think I could safely assume tht it would break if 
I dropped it from any of the floors above.  I would exclude those floors from future tests. Give that, I would 
make the middle floor the new top floor, and take the elevator down to what would be the new middle 
floor relative to what floors remain. From there I would drop another.  If the egg broke again, then I would
follow the same process. The takeaway is that I would half the value of the remaining floors until I
found where the egg didn't break after being dropped.  This is a binary search with an 0(log n) complexity.

I don't know how to write pseudo code.  Yes, you read that correctly, so I have to go out on a limb 
here to try the real deal. I did not test this.  Don't beat me up too much on this.

```
def egg_dropper(number_of_floors):    
    low = 0    
    high = len(number_of_floors) -1    
    Crunch = False    
    while low <= high and not Crunch:    
        mid = (low + high) // 2    
        if broke == number_of_floors[mid]:    
            Crunch = True    
        elif broke < number_of_floors[mid]:    
            high = mid - 1    
        else:    
            low = mid + 1    
    if Crunch == True:    
        print("The egg broke")    
    else:    
        print("The egg did not break")    
```