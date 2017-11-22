# Bib Library
This repository includes the bib database used for JabRef. 
Can be used as a stand alone repository or as a submodule. 

When being used as a stand alone repo, add the pdf files of the papers on the same parent directory inside a directory named "Papers". 
Then JabRef document links will identify the papers.

## As a Submodule
Add this repo as a submodule on another git repository (main repo).

* Add the submodule for the first time
  ```sh
  cd /repo/to/use/this/bib_library
  git submodule add https://github.com/kanishkegb/bib_library.git 
  ```
  This will create a separate directory called "bib_library" inside the main repo. Make sure to add below line on the main tex file as the bibiliography.
  ```sh
  \bibliography{bib_library/bib_library}
  ```
  
 * Update the submodule each time when you clone the main repo
    ```sh
    git submodule update --init
    ```
  
  * Push to the bib_library when you modify the bib file
    ```sh
    cd /bib_library
    add and commit the changes
    git push
    ```
