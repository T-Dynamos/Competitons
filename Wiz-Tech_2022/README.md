#  Wiz-Tech 2022
![image](https://user-images.githubusercontent.com/68729523/200016579-6486d398-c4b3-42c5-acef-63c86b95915b.png)
## Ouestions
## Solutions
* 1st Answer :
```python
import string as st

def isint(char):
    try:
        char = int(char)
        return True
    except Exception:
        return False

def check_password(string:str) -> list:
    
    num = False
    lower = False
    upper = False
    errors = []

    if len(string) >= 6 and len(string) <= 16:
        pass
    else:
        errors.append("Length not correct")
    
    if "$" in string or "#" in string  or "@" in string:
        pass
    else:
        errors.append("Special character is missing")
    
    for s in string:
        if isint(s):
            if int(s) in list(range(0,10)):
                num = True 
    if num == False:
        errors.append("No numeric character in password")
        
    for s in string:
        if s in st.ascii_lowercase:
            lower = True
        elif s in st.ascii_uppercase:
            upper = True
    
    if lower == False:
        errors.append("No lowetcase letter in the password")

    if upper == False:
        errors.append("No uppercase letter in the password")
    
    return errors

############## Test Case ########################

string =  "goat"
result = check_password(string)

if len(result) == 0:
    print("Input : {}\nOutput : Valid password".format(string))
else:
    print("Input :",string,"\nOutput : Invalid Password")
    print("Explanation : ",", ".join(result))

```
* 2nd Answer
```python
def print_pattern() -> None:
    for i in range(1,5):
        for k in range(2):
            print("   "*(4-i)," ","  ".join("*"*(i*2)),sep="")
    for i in range(2):
        print("   "*(4-4)," ","  ".join("*"*(4*2)),sep="")

print_pattern()

```
## Results
