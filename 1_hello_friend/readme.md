  ###Hello, friend!

This lab teaches basic Ruby Object syntax.

 ####Watch it fail

Your first real failure should be something like this:
`uninitialized constant Friend (NameError)`
Fix this by opening `friend.rb` and creating an empty class:

     class Friend
     end

 Save it. Run the test again.

  Watch it fail again

 Now you should see an error like this:

     NoMethodError in 'Friend says hello'
     undefined method `greeting' for <Friend:0x1180f3c>
     ./friend_spec.rb:5:

 This means that while it found the file, and it found the class, it couldn't find the method named "greeting".

  Define the "greeting" method

 In `friend.rb`, add the following inside the class (before the "end").

     def greeting
     end

 Save it. Run the test again.

  Watch it fail some more

 Hint 1: in order to get the next test to pass, you will need to pass a *parameter*:

     def greeting(who)

 Hint 2: once you do that, the **first** test might start failing again. To fix both at the same time, you need to provide a **default value** for that parameter:

     def greeting(who = nil)

