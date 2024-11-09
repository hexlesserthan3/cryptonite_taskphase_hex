# mr worldwide
A musician left us a message. What's it mean?

message: picoCTF{(35.028309, 135.753082)(46.469391, 30.740883)(39.758949, -84.191605)(41.015137, 28.979530)(24.466667, 54.366669)(3.140853, 101.693207)_(9.005401, 38.763611)(-3.989038, -79.203560)(52.377956, 4.897070)(41.085651, -73.858467)(57.790001, -152.407227)(31.205753, 29.924526)}

## Approach
This is the coordinates (very obviously) we have.
> 35.028309, 135.753082
> 46.469391, 30.740883
> 39.758949, -84.191605
> 41.015137, 28.979530
> 24.466667, 54.366669
> 3.140853, 101.693207
> _
> 9.005401, 38.763611
> -3.989038, -79.203560
> 52.377956, 4.897070
> 41.085651, -73.858467
> 57.790001, -152.407227
> 31.205753, 29.924526

I could decode this manually but i wanted to see if there is a script i could write instead, since i wasn't sure how to correlate coordinates with alphanumerals in python.
``` bash 
import requests
import re

flag = "picoCTF{(35.028309, 135.753082)(46.469391, 30.740883)(39.758949, -84.191605)(41.015137, 28.979530)(24.466667, 54.366669)(3.140853, 101.693207)_(9.005401, 38.763611)(-3.989038, -79.203560)(52.377956, 4.897070)(41.085651, -73.858467)(57.790001, -152.407227)(31.205753, 29.924526)}"

def get_letter_from_coordinate(match):
    lat = match.group(1)
    long = match.group(2)
    response = requests.get(f"https://geocode.xyz/{lat},{long}?json=1")
    data = response.json()
    
    city = data.get("city", "")
    return city[0] if city else "?"

# Use re.sub with the updated function
print(re.sub(r'\(([\d\.-]+), ([\d\.-]+)\)', get_letter_from_coordinate, flag))

```

### flag: picoCTF{KODIAK_ALASKA}
