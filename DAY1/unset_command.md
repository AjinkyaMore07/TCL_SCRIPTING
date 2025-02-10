# The unset Command in TCL

 The unset command in TCL is used to delete a variable from memory. Once a variable is unset, it no longer exists, and trying to access it will result in an error.

## Syntax of unset Command

    unset variable_name

   o This removes variable_name from memory.
   o If the variable does not exist, unset does nothing.

---

# Examples of unset Command

1. Deleting a Variable

        set myVar "Hello, TCL!"
        puts $myVar   ;# Output: Hello, TCL!
        unset myVar
        puts $myVar   ;# Error: can't read "myVar": no such variable
        
   o unset myVar removes myVar, making it inaccessible.
   o Trying to print myVar after unset gives an error.

---



2. Unsetting Multiple Variables

       set a 10
       set b 20
       set c 30
       puts "$a, $b, $c"  ;# Output: 10, 20, 30
       unset a b
       puts "$a, $b, $c"  ;# Error for a and b, but c is still valid

   o You can unset multiple variables at once.
   o unset a b removes a and b, but c still exists.

---

3. Checking If a Variable Exists Before Unsetting

        set myVar "Hello"
        if {[info exists myVar]} {
            puts "Variable exists. Deleting now..."
            unset myVar
        } else {
            puts "Variable does not exist."
        }

  o info exists myVar checks if myVar exists before trying to unset it.
  o Prevents errors when trying to unset a non-existent variable.

---

# Key Points About unset

✅ Removes a variable permanently from memory.
✅ Can unset multiple variables at once.
✅ Trying to access an unset variable causes an error.
✅ Use info exists before unset to avoid errors.
