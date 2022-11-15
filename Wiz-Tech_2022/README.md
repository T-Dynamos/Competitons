#  Wiz-Tech 2022
![image](https://user-images.githubusercontent.com/68729523/200016579-6486d398-c4b3-42c5-acef-63c86b95915b.png)
## Ouestion 1 
![IMG_20221107_195257](https://user-images.githubusercontent.com/68729523/200333968-c7685649-8954-4d7b-92ea-744486db5ce6.jpg)
## Answer 1
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
## Question 2
![IMG_20221107_195317](https://user-images.githubusercontent.com/68729523/200333994-0051e680-62a6-45f6-9797-ca295194715a.jpg)
## Answer 2
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
As expected, I loose (kind of). Reason: Bad code quality?
![IMG_20221107_195638](https://user-images.githubusercontent.com/68729523/200334478-a790f9ba-c1c4-4a8e-854e-d7d6409f400e.jpg)

## Certificates
![SAVE_20221115_230148](https://user-images.githubusercontent.com/68729523/201987832-80019933-2480-4964-9cd1-678c79afe96d.jpg)
