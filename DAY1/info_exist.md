# info exists Command in TCL

## The info exists command in TCL is used to check whether a variable (or array) exists before trying to use or unset it.

Syntax

    info exists variable_name

    Returns 1 (true) if the variable exists.
    Returns 0 (false) if the variable does not exist.
---

When and Where is info exists Used?
1. Preventing Errors Before Accessing a Variable

If you try to use an undefined variable, TCL throws an error. You can avoid this by checking if the variable exists first.

✅ Example: Checking Before Using a Variable

    set myVar "Hello, TCL!"
    
    if {[info exists myVar]} {
        puts "Variable exists: $myVar"
    } else {
        puts "Variable does not exist."
    }

Output:

    Variable exists: Hello, TCL!

If myVar was not set before, it would print "Variable does not exist." instead of causing an error.

---

2. Avoiding Errors Before Unsetting a Variable

✅ Example: Checking Before Unsetting
      
      set myVar "Hello"
      
      if {[info exists myVar]} {
          puts "Deleting variable..."
          unset myVar
      } else {
          puts "Variable does not exist."
      }

    If myVar exists, it is deleted safely.
    If it does not exist, unset myVar would normally cause an error, but info exists prevents this.

---

3. Checking If an Array Exists

✅ Example: Checking an Array Before Using It

      array set myArray {name "Ajinkya" age 25}
      
      if {[info exists myArray]} {
          puts "Array exists!"
      } else {
          puts "Array does not exist."
      }

    Ensures the array is set before accessing it.

---


4. Using info exists in Conditional Logic

✅ Example: Default Value Assignment
    
    if {![info exists user_name]} {
        set user_name "Guest"
    }
    puts "Welcome, $user_name"

    If user_name is not set, it assigns "Guest" as a default value.

---

Key Takeaways

✅ Prevents "variable not found" errors.
✅ Used before accessing, unsetting, or modifying variables.
✅ Helps in error-free scripting and handling optional variables.
✅ Works for both normal variables and arrays.
