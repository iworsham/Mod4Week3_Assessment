# Week 3 Assessment

## Setup
* Fork and Clone this repository
* Run `update-database` - let the instructors know if you run into any issues!

## Exercise (10 Points)
### Securing the Application (4 points)
* Use Secrets Managemnt to remove the database connection string from the application.
* So that we can see the full implmentation, include a screenshot below to show your `secrets.json` file

< Screen shot here >![image](https://github.com/iworsham/Mod4Week3_Assessment/assets/35874300/db5e0bdb-51da-45f4-9b19-20998642ae43)


### Maintaining Current-User (6 points)

This application includes some starter code so that we could maintain a current user.  Review the Login and Logout code in the Home Controller, along with the Login and Logout buttons in the Home/Index.cshtml file.  Building on this pre-existing structure:
* Create a cookie that holds a key for "currentUser" when a user logs in.
* Delete that cookie when a user logs out.
* Add the value of "current user" to all views

## Questions (10 Points)

For the following questions, answer as if you are in an interview!
1. Describe one strategy you have used to maintain state in a web application. (2 points)
Normally in my previous dev enviornments I would use cookies to maintain state because the HTTP process in the web application is stateless
2. How would you protect sensitive data that we need to store in our database - for example, passwords? (2 points)
Well for one I would make sure that my Database connection string is hidden and Is only able to be seen by anyone with authorized access to our server, and to further encrypt I would use the hash method to hash our data especially passwords. 
3. Describe 3 additional common security risks in web development. (make sure you discuss what you know about the risk, and if you know how to minimize the risk) (6 points)
1 could be just like I said before our DB connection string is exposed on new projects so I would take advantage of the user secrets and create a secret .json file that only we can see and hide our DB connection string in there. 2 could be our cookies, even though I use them to maintain state, they could be a security risk because of how it saves user data a way to prevent that risk would be to create a method that deletes that cookie right after one logs out or leaves the website. So that important data does not linger. And also 3 could be passwords that are saved to our database. I know I touched on this before but this is usually the most common security risk. Someone has your password they have your whole intersocial life. Instead of storing the actual password in the database we would store the hashed version of it using a series of numbers and letters thats encrpyted using the amount of bytes thats stored in that password.
