objectives

==> Set up a Git hook to run scripts (like linters or tests) before commits are finalized.

================================================================================================================

Steps followed

=> Navigated to .git/hooks
=> Created a file named "pre-commit"
=> changed the file to executable with command "chmod +x pre-commit"
=> used vim and created rules such that for a javascript file there should not be a semicolon

the rule is 

    js_files=$(git diff --cached --name-only --diff-filter=ACM | grep '\.js$')


    if [ -n "$js_files" ]; then
        for file in $js_files; do
            if grep -q ";" "$file"; then
                echo "Commit blocked! Semicolon (;) found in $file."
                exit 1  
            fi
        done
    i

    exit 0
    
=> saved it
=> created a Script.js file with a ";"
=> tested commit.
=> it displayed "Commit blocked! Semicolon (;) found in Task8/script.js."
=> created a ExecutableScript.js file without a ";"
=> commited it and executed it
=> Through this, hooks helps us in "eliminating errors" in the code base and enforces production value.
