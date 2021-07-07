This document is a set of instructions as to how to install custom packages such as custom classes (`.cls`) and stylesheet (`.sty` files). 


1. Create a custom folder anywhere. This file will be used to add *all* custom packages. Let's say we call it `packages` and we store it in the directory `C:\textbackslash` packages}
2. Inside this custom folder, create {*another*} folder specifically called `tex`. So, now we have 
`C:\packages\tex`.
1. Inside the `tex` directory, create *another* folder specifically called `latex`. So, now we have 
`C:\packages\tex\latex`.
1. Now, inside this directory, you can dump the *folders* of the custom packages. That is, the new directory is now 
`C:\packages\tex\latex\[customPackage]`,
where the stylesheets and classes live inside the `[customPackage]` folder.
1. Open MikTex and update the packages. 
2. To update a package, after updating it, open the command window and type `texhash`.
3. Run the command `mktexlsr`.

Checkout <https://tex.stackexchange.com/questions/2063/how-can-i-manually-install-a-package-on-miktex-windows> for reference.

# On linux
I followed the instructions from this [link](https://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te).

Here are the summarized instructions
1.  Type `kpsewhich -var-value TEXMFHOME` to get the latex search path. It looks something like `/hom/aalbaali/texmf`. Note that this directory may not exist (may not be created).
2.  Add your folders (`.cls` and `.sty`) into `/home/aalbaali/texmf/tex/latex/[package-name]/`. Create the necessary directories if necessary.
3.  From *within* that directory, run `texhash .` (or from anywhere type `texhassh /home/aalbaali/texmf/tex/latex`).