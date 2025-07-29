first_name=input("Enter the First name:")
last_name=input("Enter the last name:")
if first_name.isalpha():
    if last_name.isalpha():
        password=input("Enter the password:").lower()
        if first_name in password or last_name in password:
            print("Password should not include your first or last name.")
        elif len(password) < 8:
            print(" Password must be at least 8 characters long.")
        elif not (password[0].isalpha()):
            print("Password should start with an alphabet letter.")
        elif not any(check.isdigit() for check in password): 
            print(" Password must include at least one number.")
        elif  all(char.isalnum() for char in password):  
            print(" Password must include at least one special character.")
        else:
            reenter=input("Re-enter the Password:")
            if reenter==password:
                print("CONGRATS! YOUR PASSWORD HAS BEEN CREATED SUCCESSFULLY.")
            else:
                print(" Password and re-entered password do not match.")        
    else:
        print(" Last name should contain only alphabet letters (no numbers or special characters).")
else:
    print(" First name should contain only alphabet letters (no numbers or special characters).")



# password-Genration
