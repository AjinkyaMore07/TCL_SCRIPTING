The set Command in TCL

The set command in TCL (Tool Command Language) is used to assign values to variables and retrieve stored values. It is one of the most fundamental commands in TCL scripting.

## Syntax of set Command

    set variable_name value

o This assigns value to variable_name.
o If the variable already exists, set updates its value.
o If no value is provided, set retrieves the variable's current value.

---

### Examples of set Command

1. Assigning a Value to a Variable

       set myVar "Hello, TCL!"
       puts $myVar

   Output:

            Hello, TCL!

   o Here, myVar is assigned the string "Hello, TCL!".
   o The puts command prints the value stored in myVar.
   o The dollar sign $ is used to reference a variable.
   
---


  2. Retrieving a Variable's Value

    set name "Ajinkya"
    puts "My name is $name"

Output:

    My name is Ajinkya

 o The variable name stores "Ajinkya" and is accessed using $name.

---

3. Assigning Numeric Values
        
        set num1 10
        set num2 20
        set sum [expr $num1 + $num2]
        puts "Sum: $sum"


  Output:

      Sum: 30

  o The expr command evaluates mathematical expressions.
  
  o [expr $num1 + $num2] computes the sum of num1 and num2.


---


4. Updating a Variable's Value

        set counter 5
        puts "Initial: $counter"
        set counter [expr $counter + 1]
        puts "Updated: $counter"

  Output:

      Initial: 5
      Updated: 6

o The set command is used to increment the value of counter.

----

5. Using set Without a Value (Retrieval)

        set city "Pune"
        puts [set city]

  Output:

        Pune

  o When set is used without a value, it returns the stored value.

---

## Key Points About set in TCL

    Defines and updates variables in TCL scripts.
    Supports both string and numeric values.
    Used to retrieve variable values when used without a second argument.
    Works with expr for arithmetic operations.

  
