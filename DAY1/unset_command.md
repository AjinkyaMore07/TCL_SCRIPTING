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

