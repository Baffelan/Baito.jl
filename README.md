# Baito.jl
Baffelan's Julia registry for local repositories

To use this:
1. install `LocalRegistry` in your Julia instance:
   ```julia
   using.Pkg;
   Pkg.add("LocalRegistry")
   ```
2. add the _Baito_ to your registries:
   ```julia
   using LocalRegistry
   ] registry add "https://github.com/Baffelan/Baito.jl/"
   ```
3. To register a package there:
   ```Julia
   register("NameOfPackage"; registry = "Baito")
   ```
   **Warning 1** you need to be able to push to this repo, so you need to have a token or an ssh key
   **Warning 2** you need to have the local package in development (i.e., `dev /Path/To/LocalPack`)
4. To use a package from the LocalRegistry it's just the same as always:
   ```Julia
   Pkg.add("NameOfPackage")
   ```
