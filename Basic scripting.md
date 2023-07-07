# Basic Scripting 

- The two characters #! are traditionally called the hash and the bang respectively, which leads to the shortened form of “shebang” when they’re used at the beginning of a script.
- file extension for running a bash script is .sh.
- A variable can be created in bash with variable name and placing the value after the assignment operator.
- example of operator initialization - fruit="Apple"(there should not be any space between varibale name and operator and in the value also.)
- __Conditionals__ : 
    - <pre>
     if somecommand; then
        # do this if somecommand has an exit code of 0
    fi
    </pre>
    - Look for test man command and know more about test command.

- __Case__ : 
    - <pre>
    #!/bin/bash
    case "$1" in
    hello|hi)
    echo "hello yourself"
    ;;
    goodbye)
    echo "nice to have met you"
    echo "I hope to see you again"
    ;;
    *)
    echo "I didn't understand that"
    esac
      </pre>

- __Loops__ : 
    - <pre>
    #!/bin/bash

    SERVERS="servera serverb serverc"
    for S in $SERVERS; do
        echo "Doing something to $S"
    done
     </pre>
    
    - other way to run a for loop is : 
    - <pre>
    #!/bin/bash

    for NAME in Sean Jon Isaac David; do
        echo "Hello $NAME"
    done

    for S in *; do
        echo "Doing something to $S"
    done
     </pre>
    - Here glob(*) character will provide the list of all files inside the current directory to the for loop.
    
    - __While Loop__ : 
    - <pre>
        #!/bin/bash

        i=0
        while [ $i -lt 10 ]; do
            echo $i
            i=$(( $i + 1))
        done
        echo “Done counting”
        </pre>
    - Above loop is to print from 1 to 9. which uses the test([]) command to check the conditional values.
