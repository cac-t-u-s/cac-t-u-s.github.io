
# How to make an external library ?

**OM# external libraries are folders containing Lisp code** to be loaded dynamically in the environment.

> See [External libraries](libraries)

The few following rules make for the library to smoothly integrate and run in the environment: 

### Structure and Naming

- The name of the library is the name of the folder before the first white space (_"my-lib"_, _"my-lib 1.0"_, ...)
- The folder should contain a file of this name, with the extension "omlib" (e.g. _"my-lib.omlib"_)
- A subfolder sound contain the sources (optional)
- A subfolder named _"resources"_ should contain the resources, and in particular another subfolder named _"icons"_

```
my-lib/
  |---- my-lib.omlib
  |---- sources/
           |---- file-1.lisp
           |---- file-2.lisp
           |---- ...
  |---- resources/
           |---- icons/
                   |---- icon1.png
                   |---- icon2.png
                   |---- ...
           |---- ...
```

> **Warning:** GitHub users/dowloaders -- when dowloading a repository (say, for the library "my-lib"), GitHub may append the name of the branch to the downloaded packages ("my-lib-master.zip", etc.), preventing the lib to be recognised for its true name. If this is the case, just rename the folder after downloading it.

### Contents and syntax of the .omlib file

The .omlib file (_my-lib.omlib_) contains list with the information necessary to display and load the library in OM#:

```cl
(:om-lib

 (:version 1.0)
 (:doc "This library does great things.")
 (:author "My Name (2019)")

 (:source-files
    "sources/file-1" 
    "sources/file-2"
    ...
    ) 

 (:symbols
  (:classes c1 c2 ...) 
  (:functions fun1 fun2 ...)
  (:packages
   (:package 
    (:name "sub-package 1")
    (:functions ...))
   ...
   ))
)
```

#### Notes:

`:source-files` must be followed by a number of _relative pathnames_ (relative to the root folder of the library) designating the name and order of the source files to load. If the pathname has no extension (".lisp", ".xfasl", etc.) the compiled version (".\*fasl") of the source file will be loaded if available and up-to-date. Otherwise, the .lisp version of the file is loaded. 

> Compiled lisp files are generally more efficient. They require specific compilation tools and are not portable cross-platform.


`:symbols` determines the classes (`:classes`) and functions (`:functions`) that will be displayed explicitly in the user interface for this library ([Packages Library](session#the-external-libraries-tab), menus, [auto-completion lists](patch#auto-completion), auto-generated documentation, etc.) 

The symbols can also be gathered in "sub-packages": 

```cl
(:packages
   (:package 
    (:name "sub-package 1")
    (:functions ...))
   ...
   )
```

### Adapting an OpenMusic library

In general for a simple library (and if the code inside the source files is compatible!), adapting an OpenMusic library mostly requires making the .omlib file from the corresponding ".lisp" loader-file of the library (_my-lib.lisp_).  

> Note that _my-lib.lisp_ and _my-lib.omlib_ can both stay in the library folder, making the library compatible with both OpenMusic and OM#.



