# TAPL

Programs from the book "Types and Programming Languages", configured to run in
OCaml toplevel.

You might either compile and library and use it in the OCaml toplevel, or compile
and run a customized toplevel with the library preloaded. You must have OCaml installed
to use this library.

## Compile the library 
In the current directory, do the following to compile the library.

        ocamlbuild tapl.cma

You should see a message about compilation finished.
By default, ocamlbuild generate all the target file in a subdirectory called '_build',
cd into the subdirectory and invoke ocaml.

You should see the standard OCaml header and prompt from the toplevel. 
To load the library, use

        #load "tapl.cma"
Pay attention to the '#' sign, it is part of the directive, not the command prompt.

## Create a custom toplevel
Follow the first step to compile the library. Then go to the '_build' subdirectory, and
do 

        ocamlmktop tapl.cma -o tapl
You should see a new executable created in the directory. This is a customized toplevel
with the library (tapl.cma in this case) preloaded.
