# every file explained

## sections

all the pe sections out of RainbowSix.exe

**headers.bin** : pe headers. image base, section table, data directories, tells u where each bin goes

**text.bin** : .text section, 255mb. all the game code

**rdata.bin** : .rdata, 13mb of strings vtables and imports

**rdatax.bin** : second rdata section, 59k

**data.bin** : .data, 21mb of globals and initialized data

**pdata.bin** : .pdata, 3.9mb of unwind info, function start and end addresses

**rsrc.bin** : .rsrc, 1.4mb of resources

**reloc.bin** : .reloc, tiny in this one

**tls.bin** : tls section, 113k of thread local data

**00cfg.bin** : cf guard config section

**gxfg.bin** : guard xfg data, control flow guard stuff

**retplne.bin** : retpoline section

**voltbl.bin** : volatile metadata table, anticheat related

**ubx0.bin** : ubisoft custom section, 1.7mb

**ubx1.bin** : ubisoft custom section, 110mb. the fat one

## functions

**functions/functions.txt** : every named function in the game with its rva and whether its a ctor or vfunc. 6mb

**functions/class_map.txt** : every class with factory address, vtable address, and each vfunc resolved. 5.7mb

**functions/classes.txt** : just the class names and their factory addresses

**functions/field_offsets.txt** : property field ids mapped to alloc and free functions

## names

**names/imports.txt** : every import resolved, address to dll and function

**names/profiler_names.txt** : internal symbol and profiler names with reference addresses

**names/registry_names.txt** : class registry names mapped to vtable and factory addresses

## strings

**strings/strings.txt** : every string in the exe, 30mb, indexed by rva and section

**strings/source_paths.txt** : internal build paths, jenkins workspace and wwise sdk sources

## image

**image/r6_flat.img** : the full exe rebuilt as a flat image, 403mb

## screenshots

folder shots of everything above
