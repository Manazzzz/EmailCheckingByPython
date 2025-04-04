# EmailCheckingByPython
Checking if a given email-id is valid or not using python
email = input("Enter email-id : ")
flag1=0
flag2=0
flag3=0
if len(email)>=6:
  if email[0].isalpha():
    if ("@" in email) and (email.count("@")==1):
      if(email[-4]==".") ^ (email[-3]=="."):
        for i in email:
          if i==i.isspace():
            flag1=1
          elif i.isalpha():
            if i==i.upper():
              flag2=1
          elif i.isdigit():
            continue
          elif i=="_" or i=="." or i=="@":
            continue
          else:
            flag3=1

        if flag1==1 or flag2==1 or flag3==1:
            print("Invalid email")
        else:
          print("Valid email")
      else:
        print("Email is invalid as the last 4 characters should be .com or .in")
    else:
      print("Email is invalid as the count of @ character is not valid")
  else:
    print("Email is invalid as the first character should be an alphabet")
else:
  print("Email is invalid as the minimum length should be 6")
