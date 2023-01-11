>>>>## Electric Cars
>>>>> All-electric vehicles, also referred to as battery electric vehicles (BEVs), have an electric motor instead of an internal combustion engine. The vehicle uses a large traction battery pack to power the electric motor and must be plugged in to a wall outlet or charging equipment, also called electric vehicle supply equipment (EVSE). Because it runs on electricity, the vehicle emits no exhaust from a tailpipe and does not contain the typical liquid fuel components, such as a fuel pump, fuel line, or fuel tank

>>>>### Agile manifesto

<div>
  <img src="/images/agileteammanifesto.png" alt="main" style="width:90%; margin-left:4rem " >
</div>

>>>>### start of code for databse
``` from werkzeug.security import generate_password_hash, check_password_hash
import json
from datetime import date

# Define a User Class/Template
# -- A User represents the data we want to manage
def calculate_age(born):
    today = date.today()
    return today.year - born.year - ((today.month, today.day) < (born.month, born.day))
class User:    
    # constructor of a User object, initializes the instance variables within object (self)
    def __init__(self, name, uid, password, car, dob):
        self._name = name    # variables with self prefix become part of the object, 
        self._uid = uid
        self.set_password(password)
        self._car = car
        self._dob = dob


    # a name getter method, extracts name from object
    @property
    def name(self):
        return self._name
    
    # a setter function, allows name to be updated after initial object creation
    @name.setter
    def name(self, name):
        self._name = name
    

    @property
    def dob(self):
        return self._dob
    
    # a setter function, allows name to be updated after initial object creation
    @dob.setter
    def dob(self, dob):
        self._dob = dob


    # a getter method, extracts email from object
    @property
    def uid(self):
        return self._uid
    
    # a setter function, allows name to be updated after initial object creation
    @uid.setter
    def uid(self, uid):
        self._uid = uid
        
    # check if uid parameter matches user id in object, return boolean
    def is_uid(self, uid):
        return self._uid == uid
    
    @property
    def password(self):
        return self._password[0:10] + "..." # because of security only show 1st characters

    # a name getter method, extracts name from object
    @property
    def car(self):
        return self._car
    
    # a setter function, allows name to be updated after initial object creation
    @car.setter
    def car(self, car):
        self._car = car

    # update password, this is conventional setter
    def set_password(self, password):
        """Create a hashed password."""
        self._password = generate_password_hash(password, method='sha256')

    # check password parameter versus stored/encrypted password
    def is_password(self, password):
        """Check against hashed password."""
        result = check_password_hash(self._password, password)
        return result
    
    # output content using str(object) in human readable form, uses getter
    def __str__(self):
        return f'name: "{self.name}", id: "{self.uid}", psw: "{self.password}, car: "{self.car}", dob: "{self.dob}"'

    # output command to recreate the object, uses attribute directly
    def __repr__(self):
        return f'Person(name={self._name}, uid={self._uid}, password={self._password}, car={self.car}, dob: {self.dob})'


# tester method to print users
def tester(users, uid, psw, car, dob):
    result = None
    for user in users:
        # test for match in database
        if user.uid == uid and user.is_password(psw):  # check for match
            print("* ", end="")
            result = user
        # print using __str__ method
        print(str(user))
    return result
        

# place tester code inside of special if!  This allows include without tester running
if __name__ == "__main__":

    # define user objects
    u1 = User(name='Thomas Edison', uid='toby', password='123toby', car='honda', dob = calculate_age(date(2008, 12, 31)))
    u2 = User(name='Nicholas Tesla', uid='nick', password='123nick', car='lexus', dob = calculate_age(date(2010, 12, 31)))
    u3 = User(name='Alexander Graham Bell', uid='lex', password='123lex', car='tesla', dob = calculate_age(date(2004, 12, 31)))
    u4 = User(name='Eli Whitney', uid='eli', password='123eli', car='BMW', dob = calculate_age(date(2004, 12, 31)))
    u5 = User(name='Hedy Lemarr', uid='hedy', password='123hedy', car='audi', dob = calculate_age(date(2004, 12, 31)))

    # put user objects in list for convenience
    users = [u1, u2, u3, u4, u5]

    # Find user
    print("Test 1, find user 3")
    u = tester(users, u3.uid, "123lex", "nissan", date(2002, 12, 31))


    # Change user
    print("Test 2, change user 3")
    u.name = "John Mortensen"
    u.uid = "jm1021"
    u.set_password("123qwerty")
    u.car = "car"
    u.dob = calculate_age(date(2002, 12, 31))
    u = tester(users, u.uid, "123qwerty", "massda",calculate_age(date(2002, 12, 31)) )


    # Make dictionary
    ''' 
    The __dict__ in Python represents a dictionary or any mapping object that is used to store the attributes of the object. 
    Every object in Python has an attribute that is denoted by __dict__. 
    Use the json.dumps() method to convert the list of Users to a JSON string.
    '''
    print("Test 3, make a dictionary")
    json_string = json.dumps([user.__dict__ for user in users]) 
    print(json_string)

    print("Test 4, make a dictionary")
    json_string = json.dumps([vars(user) for user in users]) 
    print(json_string) ```