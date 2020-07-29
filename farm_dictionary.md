## Lab 22 "Looping with for" Challenge!

```
farms = [{"name": "NE Farm", "agriculture": ["sheep", "cows", "pigs", "chickens", "llamas", "cats"]},
         {"name": "W Farm", "agriculture": ["pigs", "chickens", "llamas"]},
         {"name": "SE Farm", "agriculture": ["chickens", "carrots", "celery"]}]
```

### EASY(ish):

• Write a for loop that returns all the animals from the NE Farm!

### MEDIUM:

• Ask a user to choose a farm (NE Farm, W Farm, or SE Farm). Return the plants/animals that are raised on that farm.

### HARD:

• Ask a user to choose a farm (NE Farm, W Farm, or SE Farm). Return the plants/animals that are raised on that farm.

• ...but only return ANIMALS from that particular farm.


"""
#!/usr/bin/python3

farms = [{"name": "NE Farm", "agriculture": ["sheep", "cows", "carrots", "pigs", "chickens", "llamas", "cats"]},
         {"name": "W Farm", "agriculture": ["pigs", "celery", "chickens", "llamas"]},
         {"name": "SE Farm", "agriculture": ["chickens", "carrots", "celery"]}]

forbidden= ["celery", "carrots"]
answer= " "

while answer != "q":
    print("""Well howdy thar, pardner! Which one of these hurr farms you wanna visit?
    1. NE Farm
    2. W Farm
    3. SE Farm""")


```
    choice= input("> ")

    if choice.lower() in ["1", "ne farm", "ne"]:
        print("Well landsakes! At NE Farm we got:")
        for i in farms[0]['agriculture']:
            if i not in forbidden:
                print(i)

    elif choice.lower() in ["2", "w farm", "w"]:
        print("At W Farm we shore as shootin' got:")
        for i in farms[1]['agriculture']:
            if i not in forbidden:
                print(i)

    elif choice.lower() in ["3", "se farm", "se"]:
        print("SE Farm is full of HIPPIES, and the only meats they got is:")
        for i in farms[2]['agriculture']:
            if i not in forbidden:
                print(i)
    else:
        print("\n Well shucks pard, that tweren't one of the options!")

    answer= input("\n Press ENTER to try again or press Q to quit!")
    answer= answer.lower()
```
