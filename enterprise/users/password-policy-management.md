# Enterprise / Users / Password Policy Management

> Since v1.0.2.66

New password policy management is located under 'Enterprise / users / Passwords policy'

<img src="./_images_/passpolicy/dialog1.jpg" class="bordered" width="400" height="auto" alt="Password policiy dialog">  

## Options

- [ ] __Set a minimum password length:__ _Default false_  
    - _It sets a minimum password length, input value must an Interger between 8 and 42_
- [ ] __Must include digits:__ _Default false_
    - _If checked, passwords must include at least one digit_
- [ ] __Must include lowercase characters:__ _Default false_
    - _If checked, passwords must include at least one lowercase character_
- [ ] __Must include uppercase characters:__ _Default false_
    - _If checked, passwords must include at least one uppercase character_
- [ ] __Must include symbols:__ _Default false_
    - _If checked, passwords must include at least one symbol_
- [ ] __Passwords expire after _N_ days:__ _Default false_
    - _If checked, new created users passwords will expire after the specified number of days_
    - _Minimum value for days is 15_
    - _This option must be checked in order to block expired password users_
    - _When active, users will get a notify prompt when password expiring date is less than 10 days_
        <br />
        <img src="./_images_/passpolicy/passexpyalert.jpg" class="bordered" width="400" height="auto" alt="Expyring password alert">  
    - _In order to extend passwords, users must change their passwords before they expire_
        - _See: [User password management](./enterprise/users/user-password-man/index)_
- [ ] __Do not allow repeating previously used passwords:__ _Default false_
    - _If checked, new passwords can't repeat previously used passwords_
- [ ] __Block account after _N_ failed attemps:__ _Default false_
    - _If checked, accounts will be blocked if login fails for the specified amount of times_
    - _Minimum value for attemps is 5_
    - _If failed attempt, a message will display attemps left_
    - _If login is succesfull attemps left will be reset to the specified value_
    - _If an account is blocked, admins can now unblock/ block accounts from the users management tab_:  
        <br />
        <img src="./_images_/passpolicy/blck_unblck.png" class="bordered" width="600" height="auto" alt="Block unblock users">  

